---
description: Référence de l’API JavaScript pour la visionneuse de zoom de base.
seo-description: Référence de l’API JavaScript pour la visionneuse de zoom de base.
seo-title: init
solution: Experience Manager
title: init
topic: Dynamic Media
uuid: a2a4fb97-89ec-41d2-ada7-8ff1775eaefa
translation-type: tm+mt
source-git-commit: e4695cc4e882351ec3f2c55fd8a3cfca455bd79d
workflow-type: tm+mt
source-wordcount: '131'
ht-degree: 2%

---


# init{#init}

Référence de l’API JavaScript pour la visionneuse de zoom de base.

`init()`

Début l’initialisation de la visionneuse de zoom de base. D’ici là, l’élément DOM du conteneur doit être créé afin que le code du lecteur puisse le trouver par son identifiant.

Si l’élément de conteneur ne fait pas encore partie de la mise en page de la page Web (il peut par exemple être masqué à l’aide du style `display:none` qui lui est affecté), le lecteur suspend son processus d’initialisation jusqu’au moment où la page Web ramène l’élément de conteneur à la mise en page. Dans ce cas, le chargement de la visionneuse reprend automatiquement.

Appelez cette méthode une seule fois pendant le cycle de vie de la visionneuse ; les appels suivants sont ignorés.

## Paramètres {#section-ad069aaaf4f145f2b50ae5ac89ca1ed2}

Aucune

## Renvoie {#section-1d3cf85bc7cc4dfe9670e038d02b9101}

`{Object}` Référence à l’instance de visionneuse.

## Exemple {#section-9e9332aa86b74a5fb321375c03fdc5b3}

```
<instance>.init()
```

