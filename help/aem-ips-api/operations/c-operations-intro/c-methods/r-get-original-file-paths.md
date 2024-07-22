---
description: Obtient les chemins d’accès aux fichiers d’origine des ressources d’une entreprise.
solution: Experience Manager
title: getOriginalFilePaths
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 81d06a8c-55c1-47d5-adc9-928ab30199c6
source-git-commit: 77c88d5fe20e048f6fad2bb23cb1abe090793acf
workflow-type: tm+mt
source-wordcount: '99'
ht-degree: 14%

---

# getOriginalFilePaths{#getoriginalfilepaths}

Obtient les chemins d’accès aux fichiers d’origine des ressources d’une entreprise.

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
| companyHandle | `xsd:string` | Oui | La poignée de la société. |
| assetHandleArray | `types:HandleArray` | Oui | Tableau de gestionnaires des ressources dont vous souhaitez obtenir le chemin d’accès au fichier d’origine. |

**Sortie (getOriginalFilePathsReturn)**

| Nom | Type | Obligatoire | Description |
|---|---|---|---|
| originalFileArray | `types:StringArray` | Oui | Tableau de chaînes représentant les chemins d’accès aux fichiers d’origine. |

## Exemples {#section-a966e783a2ba49f5b6b0f961329ab2f8}

Cet exemple de code renvoie les chemins d’accès aux fichiers des ressources spécifiées avec des gestionnaires de ressources uniques dans un tableau de gestion des ressources.

**Requête**

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
