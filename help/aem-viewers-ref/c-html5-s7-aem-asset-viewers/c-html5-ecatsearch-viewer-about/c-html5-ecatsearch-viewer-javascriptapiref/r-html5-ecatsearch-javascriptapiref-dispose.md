---
title: disposer
description: JavaScript référence de l’API pour la visionneuse de catalogue électronique.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog Search
role: Developer,User
exl-id: fda6d50f-0e1b-436c-af2e-1ccc9cd51c39
source-git-commit: 38f3e425be0ce3e241fc18b477e3f68b7b763b51
workflow-type: tm+mt
source-wordcount: '122'
ht-degree: 3%

---

# disposer{#dispose}

JavaScript référence de l’API pour la visionneuse de catalogue électronique.

[!DNL `dispose()`]

Supprime cette instance de visionneuse en libérant toutes les ressources utilisées par la logique de visionneuse et en supprimant tous les objets et composants internes créés par la visionneuse au moment de l’exécution.

Le code de page Web doit également supprimer la variable d’instance de visionneuse pour supprimer complètement la visionneuse de la mémoire du navigateur Web.

Si le code de la page Web a enregistré des écouteurs d’événements directement sur les composants SDK de la visionneuse utilisés par la visionneuse (ou stocké des références externes à de tels composants), ces écouteurs doivent être explicitement désinscrits par le code de page Web. Ces références de composants externes doivent également être supprimées avant d’appeler [!DNL `dispose()`].

N’accédez plus à l’API de visionneuse après [!DNL `dispose()`] l’appel.

## Paramètres {#section-ad069aaaf4f145f2b50ae5ac89ca1ed2}

Aucune

## Retourne {#section-1d3cf85bc7cc4dfe9670e038d02b9101}

Aucune

## Exemple {#section-9e9332aa86b74a5fb321375c03fdc5b3}

```
<instance>.dispose()
```
