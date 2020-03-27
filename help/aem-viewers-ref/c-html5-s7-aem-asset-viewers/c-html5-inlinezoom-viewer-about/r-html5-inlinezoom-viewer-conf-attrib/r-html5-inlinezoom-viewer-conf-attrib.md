---
description: Documentation des attributs de configuration pour le lecteur de contenu Fenêtre déroulante
seo-description: Documentation des attributs de configuration pour le lecteur de contenu Fenêtre déroulante
seo-title: Référence de commande - Attributs de configuration
solution: Experience Manager
title: Référence de commande - Attributs de configuration
topic: Dynamic media
uuid: 0813c334-37b7-43af-b39d-bec66658ad58
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# Référence de commande - Attributs de configuration{#command-reference-configuration-attributes}

Documentation des attributs de configuration pour le lecteur de contenu Fenêtre déroulante

Vous pouvez définir n’importe quelle commande de configuration dans l’URL. Vous pouvez également utiliser `setParam()`, `setParams()`ou les deux méthodes API. Vous pouvez également spécifier n’importe quel attribut de configuration dans l’enregistrement de configuration côté serveur.

Certaines commandes de configuration comportent un préfixe avec le nom de classe ou d’instance du composant SDK de lecteur correspondant. Un nom d’instance du composant est dynamique et dépend de l’ID de l’élément DOM  du lecteur transmis à la méthode `setContainerId()` API. La documentation comprend un préfixe facultatif pour ces commandes. Par exemple, la `zoomfactor` commande est décrite comme suit :

`[FlyoutZoomView.|<containerId>_flyout].zoomfactor`

La commande est utilisée comme suit :

* `zoomfactor` (syntaxe courte)
* `FlyoutZoomView.zoomfactor` (qualifié avec un nom de classe de composant)
* `cont_flyout.zoomfactor` (avec l’ID du composant, en supposant qu’ `cont` il s’agisse de l’ID de l’élément  du)

Voir aussi Référence de [commande commune à toutes les visionneuses - Attributs de configuration](../../../r-html5-viewer-20-cmdref-configattrib/r-html5-viewer-20-cmdref-configattrib.md#concept-850e0f2c49b949deb7cfbfd330d329bd)
