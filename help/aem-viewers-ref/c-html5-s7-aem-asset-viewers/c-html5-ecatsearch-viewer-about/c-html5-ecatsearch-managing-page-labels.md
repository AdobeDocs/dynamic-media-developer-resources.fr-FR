---
description: Gestion des libellés de page
solution: Experience Manager
title: Gestion des libellés de page
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog Search
role: Developer,User
exl-id: 73c3904f-678f-47c4-b895-86671402df79
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '263'
ht-degree: 0%

---

# Gestion des libellés de page{#managing-page-labels}

L’interface utilisateur de la visionneuse comporte deux emplacements où les libellés de page sont affichés : le mode des miniatures et la liste déroulante de la table des matières.

Il existe trois types de libellés qui peuvent être définis :

* Étiquettes définies par l’auteur à l’aide du mécanisme de localisation SYMBOL.
* Étiquettes définies par l’auteur sur le serveur principal, dans Dynamic Media Classic.
* Étiquettes générées automatiquement par la visionneuse.

Les étiquettes basées sur SYMBOL sont définies à l’aide de `MediaSet.LABEL_XX[_YY]` et de `MediaSet.LABEL_DELIM` SYMBOL, comme décrit dans la section [Localisation des éléments de l’interface utilisateur](../../c-html5-s7-aem-asset-viewers/c-html5-20-ecatalog-viewer-about/c-html5-20-ecatalog-viewer-localization.md#concept-cbfc39344c494eb7b9f6a272cff0cc74). Vous pouvez définir ces libellés pour l’ensemble de la diffusion du catalogue électronique, auquel cas vous devez utiliser une syntaxe SYMBOL courte ( `MediaSet.LABEL_XX`). Vous pouvez également le spécifier individuellement pour chaque page à l’aide de la syntaxe SYMBOL complète ( `MediaSet.LABEL_XX_YY`).

Lorsque vous définissez des libellés pour les deux pages dans la fenêtre du catalogue électronique, la visionneuse concatène ces libellés dans une chaîne à l’aide de `MediaSet.LABEL_DELIM` SYMBOL. Les libellés basés sur SYMBOL ont la priorité sur les libellés définis sur le serveur principal ou générés automatiquement par la visionneuse.

Les libellés définis dans Dynamic Media Classic sont stockés dans l’enregistrement UserData des images de page individuelles. Identique aux libellés basés sur SYMBOL. En d’autres termes, si les libellés sont définis pour les deux pages de la fenêtre du catalogue électronique, ils sont concaténés à l’aide de `MediaSet.LABEL_DELIM` SYMBOL en mode paysage. Les libellés Dynamic Media Classic ont la priorité sur les libellés générés automatiquement, mais sont remplacés par des libellés basés sur SYMBOL.

Les libellés générés automatiquement sont des numéros séquentiels attribués à toutes les pages du catalogue électronique. Les libellés générés automatiquement sont ignorés pour la diffusion donnée si des libellés basés sur SYMBOL sont définis ou si des libellés Dynamic Media Classic sont définis.

Dans la table des matières, il est possible de désactiver l&#39;affichage des libellés générés automatiquement à l&#39;aide du paramètre `showdefault` .
