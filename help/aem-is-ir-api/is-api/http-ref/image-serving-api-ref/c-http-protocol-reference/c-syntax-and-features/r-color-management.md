---
description: Image Serving prend en charge les conversions d’espace colorimétrique en fonction des d’espace colorimétrique  conformes aux spécifications ICC (International Color Consortium).
seo-description: Image Serving prend en charge les conversions d’espace colorimétrique en fonction des d’espace colorimétrique  conformes aux spécifications ICC (International Color Consortium).
seo-title: Gestion des couleurs du serveur d’images
solution: Experience Manager
title: Gestion des couleurs du serveur d’images
topic: Scene7 Image Serving - Image Rendering API
uuid: 6291372e-ec4c-4fbd-bffc-b55b1bf2f8cf
translation-type: tm+mt
source-git-commit: 4439103ccd0d63afdd9ec20bd475560e8f84dcba

---


# Gestion des couleurs du serveur d’images{#image-serving-color-management}

Image Serving prend en charge les conversions d’espace colorimétrique en fonction des d’espace colorimétrique  conformes aux spécifications ICC (International Color Consortium).

## Espaces colorimétriques par défaut {#section-8cfe60808bce49968091995e4e521dba}

Chaque catalogue d’images (et le catalogue par défaut) peut définir un ensemble de  ICC qui constituent les espaces colorimétriques par défaut de ce catalogue - une entrée et une sortie  chacune pour les données en niveaux de gris, RVB et CMJN. See ` [attribute::IccProfileRgb](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-iccprofilergb.md#reference-3479e7daac54404f84b06b98ca07b9df)`, ` [attribute::IccProfileGray](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-iccprofilegray.md#reference-13822a1596e440eea0492e86d88dad35)`, ` [attribute::IccProfileCmyk](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-iccprofilecmyk.md#reference-db89f9dac33e447cadb359ec1ba27ee0)`, ` [attribute::IccProfileSrcRgb](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-iccprofilesrcrgb.md#reference-b8e576d075b44f5c94d95bfb5aa22ae2)`, ` [attribute::IccProfileSrcGray](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-iccprofilesrcgray.md#reference-a717831da24d43f680d01393660f12f9)`, and ` [attribute::IccProfileSrcCmyk](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-iccprofilesrccmyk.md#reference-b57196dfe5db41fe88bd0828ed4ec728)`.

## Espace colorimétrique d’entrée {#section-9f08e2c1b6aa4fe4815be174972c1944}

Les images source peuvent incorporer des  ICC pour définir l’espace colorimétrique d’entrée. Si aucun  de n’est incorporé dans une image source, le catalogue `attribute::IccProfileSrc*` d’images correspondant au type de pixel de l’image source est utilisé. Si cet attribut n’est pas défini dans le catalogue d’images, `attribute::IccProfile*` est utilisé. Si cet attribut de catalogue n’est pas défini non plus, l’image n’est pas gérée par les couleurs et seules les transformations naïves sont appliquées.

## Espace colorimétrique de sortie {#section-b517bca622b64dcfa7defba6035d0716}

L’espace colorimétrique du résultat final de l’image d’une requête est défini à l’aide de la `icc=` commande. Si `icc=` n’est pas spécifié, l’espace colorimétrique de sortie par défaut (du catalogue principal de la requête) qui correspond au type de pixel de l’image de sortie est utilisé comme espace colorimétrique de sortie. Si aucun de sortie n’est défini dans le catalogue principal ou par défaut, et si le calque de base est une image avec un incorporé  correspondant au type de pixel de sortie, ce  est alors utilisé pour l’espace colorimétrique de sortie. Dans le cas contraire, l’espace colorimétrique de sortie n’est pas défini. Seules les conversions naïves de couleurs sont appliquées lors de la conversion entre les types de pixels et aucun de couleurs ne peut être incorporé dans l’image de sortie.

L’espace colorimétrique de sortie d’une requête de diffusion d’images imbriquée/incorporée est toujours identique à l’espace colorimétrique de sortie de la requête d’incorporation externe.

## Couleurs unies {#section-df03a5c5ca894e6f8b9a5ba02cf6ac03}

Les valeurs de couleur spécifiées avec `color=`, `bgcolor=`ou la commande RTF `\iscolortbl` seront associées à l’espace colorimétrique d’entrée si la valeur de couleur inclut le suffixe &quot;S&quot;, sinon elles sont associées à l’espace colorimétrique de sortie. Les valeurs de couleur spécifiées avec `bgc=` ou les commandes RTF `\colortbl` et `\cmykcolortbl` sont toujours associées à l’espace colorimétrique de sortie par défaut ou réel correspondant.

>[!NOTE]
>
>Actuellement, `bgc=` ne participe pas entièrement à la gestion des couleurs : le suffixe &quot;S&quot; est ignoré lorsqu’il est spécifié avec `bgc=`, et la conversion naïve est appliquée lorsque le type de pixel de la valeur de couleur spécifiée avec `bgc=` diffère du type de pixel de l’image de sortie. Dans le cas contraire, `bgc=` est associé à l’espace colorimétrique de sortie réel.

## Requêtes imbriquées et incorporées {#section-bdda638c31504f26a77e51ebb1ea6e3b}

L’espace colorimétrique de sortie pour les requêtes IS imbriquées et les requêtes IR incorporées est automatiquement défini sur l’espace colorimétrique de sortie de la requête la plus externe, sauf si la requête imbriquée spécifie un espace colorimétrique de sortie explicite avec `icc=`. En outre, les requêtes imbriquées/incorporées héritent également des espaces colorimétriques de sortie par défaut du catalogue principal de la requête la plus éloignée, afin d’assurer une gestion cohérente des valeurs de couleur unie.

## Conversion de l’espace colorimétrique {#section-ca87b80b8e364ea59d8a92d87121b0fb}

Le traitement d’images tente généralement de retarder les conversions de couleur pendant le traitement. Si tous les calques d’une image ont le même espace colorimétrique de calque, la conversion en espace colorimétrique de sortie est effectuée après fusion et mise à l’échelle finale. Si plusieurs espaces colorimétriques de calque sont impliqués, chaque calque est transformé en espace colorimétrique de sortie avant la fusion.

>[!NOTE]
>
>Les commandes `op_brightness=`, `op_colorbalance=`, `op_colorize=`, `op_contrast=`, `op_hue=`et `op_saturation=` sont des opérations RVB. Ces opérations conservent la fidélité des couleurs uniquement si l’espace colorimétrique du calque est de type RVB. Si elles ne sont pas RVB, les données sont converties en RVB à l’aide d’une conversion de couleur naïve, et le résultat aura une fidélité chromatique limitée. L’espace colorimétrique du calque pour ces calques doit être considéré comme indéterminé.

Les options de conversion des couleurs sont fournies avec `icc=` ou, si `icc=` elles ne sont pas spécifiées, avec `attribute::IccRenderIntent`, `attribute::IccBlackPointCompensation`et `attribute::IccDither`.

## Incorporation de de couleur {#section-261ebbae5ce046589a776ca972380052}

Le de couleurs ICC de l’espace colorimétrique de sortie, s’il est disponible, peut être incorporé dans l’image de réponse en spécifiant `iccEmbed=`.

## Gestion des  ICC {#section-eb210e4b44e64e2c8b80ee59216c5555}

Tous les de couleurs utilisés par le serveur doivent être conformes aux spécifications ICC. Les fichiers  ICC ont généralement un suffixe [!DNL .icc] ou un [!DNL .icm] fichier et sont colocalisés avec des fichiers de données image.

Bien que les  de sortie puissent être spécifiées par chemin/nom de fichier dans la `icc=` commande, il est recommandé d’enregistrer tous les fichiers  de sortie dans la carte de  ICC du catalogue d’images ou du catalogue d’images par défaut et d’utiliser des identifiants de raccourci ( `icc::Name`) au lieu des chemins d’accès aux fichiers.

Tous les ICC  référencés dans `catalog::IccProfile` et dans `attribute::IccProfile*` doivent être enregistrés dans la carte de ICC de l’image ou du catalogue par défaut.

## Restrictions {#section-fb50ede40b124b89b30679da29782ab5}

Seuls les espaces colorimétriques CMJN, RVB et Niveaux de gris sont actuellement pris en charge.

## de couleurs ICC inclus {#section-98b4a7d9f9814e8ba27d6dcf3dcf850c}

La diffusion d’images inclut la plupart des  ICC standard d’Adobe dans le catalogue d’images par défaut. Ces  sont accessibles soit par leurs noms courants (comme dans Photoshop, par exemple), soit par un identifiant un peu plus court. Le tableau suivant  tous les ICC standard . Lorsque vous référencez un dans la `icc=` commande par son nom commun, les espaces doivent être codés en tant que `%20`.

Des  supplémentaires peuvent être ajoutées au  de standard, soit au catalogue par défaut, soit à un catalogue d’images spécifique. Pour plus d’informations, reportez-vous au Guide de référence [des ](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-icc-profile-map-reference/c-icc-profile-map-reference.md#concept-57b9148ce55249cd825cb7ee19ed057c) ICC.

>[!NOTE]
>
>Le tableau suivant s’applique uniquement à *Dynamic Media Hybrid* (s’exécutant en mode `dynamicmedia` d’exécution).

|Identifiant|Nom commun|Nom du fichier||—|—|—||**RVB**||||`AdobeRGB`|Adobe RGB (1998)|AdobeRGB1998.icc||`AppleRGB`|Apple RGB|Apple RGB.icc||`CIERGB`|CIE RGB|CIERGB.icc||`ColorMatchRGB`|RVB ColorMatch|RVB ColorMatchRGB.icc||`NTSC`|NTSC (1953)|NTSC1953.icc||`PAL`|PAL/SECAM|PAL_SECAM.icc||`ProPhoto`|ProPhoto RGB|ProPhoto.icm||`SMPTE`|SMPTE-C|SMPTE-C.icc||`sRGB`|sRGB IEC61966-2.1|sRVB Color Space.icm||`WideGamutRGB`|Gamme large RVB|WideGamutRGB.icc||**CMJN**||||`CoatedFogra27`|Coated FOGRA27 (ISO 12647-2:2004)|CoatedFOGRA27.icc||`CoatedFogra39`|Coated FOGRA39 (ISO 12647-2:2004)|CoatedFOGRA39.icc||`CoatedGraCol`|Coated GRACoL 2006 (ISO 12647-2:2004)|CoatedGRACoL2006.icc||`EuropeISOCoated`|Europe ISO Coated FOGRA27|EuropeISOCoatedFOGRA27.icc||`EuroscaleCoated`|Euroscale Coated|EuroscaleCoated.icc||`EuroscaleUncoated`|Euroscale Unrevêtement v2|EuroscaleUnrevêtement.icc||`JapanColorCoated`|Couleur Japon 2001 Couleur Coated|JapanColor2001Coated.icc||`JapanColorNewspaper`|Journal couleur Japon 2002|JapanColor2002Journal.icc||`JapanColorUncoated`|Japan Color 2001 Non couché|JapanColor2001Non couché.icc||`JapanColorWebCoated`|Japan Color 2003 Web Coated|JapanColor2003WebCoated.icc||`JapanWebCoated`|Japan Web Coated (Ad)|JapanWebCoated.icc||`NewsprintSNAP2007`|US Newsprint (SNAP 2007)|USNewsprintSNAP2007.icc||`PS4Default`|Photoshop 4 CMJN par défaut|Photoshop4DefaultCMYK.icc||`PS5Default`|Photoshop 5 CMJN par défaut|Photoshop5DefaultCMYK.icc||`SheetfedCoated`|U.S. Coated v2|USSheetfedCoated.icc||`SheetfedUncoated`|U.S. Feuille non couchée v2|USSheetédéUnenduit.icc||`UncoatedFogra29`|FOGRA29 non couché (ISO 12647-2:2004)|UnrevêtementFOGRA29.icc||`WebCoated`|U.S. Web Coated (SWOP) v2|USWebCoatedSWOP.icc||`WebCoatedFogra28`|Web Coated FOGRA28 (ISO 12647-2:2004)|WebCoatedFOGRA28.icc||`WebCoatedGrade3`|Papier de 3e année 2006 avec revêtement Web|Papier de 3e année avec revêtement WebCoatedSWOP2006Grade3.icc||`WebCoatedGrade5`|Papier de classe 5 avec revêtement Web SWOP 2006|Papier WebCoatedSWOP2006Grade5.icc||`WebUncoated`|U.S. Web non couché v2|USWebUnenduit.icc|

Le tableau suivant s’applique à la diffusion d’images ** Dynamic Media Classic (Scene7) et au contenu multimédia ** dynamique (en mode `dynamicmedia_scene7` exécution).

|Identifiant|Nom commun|Nom du fichier||—|—|—||**RVB**||||`AdobeRGB`|Adobe RGB (1998)|AdobeRGB1998.icc||`AppleRGB`|Apple RGB|Apple RGB.icc||`CIERGB|CIE RGB`|CIERGB.icc||`ColorMatchRGB`|RVB ColorMatch|RVB ColorMatchRGB.icc||`NTSC`|NTSC (1953)|NTSC1953.icc||`PAL`|PAL/SECAM|PAL_SECAM.icc||`ProPhoto RGB`|ProPhoto RGB|ProPhoto RGB.icm||`SMPTE`|SMPTE-C|SMPTE-C.icc||`sRGB`|sRGB IEC61966-2.1|sRVB Color Space.icm||`WideGamutRGB`|Gamme large RVB|WideGamutRGB.icc||**CMJN**||||`CoatedFogra27`|Coated FOGRA27 (ISO 12647-2:2004)|CoatedFOGRA27.icc||`CoatedFogra39`|Coated FOGRA39 (ISO 12647-2:2004)|CoatedFOGRA39.icc||`Coated GRACoL 2006 (ISO 12647-2:2004)`|Coated GRACoL 2006 (ISO 12647-2:2004)|CoatedGRACoL2006.icc||`EuropeISOCoated`|Europe ISO Coated FOGRA27|EuropeISOCoatedFOGRA27.icc||`Euroscale Coated v2`|Euroscale Coated v2|EuroscaleCoated.icc||`EuroscaleUncoated`|Euroscale Unrevêtement v2|EuroscaleUnrevêtement.icc||`JapanColorCoated`|Couleur Japon 2001 Couleur Coated|JapanColor2001Coated.icc||`JapanColorNewspaper`|Journal couleur Japon 2002|JapanColor2002Journal.icc||`JapanColorUncoated`|Japan Color 2001 Non couché|JapanColor2001Non couché.icc||`Japan Color 2003 Web Coated`|Japan Color 2003 Web Coated|JapanColor2003WebCoated.icc||`JapanWebCoated`|Japan Web Coated (Ad)|JapanWebCoated.icc||`PS4Default`|Photoshop 4 CMJN par défaut|Photoshop4DefaultCMYK.icc||`PS5Default`|Photoshop 5 CMJN par défaut|Photoshop5DefaultCMYK.icc||`SheetfedCoated`|U.S. Coated v2|USSheetfedCoated.icc||`SheetfedUncoated`|U.S. Feuille non couchée v2|USSheetédéUnenduit.icc||`UncoatedFogra29`|FOGRA29 non couché (ISO 12647-2:2004)|UnrevêtementFOGRA29.icc||`US Newsprint (SNAP 2007)`|US Newsprint (SNAP 2007)|USNewsprintSNAP2007.icc||`WebCoated`|U.S. Web Coated (SWOP) v2|USWebCoatedSWOP.icc||`WebCoatedFogra28`|Web Coated FOGRA28 (ISO 12647-2:2004)|WebCoatedFOGRA28.icc||`Web Coated SWOP 2006 Grade 3 Paper`|Papier de 3e année 2006 avec revêtement Web|Papier de 3e année avec revêtement WebCoatedSWOP2006Grade3.icc||`Web Coated SWOP Grade 5 Paper`|Papier de classe 5 avec revêtement Web SWOP 2006|Papier WebCoatedSWOP2006Grade5.icc||`WebUncoated`|U.S. Web non couché v2|USWebUnenduit.icc|

## Voir aussi {#section-39159397e80b4efca5f631eab8b9aa06}

[International Color Consortium](http://www.color.org/index.xalter), [icc=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-icc.md#reference-182b5679e21e4df3b4d330535a5a7517), [iccEmbed=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-iccembed.md#reference-e3b774fb322046a2a6dde3a7bab5583e), [attribut::IccProfile](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-iccprofilecmyk.md#reference-db89f9dac33e447cadb359ec1ba27ee0)*, attribut ::IccProfileSrc*, attribut ::IccRenderIntent, attribut::IccBlackPointCompensation, attribut de::IccDither, ICC de référence de Carte,color=,bgc=, [](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-iccprofilesrcgray.md#reference-a717831da24d43f680d01393660f12f9)[](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-iccrenderintent.md#reference-012f207f28bd4406a5368d23ed95a51f)[](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-iccblackpointcompensation.md#reference-357626375ee140d1807f0c05171c733f)[](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-iccdither.md#reference-914d0d0567364246b4016d45c0ada85b)[](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-icc-profile-map-reference/c-icc-profile-map-reference.md#concept-57b9148ce55249cd825cb7ee19ed057c)[](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-data-types/r-is-http-color.md)[](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-bgc.md#reference-53376175f617446fbe5c69120f834b88)[*`color`*](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-data-types/r-is-http-color.md)
