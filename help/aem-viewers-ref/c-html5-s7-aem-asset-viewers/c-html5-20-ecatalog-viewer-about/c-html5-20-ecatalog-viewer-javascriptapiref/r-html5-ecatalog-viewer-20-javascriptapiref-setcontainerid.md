---
title: Paramètre setContainerId
description: JavaScript référence de l’API pour la visionneuse de catalogue électronique.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog
role: Developer,User
exl-id: 32e75d36-cc9a-42df-95e8-5b48456296e9
source-git-commit: edc127dc6e2ae2d9bd5feed08c8bc896c8c39747
workflow-type: tm+mt
source-wordcount: '84'
ht-degree: 2%

---

# Paramètre setContainerId{#setcontainerid}

JavaScript référence de l’API pour la visionneuse de catalogue électronique.

` setContainerId( *`ID conteneur`*)`

Définit l’ID du `DOM` conteneur (normalement un `DIV`) dans lequel la visionneuse est insérée. Il n’est pas nécessaire que l’élément conteneur soit créé au moment de l’appel de cette méthode. Toutefois, le conteneur doit exister lors de `init()` l’exécution. Il doit être appelé avant `init()`.

Cette méthode est facultative si les informations de configuration de la visionneuse sont transmises `config` avec l’objet JSON au constructeur.

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
