---
description: Type facultatif qui vous permet de choisir une image vidéo particulière à utiliser comme image miniature.
seo-description: Type facultatif qui vous permet de choisir une image vidéo particulière à utiliser comme image miniature.
seo-title: ThumbnailOptions
solution: Experience Manager
title: ThumbnailOptions
topic: Dynamic Media Image Production System API
uuid: 50b2ecee-8396-4323-83e1-1f5060bec6c4
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '113'
ht-degree: 5%

---


# ThumbnailOptions{#thumbnailoptions}

Type facultatif qui vous permet de choisir une image vidéo particulière à utiliser comme image miniature.

Syntaxe

## Paramètres {#section-b1777bf868764a7099d4a954b471856c}

<table id="table_C71FD0C995D94CE18994CDA2DC3460DF"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Nom </th> 
   <th colname="col2" class="entry"> Type </th> 
   <th colname="col3" class="entry"> Description </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> thumbnailTime</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:long</span> </td> 
   <td colname="col3"> <p>Définit la durée (en millisecondes depuis le début vidéo) de l’image à utiliser pour la miniature vidéo. Les valeurs sont comprises entre 0 et la fin de la vidéo. <p>Remarque : Le système utilise la première image de la vidéo pour la miniature si vous spécifiez l’heure de manière incorrecte. Voir <a href="../../types/c-data-types/r-media-options.md#reference-18618fc6803a4b6e994bbb48eba93b5b" format="dita" scope="local"> MediaOptions</a>. </p></p> </td> 
  </tr> 
 </tbody> 
</table>

## Exemple {#section-ce3b59c60fea4cd4945427a025051447}

```
<complexType name="ThumbnailOptions">
     <sequence>
        <element name="thumbnailTime" type="xsd:long" minOccurs="0"/>
      </sequence>
</complexType>
```

