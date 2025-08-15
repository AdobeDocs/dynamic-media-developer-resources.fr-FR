---
title: Référence des commandes - Attributs de configuration
description: Documentation sur les attributs de configuration de la visionneuse à 360°.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Spin Sets
role: Developer,User
exl-id: 60615258-4d20-4452-a4a3-94fb88a943d7
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '141'
ht-degree: 0%

---

# Référence des commandes - Attributs de configuration{#command-reference-configuration-attributes}

Documentation sur les attributs de configuration de la visionneuse à 360°.

Toute commande de configuration peut être définie dans l’URL ou à l’aide des méthodes d’API `setParam()`, `setParams()` ou les deux. Tout attribut de configuration peut également être spécifié dans l’enregistrement de configuration côté serveur.

Certaines commandes de configuration peuvent comporter le préfixe « class name » ou « instance name » du composant Viewer SDK correspondant. Le nom d’instance du composant est dynamique et dépend de l’identifiant de l’élément DOM du conteneur de la visionneuse transmis à `setContainerId()` méthode API. La documentation d’inclut un préfixe facultatif pour ces commandes. Par exemple, `zoomstep` commande est documentée comme suit :

`[SpinView.|<containerId>_spinView].zoomstep`

Cela signifie que vous pouvez utiliser cette commande comme suit :

* `zoomstep` (syntaxe courte)
* `SpinView.zoomstep` (qualifié avec le nom de classe du composant)
* `cont_spinView.zoomstep` (qualifié avec l’ID de composant, en supposant que `cont` soit l’ID de l’élément de conteneur)

Voir aussi [Référence des commandes commune à toutes les visionneuses - Attributs de configuration](../../../r-html5-viewer-20-cmdref-configattrib/r-html5-viewer-20-cmdref-configattrib.md#concept-850e0f2c49b949deb7cfbfd330d329bd)
