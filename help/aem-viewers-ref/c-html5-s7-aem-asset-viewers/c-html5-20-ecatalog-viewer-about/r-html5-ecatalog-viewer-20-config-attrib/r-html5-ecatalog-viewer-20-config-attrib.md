---
title: Référence de commande – Attributs de configuration
description: Documentation sur les attributs de configuration pour la visionneuse de catalogue électronique.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog
role: Developer,User
exl-id: d15061db-8941-44aa-b90d-598c1ce58a67
source-git-commit: a919130f0940d81a221b79563b6b3e41533ba788
workflow-type: tm+mt
source-wordcount: '145'
ht-degree: 0%

---

# Référence de commande – Attributs de configuration{#command-reference-configuration-attributes}

Documentation sur les attributs de configuration pour la visionneuse de catalogue électronique.

Toute commande de configuration peut être définie dans l’URL ou à l’aide de méthodes `setParam()`d’API ou des `setParams()`deux méthodes. Vous pouvez également spécifier n’importe quel attribut de configuration spécifié dans l’enregistrement de configuration côté serveur.

Pour certaines commandes de configuration, vous pouvez leur attribuer le préfixe avec le nom de classe ou le nom d’instance du composant SDK de visionneuse correspondant. Un nom d’instance du composant est dynamique et dépend de l’ID du conteneur de visionneuse élément DOM transmis à `setContainerId()` la méthode API. La documentation comprend un préfixe facultatif pour ces commandes. Par exemple, `zoomstep` la commande est documentée comme suit :

`[PageView.|<containerId>_pageView].zoomstep`

Cela signifie que vous pouvez utiliser cette commande comme

* `zoomstep` (syntaxe courte)
* `PageView.zoomstep` (qualifié avec nom de classe de composant)
* `cont_pageView.zoomstep` (qualifié avec l’ID du composant, en supposant `cont` que est l’ID de l’élément conteneur)

Voir aussi [Référence de commande commune à toutes les visionneuses - Attributs de configuration](../../../r-html5-viewer-20-cmdref-configattrib/r-html5-viewer-20-cmdref-configattrib.md#concept-850e0f2c49b949deb7cfbfd330d329bd)
