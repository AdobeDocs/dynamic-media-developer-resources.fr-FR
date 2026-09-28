---
title: Espace de noms de la visionneuse SDK
description: Espace de noms de la visionneuse SDK
solution: Experience Manager, Experience Manager Assets
feature-set: Experience Manager, Experience Manager Assets
feature: Dynamic Media Classic,Viewers,SDK/API
role: Developer,User
exl-id: 3360a3bd-8a4a-4bf9-98bf-ada7c35c58f4
autotag-review: '2026-05-13T22:16:34.426Z'
TQID: 'https://experienceleague.adobe.com/PVs-3zvwoKgc-rq6cssqCRnWH-SyyghZ5L-JguyZUl4'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
    internal-label: Experience Manager
  - id: d09181b5-a36a-43de-ba01-36641440bc43
    internal-label: Experience Manager Assets
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
    internal-label: APIs
  - id: fe490c45-63fa-5b99-b5b4-d8cfeda8aa7d
    internal-label: SDK/API
  - id: bd0d2470-932c-4269-8eca-6d939b72d9ef
    internal-label: Dynamic Media
subfeature_v2:
  - id: c12bda38-aa1a-4647-b62e-42cd4537dac6
    internal-label: Dynamic Media Classic
  - id: d17d085a-e808-49dd-b9a6-85a996b999bd
    internal-label: Viewers
role_v2:
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
    internal-label: Developer
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
    internal-label: User
source-git-commit: 0e24e07f8c91d3e7fda5510ed4252f9953e27467
workflow-type: tm+mt
source-wordcount: '220'
ht-degree: 0%
---
# Espace de noms de la visionneuse SDK{#viewer-sdk-namespace}

La visionneuse est composée de nombreux composants Viewer SDK. En règle générale, la page web n’a pas besoin d’interagir directement avec l’API des composants SDK ; tous les besoins courants sont couverts dans l’API de la visionneuse elle-même.

Cependant, certains cas d’utilisation avancés nécessitent que la page web référence un composant SDK interne à l’aide de l’API de visionneuse `getComponent()`, puis utilise toute la flexibilité des API de SDK elle-même.

L’espace de noms utilisé pour charger et initialiser les composants SDK par la visionneuse dépend de l’environnement dans lequel la visionneuse fonctionne. Si la visionneuse est en cours d’exécution dans Adobe Experience Manager, elle charge les composants SDK dans `s7viewers.s7sdk` espace de noms. De même, la visionneuse diffusée à partir de Dynamic Media Classic charge le SDK dans `s7classic.s7sdk`.

Dans les deux cas, l’espace de noms utilisé par le SDK dans la visionneuse comporte `s7viewers` ou `s7classic` comme préfixe. De plus, il est différent de l’espace de noms d’`s7sdk` brut utilisé dans le Guide de l’utilisateur de SDK ou la documentation de l’API SDK.

Pour cette raison, il est important d’utiliser un espace de noms SDK entièrement qualifié lorsque vous écrivez du code d’application personnalisé qui communique avec les composants internes de la visionneuse.

Par exemple, si vous prévoyez d’écouter `StatusEvent.NOTF_VIEW_READY` événement et que la visionneuse est diffusée à partir d’Experience Manager, le type d’événement complet est `s7viewers.s7sdk.event.StatusEvent.NOTF_VIEW_READY` et le code d’écouteur d’événement ressemble à ce qui suit :

```javascript {.line-numbers}
<instance>.setHandlers({ 
 "initComplete":function() { 
  var panoramicView = <instance>.getComponent("panoramicView"); 
   panoramicView.addEventListener(s7viewers.s7sdk.event.StatusEvent.NOTF_VIEW_READY, function(e) { 
   console.log("view ready"); 
  }, false); 
} 
});
```
