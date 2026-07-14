---
description: Gestion des libellés de page
solution: Experience Manager
title: Gestion des libellés de page
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog Search
role: Developer,User
exl-id: 73c3904f-678f-47c4-b895-86671402df79
TQID: 'https://experienceleague.adobe.com/EprHC1GFDB5Lkytg4NZf8Am0myr-jXC2wxxcefelvc8'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: f6432244ef9faba7a81488e9de8e438154ae6123
workflow-type: tm+mt
source-wordcount: 269
ht-degree: 0%

---

# Gestion des libellés de page{#managing-page-labels}

Les libellés de page s’affichent à deux endroits de l’interface utilisateur de la visionneuse : en mode miniatures et dans la liste déroulante de la table des matières.

Trois types de libellés peuvent être définis :

* Libellés définis par l’auteur à l’aide du mécanisme de localisation SYMBOL.
* Libellés définis par l’auteur sur le serveur principal, dans Dynamic Media Classic.
* Libellés générés automatiquement par la visionneuse.

Les libellés basés sur des symboles sont définis à l’aide des symboles `MediaSet.LABEL_XX[_YY]` et `MediaSet.LABEL_DELIM` comme décrit dans [Localisation des éléments de l’interface utilisateur](../../c-html5-s7-aem-asset-viewers/c-html5-20-ecatalog-viewer-about/c-html5-20-ecatalog-viewer-localization.md#concept-cbfc39344c494eb7b9f6a272cff0cc74). Vous pouvez définir ces libellés pour l’ensemble de la planche de catalogue électronique, auquel cas vous devez utiliser une syntaxe SYMBOLE courte (`MediaSet.LABEL_XX`). Vous pouvez également la spécifier pour chaque page individuellement en utilisant la syntaxe SYMBOL complète (`MediaSet.LABEL_XX_YY`).

Lorsque vous définissez des libellés pour les deux pages dans la planche de catalogue électronique, la visionneuse concatène ces libellés en une seule chaîne à l’aide `MediaSet.LABEL_DELIM` SYMBOLE . Les libellés basés sur des symboles sont prioritaires sur les libellés définis sur le serveur principal ou générés automatiquement par la visionneuse.

Les libellés définis dans Dynamic Media Classic sont stockés dans l’enregistrement UserData des images de page individuelles. Comme pour les libellés basés sur des symboles. En d’autres termes, si des libellés sont définis pour les deux pages de la planche de catalogue électronique, elles sont concaténées à l’aide du SYMBOLE `MediaSet.LABEL_DELIM` en mode paysage. Les libellés Dynamic Media Classic sont prioritaires sur les libellés générés automatiquement, mais sont remplacés par des libellés basés sur des symboles.

Les libellés générés automatiquement sont des numéros séquentiels affectés à toutes les pages du catalogue électronique. Les libellés générés automatiquement sont ignorés pour la planche donnée si des libellés basés sur des symboles ou des libellés Dynamic Media Classic sont définis.

Dans la table des matières, il est possible de désactiver l’affichage des libellés générés automatiquement à l’aide du paramètre `showdefault`.

