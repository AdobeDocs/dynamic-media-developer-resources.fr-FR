---
description: Obtient les ressources et le nombre de ressources associées à un  spécifique.
seo-description: Obtient les ressources et le nombre de ressources associées à un  spécifique.
seo-title: getAssetCount
solution: Experience Manager
title: getAssetCount
topic: Scene7 Image Production System API
uuid: 92103806-59da-444f-b69c-d045d0ebf42e
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# getAssetCount{#getassetcounts}

Obtient les ressources et le nombre de ressources associées à un  spécifique.

Le `countArray` renvoyé consiste en un tableau de `assetTypes` (type de données `xsd:string`), chacun avec son propre champ de décompte (type de données `xsd:int`), permettant la représentation de plusieurs types de ressource par élément du tableau.
Syntaxe

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

**Entrée (getAssetCountsParam)**

| Nom | Type | Obligatoire | Description |
|---|---|---|---|
| ` *`companyHandle`*` | `xsd:string` | Oui | Poignée vers le avec les ressources que vous souhaitez compter. |

**Output (getAssetCountsReturn)**

| Nom | Type | Obligatoire | Description |
|---|---|---|---|
| ` *`countArray`*` | `types:AssetCountArray` | Non | Tableau de types de ressource, chacun avec son propre champ de comptabilisation, permettant la représentation de plusieurs types de ressource par élément du tableau. |

## Exemples {#section-6052a503eb3843f6adb99e200fdba280}

Cet exemple de code utilise le nom d&#39; du comme champ dans le champ `getAssetCountsParam` envoyé au serveur de services Web IPS afin d&#39;obtenir le décompte des ressources.

**Request**

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

