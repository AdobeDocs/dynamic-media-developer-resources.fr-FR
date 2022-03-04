---
description: La diffusion d’images prend en charge les conversions d’espace colorimétrique basées sur des profils d’espace colorimétrique conformes à la spécification ICC (International Color Consortium).
solution: Experience Manager
title: Gestion des couleurs du serveur d’images
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 0c9a489c-36e0-4934-b9c5-33414a9ce0b8
source-git-commit: 790ce3aa4e9aadc019d17e663fc93d7c69772b23
workflow-type: tm+mt
source-wordcount: '1191'
ht-degree: 0%

---

# Gestion des couleurs du serveur d’images{#image-serving-color-management}

La diffusion d’images prend en charge les conversions d’espace colorimétrique basées sur des profils d’espace colorimétrique conformes à la spécification ICC (International Color Consortium).

## Espaces colorimétriques par défaut {#section-8cfe60808bce49968091995e4e521dba}

Chaque catalogue d’images (et le catalogue par défaut) peut définir un ensemble de profils ICC qui constituent les espaces colorimétriques par défaut de ce catalogue : une entrée et un profil de sortie chacun pour les données en niveaux de gris, RGB et CMJN. Voir ` [attribute::IccProfileRgb](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-iccprofilergb.md#reference-3479e7daac54404f84b06b98ca07b9df)`, ` [attribute::IccProfileGray](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-iccprofilegray.md#reference-13822a1596e440eea0492e86d88dad35)`, ` [attribute::IccProfileCmyk](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-iccprofilecmyk.md#reference-db89f9dac33e447cadb359ec1ba27ee0)`, ` [attribute::IccProfileSrcRgb](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-iccprofilesrcrgb.md#reference-b8e576d075b44f5c94d95bfb5aa22ae2)`, ` [attribute::IccProfileSrcGray](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-iccprofilesrcgray.md#reference-a717831da24d43f680d01393660f12f9)`, et ` [attribute::IccProfileSrcCmyk](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-iccprofilesrccmyk.md#reference-b57196dfe5db41fe88bd0828ed4ec728)`.

## Espace colorimétrique d’entrée {#section-9f08e2c1b6aa4fe4815be174972c1944}

Les images source peuvent incorporer des profils ICC pour définir l’espace colorimétrique d’entrée. Si aucun profil n’est incorporé dans une image source, `attribute::IccProfileSrc*` du catalogue d’images correspondant au type de pixel de l’image source est utilisé. Si cet attribut n&#39;est pas défini dans le catalogue d&#39;images, `attribute::IccProfile*` est utilisée. Si cet attribut de catalogue n’est pas défini non plus, l’image n’est pas gérée par les couleurs et seules les transformations naïves sont appliquées.

## Espace colorimétrique de sortie {#section-b517bca622b64dcfa7defba6035d0716}

L’espace colorimétrique du résultat final de l’image d’une requête est défini avec la propriété `icc=` . If `icc=` n’est pas spécifié, l’espace colorimétrique de sortie par défaut (du catalogue principal de la requête) correspondant au type de pixel de l’image de sortie est utilisé comme espace colorimétrique de sortie. Si aucun profil de sortie n’est défini dans le catalogue principal ou le catalogue par défaut, et si la couche de base est une image avec un profil incorporé correspondant au type de pixel de sortie, ce profil est utilisé pour l’espace colorimétrique de sortie. Dans le cas contraire, l’espace colorimétrique de sortie n’est pas défini : seules les conversions de couleur naïves sont appliquées lors de la conversion entre les types de pixels et aucun profil colorimétrique ne peut être incorporé dans l’image de sortie.

L’espace colorimétrique de sortie d’une requête de diffusion d’images imbriquée/incorporée est toujours identique à l’espace colorimétrique de sortie de la requête d’incorporation externe.

## Couleurs solides {#section-df03a5c5ca894e6f8b9a5ba02cf6ac03}

Valeurs de couleur spécifiées avec `color=`, `bgcolor=`, ou la commande RTF `\iscolortbl` sont associés à l’espace colorimétrique d’entrée si la valeur de couleur inclut le suffixe &quot;S&quot;, sinon ils sont associés à l’espace colorimétrique de sortie. Valeurs de couleur spécifiées avec `bgc=` ou les commandes RTF `\colortbl` et `\cmykcolortbl` sont toujours associés à l’espace colorimétrique de sortie par défaut ou réel correspondant.

>[!NOTE]
>
>À l’heure actuelle, `bgc=` ne participe pas pleinement à la gestion des couleurs ; le suffixe &quot;S&quot; est ignoré lorsqu’il est spécifié avec `bgc=`, et une conversion naïve est appliquée lorsque le type de pixel de la valeur de couleur spécifiée avec `bgc=` diffère du type de pixel de l’image de sortie. Sinon, `bgc=` est associé à l’espace colorimétrique de sortie réel.

## Requêtes imbriquées et incorporées {#section-bdda638c31504f26a77e51ebb1ea6e3b}

L’espace colorimétrique de sortie des requêtes IS imbriquées et des requêtes IR incorporées est automatiquement défini sur l’espace colorimétrique de sortie de la requête la plus éloignée, sauf si la requête imbriquée spécifie un espace colorimétrique de sortie explicite avec `icc=`. En outre, les requêtes imbriquées/incorporées héritent également des espaces colorimétriques de sortie par défaut du catalogue principal de la requête la plus éloignée, afin d’assurer une gestion cohérente des valeurs de couleur unie.

## Conversion de l’espace colorimétrique {#section-ca87b80b8e364ea59d8a92d87121b0fb}

Le service d’images tente généralement de retarder les conversions de couleurs pendant le traitement. Si tous les calques d’une image possèdent le même espace colorimétrique de calque, la conversion de l’espace colorimétrique de sortie est effectuée après la fusion et la mise à l’échelle finale. Si plusieurs espaces colorimétriques de calque sont impliqués, chaque calque est transformé en espace colorimétrique de sortie avant la fusion.

>[!NOTE]
>
>Les commandes `op_brightness=`, `op_colorbalance=`, `op_colorize=`, `op_contrast=`, `op_hue=`, et `op_saturation=` sont des opérations RGB. Ces opérations conservent la fidélité des couleurs uniquement si l’espace colorimétrique du calque est de type pixel RGB. Si elles ne sont pas RGB, les données sont converties en RGB à l’aide d’une conversion de couleurs naïve et le résultat aura une fidélité aux couleurs limitée. L’espace colorimétrique de ces calques doit être considéré comme indéterminé.

Les options de conversion des couleurs sont fournies avec `icc=` ou, si `icc=` n’est pas spécifié, avec `attribute::IccRenderIntent`, `attribute::IccBlackPointCompensation`, et `attribute::IccDither`.

## Incorporation de profils de couleur {#section-261ebbae5ce046589a776ca972380052}

Le profil colorimétrique ICC de l’espace colorimétrique de sortie, s’il est disponible, peut être incorporé dans l’image de réponse en spécifiant `iccEmbed=`.

## Gestion des profils ICC {#section-eb210e4b44e64e2c8b80ee59216c5555}

Tous les profils de couleurs utilisés par le serveur doivent être conformes à la spécification ICC. Les fichiers de profil ICC comportent généralement une [!DNL .icc] ou [!DNL .icm] suffixe du fichier et sont colocalisés avec les fichiers de données image.

Bien que les profils de sortie puissent être spécifiés par chemin/nom de fichier dans la variable `icc=` , il est recommandé d’enregistrer tous les fichiers de profil dans la carte de profil ICC du catalogue d’images ou du catalogue d’images par défaut et d’utiliser des identifiants de raccourci ( `icc::Name`) plutôt que les chemins d’accès aux fichiers.

Tous les profils ICC référencés dans `catalog::IccProfile` et dans `attribute::IccProfile*` doit être enregistré dans la carte de profil ICC de l’image ou du catalogue par défaut.

## Restrictions {#section-fb50ede40b124b89b30679da29782ab5}

Seuls les espaces colorimétriques CMJN, RGB et niveaux de gris sont actuellement pris en charge.

## Profils de couleur ICC inclus {#section-98b4a7d9f9814e8ba27d6dcf3dcf850c}

La diffusion d’images inclut la plupart des profils ICC d’Adobe standard dans le catalogue d’images par défaut. Ces profils sont accessibles soit par leurs noms communs (comme dans Photoshop, par exemple), soit avec un identifiant un peu plus court. Le tableau suivant répertorie tous les profils ICC standard. Lors du référencement d’un profil dans la variable `icc=` par son nom commun, les espaces doivent être codés comme `%20`.

Des profils supplémentaires peuvent être ajoutés aux profils standard, soit au catalogue par défaut, soit à un catalogue d’images spécifique. Reportez-vous à la section [Référence de carte des profils ICC](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-icc-profile-map-reference/c-icc-profile-map-reference.md#concept-57b9148ce55249cd825cb7ee19ed057c) pour plus d’informations.

>[!NOTE]
>
>Le tableau suivant s’applique à *Dynamic Media hybride* uniquement (s’exécutant dans `dynamicmedia` mode d’exécution).

|Identifiant|Nom commun|Nom du fichier| |— |— |— | |**RGB**|| |`AdobeRGB`|Adobe RGB (1998)|AdobeRGB1998.icc| |`AppleRGB`|RGB Apple|AppleRGB.icc| |`CIERGB`|RGB CIE|CIERGB.icc| |`ColorMatchRGB`|RGB ColorMatch|ColorMatchRGB.icc| |`NTSC`|NTSC (1953)|NTSC1953.icc| |`PAL`|PAL/SECAM|PAL_SECAM.icc| |`ProPhoto`|RGB ProPhoto|ProPhoto.icm| |`SMPTE`|SMPTE-C|SMPTE-C.icc| |`sRGB`|sRGB IEC61966-2.1|sRgb Color Space Profile.icm| |`WideGamutRGB`|RGB LargeGamut|WideGamutRGB.icc| |**CMJN**|| |`CoatedFogra27`|FOGRA27 (ISO 12647-2:2004)|CoatedFOGRA27.icc| |`CoatedFogra39`|FOGRA39 (ISO 12647-2:2004)|CoatedFOGRA39.icc| |`CoatedGraCol`|Coated GRACoL 2006 (ISO 12647-2:2004)|CoatedGRACoL2006.icc| |`EuropeISOCoated`|Europe ISO Coated FOGRA27|EuropeISOCoatedFOGRA27.icc| |`EuroscaleCoated`|Euroscale Coated|EuroscaleCoated.icc| |`EuroscaleUncoated`|Euroscale Non couché v2|EuroscaleUncouché.icc| |`JapanColorCoated`|Japan Color 2001 Coated|JapanColor2001Coated.icc| |`JapanColorNewspaper`|Journal Japan Color 2002|JapanColor2002Newspaper.icc| |`JapanColorUncoated`|Japan Color 2001 Non couché|JapanColor2001Non couché.icc| |`JapanColorWebCoated`|Japan Color 2003 Web Coated|JapanColor2003WebCoated.icc| |`JapanWebCoated`|Japan Web Coated (Ad)|JapanWebCoated.icc| |`NewsprintSNAP2007`|US Newsprint (SNA 2007)|USNewsprintSNA2007.icc| |`PS4Default`|Photoshop 4 CMJN par défaut|Photoshop4DefaultCMYK.icc| |`PS5Default`|Photoshop 5 CMJN par défaut|Photoshop5DefaultCMYK.icc| |`SheetfedCoated`|États-Unis Sheetfed Coated v2|USSheetfedCoated.icc| |`SheetfedUncoated`|États-Unis Sheetfed Non couché v2|USSheetfedUnPAW.icc| |`UncoatedFogra29`|FOGRA29 non couché (ISO 12647-2:2004)|UncondamnésFOGRA29.icc| |`WebCoated`|États-Unis Web Coated (SWOP) v2|USWebCoatedSWOP.icc| |`WebCoatedFogra28`|FOGRA Web Coated28 (ISO 12647-2:2004)|WebCoatedFOGRA28.icc| |`WebCoatedGrade3`|Papier de qualité 3 Web SWOP 2006 | WebCoatedSWOP2006Class3.icc| |`WebCoatedGrade5`|Papier de qualité 5 Web SWOP 2006 | WebCoatedSWOP2006Class5.icc| |`WebUncoated`|États-Unis Web non couché v2|USWebUncouché.icc|

Le tableau suivant s’applique à *Dynamic Media Classic Image Serving* et *Dynamic Media* (exécution dans `dynamicmedia_scene7` mode d’exécution).

|Identifiant|Nom commun|Nom du fichier| |— |— |— | |**RGB**|| |`AdobeRGB`|Adobe RGB (1998)|AdobeRGB1998.icc| |`AppleRGB`|RGB Apple|AppleRGB.icc| |`CIERGB|CIE RGB`|CIERGB.icc| |`ColorMatchRGB`|RGB ColorMatch|ColorMatchRGB.icc| |`NTSC`|NTSC (1953)|NTSC1953.icc| |`PAL`|PAL/SECAM|PAL_SECAM.icc| |`ProPhoto RGB`|RGB ProPhoto|RGB ProPhoto.icm| |`SMPTE`|SMPTE-C|SMPTE-C.icc| |`sRGB`|sRGB IEC61966-2.1|sRgb Color Space Profile.icm| |`WideGamutRGB`|RGB LargeGamut|WideGamutRGB.icc| |**CMJN**|| |`CoatedFogra27`|FOGRA27 (ISO 12647-2:2004)|CoatedFOGRA27.icc| |`CoatedFogra39`|FOGRA39 (ISO 12647-2:2004)|CoatedFOGRA39.icc| |`Coated GRACoL 2006 (ISO 12647-2:2004)`|Coated GRACoL 2006 (ISO 12647-2:2004)|CoatedGRACoL2006.icc| |`EuropeISOCoated`|Europe ISO Coated FOGRA27|EuropeISOCoatedFOGRA27.icc| |`Euroscale Coated v2`|Euroscale Coated v2|EuroscaleCoated.icc| |`EuroscaleUncoated`|Euroscale Non couché v2|EuroscaleUncouché.icc| |`JapanColorCoated`|Japan Color 2001 Coated|JapanColor2001Coated.icc| |`JapanColorNewspaper`|Journal Japan Color 2002|JapanColor2002Newspaper.icc| |`JapanColorUncoated`|Japan Color 2001 Non couché|JapanColor2001Non couché.icc| |`Japan Color 2003 Web Coated`|Japan Color 2003 Web Coated|JapanColor2003WebCoated.icc| |`JapanWebCoated`|Japan Web Coated (Ad)|JapanWebCoated.icc| |`PS4Default`|Photoshop 4 CMJN par défaut|Photoshop4DefaultCMYK.icc| |`PS5Default`|Photoshop 5 CMJN par défaut|Photoshop5DefaultCMYK.icc| |`SheetfedCoated`|États-Unis Sheetfed Coated v2|USSheetfedCoated.icc| |`SheetfedUncoated`|États-Unis Sheetfed Non couché v2|USSheetfedUnPAW.icc| |`UncoatedFogra29`|FOGRA29 non couché (ISO 12647-2:2004)|UncondamnésFOGRA29.icc| |`US Newsprint (SNAP 2007)`|US Newsprint (SNA 2007)|USNewsprintSNA2007.icc| |`WebCoated`|États-Unis Web Coated (SWOP) v2|USWebCoatedSWOP.icc| |`WebCoatedFogra28`|FOGRA Web Coated28 (ISO 12647-2:2004)|WebCoatedFOGRA28.icc| |`Web Coated SWOP 2006 Grade 3 Paper`|Papier de qualité 3 Web SWOP 2006 | WebCoatedSWOP2006Class3.icc| |`Web Coated SWOP Grade 5 Paper`|Papier de qualité 5 Web SWOP 2006 | WebCoatedSWOP2006Class5.icc| |`WebUncoated`|États-Unis Web non couché v2|USWebUncouché.icc|

## Voir aussi {#section-39159397e80b4efca5f631eab8b9aa06}

[Consortium de couleurs international](https://www.color.org/index.xalter), [icc=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-icc.md#reference-182b5679e21e4df3b4d330535a5a7517), [iccEmbed=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-iccembed.md#reference-e3b774fb322046a2a6dde3a7bab5583e), [attribute::IccProfile](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-iccprofilecmyk.md#reference-db89f9dac33e447cadb359ec1ba27ee0)*, [attribute::IccProfileSrc](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-iccprofilesrcgray.md#reference-a717831da24d43f680d01393660f12f9)*, [attribute::IccRenderIntent](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-iccrenderintent.md#reference-012f207f28bd4406a5368d23ed95a51f), [attribute::IccBlackPointCompensation](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-iccblackpointcompensation.md#reference-357626375ee140d1807f0c05171c733f), [attribute::IccDither](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-iccdither.md#reference-914d0d0567364246b4016d45c0ada85b), [Référence de carte des profils ICC](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-icc-profile-map-reference/c-icc-profile-map-reference.md#concept-57b9148ce55249cd825cb7ee19ed057c), [color=](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-data-types/r-is-http-color.md), [bgc=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-bgc.md#reference-53376175f617446fbe5c69120f834b88), [ *`color`*](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-data-types/r-is-http-color.md)
