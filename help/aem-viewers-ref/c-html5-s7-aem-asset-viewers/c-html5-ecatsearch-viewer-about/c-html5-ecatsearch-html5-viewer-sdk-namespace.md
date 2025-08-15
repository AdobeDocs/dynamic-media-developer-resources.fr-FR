---
description: Espace de noms SDK de la visionneuse
solution: Experience Manager
title: Espace de noms SDK de la visionneuse
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog Search
role: Developer,User
exl-id: aaad8f43-f6f2-440f-a6c4-52db585b48da
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '227'
ht-degree: 0%

---

# Espace de noms SDK de la visionneuse{#viewer-sdk-namespace}

La visionneuse est créée à partir de nombreux composants du kit SDK de la visionneuse. Dans la plupart des cas, la page Web n’a pas besoin d’interagir directement avec l’API des composants du SDK ; tous les besoins courants sont couverts dans l’API de visionneuse elle-même.

Toutefois, certains cas d’utilisation avancés exigent que la page Web obtienne une référence à un composant SDK interne à l’aide de l’API `getComponent()` de visionneuse, puis utilise toute la flexibilité des API du SDK lui-même.

L’espace de noms utilisé pour charger et initialiser les composants SDK par la visionneuse dépend de l’environnement dans lequel la visionneuse fonctionne. Si la visionneuse s’exécute dans AEM (Adobe Experience Manager), elle charge les composants SDK dans l’espace de `s7viewers.s7sdk` noms. Et la visionneuse servie à partir d’Dynamic Media Classic charge le SDK dans `s7classic.s7sdk`.

Dans les deux cas, l’espace de noms utilisé par le SDK à l’intérieur de la visionneuse a `s7viewers` soit comme préfixe, soit `s7classic` comme préfixe. Et, il est différent de l’espace de noms brut `s7sdk` utilisé dans le Guide de l’utilisateur SDK ou la documentation de l’API SDK.

Pour cette raison, il est important d’utiliser un espace de noms SDK complet lorsque vous écrivez du code d’application personnalisé qui communique avec les composants internes de la visionneuse.

Par exemple, si vous prévoyez d’écouter `StatusEvent.NOTF_VIEW_READY` un événement et que la visionneuse est diffusée à partir d’Dynamic Media Classic, le type d’événement complet est `s7classic.s7sdk.event.StatusEvent.NOTF_VIEW_READY`, et le code du détecteur d’événements ressemble à ce qui suit :

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
