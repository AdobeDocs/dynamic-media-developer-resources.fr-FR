---
description: Paramètre de téléchargement pour traiter les fichiers ZIP et TAR en tant que ressources Principales (Aucun) ou pour extraire et télécharger leur contenu (UnCompress).
solution: Experience Manager
title: AnnulerCompressionOptions
feature: Dynamic Media Classic, SDK/API
role: Développeur, Administrateur
translation-type: tm+mt
source-git-commit: 052bfcbcf1bd4ccf60afa7e3325bf58dd07cba85
workflow-type: tm+mt
source-wordcount: '100'
ht-degree: 7%

---


# UnCompressOptions{#uncompressoptions}

Paramètre de téléchargement pour traiter les fichiers ZIP et TAR en tant que ressources Principales (Aucun) ou pour extraire et télécharger leur contenu (UnCompress).

>[!NOTE]
>
>`None` est définie par défaut.

## Paramètres {#section-10e49e27f60743da970a4ff1c4587eab}

<table id="table_89C2F7CDB24848459E47F1F7F58D91BA"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Nom </th> 
   <th colname="col2" class="entry"> Type </th> 
   <th colname="col3" class="entry"> Description </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> processus</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> <p>Contrôle le traitement des fichiers d’archives ZIP et TAR. Propose 2 options : 
     <ul id="ul_F34E2F3B9B74450CA7E76BD9FD7137C2">
      <li id="li_E982468ED814446593B0C0A3F3D729FB"><span class="codeph"> Aucun : </span> Traiter comme des ressources Principales. </li>
      <li id="li_4A45DA99592B4EF7A1FE0A946A835104"><span class="codeph"> UnCompress : </span> Extrait et traite le contenu. </li>
     </ul><p>Remarque : Les constantes de chaîne respectent la casse. Utilisez <span class="codeph"> UnCompress</span>, et non <span class="codeph"> uncompress</span> ou <span class="codeph"> unCompress</span>. </p></p> </td> 
  </tr> 
 </tbody> 
</table>

## Exemple {#section-48fd14af768a436284c31692038579a8}

```
 <!-- uncompress zip/tar/gzip files -->
            <element name="unCompressOptions" type="types:UnCompressOptions" minOccurs="0"/>
    <complexType name="UnCompressOptions">
        <sequence>
            <!-- Options: None (default),UnCompress -->
            <element name="process" type="xsd:string"/>
        </sequence>
    </complexType>
```

## Utilisé par {#section-b2a829cf5511412e968bb2000f85cc31}

Le type `unCompressionOptions` est utilisé par :

* [UploadDirectoryJob](../../types/c-data-types/r-upload-directory-job.md#reference-e707ebf53b074c49ad983d1886e0bbb6)
* [TéléchargerPostJob](../../types/c-data-types/r-upload-post-job.md#reference-bca2339b593f4637a687c33937215ef4)
* [UploadUrlsJob](../../types/c-data-types/r-upload-urls-job.md#reference-8e9bc895268c4321b233dbeadc990398)

