---
description: Obtient les ressources et le nombre de ressources associées à une société spécifique.
solution: Experience Manager
title: getAssetCounts
feature: Dynamic Media Classic,SDK/API,Asset Management
role: Developer,Admin
exl-id: 21cb8023-d6fe-416a-b16f-636df8a37958
TQID: 'https://experienceleague.adobe.com/gvFs-dqQ8oR38MTKrEYaap31BH-MtSaRtGtJd5FO-MY'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
topic_v2:
  - id: bce87dde-a4ab-44c9-8a18-ad66e4ddb377
source-git-commit: ba0745708154402d9b6c7ebf0554deb366dde11b
workflow-type: tm+mt
source-wordcount: 141
ht-degree: 9%

---

# getAssetCounts{#getassetcounts}

Obtient les ressources et le nombre de ressources associées à une société spécifique.

Le `countArray` renvoyé se compose d’un tableau de `assetTypes` (type de données `xsd:string`), chacun ayant son propre champ de comptage (type de données `xsd:int`), ce qui permet la représentation de plusieurs types de ressources par élément du tableau.Syntaxe

## Types d’utilisateurs autorisés {#section-6234754722184e828352f10eb18fbce9}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `TrialSiteAdmin`
* `TrialSiteUser`
* `ImagePortalAdmin`
* `ImagePortalUser`
* `ImagePortalContrib`
* `ImagePortalContribUser`

## Paramètres {#section-2a9581315eca427d8a3d26cc3fca7b1f}

**Input (getAssetCountsParam)**

| Nom | Type | Obligatoire | Description |
|---|---|---|---|
| companyHandle | `xsd:string` | Oui | Identifiant de la société dont vous souhaitez comptabiliser les ressources. |

**Output (getAssetCountsReturn)**

| Nom | Type | Obligatoire | Description |
|---|---|---|---|
| countArray | `types:AssetCountArray` | Non | Tableau de types de ressources, chacun ayant son propre champ de comptage, ce qui permet la représentation de plusieurs types de ressources par élément du tableau. |

## Exemples {#section-6052a503eb3843f6adb99e200fdba280}

Cet exemple de code utilise le handle de l’entreprise comme champ dans le `getAssetCountsParam` envoyé au serveur de services Web IPS afin d’obtenir le nombre de ressources.

**Requête**

```java
<getAssetCountsParam xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
   <companyHandle>c|6</companyHandle>
</getAssetCountsParam>
```

**Réponse**

```java
<getAssetCountsReturn xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
   <countArray>
      <items>
         <assetType>Image</assetType>
         <count>44</count>
      </items>
      <items>
         <assetType>Flash</assetType>
         <count>3</count>
      </items>
   </countArray>
</getAssetCountsReturn>
```

