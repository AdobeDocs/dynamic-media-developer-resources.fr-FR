---
description: Référence de l’API JavaScript pour la visionneuse de catalogue électronique.
seo-description: Référence de l’API JavaScript pour la visionneuse de catalogue électronique.
seo-title: setContainerId
solution: Experience Manager
title: setContainerId
topic: Dynamic media
uuid: 19149e38-b9d2-4ecd-a555-92e2960f7ee3
translation-type: tm+mt
source-git-commit: 515fcf8488eba7d9ca501a4182eaa73f1936488b
workflow-type: tm+mt
source-wordcount: '91'
ht-degree: 2%

---


# setContainerId{#setcontainerid}

Référence de l’API JavaScript pour la visionneuse de catalogue électronique.

[!DNL ` setContainerId( *`containerId`*)`]

Définit l’ID du `DOM` conteneur (habituellement un `DIV`) dans lequel la visionneuse est insérée. Il n’est pas nécessaire de créer l’élément de conteneur au moment de l’appel de cette méthode. Cependant, le conteneur doit exister lors de `init()` l’exécution. Il doit être appelé avant `init()`.

Cette méthode est facultative si les informations de configuration de la visionneuse sont transmises avec l’objet `config` JSON au constructeur.

<table id="table_896DFF34A68A403DB93A6D597461A573"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> containerId </span> </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> {string} </span> ID du conteneur. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Returns {#section-1d3cf85bc7cc4dfe9670e038d02b9101}

Aucune

## Exemple {#section-9e9332aa86b74a5fb321375c03fdc5b3}

```
<instance>.setContainerId("s7viewer");
```

