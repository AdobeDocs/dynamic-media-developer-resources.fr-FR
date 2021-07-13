---
description: Référence de l’API JavaScript pour la visionneuse de vidéos interactives.
solution: Experience Manager
title: init
feature: Dynamic Media Classic,Visionneuses,SDK/API,Vidéos interactives
role: Developer,User
exl-id: 5fcc7dcd-a9a8-4a87-9c8d-42717ced8ae9
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '131'
ht-degree: 2%

---

# init{#init}

Référence de l’API JavaScript pour la visionneuse de vidéos interactives.

`init()`

Commence l’initialisation de la visionneuse de vidéos interactives. D’ici là, l’élément DOM du conteneur doit être créé afin que le code de la visionneuse puisse le trouver par son identifiant.

Si l’élément de conteneur ne fait pas encore partie de la mise en page web (il peut par exemple être masqué à l’aide du style `display:none` qui lui est affecté), la visionneuse suspend son processus d’initialisation jusqu’au moment où la page web ramène l’élément de conteneur à la mise en page. Dans ce cas, le chargement de la visionneuse reprend automatiquement.

Appelez cette méthode une seule fois pendant le cycle de vie de la visionneuse ; les appels suivants sont ignorés.

## Paramètres {#section-ad069aaaf4f145f2b50ae5ac89ca1ed2}

Aucune

## Renvoie {#section-1d3cf85bc7cc4dfe9670e038d02b9101}

`{Object}` Référence à l’instance de visionneuse.

## Exemple {#section-9e9332aa86b74a5fb321375c03fdc5b3}

```
<instance>.init()
```
