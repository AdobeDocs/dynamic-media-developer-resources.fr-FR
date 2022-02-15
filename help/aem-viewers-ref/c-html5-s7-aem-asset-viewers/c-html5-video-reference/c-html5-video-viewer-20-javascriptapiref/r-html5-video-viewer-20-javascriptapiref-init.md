---
title: init
description: Référence de l’API JavaScript pour la visionneuse de vidéos.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Video
role: Developer,User
exl-id: d46a9c8b-064a-4928-b30e-885b12d287ab
source-git-commit: 11acb9151d3ea247eecde3cfbbd295a95c10829c
workflow-type: tm+mt
source-wordcount: '124'
ht-degree: 2%

---

# init{#init}

Référence de l’API JavaScript pour la visionneuse de vidéos.

`init()`

Commence l’initialisation de la visionneuse de vidéos. D’ici là, l’élément DOM du conteneur doit être créé afin que le code de la visionneuse puisse le trouver par son identifiant.

Si l’élément de conteneur ne fait pas encore partie de la mise en page web, il peut, par exemple, être masqué à l’aide de `display:none` style qui lui est affecté : la visionneuse suspend son processus d’initialisation. Il le fait jusqu’au moment où la page web ramène l’élément de conteneur à la mise en page. Lorsque cette action se produit, le chargement de la visionneuse reprend automatiquement.

Appelez cette méthode une seule fois pendant le cycle de vie de la visionneuse ; les appels suivants sont ignorés.

## Paramètres {#section-ad069aaaf4f145f2b50ae5ac89ca1ed2}

Aucune

## Renvoie {#section-1d3cf85bc7cc4dfe9670e038d02b9101}

`{Object}` Référence à l’instance de visionneuse.

## Exemple {#section-9e9332aa86b74a5fb321375c03fdc5b3}

```
<instance>.init()
```
