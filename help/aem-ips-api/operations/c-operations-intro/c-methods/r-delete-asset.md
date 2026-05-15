---
description: Supprime une ressource.
solution: Experience Manager
title: deleteAsset
feature: Dynamic Media Classic,SDK/API,Asset Management
role: Developer,Admin
exl-id: dacea36e-3d40-4aaf-94fd-f0709830caf9
TQID: 'https://experienceleague.adobe.com/aZnVNkDpTGXy7OrqVts-KHyOB-gdsA8XYlICQ-JC6aM'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 92
ht-degree: 10%

---

# deleteAsset{#deleteasset}

Supprime une ressource.

Syntaxe

## Types d’utilisateurs autorisés {#section-e913be43b684491daf02bc73211e4290}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`
* `ImagePortalContrib`
* `ImagePortalContribUser`

>[!NOTE]
>
>L’utilisateur doit disposer d’un accès en lecture et en suppression à la ressource.

## Paramètres {#section-0eed164e278b456fbdfb7a50727a0416}

**Input (deleteAssetParam)**

| Nom | Type | Obligatoire | Description |
|---|---|---|---|
| companyHandle | `xsd:string` | Oui | Identifiant de la société à laquelle appartient le dossier. |
| assetHandle | `xsd:string` | Oui | Descripteur de la ressource à supprimer. |

**Output (deleteAssetParam)**

L’API IPS ne renvoie pas de réponse pour cette opération.

## Exemples {#section-d5657289f5234bb0a613dcf691507958}

Cet exemple de code supprime n’importe quel type de ressource d’une société spécifique. Elle nécessite un handle de ressource, que vous devez obtenir à partir d’une autre opération.

**Requête**

```java
<ns1:deleteAssetParam xmlns:ns1="http://www.scene7.com/IpsApi/xsd">
   <ns1:companyHandle>47</ns1:companyHandle>
   <ns1:assetHandle>24265|1|17061</ns1:assetHandle>
</ns1:deleteAssetParam>
```

**Réponse**

Aucune
