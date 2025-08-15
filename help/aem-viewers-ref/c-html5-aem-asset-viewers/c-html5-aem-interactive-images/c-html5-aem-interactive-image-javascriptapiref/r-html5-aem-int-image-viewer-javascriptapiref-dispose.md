---
title: disposer
description: JavaScript référence de l’API pour la visionneuse d’images vidéo.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Interactive Images
role: Developer,User
exl-id: 8af8506e-6b29-45ea-a70b-3eb3b2995047
source-git-commit: 24667a5ebab54ba22c4a3f6b52d19d7a31a93576
workflow-type: tm+mt
source-wordcount: '126'
ht-degree: 3%

---

# disposer{#dispose}

JavaScript référence de l’API pour la visionneuse d’images vidéo.

`dispose()`

Supprime cette instance de visionneuse en libérant toutes les ressources utilisées par la logique de visionneuse et en supprimant tous les objets et composants internes créés par la visionneuse au moment de l’exécution.

Le code de page Web doit également supprimer la variable d’instance de visionneuse pour supprimer complètement la visionneuse de la mémoire du navigateur Web.

Si le code de page Web a enregistré des écouteurs d’événements directement sur les composants SDK de la visionneuse utilisés par la visionneuse (ou stocké des références externes à ces composants), ces écouteurs doivent être explicitement désinscrits par le code de page Web. Ces références de composants externes doivent également être supprimées avant d’appeler `dispose()`.

N’accédez plus à l’API de visionneuse après `dispose()` l’appel.

## Paramètres {#section-ad069aaaf4f145f2b50ae5ac89ca1ed2}

Aucune

## Retourne {#section-1d3cf85bc7cc4dfe9670e038d02b9101}

Aucune

## Exemple {#section-9e9332aa86b74a5fb321375c03fdc5b3}

```
<instance>.dispose()
```
