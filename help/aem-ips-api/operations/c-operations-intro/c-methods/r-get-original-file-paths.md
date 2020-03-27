---
description: Obtient les chemins d’accès aux fichiers d’origine des ressources d’un .
seo-description: Obtient les chemins d’accès aux fichiers d’origine des ressources d’un .
seo-title: getOriginalFilePaths
solution: Experience Manager
title: getOriginalFilePaths
topic: Scene7 Image Production System API
uuid: c4acf288-1a57-4295-806b-348f15a089cc
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# getOriginalFilePaths{#getoriginalfilepaths}

Obtient les chemins d’accès aux fichiers d’origine des ressources d’un .

Syntaxe

## Types d’utilisateurs autorisés {#section-da8d8561e9174e938f3595a5d6e50089}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `TrialSiteAdmin`
* `TrialSiteUser`
* `ImagePortalContrib`
* `ImagePortalContribUser`

>[!NOTE]
>
>Nécessite un accès en lecture à la ressource.

## Paramètres {#section-a6b394daba6e49a8882cf3051035d9d1}

**Entrée (getOriginalFilePathsParam)**

| Nom | Type | Obligatoire | Description |
|---|---|---|---|
| ` *`companyHandle`*` | `xsd:string` | Oui | La poignée du. |
| ` *`assetHandleArray`*` | `types:HandleArray` | Oui | Tableau de poignées vers les fichiers dont vous souhaitez obtenir le chemin d’accès au fichier d’origine. |

**Output (getOriginalFilePathsReturn)**

| Nom | Type | Obligatoire | Description |
|---|---|---|---|
| ` *`originalFileArray`*` | `types:StringArray` | Oui | Tableau de chaînes représentant les chemins d’accès aux fichiers d’origine. |

## Exemples {#section-a966e783a2ba49f5b6b0f961329ab2f8}

Cet exemple de code renvoie les chemins d’accès aux fichiers des ressources spécifiées avec des poignées de ressources uniques dans un tableau de descripteurs de ressources.

**Request**

```java
<ns1:getOriginalFilePathsParam xmlns:ns1="http://www.scene7.com/IpsApi/xsd">
   <ns1:companyHandle>47</ns1:companyHandle>
   <ns1:assetHandleArray>
      <ns1:items>24265|1|17061</ns1:items>
      <ns1:items>24267|1|17063</ns1:items>
   </ns1:assetHandleArray>
</ns1:getOriginalFilePathsParam>
```

**Réponse**

```java
<getOriginalFilePathsReturn xmlns="http://www.scene7.com/IpsApi/xsd">
   <originalFileArray>
      <items>MyCompany/Autumn Leaves.jpg</items>
      <items>MyCompany/Desert Landscape.jpg</items>
   </originalFileArray>
</getOriginalFilePathsReturn>
```

