---
description: Espace de noms du SDK de la visionneuse
solution: Experience Manager
title: Espace de noms du SDK de la visionneuse
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog Search
role: Developer,User
exl-id: aaad8f43-f6f2-440f-a6c4-52db585b48da
source-git-commit: b89ca96947f751b750623e1f18d2a5d86f0cd759
workflow-type: tm+mt
source-wordcount: '226'
ht-degree: 0%

---

# Espace de noms du SDK de la visionneuse{#viewer-sdk-namespace}

La visionneuse est composée de nombreux composants du SDK de la visionneuse. Dans la plupart des cas, la page web n’a pas besoin d’interagir directement avec l’API des composants SDK ; tous les besoins courants sont couverts dans l’API de visionneuse elle-même.

Cependant, certains cas d’utilisation avancés nécessitent que la page web obtienne une référence à un composant SDK interne à l’aide de la fonction `getComponent()` API de visionneuse, puis utilisez toute la flexibilité des API du SDK lui-même.

L’espace de noms utilisé pour charger et initialiser les composants du SDK par la visionneuse dépend de l’environnement dans lequel la visionneuse fonctionne. Si la visionneuse s’exécute dans AEM (Adobe Experience Manager), elle charge les composants du SDK dans `s7viewers.s7sdk` espace de noms. Et la visionneuse diffusée à partir de Dynamic Media Classic charge le SDK dans `s7classic.s7sdk`.

Dans les deux cas, l’espace de noms utilisé par le SDK dans la visionneuse comporte l’une des fonctions suivantes : `s7viewers` ou `s7classic` comme préfixe. Et elle est différente de la plaine `s7sdk` Espace de noms utilisé dans le Guide de l’utilisateur du SDK ou dans la documentation de l’API du SDK.

C’est pourquoi il est important d’utiliser un espace de noms SDK complet lorsque vous écrivez du code d’application personnalisé qui communique avec les composants de visionneuse internes.

Par exemple, si vous prévoyez d’écouter `StatusEvent.NOTF_VIEW_READY` et que la visionneuse est diffusée à partir de Dynamic Media Classic, le type d’événement complet est `s7classic.s7sdk.event.StatusEvent.NOTF_VIEW_READY`et le code de l’écouteur d’événement ressemble à ce qui suit :

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
