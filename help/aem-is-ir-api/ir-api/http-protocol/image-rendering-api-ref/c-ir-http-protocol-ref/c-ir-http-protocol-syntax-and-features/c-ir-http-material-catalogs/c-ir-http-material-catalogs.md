---
description: Les catalogues de matériaux  le  plusieurs fonctionnalités.
seo-description: Les catalogues de matériaux  le  plusieurs fonctionnalités.
seo-title: Catalogues de matières *
solution: Experience Manager
title: Catalogues de matières *
topic: Scene7 Image Serving - Image Rendering API
uuid: 2a2f371e-0982-47c7-b3da-678a5ff6c7a7
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# Catalogues de matières *{#material-catalogs}

Les catalogues de matériaux  le  plusieurs fonctionnalités.

* Permettre une définition persistante des matériaux, y compris toutes les propriétés des matériaux.

   Les matériaux définis dans le catalogue de matériaux peuvent être référencés à l’aide d’un ID simple, plutôt que d’un ensemble de propriétés matérielles.
* Fournissez des valeurs par défaut pour certains attributs de requête, tels que la qualité JPEG ou une taille d’image de réponse par défaut.
* Gérez les vignettes, les  ICC et les modèles de demande.

Même si aucun catalogue de matières spécifique n&#39;est défini, toutes les caractéristiques des catalogues de matières sont disponibles via le catalogue par défaut ( [!DNL default.ini]).

Bien que les documents de rendu puissent être explicitement spécifiés dans les demandes utilisant des attributs matériels, il est souvent plus souhaitable de masquer les détails des matériaux du site Web en utilisant des catalogues matériels. les commandes src= acceptent les références de catalogue au lieu des chemins de fichier explicites. Une entrée de catalogue consiste en ` [ *[!DNL catId]*/] *[!DNL itemId]*`, où ` *[!DNL catId]*` identifie un catalogue de matières et ` *[!DNL itemId]*` identifie un enregistrement dans le catalogue. Si ` *[!DNL catId]*` n’est pas spécifié, le catalogue de sessions est utilisé (voir ci-dessous).

Un enregistrement de catalogue est mis en correspondance si a) ` *[!DNL catId]*` correspond à la `attribute::RootId` valeur d’un catalogue de matières et b) ` *[!DNL recId]*` correspond à la valeur catalog::Id dans le même catalogue. En cas de correspondance réussie, les attributs du matériau (y compris `src=`) sont définis sur les données de l’enregistrement de catalogue. Si le MSS inclut des attributs supplémentaires pour ce matériau en plus de src=, ils remplacent les valeurs de l’enregistrement de catalogue.

S’il ` *[!DNL recId]*` est impossible de faire correspondre une entrée de catalogue, ` *[!DNL catId]*` est remplacé par `attribute::RootPath` le chemin d’accès obtenu à partir du catalogue et est alors considéré comme un chemin d’accès de fichier simple. Autres attributs par défaut (ex. `attribute::Resolution`) peut également être hérité du catalogue de matériaux.

Les vignettes et les  ICC peuvent être regroupées dans des catalogues de matériaux similaires aux matériaux eux-mêmes, et des propriétés peuvent être attribuées. En outre, la carte de vignette fournit également le  des modèles.

**Voir aussi**

Référence du catalogue de matières, [`src=`](../../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-src.md#reference-62c98abad22149d68d405ed6aaff8272), `attribute::RootId`, `attribute::RootPath`, `attribute::VignettePath`
