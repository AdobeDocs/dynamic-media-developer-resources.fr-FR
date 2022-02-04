---
title: dispose
description: Référence de l’API JavaScript pour la visionneuse à 360°.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Spin Sets
role: Developer,User
exl-id: c19466a8-9fc5-440c-8bb1-c4528937a522
source-git-commit: 6f838470a7bdea8e8c0219e59746ec82ecd802a8
workflow-type: tm+mt
source-wordcount: '124'
ht-degree: 3%

---

# dispose{#dispose}

Référence de l’API JavaScript pour la visionneuse à 360°.

`dispose()`

Dispose cette instance de visionneuse en libérant toutes les ressources utilisées par la logique de la visionneuse et en supprimant tous les objets et composants internes créés par la visionneuse au moment de l’exécution.

Le code de page web doit également supprimer la variable d’instance de la visionneuse pour supprimer complètement la visionneuse de la mémoire du navigateur web.

Si le code de page web a enregistré des écouteurs d’événement directement sur les composants du SDK de la visionneuse utilisés par la visionneuse - ou si des références externes stockées à ces composants - ces écouteurs doivent être désenregistrés explicitement par le code de page web. De plus, ces références de composants externes doivent être supprimées avant d’appeler `dispose()`.

Ne plus accéder à l’API de visionneuse après `dispose()` est appelée.

## Paramètres {#section-ad069aaaf4f145f2b50ae5ac89ca1ed2}

Aucune

## Renvoie {#section-1d3cf85bc7cc4dfe9670e038d02b9101}

Aucune

## Exemple {#section-9e9332aa86b74a5fb321375c03fdc5b3}

```
<instance>.dispose()
```
