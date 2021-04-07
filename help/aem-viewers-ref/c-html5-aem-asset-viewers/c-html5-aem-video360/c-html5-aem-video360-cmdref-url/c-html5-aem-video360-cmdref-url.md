---
description: Documentation de référence sur les commandes du lecteur vidéo360.
solution: Experience Manager
title: Référence de commande - URL
feature: Dynamic Media Classic, Visionneuses, SDK/API, Vidéo 360 VR
role: Développeur, Professionnel
exl-id: eb7026cf-f28b-4426-ba64-b3472946d5d4
translation-type: tm+mt
source-git-commit: b4344397f82eb7d2d61020909f4acc7fddea210b
workflow-type: tm+mt
source-wordcount: '169'
ht-degree: 0%

---

# Référence de commande - URL{#command-reference-url}

Documentation de référence sur les commandes du lecteur vidéo360.

Vous pouvez définir n’importe quelle commande de configuration dans l’URL. Vous pouvez également utiliser les méthodes d&#39;API `setParam()` ou `setParams()`, ou les deux pour définir n&#39;importe quelle commande de configuration. Vous pouvez également spécifier n’importe quel attribut de configuration dans l’enregistrement de configuration côté serveur.

Vous pouvez préfixer certaines commandes de configuration avec le nom de classe ou le nom d’instance du composant SDK de visionneuse HTML5 correspondant. Un nom d’instance du composant est dynamique et dépend de l’identifiant de l’élément DOM du conteneur de visionneuse transmis à la méthode API `setContainerId()`. La documentation contient des préfixes facultatifs pour ces commandes. Par exemple, `playback` est documenté comme suit :

```
[Video360Player.|<containerId>_video360Player].playback
```

ce qui signifie que cette commande est utilisée de la manière suivante :

* `playback` (syntaxe courte)
* `Video360Player.playback` (qualifié avec le nom de classe de composant)
* `cont_video360Player.playback` (qualifié avec l’ID de composant, en supposant qu’ `cont` il s’agisse de l’ID de l’élément de conteneur)

Voir [Référence de commande commune à toutes les visionneuses - Attributs de configuration](../../../r-html5-viewer-20-cmdref-configattrib/r-html5-viewer-20-cmdref-configattrib.md#concept-850e0f2c49b949deb7cfbfd330d329bd) et [Référence de commande commune à toutes les visionneuses - URL](../../../c-html5-viewer-20-cmdref-url/c-html5-viewer-20-cmdref-url.md#concept-9b337f349b7b406b8c33c7ee96b3e226)
