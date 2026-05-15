---
description: Espace de noms de la visionneuse SDK
solution: Experience Manager
title: Espace de noms de la visionneuse SDK
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog Search
role: Developer,User
exl-id: aaad8f43-f6f2-440f-a6c4-52db585b48da
TQID: 'https://experienceleague.adobe.com/wS6VG2Eo73QO7-kbRLVCZ-DOrSWUb6XOB92J-zP7QV8'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 227
ht-degree: 0%

---

# Espace de noms de la visionneuse SDK{#viewer-sdk-namespace}

La visionneuse est composée de nombreux composants Viewer SDK. Dans la plupart des cas, la page web n’a pas besoin d’interagir directement avec l’API des composants SDK ; tous les besoins courants sont couverts dans l’API de la visionneuse elle-même.

Cependant, certains cas d’utilisation avancés nécessitent que la page web obtienne une référence à un composant SDK interne à l’aide de l’API de visionneuse `getComponent()`, puis utilise toute la flexibilité des API de SDK elle-même.

L’espace de noms utilisé pour charger et initialiser les composants SDK par la visionneuse dépend de l’environnement dans lequel la visionneuse fonctionne. Si la visionneuse est en cours d’exécution dans AEM (Adobe Experience Manager), elle charge les composants SDK dans `s7viewers.s7sdk` espace de noms. Et la visionneuse diffusée à partir de Dynamic Media Classic charge le SDK dans `s7classic.s7sdk`.

Dans les deux cas, l’espace de noms utilisé par le SDK dans la visionneuse comporte `s7viewers` ou `s7classic` comme préfixe. De plus, il est différent de l’espace de noms d’`s7sdk` brut utilisé dans le Guide de l’utilisateur de SDK ou la documentation de l’API SDK.

Pour cette raison, il est important d’utiliser un espace de noms SDK entièrement qualifié lorsque vous écrivez du code d’application personnalisé qui communique avec les composants internes de la visionneuse.

Par exemple, si vous prévoyez d’écouter `StatusEvent.NOTF_VIEW_READY` événement et que la visionneuse est diffusée à partir de Dynamic Media Classic, le type d’événement complet est `s7classic.s7sdk.event.StatusEvent.NOTF_VIEW_READY` et le code d’écouteur d’événement ressemble à ce qui suit :

```javascript {.line-numbers}
<instance>.setHandlers({ 
 "initComplete":function() { 
  var pageView = <instance>.getComponent("pageView"); 
   pageView.addEventListener(s7classic.s7sdk.event.StatusEvent.NOTF_VIEW_READY, function(e) { 
   console.log("view ready"); 
  }, false); 
} 
});
```
