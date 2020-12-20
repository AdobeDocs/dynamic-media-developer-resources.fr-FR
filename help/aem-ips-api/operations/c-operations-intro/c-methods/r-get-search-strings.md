---
description: Récupère les chaînes de recherche, les mots-clés et d’autres informations sur un fichier. La réponse contient des informations supplémentaires sur la ressource.
seo-description: Récupère les chaînes de recherche, les mots-clés et d’autres informations sur un fichier. La réponse contient des informations supplémentaires sur la ressource.
seo-title: getSearchStrings
solution: Experience Manager
title: getSearchStrings
topic: Scene7 Image Production System API
uuid: 9d588d6b-c79c-4531-a2e8-8467254a7985
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '115'
ht-degree: 14%

---


# getSearchStrings{#getsearchstrings}

Récupère les chaînes de recherche, les mots-clés et d’autres informations sur un fichier. La réponse contient des informations supplémentaires sur la ressource.

Syntaxe

## Types d’utilisateur autorisés {#section-b09c817a59f949a28e1c029e431f5698}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `TrialSiteAdmin`
* `ImagePortalAdmin`

## Paramètres {#section-c1efda4bb15349a68b276bafee8c18fd}

**Entrée (getSearchStringsParam)**

| Nom | Type | Obligatoire | Description |
|---|---|---|---|
| ` *`companyHandle`*` | `xsd:string` | Oui | Pose la société. |
| ` *`assetHandle`*` | `xsd:string` | Oui | Traitez le fichier. |

**Output (getSearchStringsReturn)**

| Nom | Type | Obligatoire | Description |
|---|---|---|---|
| ` *`searchStringArray`*` | `types:SearchStrings` | Oui | Tableau de chaînes de recherche de ressources. |

## Exemples {#section-e1f73bff6e4440c489d59cb9aa5384d8}

Cet exemple de code renvoie des chaînes de recherche spécifiques à un fichier. La réponse renvoie un tableau vide.

**Request**

```java
<getSearchStringsParam xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
   <companyHandle>47</ns1:companyHandle>
   <assetHandle>a|717|1|530</assetHandle>
</getSearchStringsParam>
```

**Réponse**

Aucune
