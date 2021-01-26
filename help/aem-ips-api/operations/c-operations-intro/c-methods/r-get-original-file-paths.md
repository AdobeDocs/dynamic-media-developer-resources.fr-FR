---
description: Récupère les chemins d’accès aux fichiers d’origine d’une société.
seo-description: Récupère les chemins d’accès aux fichiers d’origine d’une société.
seo-title: getOriginalFilePaths
solution: Experience Manager
title: getOriginalFilePaths
topic: Dynamic Media Image Production System API
uuid: c4acf288-1a57-4295-806b-348f15a089cc
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '109'
ht-degree: 14%

---


# getOriginalFilePaths{#getoriginalfilepaths}

Récupère les chemins d’accès aux fichiers d’origine d’une société.

Syntaxe

## Types d’utilisateur autorisés {#section-da8d8561e9174e938f3595a5d6e50089}

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
| `*`companyHandle`*` | `xsd:string` | Oui | La poignée de la société. |
| `*`assetHandleArray`*` | `types:HandleArray` | Oui | Tableau de poignées pour les fichiers dont vous souhaitez obtenir le chemin d’accès au fichier d’origine. |

**Output (getOriginalFilePathsReturn)**

| Nom | Type | Obligatoire | Description |
|---|---|---|---|
| `*`originalFileArray`*` | `types:StringArray` | Oui | Tableau de chaînes représentant les chemins d’accès aux fichiers d’origine. |

## Exemples {#section-a966e783a2ba49f5b6b0f961329ab2f8}

Cet exemple de code renvoie les chemins d&#39;accès aux fichiers des ressources spécifiées avec des gestionnaires de ressources uniques dans un tableau de descripteurs de ressources.

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

