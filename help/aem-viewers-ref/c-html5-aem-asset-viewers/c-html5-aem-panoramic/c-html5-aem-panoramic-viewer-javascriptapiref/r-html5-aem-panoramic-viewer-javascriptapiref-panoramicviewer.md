---
title: PanoramicViewer
description: Constructeur, crée une instance Visionneuse panoramique HTML5.
solution: Experience Manager, Experience Manager Assets
feature-set: Experience Manager, Experience Manager Assets
feature: Dynamic Media Classic,Viewers,SDK/API
role: Developer,User
autotag-review: '2026-05-13T22:09:54.686Z'
TQID: 'https://experienceleague.adobe.com/zSYqLmLn-LQhkIIrPe31JIouevTWijICBcrmY3fol1M'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
    internal-label: Experience Manager
  - id: d09181b5-a36a-43de-ba01-36641440bc43
    internal-label: Experience Manager Assets
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
    internal-label: APIs
  - id: fe490c45-63fa-5b99-b5b4-d8cfeda8aa7d
    internal-label: SDK/API
  - id: bd0d2470-932c-4269-8eca-6d939b72d9ef
    internal-label: Dynamic Media
subfeature_v2:
  - id: c12bda38-aa1a-4647-b62e-42cd4537dac6
    internal-label: Dynamic Media Classic
  - id: d17d085a-e808-49dd-b9a6-85a996b999bd
    internal-label: Viewers
role_v2:
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
    internal-label: Developer
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
    internal-label: User
source-git-commit: 0e24e07f8c91d3e7fda5510ed4252f9953e27467
workflow-type: tm+mt
source-wordcount: '162'
ht-degree: 4%
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
