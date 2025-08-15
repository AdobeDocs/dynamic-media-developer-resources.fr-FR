---
title: Paramètre setContainerId
description: JavaScript référence de l’API pour la visionneuse panoramique.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Panoramic
role: Developer,User
exl-id: b0145fb0-2b0d-40ce-ac18-029f54bc4050
source-git-commit: 8aebcacd5abdc23565aab1bc3506c36f055b6439
workflow-type: tm+mt
source-wordcount: '88'
ht-degree: 3%

---

# Paramètre setContainerId{#setcontainerid}

JavaScript référence de l’API pour la visionneuse panoramique.

` setContainerId( *`ID conteneur`*)`

Définit l’ID du conteneur DOM (normalement un DIV) dans lequel la visionneuse est insérée. Il n’est pas nécessaire que l’élément conteneur soit créé au moment de l’appel de cette méthode. Toutefois, le conteneur doit exister lors de `init()` l’exécution. Il doit être appelé avant `init()`.

Cette méthode est facultative si les informations de configuration de la visionneuse sont transmises avec l’objet `config` JSON au constructeur.

## Paramètre {#section-fa807db629ce43bab286b1e1dc96c492}

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
