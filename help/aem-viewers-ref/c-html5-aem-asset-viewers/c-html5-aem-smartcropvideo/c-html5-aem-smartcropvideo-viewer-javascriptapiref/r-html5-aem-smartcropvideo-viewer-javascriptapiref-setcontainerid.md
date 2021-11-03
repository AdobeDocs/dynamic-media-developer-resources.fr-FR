---
description: Référence de l’API JavaScript pour la visionneuse de vidéos avec recadrage intelligent.
solution: Experience Manager
title: setContainerId
feature: Dynamic Media Classic,Viewers,SDK/API,Smart Crop Video
role: Developer,User
exl-id: 9f2857a4-108d-4689-9c39-cb2635405d0d
source-git-commit: bdef251dcbb7c135d02813e9fd82e2e5e32300cc
workflow-type: tm+mt
source-wordcount: '89'
ht-degree: 2%

---

# setContainerId{#setcontainerid}

Référence de l’API JavaScript pour la visionneuse de vidéos avec recadrage intelligent.

` setContainerId( *`containerId`*)`

Définit l’identifiant du conteneur DOM (généralement un `DIV`) dans laquelle la visionneuse est insérée. Il n’est pas nécessaire de créer l’élément de conteneur au moment de l’appel de cette méthode. Cependant, le conteneur doit exister lorsque `init()` est exécuté. Ce paramètre est appelé avant `init()`. Cette méthode est facultative si les informations de configuration de la visionneuse sont transmises avec `config` Objet JSON au constructeur.

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
