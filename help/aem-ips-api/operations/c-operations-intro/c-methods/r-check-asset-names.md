---
description: Recherche les conflits d’ID IPS en comparant les noms de fichier à tous les noms d’un espace de nommage de catalogue de diffusion d’images/rendu d’images de société.
solution: Experience Manager
title: checkAssetNames
feature: Dynamic Media Classic,SDK/API
role: Developer,Administrator
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '123'
ht-degree: 12%

---


# checkAssetNames{#checkassetnames}

Recherche les conflits d’ID IPS en comparant les noms de fichier à tous les noms d’un espace de nommage de catalogue de diffusion d’images/rendu d’images de société.

Syntaxe

## Types d’utilisateur autorisés {#section-8efcbb3f555f417a870219e4714374db}

* `IpsUser`
* `IpsAdmin`
* `ImagePortalAdmin`
* `ImagePortalContrib`
* `ImagePortalContribUser`
* `ImagePortalUser`
* `TrialSiteAdmin`
* `TrialSiteUser`

## Paramètres {#section-9c75b00f2072453abea0bdefc6ad7c99}

**Entrée (checkAssetNamesParam)**

| Nom | Type | Obligatoire | Description |
|---|---|---|---|
| `*`companyHandle`*` | `xsd:string` | Non | Identifiant de la société contenant l’utilisateur. |
| `*`assetNamesArray`*` | `types:StringArray` | Oui | Tableau de noms de fichier à vérifier. |

**Output (checkAssetNamesReturn)**

| Nom | Type | Obligatoire | Description |
|---|---|---|---|
| `*`inUseNameArray`*` | `types:StringArray` | Oui | Tableau de noms de fichier en cours d’utilisation. |

## Exemples {#section-bc5d120d74614a63a425ca3acc337219}

Cet exemple de code demande les noms de fichier utilisés pour une société spécifiée. La réponse renvoie un tableau de noms de fichier en cours d’utilisation.

**Request**

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

