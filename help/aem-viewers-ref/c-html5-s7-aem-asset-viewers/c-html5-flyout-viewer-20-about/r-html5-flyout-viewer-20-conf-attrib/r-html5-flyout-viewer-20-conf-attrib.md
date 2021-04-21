---
description: Documentation sur les attributs de configuration pour le lecteur de contenu Fenêtre déroulante
solution: Experience Manager
title: Référence de commande - Attributs de configuration
feature: Dynamic Media Classic,Viewers,SDK/API,Flyout
role: Developer,Business Practitioner
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '152'
ht-degree: 0%

---


# Référence de commande - Attributs de configuration{#command-reference-configuration-attributes}

Documentation sur les attributs de configuration pour le lecteur de contenu Fenêtre déroulante

Vous pouvez définir n’importe quelle commande de configuration dans l’URL. Vous pouvez également utiliser les méthodes `setParam()`, `setParams()` ou les deux méthodes d&#39;API. Vous pouvez également spécifier n’importe quel attribut de configuration dans l’enregistrement de configuration côté serveur.

Certaines commandes de configuration comportent un préfixe avec le nom de classe ou d’instance du composant SDK de visionneuse correspondant. Un nom d’instance du composant est dynamique et dépend de l’identifiant de l’élément DOM du conteneur de visionneuse transmis à la méthode API `setContainerId()`. La documentation contient un préfixe facultatif pour ces commandes. Par exemple, la commande `zoomfactor` est documentée comme suit :

`[FlyoutZoomView.|<containerId>_flyout].zoomfactor`

La commande est utilisée comme suit :

* `zoomfactor` (syntaxe courte)
* `FlyoutZoomView.zoomfactor` (qualifié avec un nom de classe de composant)
* `cont_flyout.zoomfactor` (qualifié avec l’identifiant du composant, en supposant qu’ `cont` il s’agisse de l’identifiant de l’élément conteneur)

Voir aussi [Référence de commande commune à toutes les visionneuses - Attributs de configuration](../../../r-html5-viewer-20-cmdref-configattrib/r-html5-viewer-20-cmdref-configattrib.md#concept-850e0f2c49b949deb7cfbfd330d329bd)
