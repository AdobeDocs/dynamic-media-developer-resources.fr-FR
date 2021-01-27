---
description: Référence de l’API JavaScript pour la visionneuse à 360°.
seo-description: Référence de l’API JavaScript pour la visionneuse à 360°.
seo-title: init
solution: Experience Manager
title: init
topic: Dynamic Media
uuid: 1803028f-dcba-49da-9fb7-78bfd64fc47d
translation-type: tm+mt
source-git-commit: e4695cc4e882351ec3f2c55fd8a3cfca455bd79d
workflow-type: tm+mt
source-wordcount: '126'
ht-degree: 2%

---


# init{#init}

Référence de l’API JavaScript pour la visionneuse à 360°.

`init()`

Début l’initialisation de la visionneuse à 360°. A ce stade, l’élément de conteneur `DOM` doit être créé afin que le code du lecteur puisse le trouver par son identifiant.

Si l’élément de conteneur ne fait pas encore partie de la mise en page de la page Web (il peut par exemple être masqué à l’aide du style `display:none` qui lui est affecté), le lecteur suspend son processus d’initialisation jusqu’au moment où la page Web ramène l’élément de conteneur à la mise en page. Dans ce cas, le chargement du lecteur reprend automatiquement.

Appelez cette méthode une seule fois pendant le cycle de vie de la visionneuse ; les appels suivants sont ignorés.

## Paramètres {#section-ad069aaaf4f145f2b50ae5ac89ca1ed2}

Aucune

## Renvoie {#section-1d3cf85bc7cc4dfe9670e038d02b9101}

`{Object}` Référence à l’instance de visionneuse.

## Exemple {#section-9e9332aa86b74a5fb321375c03fdc5b3}

```
<instance>.init()
```

