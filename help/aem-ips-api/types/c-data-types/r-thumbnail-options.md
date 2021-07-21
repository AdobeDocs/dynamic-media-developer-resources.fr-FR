---
description: Type facultatif qui vous permet de choisir une image vidéo spécifique à utiliser comme image miniature.
solution: Experience Manager
title: ThumbnailOptions
feature: Dynamic Media Classic, SDK/API
role: Developer,Admin
exl-id: 7d84590d-2227-4d9a-9cb0-0f4b1fcabd8e
source-git-commit: fcda99340a18d5037157723bb3bdca5fa9df3277
workflow-type: tm+mt
source-wordcount: '100'
ht-degree: 6%

---

# ThumbnailOptions{#thumbnailoptions}

Type facultatif qui vous permet de choisir une image vidéo spécifique à utiliser comme image miniature.

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
   <td colname="col3"> <p>Définit la durée (en millisecondes à partir du démarrage de la vidéo) de l’image que vous souhaitez utiliser pour la miniature de la vidéo. Les valeurs sont comprises entre 0 et la fin de la vidéo. <p>Remarque : Le système utilise la première image de la vidéo pour la miniature si vous spécifiez incorrectement l’heure. Voir <a href="../../types/c-data-types/r-media-options.md#reference-18618fc6803a4b6e994bbb48eba93b5b" format="dita" scope="local"> MediaOptions</a>. </p></p> </td> 
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
