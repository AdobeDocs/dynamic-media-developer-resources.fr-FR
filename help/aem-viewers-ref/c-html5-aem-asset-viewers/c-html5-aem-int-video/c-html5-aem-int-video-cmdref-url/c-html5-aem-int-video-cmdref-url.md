---
title: Référence de la commande – URL
description: Documentation de référence des commandes pour la visionneuse de vidéos interactives.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Interactive Videos
role: Developer,User
exl-id: e0a9e269-4826-4518-9222-6a833d11746b
source-git-commit: 6aaf4eccf51a05d200c6cc780e342be646d104d8
workflow-type: tm+mt
source-wordcount: '161'
ht-degree: 0%

---

# Référence de la commande – URL{#command-reference-url}

Documentation de référence des commandes pour la visionneuse de vidéos interactives.

Vous pouvez définir n’importe quelle commande de configuration dans l’URL. Vous pouvez également utiliser les méthodes `setParam()`API , ou `setParams()`, ou les deux pour définir n’importe quelle commande de configuration. Vous pouvez également spécifier n’importe quel attribut de configuration dans l’enregistrement de configuration côté serveur.

Vous pouvez faire précéder certaines commandes de configuration du nom de classe ou du nom d’instance du composant SDK de visionneuse correspondant. Un nom d’instance du composant est dynamique et dépend de l’ID du conteneur de visionneuse élément DOM transmis à `setContainerId()` la méthode API. La documentation inclut des préfixes facultatifs pour ces commandes. Par exemple, `playback` est documenté comme suit :

```
[VideoPlayer.|<containerId>_videoPlayer].playback
```

Cela signifie que cette commande est utilisée de la manière suivante :

* `playback` (syntaxe courte)
* `VideoPlayer.playback` (qualifié avec nom de classe de composant)
* `cont_videoPlayer.playback` (qualifié avec l’ID du composant, en supposant qu’il `cont` s’agit de l’ID de l’élément conteneur)

Voir aussi [Référence de commande commune à toutes les visionneuses - Attributs](../../../r-html5-viewer-20-cmdref-configattrib/r-html5-viewer-20-cmdref-configattrib.md#concept-850e0f2c49b949deb7cfbfd330d329bd) de configuration.

Voir aussi [Référence des commandes communes à tous les visualiseurs - URL.](../../../c-html5-viewer-20-cmdref-url/c-html5-viewer-20-cmdref-url.md#concept-9b337f349b7b406b8c33c7ee96b3e226)
