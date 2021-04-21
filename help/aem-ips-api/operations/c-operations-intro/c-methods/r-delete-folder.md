---
description: Supprime un dossier.
solution: Experience Manager
title: deleteFolder
feature: Dynamic Media Classic,SDK/API
role: Developer,Administrator
translation-type: tm+mt
source-git-commit: 052bfcbcf1bd4ccf60afa7e3325bf58dd07cba85
workflow-type: tm+mt
source-wordcount: '103'
ht-degree: 10%

---


# deleteFolder{#deletefolder}

Supprime un dossier.

Syntaxe

## Types d’utilisateur autorisés {#section-1c15a74c41194744a81f5ca86fe26585}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`
* `ImagePortalContrib`
* `ImagePortalContribUser`

>[!NOTE]
>
>L’utilisateur doit avoir accès en lecture et en suppression au dossier et à tous ses enfants.

## Paramètres {#section-a793c98a481a4f26ab50bc69b16b57e7}

**Entrée (deleteFolderParam)**

| Nom | Type | Obligatoire | Description |
|---|---|---|---|
| `*`companyHandle`*` | `xsd:string` | Oui | Identifiant de la société à laquelle appartient le dossier. |
| `*`folderHandle`*` | `xsd:string` | Oui | Identifiant du dossier à supprimer. |

**Output (deleteFolderParam)**

L&#39;API IPS ne renvoie pas de réponse pour cette opération.

## Exemples {#section-9d4617b322e8442d80e59be0f8714841}

Cet exemple de code supprime un dossier de la racine de la société. Il nécessite un nom d&#39;utilisateur de dossier que vous devez obtenir d&#39;une autre opération.

**Request**

```java
<ns1:deleteFolderParam xmlns:ns1="http://www.scene7.com/IpsApi/xsd">
   <ns1:companyHandle>47</ns1:companyHandle>
   <ns1:folderHandle>MyCompany/SpinSets/</ns1:folderHandle>
</ns1:deleteFolderParam>
```

Aucune
