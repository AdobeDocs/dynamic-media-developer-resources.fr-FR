---
title: Référence de commande - URL
description: Documentation de référence des commandes pour la visionneuse de vidéos avec recadrage intelligent.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Smart Crop,Video
role: Developer,User
exl-id: d0797c10-2379-45f7-9e8d-a5eb56638db8
source-git-commit: 1aa8be858b0ba8ec9b99753d43c202b35ed58c30
workflow-type: tm+mt
source-wordcount: '163'
ht-degree: 0%

---

# Référence de commande - URL{#command-reference-url}

Documentation de référence des commandes pour la visionneuse de vidéos avec recadrage intelligent.

Vous pouvez définir n’importe quelle commande de configuration dans l’URL. Vous pouvez également utiliser les méthodes API `setParam()` ou `setParams()`, ou les deux pour définir n’importe quelle commande de configuration. Vous pouvez également spécifier n’importe quel attribut de configuration dans l’enregistrement de configuration côté serveur.

Vous pouvez préfixer certaines commandes de configuration avec le nom de classe ou le nom d’instance du composant SDK de visionneuse correspondant. Un nom d’instance du composant est dynamique et dépend de l’identifiant de l’élément DOM du conteneur de visionneuses transmis à la méthode d’API `setContainerId()`. La documentation comprend des préfixes facultatifs pour ces commandes. Par exemple, `playback` est documenté comme suit :

```
[SmartCropVideoPlayer.|<containerId>_smartCropVideoPlayer].playback
```

Cela signifie que cette commande est utilisée de la manière suivante :

* `playback` (syntaxe courte)
* `SmartCropVideoPlayer.playback` (qualifié avec le nom de classe du composant)
* `cont_smartCropVideoPlayer.playback` (qualifié avec l’identifiant du composant, en supposant que `cont` soit l’identifiant de l’élément de conteneur)

Voir aussi [Référence de commande commune à toutes les visionneuses - Attributs de configuration](../../../r-html5-viewer-20-cmdref-configattrib/r-html5-viewer-20-cmdref-configattrib.md#concept-850e0f2c49b949deb7cfbfd330d329bd).

Voir aussi [Référence de commande commune à toutes les visionneuses - URL](../../../c-html5-viewer-20-cmdref-url/c-html5-viewer-20-cmdref-url.md#concept-9b337f349b7b406b8c33c7ee96b3e226).
