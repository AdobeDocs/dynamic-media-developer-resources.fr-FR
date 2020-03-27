---
description: 'null'
seo-description: 'null'
seo-title: Gestion des libellés de page
solution: Experience Manager
title: Gestion des libellés de page
topic: Dynamic media
uuid: ab3df37d-113b-4762-ba9c-b92ffc41f1a2
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# Gestion des libellés de page{#managing-page-labels}

L’interface utilisateur du lecteur de contenu affiche les libellés de page à deux endroits : mode miniatures et liste déroulante de la table des matières.

Trois types d’étiquettes peuvent être définis :

* Étiquettes définies par l’auteur à l’aide du mécanisme de  SYMBOL.
* Etiquettes définies par l’auteur sur le serveur principal, dans SPS.
* Etiquettes générées automatiquement par le lecteur de contenu.

Les libellés basés sur SYMBOL sont définis à l’aide `MediaSet.LABEL_XX[_YY]` et `MediaSet.LABEL_DELIM` des libellés SYMBOL, comme décrit dans le [des éléments](../../c-html5-s7-aem-asset-viewers/c-html5-20-ecatalog-viewer-about/c-html5-20-ecatalog-viewer-localization.md#concept-cbfc39344c494eb7b9f6a272cff0cc74)de l’interface utilisateur. Vous pouvez définir ces libellés soit pour l’ensemble de la planche ecatalog, auquel cas vous devez utiliser une syntaxe SYMBOLE courte ( `MediaSet.LABEL_XX`). Vous pouvez également le spécifier pour chaque page individuellement à l’aide de la syntaxe SYMBOL complète ( `MediaSet.LABEL_XX_YY`).

Lorsque vous définissez des libellés pour les deux pages dans la planche catalogue, le lecteur concatène ces libellés dans une chaîne à l’aide de `MediaSet.LABEL_DELIM` SYMBOL. Les libellés SYMBOL ont la priorité sur les libellés définis sur le serveur principal ou générés automatiquement par le lecteur.

Les étiquettes définies dans SPS sont stockées dans l’enregistrement UserData des images de page individuelles. Identique aux libellés SYMBOL. En d’autres termes, si les étiquettes des deux pages de la planche catalogue sont définies, elles sont concaténées à l’aide de `MediaSet.LABEL_DELIM` SYMBOL en mode paysage. Les libellés SPS ont la priorité sur les libellés générés automatiquement, mais ils sont remplacés par des libellés SYMBOL.

Les libellés générés automatiquement sont des numéros séquentiels attribués à toutes les pages de l’catalogue. Les libellés générés automatiquement sont ignorés pour la planche donnée si des libellés SYMBOL sont définis ou si des libellés SPS sont définis.

Dans la table des matières, il est possible de désactiver l’affichage des libellés générés automatiquement à l’aide d’un `showdefault` paramètre.
