---
description: Documentation des attributs de configuration pour Interactive Image Viewer.
seo-description: Documentation des attributs de configuration pour Interactive Image Viewer.
seo-title: Référence de commande - Attributs de configuration
solution: Experience Manager
title: Référence de commande - Attributs de configuration
topic: Dynamic media
uuid: ef118730-1bd2-4b88-917c-1fa51c6a488b
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# Référence de commande - Attributs de configuration{#command-reference-configuration-attributes}

Documentation des attributs de configuration pour Interactive Image Viewer.

Toute commande de configuration peut être définie dans l’URL ou à l’aide `setParam()`, ou `setParams()`, ou les deux, des méthodes API. Tout attribut de configuration peut également être spécifié dans l’enregistrement de configuration côté serveur.

Certaines commandes de configuration peuvent être précédées du nom de classe ou d’instance du composant SDK de lecteur correspondant. Un nom d’instance du composant est dynamique et dépend de l’ID de l’élément DOM  du lecteur transmis à la méthode `setContainerId()` API. La documentation comprend un préfixe facultatif pour ces commandes. Par exemple, `zoomstep` la commande est décrite comme suit :

`[ZoomView.|<containerId>_zoomView].fmt`

ce qui signifie que vous pouvez utiliser cette commande comme suit :

* `fmt` (syntaxe courte)
* `ZoomView.fmt` (qualifié avec le nom de classe de composant)
* `cont_zoomView.fmt` (qualifié avec l’ID de composant, en supposant `cont` qu’il s’agisse de l’ID de l’élément )

Voir aussi Référence de [commande commune à toutes les visionneuses - Attributs de configuration](../../../r-html5-viewer-20-cmdref-configattrib/r-html5-viewer-20-cmdref-configattrib.md#concept-850e0f2c49b949deb7cfbfd330d329bd)
