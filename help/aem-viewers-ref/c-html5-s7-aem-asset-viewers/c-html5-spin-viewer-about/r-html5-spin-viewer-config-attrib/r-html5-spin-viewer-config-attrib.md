---
description: Documentation des attributs de configuration pour la visionneuse à 360°.
seo-description: Documentation des attributs de configuration pour la visionneuse à 360°.
seo-title: Référence de commande - Attributs de configuration
solution: Experience Manager
title: Référence de commande - Attributs de configuration
topic: Dynamic media
uuid: ba60da44-d30d-459f-b3d8-5cf3ea4bcbdb
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '150'
ht-degree: 0%

---


# Référence de commande - Attributs de configuration{#command-reference-configuration-attributes}

Documentation des attributs de configuration pour la visionneuse à 360°.

Toute commande de configuration peut être définie dans l&#39;URL ou à l&#39;aide des méthodes d&#39;API `setParam()` ou `setParams()`, ou les deux. Tout attribut de configuration peut également être spécifié dans l&#39;enregistrement de configuration côté serveur.

Certaines commandes de configuration peuvent être précédées du nom de classe ou d’instance du composant SDK de visionneuse correspondant. Un nom d’instance du composant est dynamique et dépend de l’identifiant de l’élément DOM du conteneur de visionneuse transmis à la méthode API `setContainerId()`. La documentation contient un préfixe facultatif pour ces commandes. Par exemple, la commande `zoomstep` est documentée comme suit :

`[SpinView.|<containerId>_spinView].zoomstep`

ce qui signifie que vous pouvez utiliser cette commande comme suit :

* `zoomstep` (syntaxe courte)
* `SpinView.zoomstep` (qualifié avec le nom de classe de composant)
* `cont_spinView.zoomstep` (qualifié avec l’ID de composant, en supposant  `cont` qu’il s’agisse de l’ID de l’élément de conteneur)

Voir aussi [Référence de commande commune à toutes les visionneuses - Attributs de configuration](../../../r-html5-viewer-20-cmdref-configattrib/r-html5-viewer-20-cmdref-configattrib.md#concept-850e0f2c49b949deb7cfbfd330d329bd)
