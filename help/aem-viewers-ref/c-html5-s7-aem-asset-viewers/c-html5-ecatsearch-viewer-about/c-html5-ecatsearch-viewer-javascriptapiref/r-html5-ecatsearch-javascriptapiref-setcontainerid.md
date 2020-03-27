---
description: Référence de l’API JavaScript pour la visionneuse de catalogue électronique.
seo-description: Référence de l’API JavaScript pour la visionneuse de catalogue électronique.
seo-title: setContainerId
solution: Experience Manager
title: setContainerId
topic: Dynamic media
uuid: 19149e38-b9d2-4ecd-a555-92e2960f7ee3
translation-type: tm+mt
source-git-commit: 2bd5b17e473ec53844b4bbcb4f13580b2d6bfaf4

---


# setContainerId{#setcontainerid}

Référence de l’API JavaScript pour la visionneuse de catalogue électronique.

[!DNL ` setContainerId( *`containerId`*)`]

Définit l’ID du `DOM` [!DNL (normalement un [!DNL `DIV`]) dans lequel le lecteur est inséré. Il n’est pas nécessaire que l’élément  soit créé au moment de l’appel de cette méthode. Toutefois, le  doit exister lors de [!DNL `init()`] l’exécution. Il doit être appelé avant [!DNL `init()`].

Cette méthode est facultative si les informations de configuration de la visionneuse sont transmises avec l’objet [!DNL `config`] JSON au constructeur.

<table id="table_896DFF34A68A403DB93A6D597461A573"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> containerId </span></span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> {string} </span> ID du . </p> </td> 
  </tr> 
 </tbody> 
</table>

## Returns {#section-1d3cf85bc7cc4dfe9670e038d02b9101}

Aucune

## Exemple {#section-9e9332aa86b74a5fb321375c03fdc5b3}

```
<instance>.setContainerId("s7viewer");
```

