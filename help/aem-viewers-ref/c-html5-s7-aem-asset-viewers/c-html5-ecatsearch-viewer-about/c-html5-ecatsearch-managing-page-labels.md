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

Il y a deux endroits dans l’interface utilisateur de la visionneuse où les étiquettes de page sont affichées : le mode miniatures et la liste déroulante de la table des matières.

Trois types d’étiquettes peuvent être définis :

* Étiquettes définies par l’auteur à l’aide du mécanisme de localisation SYMBOL.
* Libellés définis par l’auteur sur le serveur principal, dans Dynamic Media Classic.
* Étiquettes générées automatiquement par la visionneuse.

Les étiquettes basées sur des symboles sont définies à l’aide `MediaSet.LABEL_XX[_YY]` de SYMBOLs `MediaSet.LABEL_DELIM` comme décrit dans [Localisation des éléments](../../c-html5-s7-aem-asset-viewers/c-html5-20-ecatalog-viewer-about/c-html5-20-ecatalog-viewer-localization.md#concept-cbfc39344c494eb7b9f6a272cff0cc74) de l’interface utilisateur. Vous pouvez définir de telles étiquettes soit pour l’ensemble de la planche du catalogue électronique, auquel cas vous devez utiliser une syntaxe SYMBOL courte ( `MediaSet.LABEL_XX`). Vous pouvez également le spécifier pour chaque page individuellement en utilisant la syntaxe SYMBOL complète ( `MediaSet.LABEL_XX_YY`).

Lorsque vous définissez des étiquettes pour les deux pages de la planche du catalogue électronique, la visionneuse concatène ces étiquettes en une seule chaîne à l’aide `MediaSet.LABEL_DELIM` de SYMBOL. Les étiquettes basées sur des symboles ont priorité sur les étiquettes définies sur le serveur principal ou générées automatiquement par la visionneuse.

Les étiquettes définies dans Dynamic Media Classic sont stockées dans l’enregistrement UserData des images de page individuelles. Identique aux étiquettes à base de SYMBOLES. Autrement dit, si les deux pages de la planche du catalogue électronique ont des étiquettes définies, elles sont concaténées à l’aide de `MediaSet.LABEL_DELIM` SYMBOL en mode paysage. Dynamic Media étiquettes classiques ont priorité sur les étiquettes générées automatiquement, mais sont remplacées par des étiquettes basées sur des symboles.

Les étiquettes générées automatiquement sont des numéros séquentiels attribués à toutes les pages du catalogue électronique. Les étiquettes générées automatiquement sont ignorées pour la planche donnée si des étiquettes basées sur des symboles sont définies ou si des étiquettes classiques Dynamic Media sont définies.

Dans la table des matières, il est possible de désactiver l’affichage des étiquettes générées automatiquement à l’aide d’un `showdefault` paramètre.
