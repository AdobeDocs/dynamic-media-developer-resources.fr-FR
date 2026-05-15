---
title: Référence des commandes - Attributs de configuration
description: Documentation sur les attributs de configuration pour la visionneuse de catalogue électronique.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog
role: Developer,User
exl-id: d15061db-8941-44aa-b90d-598c1ce58a67
TQID: 'https://experienceleague.adobe.com/NRcFJ2RyskUxLayfdSmJ-jk-rHjPWiOWt0XwQJ7tvM8'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 146
ht-degree: 0%

---

# Référence des commandes - Attributs de configuration{#command-reference-configuration-attributes}

Documentation sur les attributs de configuration pour la visionneuse de catalogue électronique.

Toute commande de configuration peut être définie dans l’URL ou à l’aide des méthodes d’API `setParam()`, `setParams()` ou les deux. Vous pouvez également spécifier n’importe quel attribut de configuration spécifié dans l’enregistrement de configuration côté serveur.

Pour certaines commandes de configuration, vous pouvez les préfixer avec le nom de classe ou le nom d’instance du composant SDK de la visionneuse correspondant. Le nom d’instance du composant est dynamique et dépend de l’identifiant de l’élément DOM du conteneur de la visionneuse transmis à `setContainerId()` méthode API. La documentation inclut un préfixe facultatif pour ces commandes. Par exemple, `zoomstep` commande est documentée comme suit :

`[PageView.|<containerId>_pageView].zoomstep`

Cela signifie que vous pouvez utiliser cette commande comme suit :

* `zoomstep` (syntaxe courte)
* `PageView.zoomstep` (qualifié avec le nom de classe du composant)
* `cont_pageView.zoomstep` (qualifié avec l’ID de composant, en supposant que `cont` soit l’ID de l’élément de conteneur)

Voir aussi [Référence des commandes commune à toutes les visionneuses - Attributs de configuration](../../../r-html5-viewer-20-cmdref-configattrib/r-html5-viewer-20-cmdref-configattrib.md#concept-850e0f2c49b949deb7cfbfd330d329bd)
