---
description: Documentation des attributs de configuration pour la visionneuse de catalogue électronique.
seo-description: Documentation des attributs de configuration pour la visionneuse de catalogue électronique.
seo-title: Référence de commande - Attributs de configuration
solution: Experience Manager
title: Référence de commande - Attributs de configuration
topic: Dynamic Media
uuid: e1111ce2-67e8-449a-9cc2-bb53b61158a9
translation-type: tm+mt
source-git-commit: e4695cc4e882351ec3f2c55fd8a3cfca455bd79d
workflow-type: tm+mt
source-wordcount: '155'
ht-degree: 0%

---


# Référence de commande - Attributs de configuration{#command-reference-configuration-attributes}

Documentation des attributs de configuration pour la visionneuse de catalogue électronique.

Toute commande de configuration peut être définie dans l&#39;URL ou à l&#39;aide des méthodes d&#39;API `setParam()` ou `setParams()`, ou les deux. Vous pouvez également spécifier tout attribut de configuration spécifié dans l’enregistrement de configuration côté serveur.

Pour certaines commandes de configuration, vous pouvez les préfixer avec le nom de classe ou d’instance du composant SDK de visionneuse correspondant. Un nom d’instance du composant est dynamique et dépend de l’identifiant de l’élément DOM du conteneur de visionneuse transmis à la méthode API `setContainerId()`. La documentation inclut un préfixe facultatif pour ces commandes. Par exemple, la commande `zoomstep` est documentée comme suit :

`[PageView.|<containerId>_pageView].zoomstep`

ce qui signifie que vous pouvez utiliser cette commande comme suit :

* `zoomstep` (syntaxe courte)
* `PageView.zoomstep` (qualifié avec le nom de classe de composant)
* `cont_pageView.zoomstep` (qualifié avec l’ID de composant, en supposant  `cont` qu’il s’agisse de l’ID de l’élément de conteneur)

Voir aussi [Référence de commande commune à toutes les visionneuses - Attributs de configuration](../../../r-html5-viewer-20-cmdref-configattrib/r-html5-viewer-20-cmdref-configattrib.md#concept-850e0f2c49b949deb7cfbfd330d329bd)
