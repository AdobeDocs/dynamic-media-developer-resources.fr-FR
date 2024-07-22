---
title: icc
description: Profil de couleurs de sortie.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 8be7be8c-a23d-4a5b-93e4-44231155616b
source-git-commit: 38f3e425be0ce3e241fc18b477e3f68b7b763b51
workflow-type: tm+mt
source-wordcount: '283'
ht-degree: 1%

---

# icc{#icc}

Profil de couleurs de sortie.

`icc= *`object`*[, *`renderIntent`*[, *`blackpointComp`*[, *`dither`*]]`

<table id="simpletable_AC20916999004CDCBBB9888B3A8FB0A7"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> objet</span> </span> </p></td> 
  <td class="stentry"> <p>Profil colorimétrique ICC. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> renderIntent</span></span> </p></td> 
  <td class="stentry"> <p><span class="codeph"> perception|relative|saturation|absolu</span>. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> blackpointComp</span></span> </p></td> 
  <td class="stentry"> <p>1 pour activer, 0 pour désactiver la compensation du point noir. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> dither</span></span> </p></td> 
  <td class="stentry"> <p>1 pour activer, 0 pour désactiver le tramage. </p></td> 
 </tr> 
</table>

La valeur *`object`* spécifie le profil d’espace colorimétrique de sortie auquel l’image doit être convertie si elle est différente du profil de travail. La valeur *`profile`* doit être soit une valeur `icc::Name` valide définie dans la carte de profil ICC d’un catalogue d’images ou d’un catalogue par défaut, soit un chemin d’accès relatif à un fichier de profil (généralement avec le suffixe [!DNL .icc] ou [!DNL .icm]). Voir [*`object`*](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-data-types/r-object.md#reference-2591bd24548d462782c68d138ef795a0) pour plus d’informations.

>[!NOTE]
>
>La valeur *`object`* peut ne pas inclure de caractères &quot;,&quot;, même si elle est codée en HTTP.

La valeur *`renderIntent`* permet de remplacer l’intention de rendu par défaut.

La valeur *`blackpointComp`* active la compensation du point noir si le profil de sortie prend en charge cette fonctionnalité.

>[!NOTE]
>
>Toutes les conversions de couleurs ne prennent pas en charge tous les choix *`renderIntent`* et *`blackpointComp`*. En règle générale, ces paramètres ne sont respectés que lorsque le profil de sortie ICC caractérise un périphérique de sortie tel qu’une imprimante ou un moniteur. En outre, certains profils de sortie ICC ne prennent pas en charge tous les choix *`renderIntent`*.

Note

Le modificateur *`dither`* active le tramage (en fait, la diffusion d’erreur), ce qui peut éviter ou réduire les artefacts de bandes de couleurs.

## Propriétés {#section-9fcd3e7bd1fd43c887b0f18a2f3c7259}

Attribut de requête. Le serveur renvoie une erreur si un type d’image est spécifié avec `fmt=` qui ne correspond pas à *`profile`*.

Les modificateurs *`renderIntent`* et *`blackpointComp`* sont ignorés s’ils ne sont pas compatibles avec le profil ICC spécifié. Les profils d’appareils de sortie CMJN sont plus susceptibles de prendre en charge différents modes de rendu.

## Par défaut {#section-0b9fe2eb428447df8ae9948f11ab5aae}

Si la gestion des couleurs est activée et que `icc=` n&#39;est pas spécifié, le serveur diffuse l&#39;image convertie dans le profil de sortie ( `attribute::IccProfile*`) correspondant au type d&#39;image spécifié avec `fmt=`.

Si elle n’est pas spécifiée, *`renderIntent`* est hérité de `attribute::IccRenderIntent`, *`blackpointComp`* est hérité de `attribute::IccBlackPointCompensation` et *`dither`* est hérité de `attribute::IccDither`.

## Voir aussi {#section-37f16b0c2c4b48f3a39dcde2a350f91e}

[attribute::IccProfile*](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-iccprofilecmyk.md#reference-db89f9dac33e447cadb359ec1ba27ee0) , [attribute::IccRenderIntent](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-iccrenderintent.md#reference-012f207f28bd4406a5368d23ed95a51f), [attribute::IccBlackPointCompensation](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-iccblackpointcompensation.md#reference-357626375ee140d1807f0c05171c733f), [attribute::IccDither](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-iccdither.md#reference-914d0d0567364246b4016d45c0ada85b), [fmt=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-fmt.md#reference-cdf10043423b45ba9fe15157fb3ae37a), [object](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-data-types/r-object.md#reference-2591bd24548d462782c68d138ef795a0), [Color Management](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-color-management.md#reference-c7e4a72d589145189f7e4bcb6b4544d7) [Référence de carte de profil ICC](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-icc-profile-map-reference/c-icc-profile-map-reference.md#concept-57b9148ce55249cd825cb7ee19ed057c), [iccEmbed=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-iccembed.md#reference-e3b774fb322046a2a6dde3a7bab5583e)
