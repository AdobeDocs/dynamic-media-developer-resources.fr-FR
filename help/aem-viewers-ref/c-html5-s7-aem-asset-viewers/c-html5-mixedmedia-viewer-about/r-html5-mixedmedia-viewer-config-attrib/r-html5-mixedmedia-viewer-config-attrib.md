---
title: Référence de commande – Attributs de configuration
description: Documentation sur les attributs de configuration pour la visionneuse de supports variés.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Mixed Media Sets
role: Developer,User
exl-id: aa750941-0a2e-4591-bdff-5e71ecc342aa
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '144'
ht-degree: 0%

---

# Référence de commande – Attributs de configuration{#command-reference-configuration-attributes}

Documentation sur les attributs de configuration pour la visionneuse de supports variés.

Toute commande de configuration peut être définie dans l’URL ou à l’aide de méthodes `setParam()`d’API ou des `setParams()`deux méthodes. N’importe quel attribut de configuration peut également être spécifié dans l’enregistrement de configuration côté serveur.

Certaines commandes de configuration peuvent être précédées du nom de classe ou du nom d’instance du composant SDK de visionneuse correspondant. Un nom d’instance du composant est dynamique et dépend de l’ID du conteneur de visionneuse élément DOM transmis à `setContainerId()` la méthode API. La documentation inclut un préfixe facultatif pour ces commandes. Par exemple, `zoomstep` la commande est documentée comme suit :

`[ZoomView.|<containerId>_zoomView].zoomstep`

Cela signifie que vous pouvez utiliser cette commande comme suit :

* `zoomstep` (syntaxe courte)
* `ZoomView.zoomstep` (qualifié avec nom de classe de composant)
* `cont_zoomView.zoomstep` (qualifié avec l’ID du composant, en supposant `cont` que est l’ID de l’élément conteneur)

Voir aussi [Référence de commande commune à toutes les visionneuses - Attributs de configuration](../../../r-html5-viewer-20-cmdref-configattrib/r-html5-viewer-20-cmdref-configattrib.md#concept-850e0f2c49b949deb7cfbfd330d329bd)
