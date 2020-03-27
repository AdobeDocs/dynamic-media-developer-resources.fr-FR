---
description: Données de débit multibit.
seo-description: Données de débit multibit.
seo-title: mbrSet
solution: Experience Manager
title: mbrSet
topic: Scene7 Image Serving - Image Rendering API
uuid: 829c44ce-c66a-49a9-ba69-9e8e94ef8921
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# mbrSet{#mbrset}

Données de débit multibit.

`req=mbrSet[,text|xml[, *``*]][&fmt= *`encodingfmtType`*]`

<table id="simpletable_D2B8704E09B34337870A257CD7CB5C56"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"><span class="varname"> encodage</span></span> </p> </td> 
  <td class="stentry"> <p><span class="codeph"> UTF-8| UTF-16| UTF-16LE| UTF-16BE| ISO-8859-1</span> </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"><span class="varname"> fmtType</span></span> </p></td> 
  <td class="stentry"> <p><span class="codeph"> f4m| m3u8</span> </p></td> 
 </tr> 
</table>

Renvoie une réponse texte ou xml contenant un d’URL (et les débits correspondants) qui correspondent à des entrées vidéo valides dans la visionneuse de vidéos associées à l’ID de chemin d’accès réseau.

La condition précédente selon laquelle une entrée vidéo valide contient une valeur pour `catalog::VideoBitRate` a été assouplie. L’entrée peut contenir une valeur pour `catalog::VideoBitRate`*ou *`catalog::AudioBitRate`*ou* `catalog::TotalStreamBitRate`. Seul l’un d’eux doit être défini pour que l’entrée vidéo soit valide. Notez que les conditions requises pour `catalog::Path` et une extension de fichier vidéo valide n’ont pas changé.

Les réponses sont destinées à la consommation par les serveurs de diffusion en flux continu Apple et Flash et sont donc structurellement conformes à ces spécifications. Les URL sont générées à l’aide de préfixes `attribute::HttpAppleStreamingContext` et `attribute::HttpFlashStreamingContext`.

Les réponses m3u8 contiennent uniquement des fichiers mp4 s’il y en a dans la visionneuse de vidéos. Si aucun fichier mp4 n’est présent, ces réponses contiennent uniquement des fichiers f4v. Si aucun fichier mp4 ou f4v n’est présent, la réponse est vide.

Les réponses f4m contiennent uniquement des fichiers f4v s’il y en a dans la visionneuse de vidéos. Si aucun fichier f4v n’est présent, ces réponses contiennent uniquement des fichiers mp4. Si aucun fichier f4v ni fichier mp4 n’est présent, la réponse est vide.

Les taux de bits qui apparaissent dans les réponses f4m/m3u8 correspondent aux valeurs dans `catalog::TotalStreamBitRate` (converties en unités appropriées). Si `catalog::TotalStreamBitRate` n’est pas défini, la somme de `catalog::VideoBitRate` et `catalog::AudioBitRate` est utilisée.

La réponse HTTP peut être placée en mémoire cache via le TTL basé sur `catalog::NonImgExpiration`.
