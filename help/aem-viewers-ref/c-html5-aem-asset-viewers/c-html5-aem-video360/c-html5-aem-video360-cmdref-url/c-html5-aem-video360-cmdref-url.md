---
title: Référence de la commande – URL
description: Documentation de référence des commandes pour la visionneuse Video360.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,360 VR Video
role: Developer,User
exl-id: eb7026cf-f28b-4426-ba64-b3472946d5d4
source-git-commit: 24667a5ebab54ba22c4a3f6b52d19d7a31a93576
workflow-type: tm+mt
source-wordcount: '157'
ht-degree: 0%

---

# Référence de la commande – URL{#command-reference-url}

Documentation de référence des commandes pour la visionneuse Video360.

Vous pouvez définir n’importe quelle commande de configuration dans l’URL. Vous pouvez également utiliser les méthodes `setParam()`API , ou `setParams()`, ou les deux pour définir n’importe quelle commande de configuration. Vous pouvez également spécifier n’importe quel attribut de configuration dans l’enregistrement de configuration côté serveur.

Vous pouvez préfixer certaines commandes de configuration avec le nom de classe ou le nom d’instance du composant HTML5 Viewer SDK correspondant. Un nom d’instance du composant est dynamique et dépend de l’ID du conteneur de visionneuse élément DOM transmis à `setContainerId()` la méthode API. La documentation inclut des préfixes facultatifs pour ces commandes. Par exemple, `playback` est documenté comme suit :

```
[Video360Player.|<containerId>_video360Player].playback
```

Cela signifie que cette commande est utilisée de la manière suivante :

* `playback` (syntaxe courte)
* `Video360Player.playback` (qualifié avec nom de classe de composant)
* `cont_video360Player.playback` (qualifié avec l’ID du composant, en supposant qu’il `cont` s’agit de l’ID de l’élément conteneur)

Voir [Référence de commande commune à tous les visualiseurs - Attributs](../../../r-html5-viewer-20-cmdref-configattrib/r-html5-viewer-20-cmdref-configattrib.md#concept-850e0f2c49b949deb7cfbfd330d329bd) de configuration et [Référence de commande communs à tous les visualiseurs - URL](../../../c-html5-viewer-20-cmdref-url/c-html5-viewer-20-cmdref-url.md#concept-9b337f349b7b406b8c33c7ee96b3e226)
