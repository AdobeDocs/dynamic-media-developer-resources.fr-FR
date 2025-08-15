---
title: Espace de noms SDK de la visionneuse
description: Espace de noms SDK de la visionneuse
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Inline Zoom
role: Developer,User
exl-id: 62b61a17-f9ae-4e71-bd78-276674193044
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '220'
ht-degree: 0%

---

# Espace de noms SDK de la visionneuse{#viewer-sdk-namespace}

La visionneuse est créée à partir de nombreux composants du kit SDK de la visionneuse. En règle générale, la page Web n’a pas besoin d’interagir directement avec l’API des composants du SDK ; tous les besoins courants sont couverts dans l’API de visionneuse elle-même.

Toutefois, certains cas d’utilisation avancés nécessitent que la page Web référence un composant SDK interne à l’aide de l’API `getComponent()` de visionneuse, puis utilise toute la flexibilité des API du SDK lui-même.

L’espace de noms utilisé pour charger et initialiser les composants SDK par la visionneuse dépend de l’environnement dans lequel la visionneuse fonctionne. Si la visionneuse s’exécute dans Adobe Experience Manager, elle charge les composants SDK dans l’espace de `s7viewers.s7sdk` noms. De même, la visionneuse servie à partir de Dynamic Media Classic charge le SDK dans `s7classic.s7sdk`.

Dans les deux cas, l’espace de noms utilisé par le SDK à l’intérieur de la visionneuse a `s7viewers` soit comme préfixe, soit `s7classic` comme préfixe. Et, il est différent de l’espace de noms brut `s7sdk` utilisé dans le Guide de l’utilisateur SDK ou la documentation de l’API SDK.

Pour cette raison, il est important d’utiliser un espace de noms SDK complet lorsque vous écrivez du code d’application personnalisé qui communique avec les composants internes de la visionneuse.

Par exemple, si vous prévoyez d’écouter `StatusEvent.NOTF_VIEW_READY` un événement et que la visionneuse est diffusée à partir d’Experience Manager, le type d’événement complet est `s7viewers.s7sdk.event.StatusEvent.NOTF_VIEW_READY`, et le code du récepteur d’événement ressemble à ce qui suit :

```javascript {.line-numbers}
<instance>.setHandlers({ 
 "initComplete":function() { 
  var flyout = <instance>.getComponent("flyout"); 
   flyout.addEventListener(s7viewers.s7sdk.event.StatusEvent.NOTF_VIEW_READY, function(e) { 
   console.log("view ready"); 
  }, false); 
} 
}); 
The same code for viewer served from Dynamic Media Classic looks like this: 
<instance>.setHandlers({ 
 "initComplete":function() { 
  var flyout = <instance>.getComponent("flyout"); 
   flyout.addEventListener(s7classic.s7sdk.event.StatusEvent.NOTF_VIEW_READY, function(e) { 
   console.log("view ready"); 
  }, false); 
} 
});
```
