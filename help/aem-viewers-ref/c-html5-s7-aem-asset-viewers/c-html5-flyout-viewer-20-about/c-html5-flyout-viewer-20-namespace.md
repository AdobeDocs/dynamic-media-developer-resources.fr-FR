---
description: 'null'
seo-description: 'null'
seo-title: 'Kit de développement  du lecteur de contenu '
solution: Experience Manager
title: 'Kit de développement  du lecteur de contenu '
topic: Dynamic media
uuid: 5fa7102b-c93d-4865-9e14-fa8813403de2
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# Kit de développement  du lecteur de contenu{#viewer-sdk-namespace}

Le lecteur est constitué de nombreux composants SDK de lecteur. Dans la plupart des cas, la page Web n’a pas besoin d’interagir directement avec l’API des composants SDK ; tous les besoins courants sont traités dans l’API du lecteur lui-même.

Cependant, dans certains cas d’utilisation avancés, la page Web doit obtenir une référence à un composant SDK interne à l’aide de l’API du `getComponent()` lecteur, puis utiliser toute la flexibilité des API du SDK lui-même.

Le  de  utilisé pour charger et initialiser les composants du SDK par le lecteur dépend du  dans lequel le lecteur fonctionne. Si le lecteur s’exécute dans AEM (Adobe Experience Manager), il charge les composants du SDK dans   de. `s7viewers.s7sdk` De même, la visionneuse diffusée à partir de Scene7 Publishing System charge le SDK dans `s7classic.s7sdk`.

Dans tous les cas, le   utilisé par le kit SDK dans le lecteur de contenu comporte le préfixe `s7viewers` ou `s7classic` . Il est également différent de l’ simple `s7sdk` utilisée dans le Guide de l’utilisateur du SDK ou dans la documentation de l’API du SDK. C’est pourquoi il est important d’utiliser un SDK  complet lorsque vous écrivez un code d’application personnalisé qui communique avec les composants du lecteur interne.

Si, par exemple, vous prévoyez d’écouter les  du `StatusEvent.NOTF_VIEW_READY` et que le lecteur est diffusé à partir d’AEM, le  complet du est `s7viewers.s7sdk.event.StatusEvent.NOTF_VIEW_READY`, et le code du module d’écoute de l’ d’écoute de l’ressemble à ce qui suit :

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

