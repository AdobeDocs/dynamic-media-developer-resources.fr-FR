---
description: Référence de l’API JavaScript pour la visionneuse d’images interactive.
solution: Experience Manager
title: init
feature: Dynamic Media Classic, Visionneuses, SDK/API, Images interactives
role: Développeur, Professionnel
exl-id: 675031ab-21bb-49a5-abbc-eca8d2619e49
translation-type: tm+mt
source-git-commit: b4344397f82eb7d2d61020909f4acc7fddea210b
workflow-type: tm+mt
source-wordcount: '134'
ht-degree: 2%

---

# init{#init}

Référence de l’API JavaScript pour la visionneuse d’images interactive.

`init()`

Début l’initialisation de la visionneuse d’images interactive. D’ici là, l’élément DOM du conteneur doit être créé afin que le code du lecteur puisse le trouver par son identifiant.

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
