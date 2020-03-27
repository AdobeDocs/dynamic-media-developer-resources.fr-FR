---
description: Référence de l’API JavaScript pour la visionneuse de catalogue électronique.
seo-description: Référence de l’API JavaScript pour la visionneuse de catalogue électronique.
seo-title: setContainerId
solution: Experience Manager
title: setContainerId
topic: Dynamic media
uuid: 9aed8cb6-d89b-41f6-bd87-e390bb6002a5
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# setContainerId{#setcontainerid}

Référence de l’API JavaScript pour la visionneuse de catalogue électronique.

` setContainerId( *`containerId`*)`

Définit l’ID du `DOM` (habituellement un `DIV`) dans lequel le lecteur est inséré. Il n’est pas nécessaire que l’élément  soit créé au moment de l’appel de cette méthode. Toutefois, le  doit exister lors de `init()` l’exécution. Il doit être appelé avant `init()`.

Cette méthode est facultative si les informations de configuration de la visionneuse sont transmises avec l’objet `config` JSON au constructeur.

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

