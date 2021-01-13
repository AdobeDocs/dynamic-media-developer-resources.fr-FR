---
description: Espace de nommage SDK du lecteur
solution: Experience Manager
title: Espace de nommage SDK du lecteur
topic: Dynamic media
uuid: ce696dc2-3558-4fd4-8874-b58a0639099d
translation-type: tm+mt
source-git-commit: bf5873e5a6bdb859e19b15584ba85e9c106f853b
workflow-type: tm+mt
source-wordcount: '224'
ht-degree: 0%

---


# Espace de nommage SDK du lecteur{#viewer-sdk-namespace}

Le lecteur est constitué de nombreux composants du kit de développement de visionneuse. Dans la plupart des cas, la page Web n’a pas besoin d’interagir directement avec l’API des composants SDK ; tous les besoins courants sont couverts dans l’API du lecteur lui-même.

Cependant, dans certains cas d’utilisation avancés, la page Web doit obtenir une référence à un composant SDK interne à l’aide de l’API de lecteur `getComponent()`, puis utiliser toute la flexibilité des API du SDK lui-même.

L’espace de nommage utilisé par le lecteur pour charger et initialiser les composants du SDK dépend de l’environnement de fonctionnement du lecteur. Si le lecteur s’exécute dans AEM (Adobe Experience Manager), il charge les composants du SDK dans un espace de nommage `s7viewers.s7sdk`. De même, le lecteur fourni à partir de Scene7 Publishing System charge le SDK dans `s7classic.s7sdk`.

Dans les deux cas, l’espace de nommage utilisé par le kit SDK dans le lecteur contient le préfixe `s7viewers` ou `s7classic`. De plus, il est différent de l’espace de nommage simple `s7sdk` utilisé dans le Guide de l’utilisateur du SDK ou dans la documentation de l’API du SDK.

C’est pourquoi il est important d’utiliser un espace de nommage SDK complet lorsque vous écrivez un code d’application personnalisé qui communique avec les composants du lecteur interne.

Par exemple, si vous prévoyez d’écouter le événement `StatusEvent.NOTF_VIEW_READY` et que le lecteur est diffusé à partir d’AEM, le type d&#39;événement complet est `s7viewers.s7sdk.event.StatusEvent.NOTF_VIEW_READY` et le code du module d’écoute de événement ressemble à ce qui suit :

```
<instance>.setHandlers({ 
 "initComplete":function() { 
  var flyout = <instance>.getComponent("flyout"); 
   flyout.addEventListener(s7viewers.s7sdk.event.StatusEvent.NOTF_VIEW_READY, function(e) { 
   console.log("view ready"); 
  }, false); 
} 
}); 
The same code for viewer served from Scene7 SPS will look like this: 
<instance>.setHandlers({ 
 "initComplete":function() { 
  var flyout = <instance>.getComponent("flyout"); 
   flyout.addEventListener(s7classic.s7sdk.event.StatusEvent.NOTF_VIEW_READY, function(e) { 
   console.log("view ready"); 
  }, false); 
} 
});
```

