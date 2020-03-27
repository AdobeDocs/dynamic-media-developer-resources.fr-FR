---
description: Référence de l’API JavaScript pour la visionneuse de supports variés.
seo-description: Référence de l’API JavaScript pour la visionneuse de supports variés.
seo-title: init
solution: Experience Manager
title: init
topic: Dynamic media
uuid: f16e3cfe-4b30-4497-bd65-52d2f1edf3d3
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# init{#init}

Référence de l’API JavaScript pour la visionneuse de supports variés.

`init()`

de l’initialisation de la visionneuse de supports variés. A ce moment-là, l’élément DOM  doit être créé afin que le code du lecteur puisse le trouver par son identifiant.

Si l’élément  du ne fait pas encore partie de la mise en page de la page Web (par exemple, il peut être masqué à l’aide du `display:none` style qui lui est affecté), le lecteur suspend son processus d’initialisation jusqu’au moment où la page Web ramène l’élément  du à la mise en page. Dans ce cas, le chargement du lecteur reprend automatiquement.

Appelez cette méthode une seule fois pendant le cycle de vie de la visionneuse ; les appels suivants sont ignorés.

## Paramètres {#section-ad069aaaf4f145f2b50ae5ac89ca1ed2}

Aucune

## Returns {#section-1d3cf85bc7cc4dfe9670e038d02b9101}

`{Object}` Référence à l’instance de visionneuse.

## Exemple {#section-9e9332aa86b74a5fb321375c03fdc5b3}

```
<instance>.init()
```

