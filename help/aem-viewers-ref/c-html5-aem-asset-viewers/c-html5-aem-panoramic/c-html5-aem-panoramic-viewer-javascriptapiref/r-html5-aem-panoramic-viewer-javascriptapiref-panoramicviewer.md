---
title: Visualiseur panoramique
description: Constructeur, crée une instance de visionneuse panoramique HTML5.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Panoramic
role: Developer,User
source-git-commit: 38f3e425be0ce3e241fc18b477e3f68b7b763b51
workflow-type: tm+mt
source-wordcount: '161'
ht-degree: 3%

---

# Visualiseur panoramique{#panoramicviewer}

`PanoramicViewer([config])`Constructeur, crée une instance de visionneuse panoramique HTML5.

## Paramètre {#section-fa807db629ce43bab286b1e1dc96c492}

Fichier de configuration
{Object} objet de configuration JSON facultatif, vous permet de transmettre tous les paramètres de visionneuse au constructeur et d’éviter d’appeler des méthodes de setter individuelles. Il contient les propriétés suivantes :

* containerId – {String} ID du conteneur DOM (normalement un DIV) dans lequel la visionneuse est insérée. Il n’est pas nécessaire que l’élément conteneur soit créé au moment où cette méthode est appelée, mais le conteneur doit exister lorsque init() est exécuté. Obligatoire
* params – {Object} Objet JSON avec des paramètres de configuration de visionneuse où le nom de la propriété est une option de configuration spécifique à la visionneuse ou un modificateur SDK, et la valeur de cette propriété est une valeur de paramètres correspondante. Obligatoire
* gestionnaires – {Object} objet JSON avec rappels d’événement de visionneuse, où le nom de la propriété est le nom de l’événement de visionneuse pris en charge et la valeur de la propriété est une référence de fonction JavaScript au rappel approprié. Voir la section Rappels d’événement pour plus d’informations sur les événements de visionneuse. Facultatif.


## Retourne {#section-1d3cf85bc7cc4dfe9670e038d02b9101}

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
