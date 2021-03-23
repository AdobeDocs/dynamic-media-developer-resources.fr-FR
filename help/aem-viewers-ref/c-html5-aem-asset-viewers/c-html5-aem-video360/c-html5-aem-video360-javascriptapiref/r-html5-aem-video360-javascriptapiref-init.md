---
description: Référence de l’API JavaScript pour le lecteur vidéo360.
seo-description: Référence de l’API JavaScript pour le lecteur vidéo360.
seo-title: init
solution: Experience Manager
title: init
uuid: c7e13968-253c-4574-89e3-f3afc0f55df5
feature: Dynamic Media Classic, Visionneuses, SDK/API, Vidéo 360 VR
role: Développeur, Professionnel
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '138'
ht-degree: 2%

---


# init{#init}

Référence de l’API JavaScript pour le lecteur vidéo360.

`init()`

Début l’initialisation de la visionneuse de vidéos 360. D’ici là, l’élément DOM du conteneur doit être créé afin que le code du lecteur puisse le trouver par son identifiant.

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

