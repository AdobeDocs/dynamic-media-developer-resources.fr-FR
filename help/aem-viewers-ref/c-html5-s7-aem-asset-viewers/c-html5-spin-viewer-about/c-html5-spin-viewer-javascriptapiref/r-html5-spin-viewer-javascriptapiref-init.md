---
title: Init
description: JavaScript référence de l’API pour la visionneuse à 360°.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Spin Sets
role: Developer,User
exl-id: 5217a02a-6092-4cb9-b4fb-f959cdc85a6e
source-git-commit: 6f838470a7bdea8e8c0219e59746ec82ecd802a8
workflow-type: tm+mt
source-wordcount: '118'
ht-degree: 2%

---

# Init{#init}

JavaScript référence de l’API pour la visionneuse à 360°.

`init()`

Démarre l’initialisation de la visionneuse à 360°. À ce stade, l’élément conteneur `DOM` doit être créé de manière à ce que le code de visionneuse puisse le trouver par son identifiant.

Si l’élément conteneur ne fait pas encore partie de la mise en page Web (par exemple, il peut être masqué à l’aide d’un `display:none` style), la visionneuse suspend son processus d’initialisation. Il est suspendu jusqu’au moment où la page Web ramène l’élément conteneur à la mise en page, moment auquel le chargement de la visionneuse reprend automatiquement.

N’appelez cette méthode qu’une seule fois au cours du cycle de vie d’une visionneuse ; Les appels suivants sont ignorés.

## Paramètres {#section-ad069aaaf4f145f2b50ae5ac89ca1ed2}

Aucune

## Retourne {#section-1d3cf85bc7cc4dfe9670e038d02b9101}

`{Object}` Une référence à l’instance de visionneuse.

## Exemple {#section-9e9332aa86b74a5fb321375c03fdc5b3}

```
<instance>.init()
```
