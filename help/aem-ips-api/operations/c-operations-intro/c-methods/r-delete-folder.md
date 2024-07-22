---
description: Supprime un dossier.
solution: Experience Manager
title: deleteFolder
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: c042b87b-3f60-4608-8ed5-0fc031a66c03
source-git-commit: 77c88d5fe20e048f6fad2bb23cb1abe090793acf
workflow-type: tm+mt
source-wordcount: '96'
ht-degree: 10%

---

# deleteFolder{#deletefolder}

Supprime un dossier.

Syntaxe

## Types d’utilisateurs autorisés {#section-1c15a74c41194744a81f5ca86fe26585}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`
* `ImagePortalContrib`
* `ImagePortalContribUser`

>[!NOTE]
>
>L’utilisateur doit disposer d’un accès en lecture et suppression au dossier et à tous ses enfants.

## Paramètres {#section-a793c98a481a4f26ab50bc69b16b57e7}

**Entrée (deleteFolderParam)**

| Nom | Type | Obligatoire | Description |
|---|---|---|---|
| companyHandle | `xsd:string` | Oui | Gestionnaire de la société à laquelle appartient le dossier. |
| folderHandle | `xsd:string` | Oui | Gestionnaire du dossier à supprimer. |

**Output (deleteFolderParam)**

L’API IPS ne renvoie pas de réponse pour cette opération.

## Exemples {#section-9d4617b322e8442d80e59be0f8714841}

Cet exemple de code supprime un dossier de la racine de l’entreprise. Elle nécessite un gestionnaire de dossier, que vous devez obtenir d’une autre opération.

**Requête**

```java
<ns1:deleteFolderParam xmlns:ns1="http://www.scene7.com/IpsApi/xsd">
   <ns1:companyHandle>47</ns1:companyHandle>
   <ns1:folderHandle>MyCompany/SpinSets/</ns1:folderHandle>
</ns1:deleteFolderParam>
```

Aucune
