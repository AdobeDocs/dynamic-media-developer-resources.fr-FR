---
description: Recherche les conflits d’ID IPS en comparant les noms de ressources à tous les noms de l’espace de noms du catalogue Service d’images/Rendu d’images d’une entreprise.
solution: Experience Manager
title: checkAssetNames
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 0756c4fc-64ec-4022-a6aa-fcf1542b41b0
source-git-commit: 77c88d5fe20e048f6fad2bb23cb1abe090793acf
workflow-type: tm+mt
source-wordcount: '116'
ht-degree: 11%

---

# checkAssetNames{#checkassetnames}

Recherche les conflits d’ID IPS en comparant les noms de ressources à tous les noms de l’espace de noms du catalogue Service d’images/Rendu d’images d’une entreprise.

Syntaxe

## Types d’utilisateurs autorisés {#section-8efcbb3f555f417a870219e4714374db}

* `IpsUser`
* `IpsAdmin`
* `ImagePortalAdmin`
* `ImagePortalContrib`
* `ImagePortalContribUser`
* `ImagePortalUser`
* `TrialSiteAdmin`
* `TrialSiteUser`

## Paramètres {#section-9c75b00f2072453abea0bdefc6ad7c99}

**Input (checkAssetNamesParam)**

| Nom | Type | Obligatoire | Description |
|---|---|---|---|
| companyHandle | `xsd:string` | Non | Identifiant de la société qui contient l’utilisateur. |
| assetNamesArray | `types:StringArray` | Oui | Tableau de noms de ressources à vérifier. |

**Output (checkAssetNamesReturn)**

| Nom | Type | Obligatoire | Description |
|---|---|---|---|
| inUseNameArray | `types:StringArray` | Oui | Tableau de noms de ressources utilisés. |

## Exemples {#section-bc5d120d74614a63a425ca3acc337219}

Cet exemple de code demande les noms de ressources utilisés pour une société spécifiée. La réponse renvoie un tableau des noms de ressources en cours d’utilisation.

**Requête**

```java
<checkAssetNamesParam xmlns="http://www.scene7.com/IpsApi/xsd/2008-09-10">
   <companyHandle>c|1</companyHandle>
   <assetNameArray>
      <items>ABC123</items>
      <items>DEF456</items>
   </assetNameArray>
</checkAssetNamesParam>
```

**Réponse**

```java
<checkAssetNamesReturn xmlns="http://www.scene7.com/IpsApi/xsd/2008-09-10">
   <inUseNameArray>
      <items>DEF456</items>
   </inUseNameArray>
</checkAssetNamesReturn>
```
