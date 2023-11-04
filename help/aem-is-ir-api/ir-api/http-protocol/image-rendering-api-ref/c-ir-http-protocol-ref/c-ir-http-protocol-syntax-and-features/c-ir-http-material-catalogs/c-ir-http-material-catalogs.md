---
title: Catalogues de matières
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

# Catalogues de matières {#material-catalogs}

Les catalogues de matériaux offrent plusieurs fonctionnalités.

* Permettre la définition persistante de matériaux, y compris toutes les propriétés matérielles.

  Les matériaux définis dans le catalogue de matériaux peuvent être référencés à l’aide d’un simple ID, plutôt que d’un ensemble de propriétés matérielles.
* Indiquez les valeurs par défaut de certains attributs de requête, tels que la qualité du JPEG ou une taille d’image de réponse par défaut.
* Gestion des vignettes, des profils ICC et des modèles de requête.

Même si aucun catalogue de matières spécifique n’est défini, toutes les caractéristiques des catalogues de matériaux sont disponibles par le biais du catalogue par défaut ( [!DNL default.ini]).

Bien que les matériaux de rendu puissent être spécifiés explicitement dans les demandes utilisant des attributs matériels, il est souvent plus souhaitable de masquer les détails des matériaux du site web à l’aide de catalogues matériels. Les commandes src= acceptent les références de catalogue au lieu des chemins d’accès explicites au fichier. Une entrée de catalogue se compose de ` [ *[!DNL catId]*/] *[!DNL itemId]*`, où ` *[!DNL catId]*` identifie un catalogue de matières et ` *[!DNL itemId]*` identifie un enregistrement dans le catalogue. If ` *[!DNL catId]*` n’est pas spécifié, le catalogue de sessions est utilisé (voir ci-dessous).

Une correspondance est établie avec un enregistrement de catalogue si (a) ` *[!DNL catId]*` correspond à la variable `attribute::RootId` valeur d’un catalogue de matières et (b) ` *[!DNL recId]*` correspond à la valeur catalog::Id dans le même catalogue. En cas de correspondance réussie, les attributs du matériau (y compris `src=`) sont définis sur les données de l’enregistrement de catalogue. Si le MSS inclut des attributs supplémentaires pour ce matériel en plus de src=, ils remplacent les valeurs de l’enregistrement de catalogue.

If ` *[!DNL recId]*` ne peut pas être associé à une entrée de catalogue, puis ` *[!DNL catId]*` est remplacé par `attribute::RootPath` du catalogue et du chemin d’accès qui en résulte sont alors supposés être un chemin d’accès de fichier simple. Autres attributs par défaut (par exemple, `attribute::Resolution`) peut également être hérité du catalogue de matières.

Les vignettes et les profils ICC peuvent être répertoriés dans des catalogues de matériaux similaires aux matériaux eux-mêmes et donnés des propriétés. En outre, la carte de vignette fournit également le conteneur pour les modèles.

**Voir aussi**

Référence du catalogue de matières, [`src=`](../../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-src.md#reference-62c98abad22149d68d405ed6aaff8272), `attribute::RootId`, `attribute::RootPath`, `attribute::VignettePath`
