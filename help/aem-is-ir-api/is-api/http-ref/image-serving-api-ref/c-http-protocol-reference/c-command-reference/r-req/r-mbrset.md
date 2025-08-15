---
description: Données à débit multi-bits.
solution: Experience Manager
title: mbrSet
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 0568a4a1-7d6a-453e-83bc-05c0cde0c0f8
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '252'
ht-degree: 0%

---

# mbrSet{#mbrset}

Données à débit multi-bits.

`req=mbrSet[,text|xml[, *`encoding`*]][&fmt= *`fmtType`*]`

<table id="simpletable_D2B8704E09B34337870A257CD7CB5C56"> 
 <tr class="strow"> 
  <td class="stentry"> <p>Encodage de <span class="codeph"><span class="varname"></span></span> </p> </td> 
  <td class="stentry"> <p><span class="codeph"> UTF-8 | UTF-16 | UTF-16LE | UTF-16BE | ISO-8859-1</span> </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"><span class="varname"> fmtType </span></span> </p></td> 
  <td class="stentry"> <p><span class="codeph"> f4m | m3u8</span> </p></td> 
 </tr> 
</table>

Renvoie une réponse de type texte ou xml contenant une liste d’URL (et de débits correspondants) qui correspondent à des entrées vidéo valides dans la visionneuse de vidéos associée à l’ID de chemin d’accès réseau.

L’exigence précédente selon laquelle une entrée vidéo valide doit contenir une valeur pour `catalog::VideoBitRate` a été assouplie. L’entrée peut contenir une valeur pour `catalog::VideoBitRate`*ou* `catalog::AudioBitRate`*ou* `catalog::TotalStreamBitRate`. Un seul de ces paramètres doit être défini pour que l’entrée vidéo soit valide. Notez que les exigences relatives à la `catalog::Path` et à une extension de fichier vidéo valide n’ont pas changé.

Les réponses sont destinées à être utilisées par les serveurs de streaming Apple et Flash et sont donc structurellement conformes à ces spécifications. Les URL sont générées à l’aide des préfixes `attribute::HttpAppleStreamingContext` et `attribute::HttpFlashStreamingContext`.

les réponses m3u8 ne contiennent que des fichiers mp4 s’il en existe dans la visionneuse de vidéos. Si aucun fichier mp4 n’est présent, ces réponses ne contiennent que des fichiers f4v. Si aucun fichier mp4 ou f4v n’est présent, la réponse est vide.

les réponses f4m contiennent uniquement les fichiers f4v s’il en existe dans la visionneuse de vidéos. Si aucun fichier f4v n’est présent, ces réponses ne contiennent que des fichiers mp4. Si aucun fichier f4v ni fichier mp4 n’est présent, la réponse est vide.

Les débits qui apparaissent dans les réponses f4m/m3u8 correspondent aux valeurs de `catalog::TotalStreamBitRate` (converties en unités appropriées). Si `catalog::TotalStreamBitRate` n’est pas défini, la somme de `catalog::VideoBitRate` et `catalog::AudioBitRate` est utilisée.

La réponse HTTP peut être mise en cache avec la TTL basée sur `catalog::NonImgExpiration`.
