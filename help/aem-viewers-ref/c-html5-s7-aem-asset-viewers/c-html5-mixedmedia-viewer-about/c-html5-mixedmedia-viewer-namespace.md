---
description: Espace de noms du SDK de la visionneuse
solution: Experience Manager
title: Espace de noms du SDK de la visionneuse
feature: Dynamic Media Classic,Visionneuses,SDK/API,Visionneuses de médias mixtes
role: Developer,Business Practitioner
exl-id: 570f8eee-a7dd-40aa-b732-03f97d2544c0
source-git-commit: bfb350e68d9b7e86cec5ee75fe9280b12ce0e54e
workflow-type: tm+mt
source-wordcount: '233'
ht-degree: 0%

---

# Espace de noms du SDK de la visionneuse{#viewer-sdk-namespace}

La visionneuse est composée de nombreux composants du SDK de la visionneuse. Dans la plupart des cas, la page web n’a pas besoin d’interagir directement avec l’API des composants SDK ; tous les besoins courants sont couverts dans l’API de visionneuse elle-même.

Cependant, certains cas d’utilisation avancés nécessitent que la page web obtienne une référence à un composant SDK interne à l’aide de l’API de visionneuse `getComponent()`, puis utilise toute la flexibilité des API du SDK lui-même.

L’espace de noms utilisé pour charger et initialiser les composants du SDK par la visionneuse dépend de l’environnement dans lequel la visionneuse fonctionne. Si la visionneuse s’exécute dans AEM (Adobe Experience Manager), elle charge les composants SDK dans l’espace de noms `s7viewers.s7sdk`. De même, la visionneuse diffusée à partir de Dynamic Media Classic charge le SDK dans `s7classic.s7sdk`.

Dans les deux cas, l’espace de noms utilisé par le SDK dans la visionneuse comporte `s7viewers` ou `s7classic` comme préfixe. En outre, il diffère de l’espace de noms `s7sdk` simple utilisé dans le Guide de l’utilisateur du SDK ou dans la documentation de l’API du SDK. C’est pourquoi il est important d’utiliser un espace de noms SDK complet lorsque vous écrivez du code d’application personnalisé qui communique avec les composants de visionneuse internes.

Par exemple, si vous prévoyez d’écouter l’événement `StatusEvent.NOTF_VIEW_READY` et que la visionneuse est diffusée à partir d’AEM, le type d’événement complet est `s7viewers.s7sdk.event.StatusEvent.NOTF_VIEW_READY` et le code d’écouteur d’événement ressemble à ce qui suit :

```
<instance>.setHandlers({ 
 "initComplete":function() { 
  var zoomView = <instance>.getComponent("zoomView"); 
   zoomView.addEventListener(s7viewers.s7sdk.event.StatusEvent.NOTF_VIEW_READY, function(e) { 
   console.log("view ready"); 
  }, false); 
} 
}); 
The same code for the viewer served from Dynamic Media Classic looks like the following: 
<instance>.setHandlers({ 
 "initComplete":function() { 
  var zoomView = <instance>.getComponent("zoomView"); 
   zoomView.addEventListener(s7classic.s7sdk.event.StatusEvent.NOTF_VIEW_READY, function(e) { 
   console.log("view ready"); 
  }, false); 
} 
});
```
