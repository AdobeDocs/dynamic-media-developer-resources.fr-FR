---
description: Documentation sur les attributs de configuration de la visionneuse de supports variés.
solution: Experience Manager
title: Référence de commande - Attributs de configuration
feature: Dynamic Media Classic,Visionneuses,SDK/API,Visionneuses de médias mixtes
role: Developer,Business Practitioner
exl-id: aa750941-0a2e-4591-bdff-5e71ecc342aa
source-git-commit: bfb350e68d9b7e86cec5ee75fe9280b12ce0e54e
workflow-type: tm+mt
source-wordcount: '152'
ht-degree: 0%

---

# Référence de commande - Attributs de configuration{#command-reference-configuration-attributes}

Documentation sur les attributs de configuration de la visionneuse de supports variés.

Toute commande de configuration peut être définie dans l’URL ou à l’aide des méthodes `setParam()` ou `setParams()`, ou des deux. Tout attribut de configuration peut également être spécifié dans l’enregistrement de configuration côté serveur.

Certaines commandes de configuration peuvent comporter le préfixe du nom de classe ou du nom d’instance du composant SDK de visionneuse correspondant. Un nom d’instance du composant est dynamique et dépend de l’identifiant de l’élément DOM du conteneur de visionneuses transmis à la méthode d’API `setContainerId()`. La documentation comprend un préfixe facultatif pour ces commandes. Par exemple, la commande `zoomstep` est documentée comme suit :

`[ZoomView.|<containerId>_zoomView].zoomstep`

Cela signifie que vous pouvez utiliser cette commande comme suit :

* `zoomstep` (syntaxe courte)
* `ZoomView.zoomstep` (qualifié avec le nom de classe du composant)
* `cont_zoomView.zoomstep` (qualifié avec l’ID de composant, en supposant  `cont` qu’il s’agisse de l’ID de l’élément de conteneur)

Voir aussi [Référence de commande commune à toutes les visionneuses - Attributs de configuration](../../../r-html5-viewer-20-cmdref-configattrib/r-html5-viewer-20-cmdref-configattrib.md#concept-850e0f2c49b949deb7cfbfd330d329bd)
