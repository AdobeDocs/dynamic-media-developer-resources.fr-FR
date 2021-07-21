---
description: Obtient les ressources et le nombre de ressources associées à une société spécifique.
solution: Experience Manager
title: getAssetCounts
feature: Dynamic Media Classic,SDK/API,Gestion des ressources
role: Developer,Admin
exl-id: 21cb8023-d6fe-416a-b16f-636df8a37958
source-git-commit: fcda99340a18d5037157723bb3bdca5fa9df3277
workflow-type: tm+mt
source-wordcount: '148'
ht-degree: 10%

---

# getAssetCounts{#getassetcounts}

Obtient les ressources et le nombre de ressources associées à une société spécifique.

`countArray` renvoyé est constitué d’un tableau de `assetTypes` (type de données `xsd:string`), chacun ayant son propre champ de comptage (type de données `xsd:int`), permettant de représenter plusieurs types de ressources par élément du tableau.
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
| `*`companyHandle`*` | `xsd:string` | Oui | Gestion de l’entreprise avec les ressources que vous souhaitez compter. |

**Sortie (getAssetCountsReturn)**

| Nom | Type | Obligatoire | Description |
|---|---|---|---|
| `*`countArray`*` | `types:AssetCountArray` | Non | Tableau de types de ressources, chacun avec son propre champ de comptage, permettant de représenter plusieurs types de ressources par élément du tableau. |

## Exemples {#section-6052a503eb3843f6adb99e200fdba280}

Cet exemple de code utilise le nom d’utilisateur de la société comme champ dans la balise `getAssetCountsParam` envoyée au serveur des services Web IPS afin d’obtenir le nombre de ressources.

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
