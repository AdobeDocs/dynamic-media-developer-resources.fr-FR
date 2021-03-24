---
description: Récupère les chemins d’accès aux fichiers d’origine d’une société.
solution: Experience Manager
title: getOriginalFilePaths
feature: Dynamic Media Classic, SDK/API
role: Développeur, Administrateur
translation-type: tm+mt
source-git-commit: 052bfcbcf1bd4ccf60afa7e3325bf58dd07cba85
workflow-type: tm+mt
source-wordcount: '106'
ht-degree: 15%

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

