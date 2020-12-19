---
description: Documentation sur les attributs de configuration pour le lecteur vidéo360.
seo-description: Documentation sur les attributs de configuration pour le lecteur vidéo360.
seo-title: Référence de commande - Attributs de configuration
solution: Experience Manager
title: Référence de commande - Attributs de configuration
topic: Dynamic media
uuid: 645bba87-3d84-46e9-97fc-7019c5dd87ca
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '151'
ht-degree: 0%

---


# Référence de commande - Attributs de configuration{#command-reference-configuration-attributes}

Documentation sur les attributs de configuration pour le lecteur vidéo360.

Toute commande de configuration peut être définie dans l&#39;URL ou à l&#39;aide des méthodes d&#39;API `setParam()` ou `setParams()`, ou les deux. Tout attribut de configuration peut également être spécifié dans l&#39;enregistrement de configuration côté serveur.

Certaines commandes de configuration peuvent être précédées du nom de classe ou d’instance du composant SDK de visionneuse correspondant. Un nom d’instance du composant est dynamique et dépend de l’identifiant de l’élément DOM du conteneur de visionneuse transmis à la méthode API `setContainerId()`. La documentation contient un préfixe facultatif pour ces commandes. Par exemple, la commande `playback` est documentée comme suit :

`[VideoPlayer.|<containerId>_videoPlayer].playback`

ce qui signifie que vous pouvez utiliser cette commande comme suit :

* `playback` (syntaxe courte)
* `VideoPlayer.playback` (qualifié avec le nom de classe de composant)
* `cont_videoPlayer.playback` (qualifié avec l’ID de composant, en supposant  `cont` qu’il s’agisse de l’ID de l’élément de conteneur)

Voir aussi [Référence de commande commune à toutes les visionneuses - Attributs de configuration](../../../r-html5-viewer-20-cmdref-configattrib/r-html5-viewer-20-cmdref-configattrib.md#concept-850e0f2c49b949deb7cfbfd330d329bd)
