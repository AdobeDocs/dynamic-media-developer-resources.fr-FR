---
description: Documentation des attributs de configuration pour la visionneuse Fenêtre déroulante
solution: Experience Manager
title: Référence de commande - Attributs de configuration
feature: Dynamic Media Classic,Visionneuses,SDK/API,Fenêtre déroulante
role: Developer,User
exl-id: 2ac199ce-5dd5-4d2f-80c2-9bc370500cc4
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '149'
ht-degree: 0%

---

# Référence de commande - Attributs de configuration{#command-reference-configuration-attributes}

Documentation des attributs de configuration pour la visionneuse Fenêtre déroulante

Vous pouvez définir n’importe quelle commande de configuration dans l’URL. Vous pouvez également utiliser les méthodes `setParam()`, `setParams()` ou les deux API. Vous pouvez également spécifier n’importe quel attribut de configuration dans l’enregistrement de configuration côté serveur.

Certaines commandes de configuration comportent le préfixe du nom de classe ou du nom d’instance du composant SDK de visionneuse correspondant. Un nom d’instance du composant est dynamique et dépend de l’identifiant de l’élément DOM du conteneur de visionneuses transmis à la méthode d’API `setContainerId()`. La documentation comprend un préfixe facultatif pour ces commandes. Par exemple, la commande `zoomfactor` est documentée comme suit :

`[FlyoutZoomView.|<containerId>_flyout].zoomfactor`

La commande est utilisée comme suit :

* `zoomfactor` (syntaxe courte)
* `FlyoutZoomView.zoomfactor` (qualifié avec un nom de classe de composant)
* `cont_flyout.zoomfactor` (qualifié avec l’identifiant du composant, en supposant que  `cont` soit l’identifiant de l’élément de conteneur)

Voir aussi [Référence de commande commune à toutes les visionneuses - Attributs de configuration](../../../r-html5-viewer-20-cmdref-configattrib/r-html5-viewer-20-cmdref-configattrib.md#concept-850e0f2c49b949deb7cfbfd330d329bd)
