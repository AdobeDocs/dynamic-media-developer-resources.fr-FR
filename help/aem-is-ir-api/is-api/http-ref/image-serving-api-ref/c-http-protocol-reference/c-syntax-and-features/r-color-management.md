---
title: Gestion des couleurs du service d’images
description: Le service d’images prend en charge les conversions d’espace colorimétrique basées sur des profils d’espace colorimétrique conformes à la spécification ICC (International Color Consortium).
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 0c9a489c-36e0-4934-b9c5-33414a9ce0b8
TQID: 'https://experienceleague.adobe.com/IzOzGIHXhgknu9Wms73sua9vEF17EemCmaWPByRAp5M'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 1243
ht-degree: 0%

---

# Gestion des couleurs du service d’images{#image-serving-color-management}

Le service d’images prend en charge les conversions d’espace colorimétrique basées sur des profils d’espace colorimétrique conformes à la spécification ICC (International Color Consortium).

## Espaces colorimétriques par défaut {#section-8cfe60808bce49968091995e4e521dba}

Chaque catalogue d’images (et le catalogue par défaut) peut définir un ensemble de profils ICC qui constituent les espaces colorimétriques par défaut de ce catalogue (un profil d’entrée et un profil de sortie chacun pour les données en niveaux de gris, RGB et CMJN). voir
[attribute::IccProfileRgb](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-iccprofilergb.md)
[attribute::IccProfileGray](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-iccprofilegray.md)
[attribute::IccProfileCmyk](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-iccprofilecmyk.md)
[attribute::IccProfileSrcRgb](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-iccprofilesrcrgb.md)
[attribute::IccProfileSrcGray](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-iccprofilesrcgray.md)
[attribute::IccProfileSrcCmyk](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-iccprofilesrccmyk.md).

## Espace colorimétrique d’entrée {#section-9f08e2c1b6aa4fe4815be174972c1944}

Les images Source peuvent incorporer des profils ICC pour définir l’espace colorimétrique d’entrée. Si aucun profil n’est incorporé dans une image source, `attribute::IccProfileSrc*` du catalogue d’images applicable correspondant au type de pixel de l’image source est utilisé. Si cet attribut n’est pas défini dans le catalogue d’images, `attribute::IccProfile*` est utilisé. Si cet attribut de catalogue n’est pas défini non plus, l’image n’est pas gérée par couleur et seules les transformations naïves sont appliquées.

## Espace colorimétrique de sortie {#section-b517bca622b64dcfa7defba6035d0716}

L’espace colorimétrique du résultat d’image final d’une requête est défini avec la commande `icc=`. Si `icc=` n’est pas spécifié, l’espace colorimétrique de sortie par défaut (du catalogue principal de la requête) qui correspond au type de pixel de l’image de sortie est utilisé comme espace colorimétrique de sortie. Si aucun profil de sortie n’est défini dans le catalogue principal ou par défaut et si le calque de base est une image avec un profil incorporé correspondant au type de pixel de sortie, ce profil est utilisé pour l’espace colorimétrique de sortie. Dans le cas contraire, l’espace colorimétrique de sortie reste indéfini ; seules les conversions de couleurs naïves sont appliquées lors de la conversion entre les types de pixels et aucun profil colorimétrique ne peut être incorporé dans l’image de sortie.

L’espace colorimétrique de sortie d’une requête de diffusion d’images imbriquée/incorporée est toujours identique à l’espace colorimétrique de sortie de la requête d’incorporation externe.

## Couleurs unies {#section-df03a5c5ca894e6f8b9a5ba02cf6ac03}

Les valeurs de couleur spécifiées avec `color=`, `bgcolor=` ou les `\iscolortbl` de commande RTF sont associées à l’espace colorimétrique d’entrée si la valeur de couleur inclut le suffixe « S » ; dans le cas contraire, elles sont associées à l’espace colorimétrique de sortie. Les valeurs de couleur spécifiées avec `bgc=` ou les commandes RTF `\colortbl` et `\cmykcolortbl` sont toujours associées à l’espace colorimétrique de sortie réel ou par défaut correspondant.

>[!NOTE]
>
>Actuellement, `bgc=` ne participe pas entièrement à la gestion des couleurs : le suffixe « S » est ignoré lorsqu’il est spécifié avec `bgc=` et une conversion naïve est appliquée lorsque le type de pixel de la valeur de couleur spécifiée avec `bgc=` diffère du type de pixel de l’image de sortie. Sinon, `bgc=` est associé à l’espace colorimétrique de sortie réel.

## Requêtes imbriquées et incorporées {#section-bdda638c31504f26a77e51ebb1ea6e3b}

L’espace colorimétrique de sortie pour les requêtes IS imbriquées et les requêtes IR incorporées est automatiquement défini sur l’espace colorimétrique de sortie de la requête la plus externe, sauf si la requête imbriquée spécifie un espace colorimétrique de sortie explicite avec `icc=`. En outre, les requêtes imbriquées/incorporées héritent également des espaces colorimétriques de sortie par défaut du catalogue principal de la requête la plus à l’extérieur, afin d’assurer une gestion cohérente des valeurs de couleurs unies.

## Conversion de l’espace colorimétrique {#section-ca87b80b8e364ea59d8a92d87121b0fb}

La diffusion d’images tente généralement de retarder les conversions de couleurs pendant le traitement. Si tous les calques d’une image ont le même espace colorimétrique de calque, la conversion vers l’espace colorimétrique de sortie est effectuée après la fusion et la mise à l’échelle finale. Si plusieurs espaces colorimétriques de calque sont concernés, chaque calque est transformé en espace colorimétrique de sortie avant la fusion.

>[!NOTE]
>
>Les commandes `op_brightness=`, `op_colorbalance=`, `op_colorize=`, `op_contrast=`, `op_hue=` et `op_saturation=` sont des opérations RGB. Ces opérations conservent la fidélité des couleurs uniquement si l’espace colorimétrique du calque est de type RGB pixel. Si les données ne sont pas RGB, elles sont converties dans RGB à l’aide d’une conversion des couleurs naïve, avec pour résultat une fidélité aux couleurs limitée. L’espace colorimétrique des calques doit être considéré comme indéterminé.

Les options de conversion des couleurs sont fournies avec `icc=` ou, si `icc=` n’est pas spécifié, avec `attribute::IccRenderIntent`, `attribute::IccBlackPointCompensation` et `attribute::IccDither`.

## Incorporer des profils de couleurs {#section-261ebbae5ce046589a776ca972380052}

Le profil colorimétrique ICC de l’espace colorimétrique de sortie, s’il est disponible, peut être incorporé à l’image de réponse en spécifiant `iccEmbed=`.

## Gestion des profils ICC {#section-eb210e4b44e64e2c8b80ee59216c5555}

Tous les profils de couleurs utilisés par le serveur doivent être conformes à la spécification ICC. Les fichiers de profil ICC ont généralement un suffixe de fichier [!DNL .icc] ou [!DNL .icm] et sont co-localisés avec les fichiers de données d’image.

Bien que les profils de sortie puissent être spécifiés par chemin/nom de fichier dans la commande `icc=`, il est recommandé d’enregistrer tous les fichiers de profil dans la carte de profil ICC du catalogue par défaut ou du catalogue d’images et d’utiliser des identifiants de raccourci ( `icc::Name`) au lieu des chemins d’accès aux fichiers.

Tous les profils ICC référencés dans `catalog::IccProfile` et dans `attribute::IccProfile*` doivent être enregistrés dans la carte de profil ICC de l’image ou du catalogue par défaut.

## Restrictions {#section-fb50ede40b124b89b30679da29782ab5}

Seuls les espaces colorimétriques CMJN, RGB et de niveaux de gris sont actuellement pris en charge.

## Profils de couleurs ICC inclus {#section-98b4a7d9f9814e8ba27d6dcf3dcf850c}

La diffusion d’images inclut la plupart des profils ICC Adobe standard dans le catalogue d’images par défaut. Ces profils sont accessibles soit par leurs noms communs (par exemple, comme dans Photoshop), soit avec un identifiant un peu plus court. Le tableau suivant répertorie tous les profils ICC standard. Lors du référencement d’un profil dans la commande `icc=` par son nom commun, les espaces doivent être codés en tant que `%20`.

Vous pouvez ajouter d’autres profils aux profils standard, soit au catalogue par défaut, soit à un catalogue d’images spécifique. Pour plus d’informations, reportez-vous à la [Référence de carte de profil ICC](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-icc-profile-map-reference/c-icc-profile-map-reference.md#concept-57b9148ce55249cd825cb7ee19ed057c).

>[!NOTE]
>
>Le tableau suivant s’applique uniquement à *Dynamic Media en mode hybride* (exécuté en mode d’exécution `dynamicmedia`).

| Identifiant | Nom commun | Nom du fichier |
|-- |-- |-- |
| **** |  |  |
| `AdobeRGB` | Adobe RGB (1998) | AdobeRGB1998.icc |
| `AppleRGB` | Apple RGB | AppleRGB.icc |
| `CIERGB` | CIE RGB | CIERGB.icc |
| `ColorMatchRGB` | RGB ColorMatch | ColorMatchRGB.icc |
| `NTSC` | NTSC (1953) | NTSC1953.icc |
| `PAL` | PAL/SECAM | PAL_SECAM.icc |
| `ProPhoto` | ProPhoto RGB | ProPhoto.icm |
| `SMPTE` | SMPTE-C | SMPTE-C.icc |
| `sRGB` | sRGB IEC61966-2.1 | Profil d’espace colorimétrique sRvb.icm |
| `WideGamutRGB` | RGB à large gamme | WideGamutRGB.icc |
| **CMJN** |  |  |
| `CoatedFogra27` | Coated FOGRA27 (ISO 12647-2:2004) | CoatedFOGRA27.icc |
| `CoatedFogra39` | Coated FOGRA39 (ISO 12647-2:2004) | CoatedFOGRA39.icc |
| `CoatedGraCol` | Coated GRACoL 2006 (ISO 12647-2:2004) | CoatedGRACoL2006.icc |
| `EuropeISOCoated` | Europe ISO Coated FOGRA27 | EuropeISOCoatedFOGRA27.icc |
| `EuroscaleCoated` | Euroscale Coated | EuroscaleCoated.icc |
| `EuroscaleUncoated` | Euroscale Uncoated v2 | EuroscaleUncoated.icc |
| `JapanColorCoated` | Japan Color 2001 Coated | JapanColor2001Coated.icc |
| `JapanColorNewspaper` | Japan Color 2002 Newspaper | JapanColor2002Newspaper.icc |
| `JapanColorUncoated` | Japan Color 2001 Uncoated | JapanColor2001Uncoated.icc |
| `JapanColorWebCoated` | Japan Color 2003 Web Coated | JapanColor2003WebCoated.icc |
| `JapanWebCoated` | Japan Web Coated (Ad) | JapanWebCoated.icc |
| `NewsprintSNAP2007` | US Newsprint (SNAP 2007) | USNewsprintSNAP2007.icc |
| `PS4Default` | CMJN par défaut de Photoshop 4 | Photoshop4DefaultCMYK.icc |
| `PS5Default` | CMJN par défaut de Photoshop 5 | Photoshop5DefaultCMYK.icc |
| `SheetfedCoated` | U.S. Sheetfed Coated v2 | USSheetfedCoated.icc |
| `SheetfedUncoated` | U.S. Sheetfed Uncoated v2 | USSheetfedUncoated.icc |
| `UncoatedFogra29` | Uncoated FOGRA29 (ISO 12647-2:2004) | UncoatedFOGRA29.icc |
| `WebCoated` | U.S. Web Coated (SWOP) v2 | USWebCoatedSWOP.icc |
| `WebCoatedFogra28` | FOGRA28 web (ISO 12647-2:2004) | WebCoatedFOGRA28.icc |
| `WebCoatedGrade3` | Papier web enduit SWOP 2006 de 3e année | WebCoatedSWOP2006Grade3.icc |
| `WebCoatedGrade5` | Papier Web Coated SWOP 2006 Grade 5 | WebCoatedSWOP2006Grade5.icc |
| `WebUncoated` | U.S. Web Uncoated v2 | USWebUncoated.icc |

Le tableau suivant s’applique à la diffusion d’images Dynamic Media Classic ** et à *Dynamic Media* (s’exécutant en mode d’exécution `dynamicmedia_scene7`).

| Identifiant | Nom commun | Nom du fichier |
|-- |-- |-- |
| **** |  |  |
| `AdobeRGB` | Adobe RGB (1998) | AdobeRGB1998.icc |
| `AppleRGB` | Apple RGB | AppleRGB.icc |
| `CIERGB|CIE RGB` | CIERGB.icc |
| `ColorMatchRGB` | RGB ColorMatch | ColorMatchRGB.icc |
| `NTSC` | NTSC (1953) | NTSC1953.icc |
| `PAL` | PAL/SECAM | PAL_SECAM.icc |
| `ProPhoto RGB` | ProPhoto RGB | ProPhoto RGB.icm |
| `SMPTE` | SMPTE-C | SMPTE-C.icc |
| `sRGB` | sRGB IEC61966-2.1 | Profil d’espace colorimétrique sRvb.icm |
| `WideGamutRGB` | RGB à large gamme | WideGamutRGB.icc |
| **CMJN** |  |  |
| `CoatedFogra27` | Coated FOGRA27 (ISO 12647-2:2004) | CoatedFOGRA27.icc |
| `CoatedFogra39` | Coated FOGRA39 (ISO 12647-2:2004) | CoatedFOGRA39.icc |
| `Coated GRACoL 2006 (ISO 12647-2:2004)` | Coated GRACoL 2006 (ISO 12647-2:2004) | CoatedGRACoL2006.icc |
| `EuropeISOCoated` | Europe ISO Coated FOGRA27 | EuropeISOCoatedFOGRA27.icc |
| `Euroscale Coated v2` | Euroscale Coated v2 | EuroscaleCoated.icc |
| `EuroscaleUncoated` | Euroscale Uncoated v2 | EuroscaleUncoated.icc |
| `JapanColorCoated` | Japan Color 2001 Coated | JapanColor2001Coated.icc |
| `JapanColorNewspaper` | Japan Color 2002 Newspaper | JapanColor2002Newspaper.icc |
| `JapanColorUncoated` | Japan Color 2001 Uncoated | JapanColor2001Uncoated.icc |
| `Japan Color 2003 Web Coated` | Japan Color 2003 Web Coated | JapanColor2003WebCoated.icc |
| `JapanWebCoated` | Japan Web Coated (Ad) | JapanWebCoated.icc |
| `PS4Default` | CMJN par défaut de Photoshop 4 | Photoshop4DefaultCMYK.icc |
| `PS5Default` | CMJN par défaut de Photoshop 5 | Photoshop5DefaultCMYK.icc |
| `SheetfedCoated` | U.S. Sheetfed Coated v2 | USSheetfedCoated.icc |
| `SheetfedUncoated` | U.S. Sheetfed Uncoated v2 | USSheetfedUncoated.icc |
| `UncoatedFogra29` | Uncoated FOGRA29 (ISO 12647-2:2004) | UncoatedFOGRA29.icc |
| `US Newsprint (SNAP 2007)` | US Newsprint (SNAP 2007) | USNewsprintSNAP2007.icc |
| `WebCoated` | U.S. Web Coated (SWOP) v2 | USWebCoatedSWOP.icc |
| `WebCoatedFogra28` | FOGRA28 web (ISO 12647-2:2004) | WebCoatedFOGRA28.icc |
| `Web Coated SWOP 2006 Grade 3 Paper` | Papier web enduit SWOP 2006 de 3e année | WebCoatedSWOP2006Grade3.icc |
| `Web Coated SWOP Grade 5 Paper` | Papier Web Coated SWOP 2006 Grade 5 | WebCoatedSWOP2006Grade5.icc |
| `WebUncoated` | U.S. Web Uncoated v2 | USWebUncoated.icc |

## Voir aussi {#section-39159397e80b4efca5f631eab8b9aa06}

[International Color Consortium](https://www.color.org/index.xalter), [icc=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-icc.md#reference-182b5679e21e4df3b4d330535a5a7517), [iccEmbed=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-iccembed.md#reference-e3b774fb322046a2a6dde3a7bab5583e), [attribute::IccProfile](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-iccprofilecmyk.md#reference-db89f9dac33e447cadb359ec1ba27ee0)&#42;, [attribute::IccProfileSrc](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-iccprofilesrcgray.md#reference-a717831da24d43f680d01393660f12f9)&#42;, [attribute::IccRenderIntent](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-iccrenderintent.md#reference-012f207f28bd4406a5368d23ed95a51f), [attribute::IccBlackPointCompensation](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-iccblackpointcompensation.md#reference-357626375ee140d1807f0c05171c733f), [attribute::IccDither](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-iccdither.md#reference-914d0d0567364246b4016d45c0ada85b), [ICC Profile Map Reference](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-icc-profile-map-reference/c-icc-profile-map-reference.md#concept-57b9148ce55249cd825cb7ee19ed057c), [color=](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-data-types/r-is-http-color.md), [bgc=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-bgc.md#reference-53376175f617446fbe5c69120f834b88) [*`color`*](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-data-types/r-is-http-color.md)
