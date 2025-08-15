---
title: se débarrasser
description: Référence de l’API JavaScript pour la visionneuse Fenêtre déroulante.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Flyout
role: Developer,User
exl-id: bf38d481-d8cc-400c-9017-bcb3471f2a10
source-git-commit: 50dddf148345d2ca5243d5d7108fefa56d23dad6
workflow-type: tm+mt
source-wordcount: '124'
ht-degree: 3%

---

# se débarrasser{#dispose}

Référence de l’API JavaScript pour la visionneuse Fenêtre déroulante.

`dispose()`

Supprime cette instance de visionneuse en libérant toutes les ressources utilisées par la logique de la visionneuse et en supprimant tous les objets et composants internes créés par la visionneuse au moment de l’exécution.

Le code de la page web doit également supprimer la variable d’instance de la visionneuse pour supprimer complètement la visionneuse de la mémoire du navigateur web.

Si le code de page web a enregistré des écouteurs d’événement directement sur les composants SDK de la visionneuse utilisés par la visionneuse ou stocké des références externes à ces composants, l’annulation explicite de l’enregistrement de ces écouteurs par le code de page web doit être effectuée. De plus, ces références de composant externe doivent être supprimées avant d’appeler `dispose()`.

N’accédez plus à l’API de visionneuse après l’appel de `dispose()`.

## Paramètres {#section-ad069aaaf4f145f2b50ae5ac89ca1ed2}

Aucune

## Renvoie {#section-1d3cf85bc7cc4dfe9670e038d02b9101}

Aucune

## Exemple {#section-9e9332aa86b74a5fb321375c03fdc5b3}

```
<instance>.dispose()
```
