---
description: Données de débit multi-bits.
solution: Experience Manager
title: mbrSet
feature: Dynamic Media Classic, SDK/API
role: Developer,User
exl-id: 0568a4a1-7d6a-453e-83bc-05c0cde0c0f8
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '264'
ht-degree: 4%

---

# mbrSet{#mbrset}

Données de débit multi-bits.

`req=mbrSet[,text|xml[, *``*]][&fmt= *`encodingfmtType`*]`

<table id="simpletable_D2B8704E09B34337870A257CD7CB5C56"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"><span class="varname"> encodage</span></span> </p> </td> 
  <td class="stentry"> <p><span class="codeph"> UTF-8 | UTF-16 | UTF-16LE | UTF-16BE | ISO-8859-1</span> </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"><span class="varname"> fmtType</span></span> </p></td> 
  <td class="stentry"> <p><span class="codeph"> f4m | m3u8</span> </p></td> 
 </tr> 
</table>

Renvoie une réponse texte ou xml contenant une liste d’URL (et les débits en bits correspondants) qui correspondent à des entrées vidéo valides dans la visionneuse de vidéos associée à l’identifiant de chemin d’accès net.

L’exigence précédente qu’une entrée vidéo valide contienne une valeur pour `catalog::VideoBitRate` a désormais été assouplie. L’entrée peut contenir une valeur pour `catalog::VideoBitRate`*ou* `catalog::AudioBitRate`*ou* `catalog::TotalStreamBitRate`. Une seule d’entre elles doit être définie pour que l’entrée vidéo soit valide. Notez que les exigences pour `catalog::Path` et une extension de fichier vidéo valide n’ont pas changé.

Les réponses sont destinées à être utilisées par Apple et les serveurs de diffusion en continu de Flash et sont donc structurellement conformes à ces spécifications. Les URL sont générées à l’aide de préfixes `attribute::HttpAppleStreamingContext` et `attribute::HttpFlashStreamingContext`.

Les réponses m3u8 ne contiennent que des fichiers mp4 s’ils existent dans la visionneuse de vidéos. Si aucun fichier mp4 n’est présent, ces réponses ne contiennent que des fichiers f4v. Si aucun fichier mp4 ou f4v n’est présent, la réponse est vide.

Les réponses f4m contiennent uniquement des fichiers f4v s’il existe des fichiers dans la visionneuse de vidéos. Si aucun fichier f4v n’est présent, ces réponses contiennent uniquement des fichiers mp4. Si aucun fichier f4v ni fichier mp4 n’est présent, la réponse est vide.

Les taux de bit qui apparaissent dans les réponses f4m/m3u8 correspondent aux valeurs de `catalog::TotalStreamBitRate` (converties en unités appropriées). Si `catalog::TotalStreamBitRate` n’est pas défini, la somme de `catalog::VideoBitRate` et `catalog::AudioBitRate` est utilisée.

La réponse HTTP peut être placée en mémoire cache via le TTL basé sur `catalog::NonImgExpiration`.
