---
description: Définit les valeurs des métadonnées d’une ressource. Fonctionne avec un tableau de mises à jour de métadonnées pour définir des valeurs dans un lot.
solution: Experience Manager
title: setAssetMetadata
feature: Dynamic Media Classic,SDK/API,Metadata,Asset Management
role: Developer,Admin
exl-id: 811e44e1-774a-49bd-a2bd-a7504e5f7f5f
TQID: 'https://experienceleague.adobe.com/b8E8BK8pyJQiYlR2yNMbYPWcLVNfmAvI5WaOBuaBz1E'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: c66ffd68-0f65-42bb-aa23-b4020f12e0bdid: ff6a42d2-313e-452e-93a6-792e4fad9ff8
topic_v2: id: a004cc84-67b9-4a33-a3a7-8ec7273ef4dc
source-git-commit: 6762cee83f1b7c970ed6353450c2ae6c602e7f3a
workflow-type: tm+mt
source-wordcount: 123
ht-degree: 8%

---

# setAssetMetadata{#setassetmetadata}

Définit les valeurs des métadonnées d’une ressource. Fonctionne avec un tableau de mises à jour de métadonnées pour définir des valeurs dans un lot.

Syntaxe

## Types d’utilisateurs autorisés {#section-9dcacb0c924044648f8324bfed183dca}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`
* `ImagePortalContrib`
* `ImagePortalContribUser`

>[!NOTE]
>
>L’utilisateur doit disposer d’un accès en lecture à la ressource.

## Paramètres {#section-bcdcff30905e444388811e897b2824bd}

**Input (setAssetMetadataParam)**

| Nom | Type | Obligatoire | Description |
|---|---|---|---|
| companyHandle | `xsd:string` | Oui | Identifiant de la société contenant la ressource à mettre à jour. |
| assetHandle | `xsd:string` | Oui | Poignée de la ressource. |
| updateArray | `types:MetadataUpdateArray` | Oui | Mises à jour dans un tableau de mise à jour des métadonnées. |

**Output (setAssetMetadataReturn)**

L’API IPS ne renvoie pas de réponse pour cette opération.

## Exemples {#section-1ab412e7ee1d4d6d8469b0b403598c42}

Cet exemple de code utilise un tableau de mises à jour des métadonnées pour définir les métadonnées de la ressource spécifiée.

**Requête**

```java
<ns1:setAssetMetadataParam xmlns:ns1="http://www.scene7.com/IpsApi/xsd">
   <ns1:companyHandle>47</ns1:companyHandle>
   <ns1:assetHandle>24265|1|17061</ns1:assetHandle>
   <ns1:updateArray>
      <ns1:items>
         <ns1:fieldHandle>47|ALL|Resolution</ns1:fieldHandle>
         <ns1:value>320</ns1:value>
      </ns1:items>
   </ns1:updateArray>
</ns1:setAssetMetadataParam>
```

**Réponse**

Aucune

