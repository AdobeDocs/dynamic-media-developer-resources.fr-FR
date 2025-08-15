---
title: Init
description: JavaScript référence de l’API pour la visionneuse panoramique.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Panoramic
role: Developer,User
exl-id: cb543620-e774-407b-bf33-bfd2261511c4
source-git-commit: 8aebcacd5abdc23565aab1bc3506c36f055b6439
workflow-type: tm+mt
source-wordcount: '125'
ht-degree: 2%

---

# Init{#init}

JavaScript référence de l’API pour la visionneuse panoramique.

`init()`

Lance l’initialisation de la visionneuse panoramique. À ce stade, l’élément DOM conteneur doit être créé afin que le code de visionneuse puisse le trouver par son identifiant.

Si l’élément conteneur ne fait pas encore partie de la mise en page Web (par exemple, il peut être masqué à l’aide `display:none` du style qui lui est attribué), la visionneuse suspend son processus d’initialisation. Il le fait jusqu’au moment où la page Web ramène l’élément conteneur à la mise en page. Lorsque cet événement se produit, le chargement de la visionneuse reprend automatiquement.

Cette méthode ne doit être appelée qu’une seule fois au cours du cycle de vie d’une visionneuse, les appels suivants étant ignorés.

## Paramètres {#section-ad069aaaf4f145f2b50ae5ac89ca1ed2}

Aucune

## Retourne {#section-1d3cf85bc7cc4dfe9670e038d02b9101}

`{Object}` Une référence à l’instance de visionneuse.

## Exemple {#section-9e9332aa86b74a5fb321375c03fdc5b3}

```
<instance>.init()
```
