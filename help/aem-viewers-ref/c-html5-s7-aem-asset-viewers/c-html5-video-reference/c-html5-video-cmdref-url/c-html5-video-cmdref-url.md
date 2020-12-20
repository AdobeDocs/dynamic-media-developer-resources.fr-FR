---
description: Documentation de référence des commandes pour la visionneuse de vidéos.
seo-description: Documentation de référence des commandes pour la visionneuse de vidéos.
seo-title: Référence de commande - URL
solution: Experience Manager
title: Référence de commande - URL
topic: Dynamic media
uuid: 4f9e4a79-6865-4e41-b30b-84ff2c6f6045
translation-type: tm+mt
source-git-commit: 3266e8682711dac379a09a0e992d33b8ffc7b5a4
workflow-type: tm+mt
source-wordcount: '168'
ht-degree: 0%

---


# Référence de commande - URL{#command-reference-url}

Documentation de référence des commandes pour la visionneuse de vidéos.

Vous pouvez définir n’importe quelle commande de configuration dans l’URL. Vous pouvez également utiliser les méthodes d&#39;API `setParam()` ou `setParams()`, ou les deux pour définir n&#39;importe quelle commande de configuration. Vous pouvez également spécifier n’importe quel attribut de configuration dans l’enregistrement de configuration côté serveur.

Vous pouvez préfixer certaines commandes de configuration avec le nom de classe ou le nom d’instance du composant SDK de visionneuse correspondant. Un nom d’instance du composant est dynamique et dépend de l’identifiant de l’élément DOM du conteneur de visionneuse transmis à la méthode API `setContainerId()`. La documentation contient des préfixes facultatifs pour ces commandes. Par exemple, `playback` est documenté comme suit :

```
[VideoPlayer.|<containerId>_videoPlayer].playback
```

ce qui signifie que cette commande est utilisée de la manière suivante :

* `playback` (syntaxe courte)
* `VideoPlayer.playback` (qualifié avec le nom de classe de composant)
* `cont_videoPlayer.playback` (qualifié avec l’ID de composant, en supposant qu’ `cont` il s’agisse de l’ID de l’élément de conteneur)

Voir aussi [Référence de commande commune à toutes les visionneuses - Attributs de configuration](../../../r-html5-viewer-20-cmdref-configattrib/r-html5-viewer-20-cmdref-configattrib.md#concept-850e0f2c49b949deb7cfbfd330d329bd).

Voir aussi [Référence de commande commune à toutes les visionneuses - URL](../../../c-html5-viewer-20-cmdref-url/c-html5-viewer-20-cmdref-url.md#concept-9b337f349b7b406b8c33c7ee96b3e226).
