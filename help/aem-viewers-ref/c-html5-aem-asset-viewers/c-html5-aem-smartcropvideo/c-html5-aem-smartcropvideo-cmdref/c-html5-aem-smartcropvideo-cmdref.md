---
title: Référence de commande – Attributs de configuration
description: Documentation sur les attributs de configuration pour la visionneuse de vidéos avec recadrage intelligent.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Smart Crop,Video
role: Developer,User
mini-toc-levels: 3
exl-id: 698c03b1-bec0-44bf-9c79-c66e0192344a
source-git-commit: eaf59166fcc1ff8ec5a2e846ef0eb180c8cbdd5a
workflow-type: tm+mt
source-wordcount: '163'
ht-degree: 0%

---


# Référence de commande – Attributs de configuration{#command-reference-configuration-attributes}

Documentation sur les attributs de configuration pour la visionneuse de vidéos avec recadrage intelligent.

Vous pouvez définir n’importe quelle commande de configuration dans l’URL. Vous pouvez également utiliser les méthodes `setParam()`API , ou `setParams()`, ou les deux pour définir n’importe quelle commande de configuration. Vous pouvez également spécifier n’importe quel attribut de configuration dans l’enregistrement de configuration côté serveur.

Vous pouvez faire précéder certaines commandes de configuration du nom de classe ou du nom d’instance du composant SDK de visionneuse correspondant. Un nom d’instance du composant est dynamique et dépend de l’ID du conteneur de visionneuse élément DOM transmis à `setContainerId()` la méthode API. La documentation inclut des préfixes facultatifs pour ces commandes. Par exemple, `playback` est documenté comme suit :

```
[SmartCropVideoPlayer.|<containerId>_smartCropVideoPlayer].playback
```

Cela signifie que cette commande est utilisée de la manière suivante :

* `playback` (syntaxe courte)
* `SmartCropVideoPlayer.playback` (qualifié avec nom de classe de composant)
* `cont_videoPlayer.playback` (qualifié avec l’ID du composant, en supposant qu’il `cont` s’agit de l’ID de l’élément conteneur)

Voir [Référence de commande commune à toutes les visionneuses - Attributs de configuration](../../../r-html5-viewer-20-cmdref-configattrib/r-html5-viewer-20-cmdref-configattrib.md#concept-850e0f2c49b949deb7cfbfd330d329bd)

Voir [Référence de commande commune à tous les visualiseurs - URL](../../../c-html5-viewer-20-cmdref-url/c-html5-viewer-20-cmdref-url.md#concept-9b337f349b7b406b8c33c7ee96b3e226)
