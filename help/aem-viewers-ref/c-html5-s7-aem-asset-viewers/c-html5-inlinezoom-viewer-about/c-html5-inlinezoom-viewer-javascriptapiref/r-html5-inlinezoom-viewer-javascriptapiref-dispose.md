---
description: Référence de l’API JavaScript pour la visionneuse de zoom intégrée.
solution: Experience Manager
title: dispose
feature: Dynamic Media Classic,Visionneuses,SDK/API,Zoom intégré
role: Developer,User
exl-id: 7e525bc1-6986-414c-acc0-e011dfd7b84b
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '134'
ht-degree: 2%

---

# dispose{#dispose}

Référence de l’API JavaScript pour la visionneuse de zoom intégrée.

`dispose()`

Dispose cette instance de visionneuse en libérant toutes les ressources utilisées par la logique de la visionneuse et en supprimant tous les objets et composants internes créés par la visionneuse au moment de l’exécution.

Le code de page web doit également supprimer la variable d’instance de la visionneuse pour supprimer complètement la visionneuse de la mémoire du navigateur web.

Si le code de page web a enregistré des écouteurs d’événement directement sur les composants du SDK de la visionneuse utilisés par la visionneuse ou les références externes stockées à ces écouteurs de composants, ces derniers doivent être désenregistrés explicitement par le code de page web, et ces références de composants externes doivent être supprimées avant d’appeler `dispose()`.

N’accédez plus à l’API de visionneuse après l’appel de `dispose()`.

## Paramètres {#section-ad069aaaf4f145f2b50ae5ac89ca1ed2}

Aucune

## Renvoie {#section-1d3cf85bc7cc4dfe9670e038d02b9101}

Aucune

## Exemple {#section-9e9332aa86b74a5fb321375c03fdc5b3}

```
<instance>.dispose()
```
