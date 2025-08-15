---
title: cpi
description: Profil de couleurs de sortie.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 39b25f7c-ed3c-4132-8241-e7f3aab07b00
source-git-commit: 3be1d948ac22f907169ef09b509f1cebceaec5c4
workflow-type: tm+mt
source-wordcount: '234'
ht-degree: 1%

---

# cpi{#icc}

Profil de couleurs de sortie.

icc= *`profile`*[, *`renderIntent`*[,*`blackpointComp`*]]

<table id="simpletable_DF1914FD351E4F2BA61372A52F0CFFBF"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> profil</span></span> </p></td> 
  <td class="stentry"> <p>Profil de couleurs ICC. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> renderIntent </span> </span> </p></td> 
  <td class="stentry"> <p>perceptif | relatif | saturation | absolu </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> blackpointComp</span> </span> </p></td> 
  <td class="stentry"> <p>1 pour activer, 0 pour désactiver la compensation du point de noir. </p></td> 
 </tr> 
</table>

*`profile`* Indique le profil de l’espace colorimétrique de sortie vers lequel l’image rendue doit être convertie si elle est différente du profil en cours d’utilisation. *`profile`* Doit être un `icc::Name` valide défini dans la carte de profil ICC d’un catalogue d’images ou d’un catalogue par défaut, ou un chemin d’accès relatif à un fichier de profil (généralement avec un suffixe [!DNL `.icc`] ou [!DNL `.icm`]).

>[!NOTE]
>
>*`profile`* Ne peut pas inclure de caractères « , », même s’ils sont codés en HTTP.

*`renderIntent`* Permet de remplacer l’intention de rendu par défaut.

*`blackpointComp`* Active la compensation du point de noir si le profil de sortie prend en charge cette fonctionnalité.

>[!NOTE]
>
>Toutes les conversions de couleurs ne prennent pas en charge tous les choix *`renderIntent`* et *`blackpointComp`*. En règle générale, ces paramètres ne sont respectés que lorsque le profil de sortie ICC caractérise un périphérique de sortie tel qu’une imprimante ou un moniteur. En outre, certains profils de sortie ICC ne prennent pas en charge tous les choix *`renderIntent`*.

## Propriétés {#section-b4042623a8ea40248c11b2153e5906b1}

Peut se produire n’importe où dans la requête. Une erreur est renvoyée si le type d’image spécifié avec `fmt=` ne correspond pas à *`profile`*.

Les *`renderIntent`* et *`blackpointComp`* sont ignorés s’ils ne sont pas compatibles avec le profil ICC spécifié.

Les profils de périphérique de sortie CMJN sont plus susceptibles de prendre en charge différentes intentions de rendu.

## Par défaut {#section-bbd3206fdcac4dc48a08fc9eba14fc90}

Si la gestion des couleurs est activée et que `icc=` n’est pas spécifié, le serveur diffuse l’image convertie en profil de sortie ( `attribute::IccProfile*`) correspondant au type d’image spécifié avec `fmt=`.

Si elle n’est pas spécifiée, *`renderIntent`* est hérité de `attribute::IccRenderIntent` et *`blackpointComp`* est hérité de `attribute::IccBlackPointCompensation`.

## Voir aussi {#section-37ef83149fd74345956a98f633cc0294}

[Gestion des couleurs](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-syntax-and-features/c-ir-color-management.md#concept-7bac7c2c41be42c1b301eae80abe6b8d), [attribute::IccProfile*](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-iccprofilecmyk.md#reference-55aead2d924847ffbd1be4c46add7127), [iccEmbed=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-iccembed.md#reference-47a433138c7c4b29b9b29871b2491a7f), [fmt=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-fmt.md#reference-4c743f67d56b47c5b774fcc900ff758c), [attribute::IccRenderIntent](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-iccrenderintent.md#reference-3b80b7a4c25545a593c5076f318b5c40), [attribute::IccBlackPointCompensation](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-iccblackpointcompensation.md#reference-d939b0cdf6564baaa88deb1059e3b7f0)
