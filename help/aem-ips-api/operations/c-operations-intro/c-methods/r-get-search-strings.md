---
description: Récupère les chaînes de recherche, les mots-clés et d’autres informations sur une ressource. La réponse contient des informations supplémentaires sur la ressource.
solution: Experience Manager
title: getSearchStrings
feature: Dynamic Media Classic, SDK/API
role: Developer,Admin
exl-id: e94215b8-1121-4be6-a8a9-e9444c57495d
source-git-commit: fcda99340a18d5037157723bb3bdca5fa9df3277
workflow-type: tm+mt
source-wordcount: '100'
ht-degree: 17%

---

# getSearchStrings{#getsearchstrings}

Récupère les chaînes de recherche, les mots-clés et d’autres informations sur une ressource. La réponse contient des informations supplémentaires sur la ressource.

Syntaxe

## Types d’utilisateurs autorisés {#section-b09c817a59f949a28e1c029e431f5698}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `TrialSiteAdmin`
* `ImagePortalAdmin`

## Paramètres {#section-c1efda4bb15349a68b276bafee8c18fd}

**Entrée (getSearchStringsParam)**

| Nom | Type | Obligatoire | Description |
|---|---|---|---|
| `*`companyHandle`*` | `xsd:string` | Oui | Gérer la société. |
| `*`assetHandle`*` | `xsd:string` | Oui | Gérer la ressource. |

**Sortie (getSearchStringsReturn)**

| Nom | Type | Obligatoire | Description |
|---|---|---|---|
| `*`searchStringArray`*` | `types:SearchStrings` | Oui | Tableau de chaînes de recherche de ressources. |

## Exemples {#section-e1f73bff6e4440c489d59cb9aa5384d8}

Cet exemple de code renvoie des chaînes de recherche spécifiques à une ressource. La réponse renvoie un tableau vide.

**Request**

```java
<getSearchStringsParam xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
   <companyHandle>47</ns1:companyHandle>
   <assetHandle>a|717|1|530</assetHandle>
</getSearchStringsParam>
```

**Réponse**

Aucune
