---
description: ' de couleurs de sortie.'
seo-description: ' de couleurs de sortie.'
seo-title: icc
solution: Experience Manager
title: icc
topic: Scene7 Image Serving - Image Rendering API
uuid: 95a05fe5-d6b3-4118-aab4-4664ccee2850
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# icc{#icc}

 de couleurs de sortie.

icc= *`profile`*[, *`renderIntent`*[,*`blackpointComp`*]]

<table id="simpletable_DF1914FD351E4F2BA61372A52F0CFFBF"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">  <span class="varname"></span></span> </p></td> 
  <td class="stentry"> <p>de couleurs ICC. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> mode de rendu </span></span> </p></td> 
  <td class="stentry"> <p>perceptif| relatif| saturation| absolu </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> blackpointComp</span></span> </p></td> 
  <td class="stentry"> <p>1 pour activer, 0 pour désactiver la compensation des points noirs. </p></td> 
 </tr> 
</table>

*`profile`* spécifie le d’espace colorimétrique de sortie auquel l’image rendue doit être convertie si elle est différente de la  de travail. *`profile`* doit être un chemin d’accès valide `icc::Name` défini dans le mappage de  ICC d’un catalogue d’images ou d’un catalogue par défaut, ou un chemin d’accès relatif à un fichier  de (généralement avec [!DNL .icc]ou [!DNL .icm] suffixe).

>[!NOTE]
>
>*`profile`* ne peuvent pas inclure de caractères &quot;,&quot;, même si le code est HTTP.

*`renderIntent`* permet de remplacer le mode de rendu par défaut.

*`blackpointComp`* active la compensation des points noirs si le de sortie  prend en charge cette fonctionnalité.

>[!NOTE]
>
>Toutes les conversions de couleurs ne prennent pas en charge tous les *`renderIntent`* choix et *`blackpointComp`* les choix. En règle générale, ces paramètres ne sont respectés que lorsque le de sortie ICC caractérise un périphérique de sortie tel qu’une imprimante ou un moniteur. En outre, certains de sortie ICC ne prennent pas en charge tous les *`renderIntent`* choix.

## Propriétés {#section-b4042623a8ea40248c11b2153e5906b1}

Peut se produire n’importe où dans la requête. Une erreur est renvoyée si le type d’image spécifié avec `fmt=` ne correspond pas *`profile`*.

*`renderIntent`* et *`blackpointComp`* sont ignorées si elles ne sont pas compatibles avec le ICC spécifié.

Les  de périphériques de sortie CMJN sont plus susceptibles de prendre en charge différents modes de rendu.

## Par défaut {#section-bbd3206fdcac4dc48a08fc9eba14fc90}

Si la gestion des couleurs est activée et `icc=` n’est pas spécifiée, le serveur distribue l’image convertie dans le de sortie ( `attribute::IccProfile*`) correspondant au type d’image spécifié par `fmt=`.

S’il n’est pas spécifié, *`renderIntent`* est hérité de `attribute::IccRenderIntent`et *`blackpointComp`* est hérité de `attribute::IccBlackPointCompensation`.

## Voir aussi {#section-37ef83149fd74345956a98f633cc0294}

[Gestion](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-syntax-and-features/c-ir-color-management.md#concept-7bac7c2c41be42c1b301eae80abe6b8d)des couleurs, [attribut::IccProfile*](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-iccprofilecmyk.md#reference-55aead2d924847ffbd1be4c46add7127), [iccEmbed=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-iccembed.md#reference-47a433138c7c4b29b9b29871b2491a7f), [fmt=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-fmt.md#reference-4c743f67d56b47c5b774fcc900ff758c), attribut ::IccRenderIntent, attribut ::IccBlackPointCompensation[](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-iccrenderintent.md#reference-3b80b7a4c25545a593c5076f318b5c40)[](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-iccblackpointcompensation.md#reference-d939b0cdf6564baaa88deb1059e3b7f0)
