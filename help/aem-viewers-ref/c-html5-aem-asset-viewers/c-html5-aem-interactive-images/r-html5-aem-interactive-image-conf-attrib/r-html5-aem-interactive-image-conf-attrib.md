---
description: Documentation sur les attributs de configuration de la visionneuse d’images interactives.
solution: Experience Manager
title: Référence de commande - Attributs de configuration
feature: Dynamic Media Classic,Visionneuses,SDK/API,Images interactives
role: Developer,User
exl-id: 53c4b304-3b45-4ff0-91aa-a14f39ab1e94
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '151'
ht-degree: 0%

---

# Référence de commande - Attributs de configuration{#command-reference-configuration-attributes}

Documentation sur les attributs de configuration de la visionneuse d’images interactives.

Toute commande de configuration peut être définie dans l’URL ou à l’aide des méthodes `setParam()` ou `setParams()`, ou des deux. Tout attribut de configuration peut également être spécifié dans l’enregistrement de configuration côté serveur.

Certaines commandes de configuration peuvent comporter le préfixe du nom de classe ou du nom d’instance du composant SDK de visionneuse correspondant. Un nom d’instance du composant est dynamique et dépend de l’identifiant de l’élément DOM du conteneur de visionneuses transmis à la méthode d’API `setContainerId()`. La documentation comprend un préfixe facultatif pour ces commandes. Par exemple, la commande `zoomstep` est documentée comme suit :

`[ZoomView.|<containerId>_zoomView].fmt`

Cela signifie que vous pouvez utiliser cette commande comme suit :

* `fmt` (syntaxe courte)
* `ZoomView.fmt` (qualifié avec le nom de classe du composant)
* `cont_zoomView.fmt` (qualifié avec l’ID de composant, en supposant  `cont` qu’il s’agisse de l’ID de l’élément de conteneur)

Voir aussi [Référence de commande commune à toutes les visionneuses - Attributs de configuration](../../../r-html5-viewer-20-cmdref-configattrib/r-html5-viewer-20-cmdref-configattrib.md#concept-850e0f2c49b949deb7cfbfd330d329bd)
