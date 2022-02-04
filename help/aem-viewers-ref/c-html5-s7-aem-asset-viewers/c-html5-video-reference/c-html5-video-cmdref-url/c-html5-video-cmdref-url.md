---
title: Référence de commande - URL
description: Documentation de référence des commandes pour la visionneuse de vidéos.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Video
role: Developer,User
exl-id: 1ed78e0d-9b93-4c66-b558-fac15c51e944
source-git-commit: 6f838470a7bdea8e8c0219e59746ec82ecd802a8
workflow-type: tm+mt
source-wordcount: '159'
ht-degree: 0%

---

# Référence de commande - URL{#command-reference-url}

Documentation de référence des commandes pour la visionneuse de vidéos.

Vous pouvez définir n’importe quelle commande de configuration dans l’URL. Vous pouvez également utiliser les méthodes de l’API. `setParam()`ou `setParams()`ou les deux pour définir toute commande de configuration. Vous pouvez également spécifier n’importe quel attribut de configuration dans l’enregistrement de configuration côté serveur.

Vous pouvez préfixer certaines commandes de configuration avec le nom de classe ou le nom d’instance du composant SDK de visionneuse correspondant. Un nom d’instance du composant est dynamique et dépend de l’identifiant de l’élément DOM du conteneur de visionneuses transmis à `setContainerId()` méthode API. La documentation comprend des préfixes facultatifs pour ces commandes. Par exemple : `playback` est documenté comme suit :

```
[VideoPlayer.|<containerId>_videoPlayer].playback
```

Cela signifie que cette commande est utilisée de la manière suivante :

* `playback` (syntaxe courte)
* `VideoPlayer.playback` (qualifié avec le nom de classe du composant)
* `cont_videoPlayer.playback` (qualifié avec l’ID de composant, en supposant que `cont` est l’identifiant de l’élément de conteneur)

Voir aussi [Référence de commande commune à toutes les visionneuses - Attributs de configuration](../../../r-html5-viewer-20-cmdref-configattrib/r-html5-viewer-20-cmdref-configattrib.md#concept-850e0f2c49b949deb7cfbfd330d329bd).

Voir aussi [Référence de commande commune à toutes les visionneuses - URL](../../../c-html5-viewer-20-cmdref-url/c-html5-viewer-20-cmdref-url.md#concept-9b337f349b7b406b8c33c7ee96b3e226).
