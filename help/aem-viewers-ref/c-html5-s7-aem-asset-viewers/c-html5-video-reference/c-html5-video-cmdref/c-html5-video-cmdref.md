---
description: Documentation des attributs de configuration pour la visionneuse de vidéos.
solution: Experience Manager
title: Référence de commande - Attributs de configuration
feature: Dynamic Media Classic,Visionneuses,SDK/API,Vidéo
role: Developer,User
exl-id: 5992e5cd-7783-408e-a23f-fdcc3a3d6b69
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '166'
ht-degree: 0%

---

# Référence de commande - Attributs de configuration{#command-reference-configuration-attributes}

Documentation des attributs de configuration pour la visionneuse de vidéos.

Vous pouvez définir n’importe quelle commande de configuration dans l’URL. Vous pouvez également utiliser les méthodes d’API `setParam()` ou `setParams()`, ou les deux pour définir n’importe quelle commande de configuration. Vous pouvez également spécifier n’importe quel attribut de configuration dans l’enregistrement de configuration côté serveur.

Vous pouvez préfixer certaines commandes de configuration avec le nom de classe ou le nom d’instance du composant SDK de visionneuse correspondant. Un nom d’instance du composant est dynamique et dépend de l’identifiant de l’élément DOM du conteneur de visionneuses transmis à la méthode d’API `setContainerId()`. La documentation comprend des préfixes facultatifs pour ces commandes. Par exemple, `playback` est documenté comme suit :

```
[VideoPlayer.|<containerId>_videoPlayer].playback
```

Cela signifie que cette commande est utilisée de la manière suivante :

* `playback` (syntaxe courte)
* `VideoPlayer.playback` (qualifié avec le nom de classe du composant)
* `cont_videoPlayer.playback` (qualifié avec l’ID de composant, en supposant que  `cont` soit l’ID de l’élément de conteneur)

Voir [Référence de commande commune à toutes les visionneuses - Attributs de configuration](../../../r-html5-viewer-20-cmdref-configattrib/r-html5-viewer-20-cmdref-configattrib.md#concept-850e0f2c49b949deb7cfbfd330d329bd)

Voir [Référence de commande commune à toutes les visionneuses - URL](../../../c-html5-viewer-20-cmdref-url/c-html5-viewer-20-cmdref-url.md#concept-9b337f349b7b406b8c33c7ee96b3e226)
