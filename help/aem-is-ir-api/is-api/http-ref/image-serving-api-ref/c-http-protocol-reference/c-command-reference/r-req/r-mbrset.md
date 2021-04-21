---
description: Données de débit multibits.
solution: Experience Manager
title: mbrSet
feature: Dynamic Media Classic,SDK/API
role: Developer,Business Practitioner
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '267'
ht-degree: 4%

---


# mbrSet{#mbrset}

Données de débit multibits.

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

Renvoie un texte ou une réponse xml contenant une liste d’URL (et les débits correspondants) qui correspondent à des entrées vidéo valides dans la visionneuse de vidéos associées à l’ID de chemin d’accès réseau.

La condition précédente selon laquelle une entrée vidéo valide doit contenir une valeur pour `catalog::VideoBitRate` a été maintenant assouplie. L&#39;entrée peut contenir une valeur pour `catalog::VideoBitRate`*ou* `catalog::AudioBitRate`*ou* `catalog::TotalStreamBitRate`. Un seul d&#39;entre eux doit être défini pour que l&#39;entrée vidéo soit valide. Notez que les exigences relatives à `catalog::Path` et à une extension de fichier vidéo valide n’ont pas été modifiées.

Les réponses sont destinées à la consommation par Apple et les serveurs de diffusion en flux continu de Flash et sont donc structurellement conformes à ces spécifications. Les URL sont générées à l’aide de préfixes `attribute::HttpAppleStreamingContext` et `attribute::HttpFlashStreamingContext`.

Les réponses m3u8 ne contiennent que des fichiers mp4 s’il y en a dans la visionneuse de vidéos. Si aucun fichier mp4 n’est présent, ces réponses contiennent uniquement des fichiers f4v. Si aucun fichier mp4 ou f4v n’est présent, la réponse est vide.

Les réponses f4m contiennent uniquement des fichiers f4v s’il en existe dans la visionneuse de vidéos. Si aucun fichier f4v n’est présent, ces réponses contiennent uniquement des fichiers mp4. Si aucun fichier f4v ni fichier mp4 n’est présent, la réponse est vide.

Les taux de bits qui apparaissent dans les réponses f4m/m3u8 correspondent aux valeurs de `catalog::TotalStreamBitRate` (converties en unités appropriées). Si `catalog::TotalStreamBitRate` n&#39;est pas défini, la somme de `catalog::VideoBitRate` et `catalog::AudioBitRate` est utilisée.

La réponse HTTP peut être placée en mémoire cache via le TTL basé sur `catalog::NonImgExpiration`.
