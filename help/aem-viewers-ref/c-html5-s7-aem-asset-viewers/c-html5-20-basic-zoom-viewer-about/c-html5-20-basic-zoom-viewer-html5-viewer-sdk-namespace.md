---
title: Espace de noms de la visionneuse SDK
description: Espace de noms de la visionneuse SDK
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Zoom
role: Developer,User
exl-id: 4ccdf8c2-6cf5-4cb3-af61-fab50f410566
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '221'
ht-degree: 0%

---

# Espace de noms de la visionneuse SDK{#viewer-sdk-namespace}

La visionneuse est composée de nombreux composants Viewer SDK. En règle générale, la page web n’a pas besoin d’interagir directement avec l’API des composants SDK ; tous les besoins courants sont couverts dans l’API de la visionneuse elle-même.

Cependant, certains cas d’utilisation avancés nécessitent que la page web référence un composant SDK interne à l’aide de l’API de visionneuse `getComponent()`, puis utilise toute la flexibilité des API de SDK elle-même.

L’espace de noms utilisé pour charger et initialiser les composants SDK par la visionneuse dépend de l’environnement dans lequel la visionneuse fonctionne. Si la visionneuse est en cours d’exécution dans Adobe Experience Manager, elle charge les composants SDK dans `s7viewers.s7sdk` espace de noms. Et la visionneuse diffusée à partir de Dynamic Media Classic charge le SDK dans `s7classic.s7sdk`.

Dans les deux cas, l’espace de noms utilisé par le SDK dans la visionneuse comporte `s7viewers` ou `s7classic` comme préfixe. De plus, il est différent de l’espace de noms d’`s7sdk` brut utilisé dans le Guide de l’utilisateur de SDK ou la documentation de l’API SDK.

Pour cette raison, il est important d’utiliser un espace de noms SDK entièrement qualifié lorsque vous écrivez du code d’application personnalisé qui communique avec les composants internes de la visionneuse.

Par exemple, si vous prévoyez d’écouter l’événement `StatusEvent.NOTF_VIEW_READY` et que la visionneuse est diffusée par Experience Manager, le type d’événement complet est `s7viewers.s7sdk.event.StatusEvent.NOTF_VIEW_READY` et le code d’écouteur d’événement ressemble à ce qui suit :

```javascript {.line-numbers}
<instance>.setHandlers({ 
 "initComplete":function() { 
  var zoomView = <instance>.getComponent("zoomView"); 
   zoomView.addEventListener(s7viewers.s7sdk.event.StatusEvent.NOTF_VIEW_READY, function(e) { 
   console.log("view ready"); 
  }, false); 
} 
}); 
The same code for viewer served from Dynamic Media Classic looks like this: 
<instance>.setHandlers({ 
 "initComplete":function() { 
  var zoomView = <instance>.getComponent("zoomView"); 
   zoomView.addEventListener(s7classic.s7sdk.event.StatusEvent.NOTF_VIEW_READY, function(e) { 
   console.log("view ready"); 
  }, false); 
} 
}); 
```
