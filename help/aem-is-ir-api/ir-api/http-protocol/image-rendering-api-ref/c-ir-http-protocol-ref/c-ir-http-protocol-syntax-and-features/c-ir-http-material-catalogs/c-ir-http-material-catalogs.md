---
title: Catalogues de matériaux
description: Les catalogues de matériaux offrent plusieurs fonctionnalités.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 502f80f5-fdd1-468b-89a9-64cc9128d655
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '298'
ht-degree: 0%

---

# Catalogues de matériaux {#material-catalogs}

Les catalogues de matériaux offrent plusieurs fonctionnalités.

* Permet une définition persistante des matériaux, y compris de toutes les propriétés des matériaux.

  Les matériaux définis dans le catalogue de matériaux peuvent être référencés à l’aide d’un ID simple, plutôt que d’un ensemble de propriétés de matériau.
* Fournissez des valeurs par défaut pour certains attributs de requête, tels que la qualité JPEG ou une taille d’image de réponse par défaut.
* Gérez les vignettes, les profils ICC et les modèles de demande.

Même si aucun catalogue de matériaux spécifique n’est défini, toutes les fonctionnalités des catalogues de matériaux sont disponibles via le catalogue par défaut ( [!DNL default.ini]).

Bien que les matériaux de rendu puissent être spécifiés explicitement dans les demandes utilisant des attributs matériels, il est souvent plus souhaitable de masquer les détails des matériaux du site Web à l’aide de catalogues de matériaux. Les commandes src= acceptent les références au catalogue au lieu des chemins explicites aux fichiers. Une entrée de catalogue se compose de ` [ *[!DNL catId]*/] *[!DNL itemId]*`, où ` *[!DNL catId]*` identifie un catalogue de matériaux et ` *[!DNL itemId]*` identifie un enregistrement dans le catalogue. Si ` *[!DNL catId]*` cette option n’est pas spécifiée, le catalogue des sessions est utilisé (voir ci-dessous).

Un enregistrement de catalogue est mis en correspondance avec succès si (a) ` *[!DNL catId]*` correspond à la `attribute::RootId` valeur d’un catalogue de matériaux et (b) ` *[!DNL recId]*` correspond à la valeur catalog ::Id dans le même catalogue. En cas de correspondance réussie, les attributs de l’article (y compris `src=`) sont définis sur les données de la notice de catalogue. Si le MSS inclut des attributs supplémentaires pour ce matériau en plus de src=, ils remplacent les valeurs de la notice du catalogue.

S’il ` *[!DNL recId]*` ne peut pas correspondre à une entrée de catalogue, est ` *[!DNL catId]*` remplacé par `attribute::RootPath` à partir du catalogue et le chemin résultant est alors supposé être un chemin de fichier simple. D’autres attributs par défaut (par exemple, `attribute::Resolution`) peuvent également être hérités du catalogue de matériaux.

Les vignettes et les profils ICC peuvent être détaillés dans des catalogues de matériaux similaires aux matériaux eux-mêmes, et des propriétés données. En outre, la carte de vignette fournit également le conteneur pour les modèles.

**Voir aussi**

Référence du catalogue de matériaux, [`src=`](../../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-src.md#reference-62c98abad22149d68d405ed6aaff8272), , `attribute::RootId`, `attribute::RootPath``attribute::VignettePath`
