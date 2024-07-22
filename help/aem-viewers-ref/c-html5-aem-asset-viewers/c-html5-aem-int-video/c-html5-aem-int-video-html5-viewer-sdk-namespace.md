---
title: Espace de noms du SDK de la visionneuse
description: Espace de noms du SDK de la visionneuse
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Interactive Videos
role: Developer,User
exl-id: 4a4d821e-9351-4efa-8849-968e746911f3
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '220'
ht-degree: 0%

---

# Espace de noms du SDK de la visionneuse{#viewer-sdk-namespace}

La visionneuse est composée de nombreux composants du SDK de la visionneuse. En règle générale, la page web n’a pas besoin d’interagir directement avec l’API des composants du SDK ; tous les besoins courants sont couverts dans l’API de visionneuse elle-même.

Cependant, certains cas d’utilisation avancés nécessitent que la page web référence un composant SDK interne à l’aide de l’API de visionneuse `getComponent()`, puis utilise toute la flexibilité des API du SDK lui-même.

L’espace de noms utilisé pour charger et initialiser les composants du SDK par la visionneuse dépend de l’environnement dans lequel la visionneuse fonctionne. Si la visionneuse s’exécute dans Adobe Experience Manager, elle charge les composants du SDK dans l’espace de noms `s7viewers.s7sdk`. De même, la visionneuse diffusée à partir de Dynamic Media Classic charge le SDK dans `s7classic.s7sdk`.

Dans les deux cas, l’espace de noms utilisé par le SDK dans la visionneuse comporte `s7viewers` ou `s7classic` comme préfixe. De plus, il est différent de l’espace de noms simple `s7sdk` utilisé dans le Guide de l’utilisateur du SDK ou dans la documentation de l’API du SDK.

C’est pourquoi il est important d’utiliser un espace de noms SDK complet lorsque vous écrivez du code d’application personnalisé qui communique avec les composants de visionneuse internes.

Par exemple, si vous prévoyez d’écouter l’événement `StatusEvent.NOTF_VIEW_READY` et que la visionneuse est diffusée à partir d’un Experience Manager, le type d’événement complet est `s7viewers.s7sdk.event.StatusEvent.NOTF_VIEW_READY` et le code d’écouteur d’événement ressemble à ce qui suit :

```javascript {.line-numbers}
<instance>.setHandlers({ 
 "initComplete":function() { 
  var videoPlayer = <instance>.getComponent("videoPlayer"); 
   videoPlayer.addEventListener(s7viewers.s7sdk.event.StatusEvent.NOTF_VIEW_READY, function(e) { 
   console.log("view ready"); 
  }, false); 
} 
});
```
