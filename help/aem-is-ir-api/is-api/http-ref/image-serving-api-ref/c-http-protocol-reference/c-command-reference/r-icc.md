---
description: Profil de couleur cible.
seo-description: Profil de couleur cible.
seo-title: icc
solution: Experience Manager
title: icc
topic: Dynamic Media Image Serving - Image Rendering API
uuid: cfbd18aa-cbba-4085-920d-1f54645d0f89
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '271'
ht-degree: 5%

---


# icc{#icc}

Profil de couleur cible.

`icc= *``*[, *``*[, *``*[, *`objectrenderIntentblackpointCompdither`*]]`

<table id="simpletable_AC20916999004CDCBBB9888B3A8FB0A7"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> objet</span> </span> </p></td> 
  <td class="stentry"> <p>PROFIL de couleur ICC. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> renderIntent</span></span> </p></td> 
  <td class="stentry"> <p><span class="codeph"> perceptuel|relatif|saturation|absolu</span>. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> blackpointComp</span></span> </p></td> 
  <td class="stentry"> <p>1 pour activer, 0 pour désactiver la compensation des points noirs. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> dither</span></span> </p></td> 
  <td class="stentry"> <p>1 pour activer, 0 pour désactiver l’infiltration. </p></td> 
 </tr> 
</table>

*`object`* spécifie le profil d’espace colorimétrique de sortie auquel l’image doit être convertie si elle est différente du profil de travail. *`profile`* doit être un chemin d’accès valide  `icc::Name` défini dans la carte de profil ICC d’un catalogue d’images ou d’un catalogue par défaut, ou un chemin d’accès relatif à un fichier de profil (généralement avec  [!DNL .icc] ou  [!DNL .icm] un suffixe). Voir [ *`object`*](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-data-types/r-object.md#reference-2591bd24548d462782c68d138ef795a0)pour plus d&#39;informations.

>[!NOTE]
>
>*`object`* ne peut pas inclure de caractères &quot;,&quot;, même si le code est HTTP.

*`renderIntent`* permet de remplacer le mode de rendu par défaut.

*`blackpointComp`* active la compensation des points noirs si le profil de sortie prend en charge cette fonctionnalité.

>[!NOTE]
>
>Toutes les conversions de couleurs ne prennent pas en charge tous les choix *`renderIntent`* et *`blackpointComp`*. En règle générale, ces paramètres ne sont respectés que lorsque le profil de sortie ICC caractérise un périphérique de sortie tel qu’une imprimante ou un moniteur. En outre, certains profils de sortie ICC ne prennent pas en charge tous les choix *`renderIntent`*.

Note

*`dither`* permet l&#39;entrelacement (en fait la diffusion d&#39;erreurs), ce qui peut éviter ou réduire les artefacts de bandes de couleur.

## Propriétés {#section-9fcd3e7bd1fd43c887b0f18a2f3c7259}

Attribut de requête. Le serveur renvoie une erreur si un type d&#39;image est spécifié avec `fmt=` qui ne correspond pas à *`profile`*.

*`renderIntent`* et  *`blackpointComp`* sont ignorées si elles ne sont pas compatibles avec le profil ICC spécifié. Les profils des périphériques de sortie CMJN sont plus susceptibles de prendre en charge différents modes de rendu.

## Par défaut {#section-0b9fe2eb428447df8ae9948f11ab5aae}

Si la gestion des couleurs est activée et que `icc=` n’est pas spécifié, le serveur diffuse l’image convertie au profil de sortie ( `attribute::IccProfile*`) correspondant au type d’image spécifié avec `fmt=`.

Si elle n&#39;est pas spécifiée, *`renderIntent`* est hérité de `attribute::IccRenderIntent`, *`blackpointComp`* est hérité de `attribute::IccBlackPointCompensation` et *`dither`* est hérité de `attribute::IccDither`.

## Voir aussi {#section-37f16b0c2c4b48f3a39dcde2a350f91e}

[attribut ::IccProfile*](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-iccprofilecmyk.md#reference-db89f9dac33e447cadb359ec1ba27ee0) ,  [attribut ::IccRenderIntent](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-iccrenderintent.md#reference-012f207f28bd4406a5368d23ed95a51f),  [attribut ::IccBlackPointCompensation](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-iccblackpointcompensation.md#reference-357626375ee140d1807f0c05171c733f),  [attribut ::IccDither](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-iccdither.md#reference-914d0d0567364246b4016d45c0ada85b), fmt=, objetProfil,  de gestion des couleurs,  de référence de carte de  ICC,  iccEmbed=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-iccembed.md#reference-e3b774fb322046a2a6dde3a7bab5583e)[](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-fmt.md#reference-cdf10043423b45ba9fe15157fb3ae37a)[](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-data-types/r-object.md#reference-2591bd24548d462782c68d138ef795a0)[](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-color-management.md#reference-c7e4a72d589145189f7e4bcb6b4544d7)[](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-icc-profile-map-reference/c-icc-profile-map-reference.md#concept-57b9148ce55249cd825cb7ee19ed057c)[
