---
title: init
description: Référence de l’API JavaScript pour la visionneuse de vidéos.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Zoom
role: Developer,User
exl-id: 9e83b773-c059-45c6-a249-ef0ed2799a05
source-git-commit: ec2a15e2e76bae5da4fbabc9b6912b12dc080f66
workflow-type: tm+mt
source-wordcount: '120'
ht-degree: 2%

---

# init{#init}

Référence de l’API JavaScript pour la visionneuse de vidéos.

`init()`

Démarre l’initialisation de la visionneuse de vidéos. À ce stade, l’élément DOM du conteneur doit être créé afin que le code de la visionneuse puisse le trouver à l’aide de son identifiant.

Si l’élément de conteneur ne fait pas encore partie de la mise en page de la page web (par exemple, il peut être masqué à l’aide du style `display:none` ), la visionneuse suspend son processus d’initialisation. Il le fait jusqu’au moment où la page web ramène l’élément de conteneur à la mise en page. Lorsque ce processus se produit, le chargement de la visionneuse reprend automatiquement.

Appelez cette méthode une seule fois pendant le cycle de vie de la visionneuse ; les appels suivants sont ignorés.

## Paramètres {#section-ad069aaaf4f145f2b50ae5ac89ca1ed2}

Aucune

## Renvoie {#section-1d3cf85bc7cc4dfe9670e038d02b9101}

`{Object}` Référence à l’instance de visionneuse.

## Exemple {#section-9e9332aa86b74a5fb321375c03fdc5b3}

```
<instance>.init()
```
