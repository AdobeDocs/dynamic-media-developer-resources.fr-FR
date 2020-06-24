---
description: Référence de l’API JavaScript pour la visionneuse d’images interactive.
seo-description: Référence de l’API JavaScript pour la visionneuse d’images interactive.
seo-title: init
solution: Experience Manager
title: init
topic: Dynamic media
uuid: 915f15cf-152a-424d-b7ea-a083891bb954
translation-type: tm+mt
source-git-commit: bea6e8f949a9ef0f3f56faac40092b5681a16ff6
workflow-type: tm+mt
source-wordcount: '131'
ht-degree: 2%

---


# init{#init}

Référence de l’API JavaScript pour la visionneuse d’images interactive.

`init()`

Début l’initialisation de la visionneuse d’images interactive. D’ici là, l’élément DOM du conteneur doit être créé afin que le code du lecteur puisse le trouver par son identifiant.

Si l’élément conteneur ne fait pas encore partie de la mise en page de la page Web (par exemple, il peut être masqué à l’aide du `display:none` style qui lui est affecté), le lecteur suspend son processus d’initialisation jusqu’au moment où la page Web ramène l’élément conteneur à la mise en page. Dans ce cas, le chargement du lecteur reprend automatiquement.

Appelez cette méthode une seule fois pendant le cycle de vie de la visionneuse ; les appels suivants sont ignorés.

## Paramètres {#section-ad069aaaf4f145f2b50ae5ac89ca1ed2}

Aucune

## Returns {#section-1d3cf85bc7cc4dfe9670e038d02b9101}

`{Object}` Référence à l’instance de visionneuse.

## Exemple {#section-9e9332aa86b74a5fb321375c03fdc5b3}

```
<instance>.init()
```

