---
title: Paramètre setContainerId
description: JavaScript référence de l’API pour la visionneuse vidéo.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Video
role: Developer,User
exl-id: 9f2857a4-108d-4689-9c39-cb2635405d0d
source-git-commit: 11acb9151d3ea247eecde3cfbbd295a95c10829c
workflow-type: tm+mt
source-wordcount: '85'
ht-degree: 2%

---

# Paramètre setContainerId{#setcontainerid}

JavaScript référence de l’API pour la visionneuse vidéo.

` setContainerId( *`ID conteneur`*)`

Définit l’ID du conteneur DOM (normalement un `DIV`) dans lequel la visionneuse est insérée. Il n’est pas nécessaire que l’élément conteneur soit créé au moment de l’appel de cette méthode. Toutefois, le conteneur doit exister lors de `init()` l’exécution. Ce paramètre est appelé avant `init()`. Cette méthode est facultative si les informations de configuration de la visionneuse sont transmises `config` avec l’objet JSON au constructeur.

<table id="table_896DFF34A68A403DB93A6D597461A573"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"><span class="varname"> ID conteneur </span> </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph">{string} </span> ID du conteneur. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Retourne {#section-1d3cf85bc7cc4dfe9670e038d02b9101}

Aucune

## Exemple {#section-9e9332aa86b74a5fb321375c03fdc5b3}

```
<instance>.setContainerId("s7viewer");
```
