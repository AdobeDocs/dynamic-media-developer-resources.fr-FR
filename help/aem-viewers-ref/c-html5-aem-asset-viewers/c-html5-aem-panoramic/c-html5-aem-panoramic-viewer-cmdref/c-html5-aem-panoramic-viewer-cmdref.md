---
title: Référence des commandes - Attributs de configuration
description: Documentation sur les attributs de configuration de la visionneuse panoramique.
solution: Experience Manager
role: Developer,User
autotag-review: '2026-05-13T22:15:11.019Z'
TQID: 'https://experienceleague.adobe.com/-6kskMStr-k7aFwy9GpQE-wjq4iAgwuEqzP2H1BWk2U'
product_v2: id: beaff0dd-a904-4c6b-8290-b527cd877d75id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
source-git-commit: e76d4c499daf8c8a7a0be31e56d84f917c643095
workflow-type: tm+mt
source-wordcount: 149
ht-degree: 0%

---

# Référence des commandes - Attributs de configuration{#command-reference-configuration-attributes}

<!--
feature: Dynamic Media Classic,Viewers,SDK/API
-->

Documentation sur les attributs de configuration de la visionneuse panoramique.

Toute commande de configuration peut être définie dans une URL ou à l’aide de méthodes d’API `setParam()` et/ou `setParams()`. Tout attribut de configuration peut également être spécifié dans l’enregistrement de configuration côté serveur.

Certaines commandes de configuration peuvent être précédées du nom de classe ou du nom d’instance du composant SDK HTML5 correspondant. Le nom d’instance du composant est dynamique et dépend de l’identifiant de l’élément DOM du conteneur de la visionneuse transmis à `setContainerId()` méthode API. La documentation inclut un préfixe facultatif pour ces commandes. Par exemple, `vrrender` commande est documentée comme suit :

```
[PanoramicView.|<containerId>_panoramicView].vrrender
```

Cela signifie que cette commande est utilisée de la manière suivante :

* `vrrender` (syntaxe courte)
* `PanoramicView.vrrender` (qualifié avec le nom de classe du composant)
* `cont_panoramicView.vrrender` (qualifié avec l’ID de composant, en supposant que cont soit l’identifiant de l’élément de conteneur)


Voir [Référence des commandes commune à toutes les visionneuses - Attributs de configuration](../../../r-html5-viewer-20-cmdref-configattrib/r-html5-viewer-20-cmdref-configattrib.md#concept-850e0f2c49b949deb7cfbfd330d329bd)

Voir [Référence des commandes commune à toutes les visionneuses - URL](../../../c-html5-viewer-20-cmdref-url/c-html5-viewer-20-cmdref-url.md#concept-9b337f349b7b406b8c33c7ee96b3e226)
