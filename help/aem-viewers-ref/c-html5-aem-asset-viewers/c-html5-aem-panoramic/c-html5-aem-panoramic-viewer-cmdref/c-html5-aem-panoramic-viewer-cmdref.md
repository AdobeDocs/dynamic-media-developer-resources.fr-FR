---
title: Référence de commande - Attributs de configuration
description: Documentation des attributs de configuration pour la visionneuse panoramique.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Panoramic
role: Developer,User
source-git-commit: 50dddf148345d2ca5243d5d7108fefa56d23dad6
workflow-type: tm+mt
source-wordcount: '149'
ht-degree: 0%

---

# Référence de commande - Attributs de configuration{#command-reference-configuration-attributes}

Documentation des attributs de configuration pour la visionneuse panoramique.

Toute commande de configuration peut être définie dans une URL ou à l’aide de `setParam()` et/ou `setParams()` méthodes API. Any config attribute can be also specified in server-side configuration record.

Some configuration commands may be prefixed with the class name or instance name of corresponding HTML5 SDK component. Un nom d’instance du composant est dynamique et dépend de l’identifiant de l’élément DOM du conteneur de visionneuses transmis à `setContainerId()` méthode API. La documentation inclura un préfixe facultatif pour ces commandes. Par exemple : `vrrender` La commande est documentée comme suit :

```
[PanoramicView.|<containerId>_panoramicView].vrrender
```

Cela signifie que cette commande est utilisée de la manière suivante :

* `vrrender` (syntaxe courte)
* `PanoramicView.vrrender` (qualifié avec le nom de classe du composant)
* `cont_panoramicView.vrrender` (qualifié avec l’ID de composant, en supposant que le nombre soit l’ID de l’élément de conteneur)


Voir [Référence de commande commune à toutes les visionneuses - Attributs de configuration](../../../r-html5-viewer-20-cmdref-configattrib/r-html5-viewer-20-cmdref-configattrib.md#concept-850e0f2c49b949deb7cfbfd330d329bd)

Voir [Référence de commande commune à toutes les visionneuses - URL](../../../c-html5-viewer-20-cmdref-url/c-html5-viewer-20-cmdref-url.md#concept-9b337f349b7b406b8c33c7ee96b3e226)
