---
title: Référence de commande - Attributs de configuration
description: Documentation sur les attributs de configuration de la visionneuse de zoom.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Zoom
role: Developer,User
exl-id: 03982627-9298-4032-a15a-a5afe4ec1fb5
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '140'
ht-degree: 0%

---

# Référence de commande - Attributs de configuration{#command-reference-configuration-attributes}

Documentation sur les attributs de configuration de la visionneuse de zoom.

Toute commande de configuration peut être définie dans une URL ou à l’aide de `setParam()`, ou `setParams()`, ou les deux, méthodes API. Tout attribut de configuration peut également être spécifié dans l’enregistrement de configuration côté serveur.

Certaines commandes de configuration peuvent comporter le préfixe du nom de classe ou du nom d’instance du composant SDK de visionneuse correspondant. Un nom d’instance du composant est dynamique et dépend de l’identifiant de l’élément DOM du conteneur de visionneuses transmis à `setContainerId()` méthode API. La documentation comprend un préfixe facultatif pour ces commandes. Par exemple : `zoomstep` La commande est documentée comme suit :

`[ZoomView.|<containerId>_zoomView].zoomstep`

Ce qui signifie que vous pouvez utiliser la commande comme

* `zoomstep` (syntaxe courte)
* `ZoomView.zoomstep` (qualifié avec le nom de classe du composant)
* `cont_zoomView.zoomstep` (qualifié avec l’ID de composant, en supposant `cont` est l’identifiant de l’élément de conteneur)

Voir aussi [Référence de commande commune à toutes les visionneuses - Attributs de configuration](../../../r-html5-viewer-20-cmdref-configattrib/r-html5-viewer-20-cmdref-configattrib.md#concept-850e0f2c49b949deb7cfbfd330d329bd)
