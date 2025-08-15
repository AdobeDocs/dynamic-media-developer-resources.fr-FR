---
title: Init
description: JavaScript référence de l’API pour la visionneuse de zoom intégrée.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Inline Zoom
role: Developer,User
exl-id: c4419728-1e1a-4e11-88fe-24eb0c968c5c
source-git-commit: 50dddf148345d2ca5243d5d7108fefa56d23dad6
workflow-type: tm+mt
source-wordcount: '125'
ht-degree: 2%

---

# Init{#init}

JavaScript référence de l’API pour la visionneuse de zoom intégrée.

`init()`

Démarre l’initialisation de la visionneuse afin que le code de la visionneuse puisse la trouver par son identifiant. À ce stade, l’élément DOM de conteneur doit être créé.

Si l’élément conteneur ne fait pas encore partie de la mise en page Web (par exemple, il peut être masqué à l’aide `display:none` du style qui lui est attribué), la visionneuse suspend son processus d’initialisation. Il le fait jusqu’au moment où la page Web ramène l’élément conteneur à la mise en page. Lorsque cette action se produit, le chargement de la visionneuse reprend automatiquement.

N’appelez cette méthode qu’une seule fois au cours du cycle de vie de la visionneuse ; Les appels suivants sont ignorés.

## Paramètres {#section-ad069aaaf4f145f2b50ae5ac89ca1ed2}

Aucune

## Retourne {#section-1d3cf85bc7cc4dfe9670e038d02b9101}

`{Object}` Une référence à l’instance de visionneuse.

## Exemple {#section-9e9332aa86b74a5fb321375c03fdc5b3}

```
<instance>.init()
```
