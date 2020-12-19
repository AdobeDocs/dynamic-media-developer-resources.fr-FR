---
description: 'null'
seo-description: 'null'
seo-title: Gestion des étiquettes de page
solution: Experience Manager
title: Gestion des étiquettes de page
topic: Dynamic media
uuid: ab3df37d-113b-4762-ba9c-b92ffc41f1a2
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '257'
ht-degree: 0%

---


# Gestion des étiquettes de page{#managing-page-labels}

Deux emplacements de l’interface utilisateur du lecteur de contenu affichent les étiquettes de page : mode miniatures et liste déroulante de la table des matières.

Trois types d’étiquettes peuvent être définis :

* Étiquettes définies par l&#39;auteur à l&#39;aide du mécanisme de localisation SYMBOL.
* Libellés définis par l’auteur sur le serveur principal, dans SPS.
* Étiquettes générées automatiquement par le lecteur de contenu.

Les libellés SYMBOL sont définis à l&#39;aide de `MediaSet.LABEL_XX[_YY]` et `MediaSet.LABEL_DELIM` SYMBOL, comme décrit dans [Localisation des éléments de l&#39;interface utilisateur](../../c-html5-s7-aem-asset-viewers/c-html5-20-ecatalog-viewer-about/c-html5-20-ecatalog-viewer-localization.md#concept-cbfc39344c494eb7b9f6a272cff0cc74). Vous pouvez définir de tels libellés soit pour l&#39;ensemble de la planche du catalogue électronique, auquel cas vous devez utiliser une syntaxe SYMBOL courte ( `MediaSet.LABEL_XX`). Ou, spécifiez-le pour chaque page individuellement en utilisant la syntaxe SYMBOL complète ( `MediaSet.LABEL_XX_YY`).

Lorsque vous définissez des libellés pour les deux pages dans la planche de catalogue électronique, le lecteur de contenu concatène ces libellés en une seule chaîne à l’aide de `MediaSet.LABEL_DELIM` SYMBOL. Les libellés basés sur SYMBOL ont la priorité sur les libellés définis sur le serveur principal ou générés automatiquement par le lecteur.

Les étiquettes définies dans SPS sont stockées dans l’enregistrement UserData des images de page individuelles. Identique aux étiquettes SYMBOL. En d’autres termes, si les étiquettes des deux pages de la planche catalogue électronique sont définies, elles sont concaténées à l’aide de `MediaSet.LABEL_DELIM` SYMBOL en mode paysage. Les libellés SPS ont la priorité sur les libellés générés automatiquement, mais sont remplacés par des libellés SYMBOL.

Les étiquettes générées automatiquement sont des numéros séquentiels attribués à toutes les pages du catalogue électronique. Les libellés générés automatiquement sont ignorés pour la planche donnée si des libellés basés sur SYMBOL sont définis ou si des libellés SPS sont définis.

Dans la table des matières, il est possible de désactiver l&#39;affichage des étiquettes générées automatiquement à l&#39;aide du paramètre `showdefault`.
