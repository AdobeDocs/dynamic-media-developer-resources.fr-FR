---
title: Référence des commandes - Attributs de configuration
description: Documentation sur les attributs de configuration pour la visionneuse de vidéos avec recadrage intelligent.
solution: Experience Manager, Experience Manager Assets
feature-set: Experience Manager, Experience Manager Assets
feature: Dynamic Media Classic,Viewers,SDK/API,Smart Crop,Video
role: Developer,User
mini-toc-levels: 3
exl-id: 698c03b1-bec0-44bf-9c79-c66e0192344a
TQID: 'https://experienceleague.adobe.com/fTLIy9C3f-00e-wpBTVbQroziLWBo2YT8ieDrdlrnak'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 164
ht-degree: 0%

---

# Référence des commandes - Attributs de configuration{#command-reference-configuration-attributes}

Documentation sur les attributs de configuration pour la visionneuse de vidéos avec recadrage intelligent.

Vous pouvez définir n’importe quelle commande de configuration dans l’URL. Vous pouvez également utiliser les méthodes d’API `setParam()`, ou `setParams()`, ou les deux pour définir n’importe quelle commande de configuration. Vous pouvez également spécifier n’importe quel attribut de configuration dans l’enregistrement de configuration côté serveur.

Vous pouvez faire précéder certaines commandes de configuration du nom de classe ou du nom d’instance du composant SDK de la visionneuse correspondant. Le nom d’instance du composant est dynamique et dépend de l’identifiant de l’élément DOM du conteneur de la visionneuse transmis à `setContainerId()` méthode API. La documentation de inclut des préfixes facultatifs pour ces commandes. Par exemple, la `playback` est documentée comme suit :

```
[SmartCropVideoPlayer.|<containerId>_smartCropVideoPlayer].playback
```

Cela signifie que cette commande est utilisée de la manière suivante :

* `playback` (syntaxe courte)
* `SmartCropVideoPlayer.playback` (qualifié avec le nom de classe du composant)
* `cont_videoPlayer.playback` (qualifié avec l’ID de composant, en supposant que `cont` soit l’ID de l’élément de conteneur)

Voir [Référence des commandes commune à toutes les visionneuses - Attributs de configuration](../../../r-html5-viewer-20-cmdref-configattrib/r-html5-viewer-20-cmdref-configattrib.md#concept-850e0f2c49b949deb7cfbfd330d329bd)

Voir [Référence des commandes commune à toutes les visionneuses - URL](../../../c-html5-viewer-20-cmdref-url/c-html5-viewer-20-cmdref-url.md#concept-9b337f349b7b406b8c33c7ee96b3e226)
