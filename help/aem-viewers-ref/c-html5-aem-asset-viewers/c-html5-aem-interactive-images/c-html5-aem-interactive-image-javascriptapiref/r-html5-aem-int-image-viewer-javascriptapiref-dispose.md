---
description: Référence de l’API JavaScript pour la visionneuse d’images vidéo.
seo-description: Référence de l’API JavaScript pour la visionneuse d’images vidéo.
seo-title: disposer
solution: Experience Manager
title: disposer
topic: Dynamic media
uuid: d9698486-8ffd-4b12-844b-e80b929675ec
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '134'
ht-degree: 2%

---


# disposer{#dispose}

Référence de l’API JavaScript pour la visionneuse d’images vidéo.

`dispose()`

Dispose cette instance de visionneuse en libérant toutes les ressources utilisées par la logique de visionneuse et en supprimant tous les objets et composants internes créés par la visionneuse au moment de l’exécution.

Le code de la page Web doit également supprimer la variable d’instance du lecteur de contenu pour supprimer complètement le lecteur de la mémoire du navigateur Web.

Si le code de page Web a enregistré des écouteurs de événement directement sur les composants du kit de développement de visionneuse utilisés par le lecteur ou des références externes stockées à ces composants, ces écouteurs doivent être désenregistrés explicitement par le code de page Web et ces références de composants externes doivent être supprimées avant d&#39;appeler `dispose()`.

N’accédez plus à l’API du lecteur après l’appel de `dispose()`.

## Paramètres {#section-ad069aaaf4f145f2b50ae5ac89ca1ed2}

Aucune

## Renvoie {#section-1d3cf85bc7cc4dfe9670e038d02b9101}

Aucune

## Exemple {#section-9e9332aa86b74a5fb321375c03fdc5b3}

```
<instance>.dispose()
```

