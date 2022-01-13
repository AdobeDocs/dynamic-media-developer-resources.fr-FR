---
title: Référence de commande - Attributs de configuration
description: Documentation des attributs de configuration pour la visionneuse Fenêtre déroulante
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Inline Zoom
role: Developer,User
exl-id: 15e7881f-ec4f-4e44-9833-1cf965800760
source-git-commit: 50dddf148345d2ca5243d5d7108fefa56d23dad6
workflow-type: tm+mt
source-wordcount: '142'
ht-degree: 0%

---

# Référence de commande - Attributs de configuration{#command-reference-configuration-attributes}

Documentation des attributs de configuration pour la visionneuse Fenêtre déroulante

Vous pouvez définir n’importe quelle commande de configuration dans l’URL. Vous pouvez également utiliser `setParam()`, `setParams()`ou les deux méthodes d’API. Vous pouvez également spécifier n’importe quel attribut de configuration dans l’enregistrement de configuration côté serveur.

Certaines commandes de configuration comportent le préfixe du nom de classe ou du nom d’instance du composant SDK de visionneuse correspondant. Un nom d’instance du composant est dynamique et dépend de l’identifiant de l’élément DOM du conteneur de visionneuses transmis à `setContainerId()` méthode API. La documentation comprend un préfixe facultatif pour ces commandes. Par exemple, la variable `zoomfactor` La commande est documentée comme suit :

`[FlyoutZoomView.|<containerId>_flyout].zoomfactor`

La commande est utilisée comme suit :

* `zoomfactor` (syntaxe courte)
* `FlyoutZoomView.zoomfactor` (qualifié avec un nom de classe de composant)
* `cont_flyout.zoomfactor` (qualifié avec l’identifiant du composant, en supposant que `cont` est l’identifiant de l’élément de conteneur)

Voir aussi [Référence de commande commune à toutes les visionneuses - Attributs de configuration](../../../r-html5-viewer-20-cmdref-configattrib/r-html5-viewer-20-cmdref-configattrib.md#concept-850e0f2c49b949deb7cfbfd330d329bd)
