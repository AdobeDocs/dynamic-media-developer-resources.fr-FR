---
description: Référence de l’API JavaScript pour Carousel Viewer.
solution: Experience Manager
title: disposer
feature: Dynamic Media Classic, Visionneuses, SDK/API, Bannières de carrousel
role: Développeur, Professionnel
exl-id: 64e9f83f-e17e-4544-825a-fd458e15fdb5
translation-type: tm+mt
source-git-commit: b4344397f82eb7d2d61020909f4acc7fddea210b
workflow-type: tm+mt
source-wordcount: '135'
ht-degree: 2%

---

# disposer{#dispose}

Référence de l’API JavaScript pour Carousel Viewer.

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
