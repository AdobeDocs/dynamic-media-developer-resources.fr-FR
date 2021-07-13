---
description: Référence de l’API JavaScript pour la visionneuse de zoom intégrée.
solution: Experience Manager
title: init
feature: Dynamic Media Classic,Visionneuses,SDK/API,Zoom intégré
role: Developer,User
exl-id: c4419728-1e1a-4e11-88fe-24eb0c968c5c
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '130'
ht-degree: 2%

---

# init{#init}

Référence de l’API JavaScript pour la visionneuse de zoom intégrée.

`init()`

Commence l’initialisation de la visionneuse de sorte que le code de la visionneuse puisse la trouver par son identifiant. D’ici là, l’élément DOM du conteneur doit être créé.

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
