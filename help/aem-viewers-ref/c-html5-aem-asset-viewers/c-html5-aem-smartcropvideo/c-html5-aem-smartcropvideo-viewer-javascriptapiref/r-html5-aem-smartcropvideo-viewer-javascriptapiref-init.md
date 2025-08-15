---
title: Init
description: JavaScript référence de l’API pour la visionneuse de vidéos avec recadrage intelligent.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Smart Crop,Video
role: Developer,User
exl-id: e197c4dd-346d-4ef4-beb7-cbd0049dff05
source-git-commit: 1aa8be858b0ba8ec9b99753d43c202b35ed58c30
workflow-type: tm+mt
source-wordcount: '130'
ht-degree: 2%

---

# Init{#init}

JavaScript référence de l’API pour la visionneuse de vidéos avec recadrage intelligent.

`init()`

Démarre l’initialisation de la visionneuse de vidéos avec recadrage intelligent. À ce stade, l’élément DOM conteneur doit être créé afin que le code de visionneuse puisse le trouver par son identifiant.

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
