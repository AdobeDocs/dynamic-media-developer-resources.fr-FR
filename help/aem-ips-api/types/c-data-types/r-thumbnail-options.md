---
description: Type facultatif permettant de choisir une image vidéo particulière à utiliser comme miniature.
solution: Experience Manager
title: ThumbnailOptions
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 7d84590d-2227-4d9a-9cb0-0f4b1fcabd8e
TQID: 'https://experienceleague.adobe.com/jwSdazwO-DxdDktvMfk7jC3Os3YL5IkE6hyi-eKwaoE'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: c66ffd68-0f65-42bb-aa23-b4020f12e0bdid: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 70c478ebbe0b38d9e35c1bb26074a458c0197b2b
workflow-type: tm+mt
source-wordcount: 94
ht-degree: 6%

---

# [!DNL ThumbnailOptions]{#thumbnailoptions}

Type facultatif permettant de choisir une image vidéo particulière à utiliser comme miniature.

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
   <td colname="col1"> <span class="codeph"> <span class="varname"> thumbnailTime </span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:long</span> </td> 
   <td colname="col3"> <p>Définit l’heure (en millisecondes à partir du début de la vidéo) de l’image que vous souhaitez utiliser pour la miniature de la vidéo. Les valeurs sont comprises entre 0 et la fin de la vidéo. <p>Remarque : le système utilise la première image de la vidéo pour la miniature si vous indiquez l’heure de manière incorrecte. Voir <a href="../../types/c-data-types/r-media-options.md#reference-18618fc6803a4b6e994bbb48eba93b5b" format="dita" scope="local"> MediaOptions</a>. </p></p> </td> 
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

