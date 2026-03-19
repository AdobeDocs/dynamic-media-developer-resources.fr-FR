---
title: PanoramicViewer
description: Constructeur, crée une instance Visionneuse panoramique HTML5.
solution: Experience Manager, Experience Manager Assets
feature-set: Experience Manager, Experience Manager Assets
feature: Dynamic Media Classic,Viewers,SDK/API
role: Developer,User
source-git-commit: 07380e01e4eed6a65ba8821eee3db6fd9bb19639
workflow-type: tm+mt
source-wordcount: '161'
ht-degree: 3%

---

# PanoramicViewer{#panoramicviewer}

`PanoramicViewer([config])`
Constructeur, crée une instance Visionneuse panoramique HTML5.

## Paramètre {#section-fa807db629ce43bab286b1e1dc96c492}

config
{Object} objet de configuration JSON facultatif, vous permet de transmettre tous les paramètres de la visionneuse au constructeur et d’éviter d’appeler des méthodes setter individuelles. Il contient les propriétés suivantes :

* containerId : ID {String} du conteneur DOM (normalement un DIV) dans lequel la visionneuse est insérée. Il n’est pas nécessaire que l’élément de conteneur soit créé lors de l’appel de cette méthode. Cependant, le conteneur doit exister lorsque init() est exécuté. Obligatoire
* params - {Object} objet JSON avec les paramètres de configuration de la visionneuse où le nom de la propriété est une option de configuration spécifique à la visionneuse ou un modificateur SDK et où la valeur de cette propriété est une valeur de paramètres correspondante. Obligatoire
* gestionnaires - {Object} objet JSON avec des rappels d’événement de visionneuse, où le nom de la propriété est le nom de l’événement de visionneuse pris en charge et la valeur de la propriété est une référence de fonction JavaScript au rappel approprié. Voir la section Rappels d’événement pour plus d’informations sur les événements de visionneuse. Facultatif.


## Renvoie {#section-1d3cf85bc7cc4dfe9670e038d02b9101}

Aucune

## Exemple {#section-9e9332aa86b74a5fb321375c03fdc5b3}

```javascript {.line-numbers}
var panoramicViewer = new s7viewers.PanoramicViewer({
    "containerId":"s7viewer",
"params":{
    "asset":"Scene7SharedAssets/PanoramicImage-Sample",
    "serverurl":"http://s7d1.scene7.com/is/image/"
},
"handlers":{
    "initComplete":function() {
        console.log("init complete");
}
}
});
```
