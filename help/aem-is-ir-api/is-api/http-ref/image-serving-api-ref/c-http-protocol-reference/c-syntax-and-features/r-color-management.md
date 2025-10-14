---
title: Gestion des couleurs du service d’images
description: Image Serving prend en charge les conversions d’espace colorimétrique basées sur des profils d’espace colorimétrique conformes à la spécification ICC (International Color Consortium).
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 0c9a489c-36e0-4934-b9c5-33414a9ce0b8
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '1210'
ht-degree: 0%

---

# Gestion des couleurs du service d’images{#image-serving-color-management}

Image Serving prend en charge les conversions d’espace colorimétrique basées sur des profils d’espace colorimétrique conformes à la spécification ICC (International Color Consortium).

## Espaces colorimétriques par défaut {#section-8cfe60808bce49968091995e4e521dba}

Chaque catalogue d’images (et le catalogue par défaut) peut définir un ensemble de profils ICC qui constituent les espaces colorimétriques par défaut de ce catalogue - un profil d’entrée et un profil de sortie chacun pour les données en niveaux de gris, RVB et CMJN. Voir
[attribut ::IccProfileRgb](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-iccprofilergb.md) [attribute ::IccProfileGray attribute ::IccProfileCmyk](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-iccprofilegray.md) [attribute ::IccProfileSrcRgb](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-iccprofilecmyk.md) [attribute ::IccProfileSrcGray](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-iccprofilesrcrgb.md) [attribute ::IccProfileSrcCmyk.](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-iccprofilesrcgray.md) [&#128279;](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-iccprofilesrccmyk.md)






## Espace colorimétrique d’entrée {#section-9f08e2c1b6aa4fe4815be174972c1944}

Les images sources peuvent intégrer des profils ICC pour définir l’espace colorimétrique d’entrée. Si aucun profil n’est incorporé dans une image source, `attribute::IccProfileSrc*` du catalogue d’images applicable correspondant au type de pixel de l’image source est utilisé. Si cet attribut n’est pas défini dans le catalogue d’images, `attribute::IccProfile*` est utilisé. Si cet attribut de catalogue n’est pas défini non plus, l’image n’est pas gérée par les couleurs et seules des transformations naïves sont appliquées.

## Output espace colorimétrique {#section-b517bca622b64dcfa7defba6035d0716}

L’espace colorimétrique du résultat final de l’image d’une requête est défini avec la `icc=` commande. Si `icc=` n’est pas spécifié, l’espace colorimétrique de sortie par défaut (à partir du catalogue principal de la requête) qui correspond au type de pixels de l’image de sortie est utilisé comme espace colorimétrique de sortie. Si aucun profil de sortie n’est défini dans le catalogue principal ou par défaut, et si le calque de base est une image avec un profil incorporé correspondant au type de pixel de sortie, ce profil est utilisé pour l’espace colorimétrique de sortie. Sinon, l’espace colorimétrique de sortie reste indéfini - seules des conversions de couleurs naïves sont appliquées lors de la conversion entre types de pixels et aucun profil de couleur ne peut être incorporé dans l’image de sortie.

L’espace colorimétrique de sortie d’une demande de diffusion d’images imbriquée/incorporée est toujours identique à l’espace colorimétrique de sortie de la demande d’incorporation extérieure.

## Couleurs unies {#section-df03a5c5ca894e6f8b9a5ba02cf6ac03}

Les valeurs colorimétriques spécifiées avec `color=`, `bgcolor=`ou la commande `\iscolortbl` RTF sont associées à l’espace colorimétrique d’entrée si la valeur colorimétrique inclut le suffixe &#39;S&#39;, sinon elles sont associées à l’espace colorimétrique de sortie. Valeurs colorimétriques spécifiées `bgc=` avec `\colortbl` ou les commandes RTF et `\cmykcolortbl` sont toujours associées à l’espace colorimétrique de sortie par défaut ou réel correspondant.

>[!NOTE]
>
>À ce stade, `bgc=` ne participe pas entièrement à la gestion des couleurs. le suffixe « S » est ignoré lorsqu’il est spécifié avec `bgc=`, et la conversion naïve est appliquée lorsque le type de pixel de la valeur de couleur spécifiée avec `bgc=` diffère du type de pixel de l’image de sortie. Sinon, `bgc=` est associée à l’espace colorimétrique cible réel.

## Requêtes imbriquées et intégrées {#section-bdda638c31504f26a77e51ebb1ea6e3b}

L’espace colorimétrique de sortie pour les requêtes IS imbriquées et les requêtes IR intégrées est automatiquement défini sur l’espace colorimétrique de sortie de la requête la plus externe, sauf si la requête imbriquée spécifie un espace colorimétrique de sortie explicite avec `icc=`. En outre, les requêtes imbriquées/incorporées héritent également des espaces colorimétriques de sortie par défaut du catalogue principal de la requête la plus externe, afin de garantir une gestion cohérente des valeurs de couleur unie.

## Conversion de l’espace colorimétrique {#section-ca87b80b8e364ea59d8a92d87121b0fb}

La diffusion d’images tente généralement de retarder les conversions de couleurs au cours du traitement. Si tous les calques d’une image ont le même espace colorimétrique de calque, la conversion vers l’espace colorimétrique de sortie est effectuée après la fusion et la mise à l’échelle finale. Si plusieurs espaces colorimétriques de calque sont impliqués, chaque calque est transformé en espace colorimétrique de sortie avant la fusion.

>[!NOTE]
>
>Les commandes `op_brightness=`, `op_colorbalance=`, `op_colorize=`, , `op_contrast=` `op_hue=`et `op_saturation=` sont des opérations RVB. Ces opérations maintiennent la fidélité des couleurs uniquement si l’espace colorimétrique du calque est de type pixel RVB. Si elles sont autres que RVB, les données sont converties en RVB à l’aide d’une conversion naïve des couleurs, et le résultat a une fidélité des couleurs limitée. L’espace colorimétrique de calque pour ces calques doit être considéré comme indéterminé.

Les options de conversion des couleurs sont fournies avec `icc=` ou, si `icc=` non spécifié, avec `attribute::IccRenderIntent`, `attribute::IccBlackPointCompensation`et `attribute::IccDither`.

## Intégration des profils colorimétriques {#section-261ebbae5ce046589a776ca972380052}

Le profil de couleurs ICC de l’espace colorimétrique de sortie, s’il est disponible, peut être incorporé dans l’image de réponse en spécifiant `iccEmbed=`.

## Gestion des profils ICC {#section-eb210e4b44e64e2c8b80ee59216c5555}

Tous les profils de couleurs utilisés par le serveur doivent être conformes aux spécifications ICC. Les fichiers de profil ICC ont généralement un [!DNL .icc] suffixe de fichier OR [!DNL .icm] et sont colocalisés avec les fichiers de données image.

Bien que les profils de sortie puissent être spécifiés par chemin/nom de fichier dans la `icc=` commande, il est recommandé d’enregistrer tous les fichiers de profil dans la carte de profil ICC du catalogue ou du catalogue d’images par défaut et d’utiliser des identificateurs de raccourci ( `icc::Name`) au lieu de chemins d’accès aux fichiers.

Tous les profils ICC référencés dans `catalog::IccProfile` et dans `attribute::IccProfile*` doivent être enregistrés dans la carte de profils ICC de l’image ou du catalogue par défaut.

## Restrictions {#section-fb50ede40b124b89b30679da29782ab5}

Seuls les espaces colorimétriques CMJN, RVB et niveaux de gris sont actuellement pris en charge.

## Profils de couleurs ICC inclus {#section-98b4a7d9f9814e8ba27d6dcf3dcf850c}

Image Serving inclut la plupart des profils ICC Adobe standard dans le catalogue d’images par défaut. Ces profils sont accessibles soit par leur nom commun (par exemple, comme illustré à la Photoshop), soit par un identifiant un peu plus court. Le tableau suivant répertorie tous les profils ICC standard. Lors de la référence à un profil dans la `icc=` commande par son nom commun, les espaces doivent être codés comme `%20`.

Des profils supplémentaires peuvent être ajoutés aux profils standard, soit au catalogue par défaut, soit à un catalogue d’images spécifique. Consultez la référence[&#x200B; de &#x200B;](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-icc-profile-map-reference/c-icc-profile-map-reference.md#concept-57b9148ce55249cd825cb7ee19ed057c)carte de profil ICC pour plus de détails.

>[!NOTE]
>
>Le tableau suivant s’applique uniquement à *Dynamic Media Hybrid* (fonctionnant en `dynamicmedia` mode exécution).

| Identificateur | Nom commun | Nom du fichier |
|-- |-- |-- |
| **RVB** |  |  |
| `AdobeRGB` | Adobe RGB (1998) | AdobeRGB1998.icc |
| `AppleRGB` | Apple RVB | AppleRGB.icc |
| `CIERGB` | CIE RVB | CIERGB.icc |
| `ColorMatchRGB` | ColorMatch RVB | ColorMatchRGB.icc |
| `NTSC` | NTSC (1953) | NTSC1953.icc |
| `PAL` | PAL/SECAM | PAL_SECAM.icc |
| `ProPhoto` | ProPhoto RVB | ProPhoto.icm |
| `SMPTE` | SMPTE-C | SMPTE-C.icc |
| `sRGB` | sRVB IEC61966-2.1 | Espace colorimétrique sRgb Profile.icm |
| `WideGamutRGB` | Large gamme RVB | WideGamutRGB.icc |
| **CMJN** |  |  |
| `CoatedFogra27` | FOGRA27 enduit (ISO 12647-2:2004) | CoatedFOGRA27.icc |
| `CoatedFogra39` | FOGRA39 revêtu (ISO 12647-2:2004) | CoatedFOGRA39.icc |
| `CoatedGraCol` | Revêtement GRACoL 2006 (ISO 12647-2:2004) | CoatedGRACoL2006.icc |
| `EuropeISOCoated` | Europe ISO Coated FOGRA27 | EuropeISOCoatedFOGRA27.icc |
| `EuroscaleCoated` | Euroscale Coated | EuroscaleCoated.icc |
| `EuroscaleUncoated` | Euroscale Uncoated v2 | EuroscaleUncoated.icc |
| `JapanColorCoated` | Japan Color 2001 Coated | JapanColor2001Coated.icc |
| `JapanColorNewspaper` | Japan Color 2002 Journal | JapanColor2002Newspaper.icc |
| `JapanColorUncoated` | Japan Color 2001 Non couché | JapanColor2001Uncoated.icc |
| `JapanColorWebCoated` | Japan Color 2003 Web Coated | JapanColor2003WebCoated.icc |
| `JapanWebCoated` | Japan Web Coated (publicité) | JapanWebCoated.icc |
| `NewsprintSNAP2007` | Papier journal américain (SNAP 2007) | USNewsprintSNAP2007.icc |
| `PS4Default` | Photoshop 4 Paramètre CMJN par défaut | Photoshop4DefaultCMYK.icc |
| `PS5Default` | Photoshop 5 Default CMJN | Photoshop5DefaultCMYK.icc |
| `SheetfedCoated` | U.S. Sheetfed Coated v2 | USSheetfedCoated.icc |
| `SheetfedUncoated` | U.S. Sheetfed Uncoated v2 | USSheetfedUncoated.icc |
| `UncoatedFogra29` | FOGRA29 non revêtu (ISO 12647-2:2004) | UncoatedFOGRA29.icc |
| `WebCoated` | U.S. Web Coated (SWOP) v2 | USWebCoatedSWOP.icc |
| `WebCoatedFogra28` | FOGRA28 revêtu de toile (ISO 12647-2:2004) | WebCoatedFOGRA28.icc |
| `WebCoatedGrade3` | Papier SWOP 2006 Grade 3 | WebCoatedSWOP2006Grade3.icc |
| `WebCoatedGrade5` | Papier SWOP 2006 Grade 5 | WebCoatedSWOP2006Grade5.icc |
| `WebUncoated` | U.S. Web Uncoated v2 | USWebUncoated.icc |

Le tableau suivant s’applique à Dynamic Media diffusion et Dynamic Media d’images *classiques (exécution en* mode exécution).**`dynamicmedia_scene7`

| Identificateur | Nom commun | Nom du fichier |
|-- |-- |-- |
| **RVB** |  |  |
| `AdobeRGB` | Adobe RGB (1998) | AdobeRGB1998.icc |
| `AppleRGB` | Apple RVB | AppleRGB.icc |
| `CIERGB|CIE RGB` | CIERGB.icc |
| `ColorMatchRGB` | ColorMatch RVB | ColorMatchRGB.icc |
| `NTSC` | NTSC (1953) | NTSC1953.icc |
| `PAL` | PAL/SECAM | PAL_SECAM.icc |
| `ProPhoto RGB` | ProPhoto RVB | ProPhoto RGB.icm |
| `SMPTE` | SMPTE-C | SMPTE-C.icc |
| `sRGB` | sRVB IEC61966-2.1 | Espace colorimétrique sRgb Profile.icm |
| `WideGamutRGB` | Large gamme RVB | WideGamutRGB.icc |
| **CMJN** |  |  |
| `CoatedFogra27` | FOGRA27 enduit (ISO 12647-2:2004) | CoatedFOGRA27.icc |
| `CoatedFogra39` | FOGRA39 revêtu (ISO 12647-2:2004) | CoatedFOGRA39.icc |
| `Coated GRACoL 2006 (ISO 12647-2:2004)` | Revêtement GRACoL 2006 (ISO 12647-2:2004) | CoatedGRACoL2006.icc |
| `EuropeISOCoated` | Europe ISO Coated FOGRA27 | EuropeISOCoatedFOGRA27.icc |
| `Euroscale Coated v2` | Euroscale Coated v2 | EuroscaleCoated.icc |
| `EuroscaleUncoated` | Euroscale Uncoated v2 | EuroscaleUncoated.icc |
| `JapanColorCoated` | Japan Color 2001 Coated | JapanColor2001Coated.icc |
| `JapanColorNewspaper` | Japan Color 2002 Journal | JapanColor2002Newspaper.icc |
| `JapanColorUncoated` | Japan Color 2001 Non couché | JapanColor2001Uncoated.icc |
| `Japan Color 2003 Web Coated` | Japan Color 2003 Web Coated | JapanColor2003WebCoated.icc |
| `JapanWebCoated` | Japan Web Coated (publicité) | JapanWebCoated.icc |
| `PS4Default` | Photoshop 4 Paramètre CMJN par défaut | Photoshop4DefaultCMYK.icc |
| `PS5Default` | Photoshop 5 Default CMJN | Photoshop5DefaultCMYK.icc |
| `SheetfedCoated` | U.S. Sheetfed Coated v2 | USSheetfedCoated.icc |
| `SheetfedUncoated` | U.S. Sheetfed Uncoated v2 | USSheetfedUncoated.icc |
| `UncoatedFogra29` | FOGRA29 non revêtu (ISO 12647-2:2004) | UncoatedFOGRA29.icc |
| `US Newsprint (SNAP 2007)` | Papier journal américain (SNAP 2007) | USNewsprintSNAP2007.icc |
| `WebCoated` | U.S. Web Coated (SWOP) v2 | USWebCoatedSWOP.icc |
| `WebCoatedFogra28` | FOGRA28 revêtu de toile (ISO 12647-2:2004) | WebCoatedFOGRA28.icc |
| `Web Coated SWOP 2006 Grade 3 Paper` | Papier SWOP 2006 Grade 3 | WebCoatedSWOP2006Grade3.icc |
| `Web Coated SWOP Grade 5 Paper` | Papier SWOP 2006 Grade 5 | WebCoatedSWOP2006Grade5.icc |
| `WebUncoated` | U.S. Web Uncoated v2 | USWebUncoated.icc |

## Voir aussi {#section-39159397e80b4efca5f631eab8b9aa06}

[International Color Consortium](https://www.color.org/index.xalter), [icc=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-icc.md#reference-182b5679e21e4df3b4d330535a5a7517), [iccEmbed=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-iccembed.md#reference-e3b774fb322046a2a6dde3a7bab5583e), [attribute ::IccProfile](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-iccprofilecmyk.md#reference-db89f9dac33e447cadb359ec1ba27ee0)&#42;, [attribute ::IccProfileSrc](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-iccprofilesrcgray.md#reference-a717831da24d43f680d01393660f12f9)&#42;, [attribute ::IccRenderIntent](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-iccrenderintent.md#reference-012f207f28bd4406a5368d23ed95a51f), [attribute ::IccBlackPointCompensation](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-iccblackpointcompensation.md#reference-357626375ee140d1807f0c05171c733f), [attribute ::IccDither](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-iccdither.md#reference-914d0d0567364246b4016d45c0ada85b), [ICC Profile Map Reference](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-icc-profile-map-reference/c-icc-profile-map-reference.md#concept-57b9148ce55249cd825cb7ee19ed057c), [color=](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-data-types/r-is-http-color.md), [bgc=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-bgc.md#reference-53376175f617446fbe5c69120f834b88), [*`color`*](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-data-types/r-is-http-color.md)
