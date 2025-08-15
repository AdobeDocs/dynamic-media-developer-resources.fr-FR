---
description: Génère une image miniature pour votre vidéo.
solution: Experience Manager
title: Options médias
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: f37d935d-fe74-4878-8477-d2144d58d982
source-git-commit: f42378a20b58e4c5ebc961c6526d7cecabc2ae38
workflow-type: tm+mt
source-wordcount: '124'
ht-degree: 4%

---

# [!DNL MediaOptions]{#mediaoptions}

Génère une image miniature pour votre vidéo.

Syntaxe

## Paramètres {#section-2fc9bea56b6d4b72b80d4f04c5f9b862}

<table id="table_04100BB8ABD84EF68B0A7CE3AD946414"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Nom </th> 
   <th colname="col2" class="entry"> Type </th> 
   <th colname="col3" class="entry"> Description </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <span class="codeph"><span class="varname"> Tableau des préréglages</span> de codage vidéo </span> </td> 
   <td colname="col2"> <span class="codeph"> types :HandleArray</span> </td> 
   <td colname="col3">Un ensemble de <span class="codeph"> PropertySet</span> gère le référencement des paramètres prédéfinis de codage vidéo pour le transcodage de vidéos. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"><span class="varname"> générer la miniature</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd :booléen</span> </td> 
   <td colname="col3"> Si la valeur est true, la première image de la vidéo est extraite et utilisée comme image miniature. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"><span class="varname"> thumbnailOptions</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> types :ThumbnailOptions</span> </td> 
   <td colname="col3">Optionnel. Vous permet de choisir une image vidéo particulière à utiliser comme image miniature. <p>Pour spécifier une image miniature, transmettez l’heure (en millisecondes à compter du début de la vidéo) pour l’image que vous souhaitez utiliser. Les valeurs sont comprises entre 0 et la fin de la vidéo. <p>Remarque : Si vous spécifiez l’heure de manière incorrecte, <span class="codeph"> generateThumbnail</span> prend la valeur true par défaut. </p></p><p>Voir <a href="../../types/c-data-types/r-thumbnail-options.md#reference-370088b0a4ce4096b9b3e5489a368b5c" format="dita" scope="local"> Options des miniatures</a>. </p></td> 
  </tr> 
 </tbody> 
</table>

## Exemple {#section-a9356de782d74af6933c39fa7ad12212}

```
<complexType name="MediaOptions">
        <sequence>
            <element name="videoEncodingPresetsArray" type="types:HandleArray" minOccurs="0"/>
            <element name="generateThumbnail" type="xsd:boolean" minOccurs="0"/>
            <element name="thumbnailOptions" type="types:ThumbnailOptions" minOccurs="0"/>
        </sequence>
    </complexType>
```

## Utilisé par {#section-87cb83407198432c95eaa2db9f12f9db}

Le `mediaOptions` type est utilisé par :

* [Tâche d’annuaire de téléchargement](../../types/c-data-types/r-upload-directory-job.md#reference-e707ebf53b074c49ad983d1886e0bbb6)
* [UploadPostJob](../../types/c-data-types/r-upload-post-job.md#reference-bca2339b593f4637a687c33937215ef4)
* [UploadURLsJob](../../types/c-data-types/r-upload-urls-job.md#reference-8e9bc895268c4321b233dbeadc990398)
