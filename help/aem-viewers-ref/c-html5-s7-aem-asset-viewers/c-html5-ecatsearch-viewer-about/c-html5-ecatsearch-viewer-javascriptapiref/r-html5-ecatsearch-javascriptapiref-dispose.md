---
title: se débarrasser
description: Référence de l’API JavaScript pour la visionneuse de catalogue électronique.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog Search
role: Developer,User
exl-id: fda6d50f-0e1b-436c-af2e-1ccc9cd51c39
TQID: 'https://experienceleague.adobe.com/sV3h7e6C2e6lcs24hLgqASaNgMc8wAkcZ9jPvZ-Gz54'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 124
ht-degree: 3%

---

# se débarrasser{#dispose}

Référence de l’API JavaScript pour la visionneuse de catalogue électronique.

[!DNL `dispose()`]

Supprime cette instance de visionneuse en libérant toutes les ressources utilisées par la logique de la visionneuse et en supprimant tous les objets et composants internes créés par la visionneuse au moment de l’exécution.

Le code de la page web doit également supprimer la variable d’instance de la visionneuse pour supprimer complètement la visionneuse de la mémoire du navigateur web.

Si le code de la page web a enregistré des écouteurs d’événement directement sur les composants SDK de la visionneuse utilisés par la visionneuse ou stocké des références externes à ces composants, ces écouteurs doivent être explicitement désenregistrés par le code de la page web. De plus, ces références de composant externe doivent être supprimées avant d’appeler [!DNL `dispose()`].

N’accédez plus à l’API de visionneuse après l’appel de [!DNL `dispose()`].

## Paramètres {#section-ad069aaaf4f145f2b50ae5ac89ca1ed2}

Aucune

## Renvoie {#section-1d3cf85bc7cc4dfe9670e038d02b9101}

Aucune

## Exemple {#section-9e9332aa86b74a5fb321375c03fdc5b3}

```
<instance>.dispose()
```
