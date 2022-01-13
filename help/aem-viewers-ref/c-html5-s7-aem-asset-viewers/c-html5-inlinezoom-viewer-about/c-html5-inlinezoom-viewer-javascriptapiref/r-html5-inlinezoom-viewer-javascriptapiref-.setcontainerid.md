---
title: setContainerId
description: Référence de l’API JavaScript pour la visionneuse de zoom intégrée.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Inline Zoom
role: Developer,User
exl-id: ab3359f0-0c58-4984-815a-e0246728100e
source-git-commit: 50dddf148345d2ca5243d5d7108fefa56d23dad6
workflow-type: tm+mt
source-wordcount: '86'
ht-degree: 2%

---

# setContainerId{#setcontainerid}

Référence de l’API JavaScript pour la visionneuse de zoom intégrée.

` setContainerId( *`containerId`*)`

Définit l’identifiant du conteneur DOM (généralement un `DIV`) dans laquelle la visionneuse est insérée. Il n’est pas nécessaire de créer l’élément de conteneur au moment de l’appel de cette méthode. Cependant, le conteneur doit exister lorsque `init()` est exécuté. Elle doit être appelée avant `init()`. Cette méthode est facultative si les informations de configuration de la visionneuse sont transmises avec `config` Objet JSON au constructeur.

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
