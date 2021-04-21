---
description: Image Serving prend en charge les conversions d’espace colorimétrique en fonction de profils d’espace colorimétrique conformes à la spécification ICC (International Color Consortium).
solution: Experience Manager
title: Gestion des couleurs de la diffusion d’images
feature: Dynamic Media Classic,SDK/API
role: Developer,Business Practitioner
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '1203'
ht-degree: 0%

---


# Gestion des couleurs de la diffusion d’images {#image-serving-color-management}

Image Serving prend en charge les conversions d’espace colorimétrique en fonction de profils d’espace colorimétrique conformes à la spécification ICC (International Color Consortium).

## Espaces de couleur par défaut {#section-8cfe60808bce49968091995e4e521dba}

Chaque catalogue d’images (et le catalogue par défaut) peut définir un ensemble de profils ICC qui constituent les espaces colorimétriques par défaut de ce catalogue - un profil d’entrée et un  de sortie chacun pour les données en niveaux de gris, RVB et CMJN. Voir ` [attribute::IccProfileRgb](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-iccprofilergb.md#reference-3479e7daac54404f84b06b98ca07b9df)`, ` [attribute::IccProfileGray](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-iccprofilegray.md#reference-13822a1596e440eea0492e86d88dad35)`, ` [attribute::IccProfileCmyk](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-iccprofilecmyk.md#reference-db89f9dac33e447cadb359ec1ba27ee0)`, ` [attribute::IccProfileSrcRgb](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-iccprofilesrcrgb.md#reference-b8e576d075b44f5c94d95bfb5aa22ae2)`, ` [attribute::IccProfileSrcGray](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-iccprofilesrcgray.md#reference-a717831da24d43f680d01393660f12f9)` et ` [attribute::IccProfileSrcCmyk](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-iccprofilesrccmyk.md#reference-b57196dfe5db41fe88bd0828ed4ec728)`.

## Espace colorimétrique d&#39;entrée {#section-9f08e2c1b6aa4fe4815be174972c1944}

Les images source peuvent incorporer des profils ICC pour définir l’espace colorimétrique d’entrée. Si aucun profil n’est incorporé dans une image source, `attribute::IccProfileSrc*` du catalogue d’images approprié correspondant au type de pixel de l’image source est utilisé. Si cet attribut n&#39;est pas défini dans le catalogue d&#39;images, `attribute::IccProfile*` est utilisé. Si cet attribut de catalogue n’est pas défini non plus, l’image n’est pas gérée par les couleurs et seules les transformations naïves sont appliquées.

## Espace colorimétrique de sortie {#section-b517bca622b64dcfa7defba6035d0716}

L’espace colorimétrique du résultat final de l’image d’une requête est défini à l’aide de la commande `icc=`. Si `icc=` n’est pas spécifié, l’espace colorimétrique de sortie par défaut (du catalogue principal de la requête) qui correspond au type de pixel de l’image de sortie est utilisé comme espace colorimétrique de sortie. Si aucun profil de sortie n’est défini dans le catalogue principal ou par défaut et si le calque de base est une image avec un profil incorporé correspondant au type de pixel de sortie, ce profil est utilisé pour l’espace colorimétrique de sortie. Dans le cas contraire, l’espace colorimétrique de sortie n’est pas défini. Seules les conversions naïves de couleur seront appliquées lors de la conversion entre les types de pixels et aucun profil de couleur ne peut être incorporé à l’image de sortie.

L’espace colorimétrique de sortie d’une demande de diffusion d’images imbriquée/incorporée est toujours identique à l’espace colorimétrique de sortie de la demande d’incorporation externe.

## Couleurs unies {#section-df03a5c5ca894e6f8b9a5ba02cf6ac03}

Les valeurs de couleur spécifiées avec `color=`, `bgcolor=` ou la commande RTF `\iscolortbl` seront associées à l’espace colorimétrique d’entrée si la valeur de couleur inclut le suffixe &#39;S&#39;, sinon elles sont associées à l’espace colorimétrique de sortie. Les valeurs de couleur spécifiées avec les commandes `bgc=` ou RTF `\colortbl` et `\cmykcolortbl` sont toujours associées à l’espace colorimétrique de sortie par défaut ou réel correspondant.

>[!NOTE]
>
>Actuellement, `bgc=` ne participe pas pleinement à la gestion des couleurs ; le suffixe &quot;S&quot; est ignoré lorsqu’il est spécifié avec `bgc=` et une conversion naïve est appliquée lorsque le type de pixel de la valeur de couleur spécifiée avec `bgc=` diffère du type de pixel de l’image de sortie. Sinon, `bgc=` est associé à l’espace colorimétrique de sortie réel.

## Requêtes imbriquées et incorporées {#section-bdda638c31504f26a77e51ebb1ea6e3b}

L’espace colorimétrique de sortie pour les requêtes IS imbriquées et les requêtes IR incorporées est automatiquement défini sur l’espace colorimétrique de sortie de la requête la plus externe, sauf si la requête imbriquée spécifie un espace colorimétrique de sortie explicite avec `icc=`. En outre, les requêtes imbriquées/incorporées héritent également des espaces colorimétriques de sortie par défaut du catalogue principal de la requête la plus externe, afin de garantir une gestion cohérente des valeurs de couleur unie.

## Conversion de l’espace colorimétrique {#section-ca87b80b8e364ea59d8a92d87121b0fb}

La diffusion d’images tente généralement de retarder les conversions de couleur pendant le traitement. Si tous les calques d’une image ont le même espace colorimétrique de calque, la conversion en espace colorimétrique de sortie est effectuée après fusion et mise à l’échelle finale. Si plusieurs espaces colorimétriques de calque sont impliqués, chaque calque est transformé en espace colorimétrique de sortie avant la fusion.

>[!NOTE]
>
>Les commandes `op_brightness=`, `op_colorbalance=`, `op_colorize=`, `op_contrast=`, `op_hue=` et `op_saturation=` sont des opérations RVB. Ces opérations conservent la fidélité des couleurs uniquement si l’espace colorimétrique du calque est de type pixel RVB. Si elles ne sont pas RVB, les données sont converties en RVB à l’aide d’une conversion de couleur naïve, et le résultat aura une fidélité des couleurs limitée. L’espace colorimétrique de ces calques doit être considéré comme indéterminé.

Les options de conversion des couleurs sont fournies avec `icc=` ou, si `icc=` n&#39;est pas spécifié, avec `attribute::IccRenderIntent`, `attribute::IccBlackPointCompensation` et `attribute::IccDither`.

## Incorporation de profils de couleur {#section-261ebbae5ce046589a776ca972380052}

Le profil de couleurs ICC de l’espace colorimétrique de sortie, s’il est disponible, peut être incorporé à l’image de réponse en spécifiant `iccEmbed=`.

## Gestion des profils ICC {#section-eb210e4b44e64e2c8b80ee59216c5555}

Tous les profils de couleur utilisés par le serveur doivent être conformes à la spécification ICC. Les fichiers de profil ICC ont généralement un suffixe de fichier [!DNL .icc] ou [!DNL .icm] et sont colocalisés avec les fichiers de données d’image.

Bien que les profils de sortie puissent être spécifiés par chemin/nom de fichier dans la commande `icc=`, il est recommandé d&#39;enregistrer tous les fichiers de profil dans la carte de Profil ICC du catalogue par défaut ou du catalogue d&#39;images et d&#39;utiliser des identifiants de raccourci ( `icc::Name`) au lieu des chemins d&#39;accès aux fichiers.

Tous les profils ICC référencés dans `catalog::IccProfile` et dans `attribute::IccProfile*` doivent être enregistrés dans la carte de Profil ICC de l’image ou du catalogue par défaut.

## Restrictions {#section-fb50ede40b124b89b30679da29782ab5}

Pour le moment, seuls les espaces colorimétriques CMJN, RVB et Niveaux de gris sont pris en charge.

## Profils de couleur ICC {#section-98b4a7d9f9814e8ba27d6dcf3dcf850c} inclus

La diffusion d’images inclut la plupart des profils ICC d’Adobe standard dans le catalogue d’images par défaut. Ces profils sont accessibles soit par leur nom commun (comme dans Photoshop, par exemple), soit par un identifiant un peu plus court. Le tableau suivant liste tous les profils ICC standard. Lorsque vous référencez un profil dans la commande `icc=` par son nom commun, les espaces doivent être codés en tant que `%20`.

D’autres profils peuvent être ajoutés aux profils standard, soit au catalogue par défaut, soit à un catalogue d’images spécifique. Pour plus d’informations, consultez le [Guide de référence de la carte de Profil ICC](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-icc-profile-map-reference/c-icc-profile-map-reference.md#concept-57b9148ce55249cd825cb7ee19ed057c).

>[!NOTE]
>
>Le tableau suivant s’applique uniquement à *Dynamic Media Hybrid* (s’exécutant en mode d’exécution `dynamicmedia`).

|Identificateur|Nom commun|Nom du fichier|
|— |— |— |
|**RGB**|||
|`AdobeRGB`|Adobe RGB (1998)|AdobeRGB1998.icc|
|`AppleRGB`|Apple RGB|Apple RGB.icc|
|`CIERGB`|CIE RGB|CIERGB.icc|
|`ColorMatchRGB`|ColorMatch RGB|ColorMatchRGB.icc|
|`NTSC`|NTSC (1953)|NTSC1953.icc|
|`PAL`|PAL/SECAM|PAL_SECAM.icc|
|`ProPhoto`|ProPhoto RGB|ProPhoto.icm|
|`SMPTE`|SMPTE-C|SMPTE-C.icc|
|`sRGB`|sRGB IEC61966-2.1|sRgb Color Space Profil.icm|
|`WideGamutRGB`|Wide Gamut RGB|WideGamutRGB.icc|
|**CMJN**|||
|`CoatedFogra27`|Coated FOGRA27 (ISO 12647-2:2004)|CoatedFOGRA27.icc|
|`CoatedFogra39`|Coated FOGRA39 (ISO 12647-2:2004)|CoatedFOGRA39.icc|
|`CoatedGraCol`|Coated GRACoL 2006 (ISO 12647-2:2004)|CoatedGRACoL2006.icc|
|`EuropeISOCoated`|Europe ISO Coated FOGRA27|EuropeISOCoatedFOGRA27.icc|
|`EuroscaleCoated`|Euroscale Coated|EuroscaleCoated.icc|
|`EuroscaleUncoated`|Euroscale Unenduit v2|EuroscaleUnenduit.icc|
|`JapanColorCoated`|Couleur japonaise 2001 Coated|JapanColor2001Coated.icc|
|`JapanColorNewspaper`|Journal de la couleur du Japon 2002|Journal de la couleur du Japon 2002|Journal de la couleur du Japon 2002.icc|
|`JapanColorUncoated`|Japan Color 2001 Unenduit|JapanColor2001Unenduit.icc|
|`JapanColorWebCoated`|Couleur japonaise 2003 Couleur Web Coated|JapanColor2003WebCoated.icc|
|`JapanWebCoated`|Japan Web Coated (Ad)|JapanWebCoated.icc|
|`NewsprintSNAP2007`|US Newsprint (SNAP 2007)|USNewsprintSNAP2007.icc|
|`PS4Default`|Photoshop 4 CMJN par défaut|Photoshop4DefaultCMYK.icc|
|`PS5Default`|Photoshop 5 CMJN par défaut|Photoshop5DefaultCMYK.icc|
|`SheetfedCoated`|U.S. Sheetfed Coated v2|USSheetfedCoated.icc|
|`SheetfedUncoated`|U.S. Feuille non couchée v2|USSheetfedUnenduit.icc|
|`UncoatedFogra29`|FOGRA29 non couché (ISO 12647-2:2004)|UnbeddedFOGRA29.icc|
|`WebCoated`|U.S. Web Coated (SWOP) v2|USWebCoatedSWOP.icc|
|`WebCoatedFogra28`|Web Coated FOGRA28 (ISO 12647-2:2004)|WebCoatedFOGRA28.icc|
|`WebCoatedGrade3`|Papier de 3e année avec revêtement Web SWOP 2006|Papier WebCoatedSWOP2006Grade3.icc|
|`WebCoatedGrade5`|Papier de classe 5 avec revêtement Web SWOP 2006|Papier WebCoatedSWOP2006Grade5.icc|
|`WebUncoated`|U.S. Web non couché v2|USWebUnenduit.icc|

Le tableau suivant s’applique à *Dynamic Media Classic Image Serving* et *Dynamic Media* (s’exécutant en mode d’exécution `dynamicmedia_scene7`).

|Identificateur|Nom commun|Nom du fichier|
|— |— |— |
|**RGB**|||
|`AdobeRGB`|Adobe RGB (1998)|AdobeRGB1998.icc|
|`AppleRGB`|Apple RGB|Apple RGB.icc|
|`CIERGB|CIE RGB`|CIERGB.icc|
|`ColorMatchRGB`|ColorMatch RGB|ColorMatchRGB.icc|
|`NTSC`|NTSC (1953)|NTSC1953.icc|
|`PAL`|PAL/SECAM|PAL_SECAM.icc|
|`ProPhoto RGB`|ProPhoto RGB|ProPhoto RGB.icm|
|`SMPTE`|SMPTE-C|SMPTE-C.icc|
|`sRGB`|sRGB IEC61966-2.1|sRgb Color Space Profil.icm|
|`WideGamutRGB`|Wide Gamut RGB|WideGamutRGB.icc|
|**CMJN**|||
|`CoatedFogra27`|Coated FOGRA27 (ISO 12647-2:2004)|CoatedFOGRA27.icc|
|`CoatedFogra39`|Coated FOGRA39 (ISO 12647-2:2004)|CoatedFOGRA39.icc|
|`Coated GRACoL 2006 (ISO 12647-2:2004)`|Coated GRACoL 2006 (ISO 12647-2:2004)|CoatedGRACoL2006.icc|
|`EuropeISOCoated`|Europe ISO Coated FOGRA27|EuropeISOCoatedFOGRA27.icc|
|`Euroscale Coated v2`|Euroscale Coated v2|EuroscaleCoated.icc|
|`EuroscaleUncoated`|Euroscale Unenduit v2|EuroscaleUnenduit.icc|
|`JapanColorCoated`|Couleur japonaise 2001 Coated|JapanColor2001Coated.icc|
|`JapanColorNewspaper`|Journal de la couleur du Japon 2002|Journal de la couleur du Japon 2002|Journal de la couleur du Japon 2002.icc|
|`JapanColorUncoated`|Japan Color 2001 Unenduit|JapanColor2001Unenduit.icc|
|`Japan Color 2003 Web Coated`|Couleur japonaise 2003 Couleur Web Coated|JapanColor2003WebCoated.icc|
|`JapanWebCoated`|Japan Web Coated (Ad)|JapanWebCoated.icc|
|`PS4Default`|Photoshop 4 CMJN par défaut|Photoshop4DefaultCMYK.icc|
|`PS5Default`|Photoshop 5 CMJN par défaut|Photoshop5DefaultCMYK.icc|
|`SheetfedCoated`|U.S. Sheetfed Coated v2|USSheetfedCoated.icc|
|`SheetfedUncoated`|U.S. Feuille non couchée v2|USSheetfedUnenduit.icc|
|`UncoatedFogra29`|FOGRA29 non couché (ISO 12647-2:2004)|UnbeddedFOGRA29.icc|
|`US Newsprint (SNAP 2007)`|US Newsprint (SNAP 2007)|USNewsprintSNAP2007.icc|
|`WebCoated`|U.S. Web Coated (SWOP) v2|USWebCoatedSWOP.icc|
|`WebCoatedFogra28`|Web Coated FOGRA28 (ISO 12647-2:2004)|WebCoatedFOGRA28.icc|
|`Web Coated SWOP 2006 Grade 3 Paper`|Papier de 3e année avec revêtement Web SWOP 2006|Papier WebCoatedSWOP2006Grade3.icc|
|`Web Coated SWOP Grade 5 Paper`|Papier de classe 5 avec revêtement Web SWOP 2006|Papier WebCoatedSWOP2006Grade5.icc|
|`WebUncoated`|U.S. Web non couché v2|USWebUnenduit.icc|

## Voir aussi {#section-39159397e80b4efca5f631eab8b9aa06}

[Consortium](http://www.color.org/index.xalter) international de couleurs,  [icc=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-icc.md#reference-182b5679e21e4df3b4d330535a5a7517),  [iccEmbed=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-iccembed.md#reference-e3b774fb322046a2a6dde3a7bab5583e),  [attribut::IccProfile](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-iccprofilecmyk.md#reference-db89f9dac33e447cadb359ec1ba27ee0)*, attribut::IccProfileSrc*, attribut ::IccRenderIntentProfil, attribut ::IccBlackPointCompensation, attribut ::IccDitherICC  de référence de carte de , color=, bgc=,  [ *`color`*](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-data-types/r-is-http-color.md)[](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-iccprofilesrcgray.md#reference-a717831da24d43f680d01393660f12f9)[](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-iccrenderintent.md#reference-012f207f28bd4406a5368d23ed95a51f)[](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-iccblackpointcompensation.md#reference-357626375ee140d1807f0c05171c733f)[](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-iccdither.md#reference-914d0d0567364246b4016d45c0ada85b)[](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-icc-profile-map-reference/c-icc-profile-map-reference.md#concept-57b9148ce55249cd825cb7ee19ed057c)[](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-data-types/r-is-http-color.md)[](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-bgc.md#reference-53376175f617446fbe5c69120f834b88)
