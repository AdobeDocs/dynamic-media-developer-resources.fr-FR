---
description: Obtient les actifs et le nombre de ressources associées à une société spécifique.
seo-description: Obtient les actifs et le nombre de ressources associées à une société spécifique.
seo-title: getAssetCounts
solution: Experience Manager
title: getAssetCounts
topic: Dynamic Media Image Production System API
uuid: 92103806-59da-444f-b69c-d045d0ebf42e
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '155'
ht-degree: 9%

---


# getAssetCounts{#getassetcounts}

Obtient les actifs et le nombre de ressources associées à une société spécifique.

Le `countArray` renvoyé est constitué d&#39;un tableau de `assetTypes` (type de données `xsd:string`), chacun avec son propre champ de comptabilisation (type de données `xsd:int`), ce qui permet de représenter plusieurs types de ressource par élément du tableau.
Syntaxe

## Types d’utilisateur autorisés {#section-6234754722184e828352f10eb18fbce9}

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
| `*`companyHandle`*` | `xsd:string` | Oui | Poignée de la société contenant les ressources que vous souhaitez comptabiliser. |

**Sortie (getAssetCountsReturn)**

| Nom | Type | Obligatoire | Description |
|---|---|---|---|
| `*`countArray`*` | `types:AssetCountArray` | Non | Tableau de types de ressource, chacun avec son propre champ de comptabilisation, permettant la représentation de plusieurs types de ressource par élément du tableau. |

## Exemples {#section-6052a503eb3843f6adb99e200fdba280}

Cet exemple de code utilise le nom d&#39;utilisateur de la société comme champ dans le `getAssetCountsParam` envoyé au serveur de services Web IPS afin d&#39;obtenir le nombre de ressources.

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

