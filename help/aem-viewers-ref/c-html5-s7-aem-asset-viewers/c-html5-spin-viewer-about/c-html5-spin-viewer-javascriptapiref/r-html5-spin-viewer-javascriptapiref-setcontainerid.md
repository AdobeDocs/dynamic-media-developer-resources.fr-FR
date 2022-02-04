---
title: setContainerId
description: Référence de l’API JavaScript pour la visionneuse à 360°.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Spin Sets
role: Developer,User
exl-id: 5859800f-7d01-4c32-a67f-211578d5c50b
source-git-commit: 6f838470a7bdea8e8c0219e59746ec82ecd802a8
workflow-type: tm+mt
source-wordcount: '86'
ht-degree: 2%

---

# setContainerId{#setcontainerid}

Référence de l’API JavaScript pour la visionneuse à 360°.

` setContainerId( *`containerId`*)`

Définit l’identifiant du conteneur DOM (normalement un DIV) dans lequel la visionneuse est insérée. Il n’est pas nécessaire de créer l’élément de conteneur au moment de l’appel de cette méthode. Cependant, le conteneur doit exister lorsque `init()` est exécuté. Elle doit être appelée avant `init()`.

Cette méthode est facultative si les informations de configuration de la visionneuse sont transmises avec `config` Objet JSON au constructeur.

<table id="table_896DFF34A68A403DB93A6D597461A573"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> containerId </span> </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> {string} </span> ID du conteneur. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Renvoie {#section-1d3cf85bc7cc4dfe9670e038d02b9101}

Aucune

## Exemple {#section-9e9332aa86b74a5fb321375c03fdc5b3}

```
<instance>.setContainerId("s7viewer");
```
