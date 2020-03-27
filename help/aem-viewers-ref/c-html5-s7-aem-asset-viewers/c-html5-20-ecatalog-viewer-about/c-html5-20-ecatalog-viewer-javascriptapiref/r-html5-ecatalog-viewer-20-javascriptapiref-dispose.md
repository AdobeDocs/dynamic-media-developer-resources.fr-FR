---
description: Référence de l’API JavaScript pour la visionneuse de catalogue électronique.
seo-description: Référence de l’API JavaScript pour la visionneuse de catalogue électronique.
seo-title: disposer
solution: Experience Manager
title: disposer
topic: Dynamic media
uuid: b2073d03-a0a0-4f55-a350-7336ddcf031d
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# disposer{#dispose}

Référence de l’API JavaScript pour la visionneuse de catalogue électronique.

`dispose()`

Supprime cette instance de visionneuse en libérant toutes les ressources utilisées par la logique de la visionneuse et en supprimant tous les objets et composants internes créés par la visionneuse au moment de l’exécution.

Le code de page Web doit également supprimer la variable d’instance du lecteur de contenu pour supprimer complètement le lecteur de la mémoire du navigateur Web.

Si le code de la page Web a enregistré  écouteurs directement sur les composants du kit de développement de visionneuse utilisés par le lecteur ou les références externes stockées à ces composants, ces écouteurs doivent être explicitement désenregistrés par le code de la page Web et ces références de composants externes doivent être supprimées avant l’appel `dispose()`.

N’accédez plus à l’API du lecteur après `dispose()` l’appel.

## Paramètres {#section-ad069aaaf4f145f2b50ae5ac89ca1ed2}

Aucune

## Returns {#section-1d3cf85bc7cc4dfe9670e038d02b9101}

Aucune

## Exemple {#section-9e9332aa86b74a5fb321375c03fdc5b3}

```
<instance>.dispose()
```

