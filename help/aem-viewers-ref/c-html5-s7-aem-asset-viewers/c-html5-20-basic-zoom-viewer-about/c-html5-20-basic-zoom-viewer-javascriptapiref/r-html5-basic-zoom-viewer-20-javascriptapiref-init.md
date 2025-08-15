---
title: Init
description: JavaScript référence de l’API pour la visionneuse de zoom de base.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Zoom
role: Developer,User
exl-id: cef585ae-44d7-406c-96f9-e03959a8e518
source-git-commit: 61e3a1fd0e21d336eaf5232096f5b1b54f2a6353
workflow-type: tm+mt
source-wordcount: '126'
ht-degree: 2%

---

# Init{#init}

JavaScript référence de l’API pour la visionneuse de zoom de base.

`init()`

Démarre l’initialisation de la visionneuse de zoom de base. À ce stade, l’élément DOM conteneur doit être créé afin que le code de visionneuse puisse le trouver par son identifiant.

Si l’élément conteneur ne fait pas encore partie de la mise en page Web (par exemple, il peut être masqué à l’aide `display:none` du style qui lui est attribué), la visionneuse suspend son processus d’initialisation. Il le fait jusqu’au moment où la page Web ramène l’élément conteneur à la mise en page. Lorsque cette action se produit, le chargement de la visionneuse reprend automatiquement.

N’appelez cette méthode qu’une seule fois au cours du cycle de vie de la visionneuse ; Les appels suivants sont ignorés.

## Paramètres {#section-ad069aaaf4f145f2b50ae5ac89ca1ed2}

Aucune

## Retourne {#section-1d3cf85bc7cc4dfe9670e038d02b9101}

`{Object}` Référence à l’instance de la visionneuse.

## Exemple {#section-9e9332aa86b74a5fb321375c03fdc5b3}

```
<instance>.init()
```
