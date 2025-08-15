---
title: Paramètre setContainerId
description: JavaScript référence de l’API pour la visionneuse de zoom de base.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Zoom
role: Developer,User
exl-id: dae07170-24bb-4e8c-86d6-5313db33736f
source-git-commit: 7eddc50fb9803eacdd1f513c6132380793b6f88d
workflow-type: tm+mt
source-wordcount: '87'
ht-degree: 2%

---

# Paramètre setContainerId{#setcontainerid}

JavaScript référence de l’API pour la visionneuse de zoom de base.

` setContainerId( *`ID conteneur`*)`

Définit l’ID du conteneur DOM (normalement un DIV) dans lequel la visionneuse est insérée. Il n’est pas nécessaire que l’élément conteneur soit créé au moment de l’appel de cette méthode. Toutefois, le conteneur doit exister lors de `init()` l’exécution. Il doit être appelé avant `init()`.

Cette méthode est facultative si les informations de configuration de la visionneuse ont été transmises `config` avec l’objet JSON au constructeur.

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
