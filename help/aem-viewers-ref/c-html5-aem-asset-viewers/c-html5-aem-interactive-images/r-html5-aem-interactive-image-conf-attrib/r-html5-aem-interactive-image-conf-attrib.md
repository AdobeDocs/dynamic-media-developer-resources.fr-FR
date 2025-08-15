---
title: Référence de commande – Attributs de configuration
description: Documentation sur les attributs de configuration pour la visionneuse d’images interactive.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Interactive Images
role: Developer,User
exl-id: 53c4b304-3b45-4ff0-91aa-a14f39ab1e94
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '142'
ht-degree: 0%

---

# Référence de commande – Attributs de configuration{#command-reference-configuration-attributes}

Documentation sur les attributs de configuration pour la visionneuse d’images interactive.

Toute commande de configuration peut être définie dans l’URL ou à l’aide de méthodes `setParam()`d’API ou des `setParams()`deux méthodes. N’importe quel attribut de configuration peut également être spécifié dans l’enregistrement de configuration côté serveur.

Certaines commandes de configuration peuvent être précédées du nom de classe ou du nom d’instance du composant SDK de visionneuse correspondant. Un nom d’instance du composant est dynamique et dépend de l’ID du conteneur de visionneuse élément DOM transmis à `setContainerId()` la méthode API. La documentation inclut un préfixe facultatif pour ces commandes. Par exemple, `zoomstep` la commande est documentée comme suit :

`[ZoomView.|<containerId>_zoomView].fmt`

Cela signifie que vous pouvez utiliser cette commande comme :

* `fmt` (syntaxe courte)
* `ZoomView.fmt` (qualifié avec nom de classe de composant)
* `cont_zoomView.fmt` (qualifié avec l’ID du composant, en supposant `cont` que est l’ID de l’élément conteneur)

Voir aussi [Référence de commande commune à toutes les visionneuses - Attributs de configuration](../../../r-html5-viewer-20-cmdref-configattrib/r-html5-viewer-20-cmdref-configattrib.md#concept-850e0f2c49b949deb7cfbfd330d329bd)
