---
description: Les catalogues de matériaux offre plusieurs fonctionnalités.
solution: Experience Manager
title: Catalogues de matières *
feature: Dynamic Media Classic, SDK/API
role: Développeur, Professionnel
translation-type: tm+mt
source-git-commit: d0bc88f55f857762b3bab4c76d1e3f3dd2733d60
workflow-type: tm+mt
source-wordcount: '305'
ht-degree: 0%

---


# Catalogues de matières *{#material-catalogs}

Les catalogues de matériaux offre plusieurs fonctionnalités.

* Permettre une définition permanente des matériaux, y compris toutes les propriétés des matériaux.

   Les matériaux définis dans le catalogue de matériaux peuvent être référencés à l’aide d’un ID simple, plutôt que d’un ensemble de propriétés matérielles.
* Fournissez des valeurs par défaut pour certains attributs de requête, tels que la qualité JPEG ou une taille d’image de réponse par défaut.
* Gérez les vignettes, les profils ICC et les modèles de demande.

Même si aucun catalogue de matières spécifique n&#39;est défini, toutes les caractéristiques des catalogues de matières sont disponibles par le biais du catalogue par défaut ( [!DNL default.ini]).

Bien que les documents de rendu puissent être explicitement spécifiés dans les demandes utilisant des attributs matériels, il est souvent plus souhaitable de masquer les détails des documents du site Web en utilisant des catalogues matériels. les commandes src= acceptent les références de catalogue plutôt que les chemins d’accès explicites aux fichiers. Une entrée de catalogue se compose de ` [ *[!DNL catId]*/] *[!DNL itemId]*`, où ` *[!DNL catId]*` identifie un catalogue de matières et ` *[!DNL itemId]*` identifie un enregistrement dans le catalogue. Si ` *[!DNL catId]*` n&#39;est pas spécifié, le catalogue de sessions est utilisé (voir ci-dessous).

Un enregistrement de catalogue est mis en correspondance si a) ` *[!DNL catId]*` correspond à la valeur `attribute::RootId` d&#39;un catalogue de matières et b) ` *[!DNL recId]*` correspond à la valeur catalog::Id dans le même catalogue. En cas de correspondance réussie, les attributs du matériau (y compris `src=`) sont définis sur les données de l&#39;enregistrement catalogue. Si le MSS inclut des attributs supplémentaires pour ce matériel en plus de src=, ils remplacent les valeurs de l’enregistrement catalogue.

Si ` *[!DNL recId]*` ne peut pas être associé à une entrée de catalogue, ` *[!DNL catId]*` est remplacé par `attribute::RootPath` du catalogue et le chemin d&#39;accès qui en résulte est alors supposé être un chemin d&#39;accès de fichier simple. Autres attributs par défaut (ex. `attribute::Resolution`) peut également être hérité du catalogue de matières.

Les vignettes et les profils ICC peuvent être répertoriés dans des catalogues de matériaux similaires aux matériaux eux-mêmes, et des propriétés peuvent être attribuées. En outre, la carte des vignettes fournit également le conteneur des modèles.

**Voir aussi**

Référence du catalogue de matières, [ `src=`](../../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-src.md#reference-62c98abad22149d68d405ed6aaff8272), `attribute::RootId`, `attribute::RootPath`, `attribute::VignettePath`
