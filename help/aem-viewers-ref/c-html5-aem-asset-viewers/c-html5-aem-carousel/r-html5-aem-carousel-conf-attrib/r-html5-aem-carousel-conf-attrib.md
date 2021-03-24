---
description: Documentation sur les attributs de configuration pour la visionneuse de carrousel.
solution: Experience Manager
title: Référence de commande - Attributs de configuration
feature: Dynamic Media Classic, Visionneuses, SDK/API, Bannières de carrousel
role: Développeur, Professionnel
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '152'
ht-degree: 0%

---


# Référence de commande - Attributs de configuration{#command-reference-configuration-attributes}

Documentation sur les attributs de configuration pour la visionneuse de carrousel.

Toute commande de configuration peut être définie dans l&#39;URL ou à l&#39;aide des méthodes d&#39;API `setParam()` ou `setParams()`, ou les deux. Tout attribut de configuration peut également être spécifié dans l’enregistrement de configuration côté serveur.

Certaines commandes de configuration peuvent être précédées du nom de classe ou d’instance du composant SDK de visionneuse correspondant. Un nom d’instance du composant est dynamique et dépend de l’identifiant de l’élément DOM du conteneur de visionneuse transmis à la méthode API `setContainerId()`. La documentation contient un préfixe facultatif pour ces commandes. Par exemple, la commande `zoomstep` est documentée comme suit :

`[ZoomView.|<containerId>_carouselView].fmt`

ce qui signifie que vous pouvez utiliser cette commande comme suit :

* `fmt` (syntaxe courte)
* `CarouselView.fmt` (qualifié avec le nom de classe de composant)
* `cont_carouselView.fmt` (qualifié avec l’ID de composant, en supposant  `cont` qu’il s’agisse de l’ID de l’élément de conteneur)

Voir aussi [Référence de commande commune à toutes les visionneuses - Attributs de configuration](../../../r-html5-viewer-20-cmdref-configattrib/r-html5-viewer-20-cmdref-configattrib.md#concept-850e0f2c49b949deb7cfbfd330d329bd)
