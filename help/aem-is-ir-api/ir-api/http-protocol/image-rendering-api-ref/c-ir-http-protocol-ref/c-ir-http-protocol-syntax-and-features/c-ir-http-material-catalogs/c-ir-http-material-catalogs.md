---
title: Catalogues de matières
description: Les catalogues de matériaux offrent plusieurs fonctionnalités.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 502f80f5-fdd1-468b-89a9-64cc9128d655
TQID: 'https://experienceleague.adobe.com/0ALFMea9A1hJtuPr3vG0cd34S-cLfTUNUGpIXZBpZBY'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 4339f336345d7d7f3c05c7f5a18fbd28bcfd382b
workflow-type: tm+mt
source-wordcount: 298
ht-degree: 0%

---

# Catalogues de matières {#material-catalogs}

Les catalogues de matériaux offrent plusieurs fonctionnalités.

* Autoriser la définition persistante des matériaux, y compris toutes leurs propriétés.

  Les matériaux définis dans le catalogue de matériaux peuvent être référencés à l&#39;aide d&#39;un identifiant simple, plutôt que d&#39;un ensemble de propriétés de matériau.
* Fournissez des valeurs par défaut pour certains attributs de requête, tels que la qualité de JPEG ou une taille d’image de réponse par défaut.
* Gérez les vignettes, les profils ICC et les modèles de demande.

Même si aucun catalogue de matières spécifique n&#39;est défini, toutes les fonctions des catalogues de matières sont disponibles par le biais du catalogue par défaut ( [!DNL default.ini]).

Bien que les matériaux de rendu puissent être spécifiés explicitement dans les demandes à l&#39;aide d&#39;attributs de matériau, il est souvent préférable de masquer les détails des matériaux du site Web à l&#39;aide de catalogues de matériaux. Les commandes src= acceptent des références de catalogue au lieu de chemins d’accès explicites aux fichiers. Une entrée de catalogue se compose de ` [ *[!DNL catId]*/] *[!DNL itemId]*`, où ` *[!DNL catId]*` identifie un catalogue de matières et ` *[!DNL itemId]*` identifie un enregistrement dans le catalogue. Si ` *[!DNL catId]*` n’est pas spécifié, le catalogue de sessions est utilisé (voir ci-dessous).

Un enregistrement de catalogue est mis en correspondance avec succès si (a) ` *[!DNL catId]*` correspond à la valeur `attribute::RootId` d&#39;un catalogue de matières et (b) ` *[!DNL recId]*` correspond à la valeur catalog::Id dans le même catalogue. En cas de correspondance réussie, les attributs du matériau (y compris `src=`) sont définis sur les données de l&#39;enregistrement du catalogue. Si le MSS inclut des attributs supplémentaires pour ce matériau en plus de src=, ils remplacent les valeurs de l’enregistrement du catalogue.

Si ` *[!DNL recId]*` ne peut pas être associé à une entrée de catalogue, ` *[!DNL catId]*` est remplacé par `attribute::RootPath` du catalogue et le chemin d’accès qui en résulte est alors supposé être un simple chemin d’accès au fichier. D&#39;autres attributs par défaut (par exemple, `attribute::Resolution`) peuvent également être hérités du catalogue des matières.

Les vignettes et les profils ICC peuvent être répertoriés dans des catalogues de matériaux similaires aux matériaux eux-mêmes et dotés de propriétés données. En outre, la carte des vignettes fournit également le conteneur des modèles.

**Voir aussi**

Référence du catalogue de matériaux, [`src=`](../../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-src.md#reference-62c98abad22149d68d405ed6aaff8272), `attribute::RootId`, `attribute::RootPath`, `attribute::VignettePath`

