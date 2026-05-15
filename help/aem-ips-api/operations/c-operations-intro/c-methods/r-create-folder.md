---
title: createFolder
description: Crée un dossier.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 569130ae-5515-4b14-a410-2bd6f9fc7638
TQID: 'https://experienceleague.adobe.com/iQNFDdsbxhklGSfUb1pmcNhzIT8kJYc19xFglU7Blc8'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 118
ht-degree: 16%

---

# [!DNL createFolder]{#createfolder}

Crée un dossier.

>[!NOTE]
>
>Le nouveau dossier est subordonné au dossier Images, même si vous spécifiez un `/` pour indiquer la racine de la société.

Syntaxe

## Types d’utilisateurs autorisés {#section-14ef6368056b4e8f96198c20b6d93b9b}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`
* `ImagePortalContrib`
* `ImagePortalContribUser`

>[!NOTE]
>
>L’utilisateur doit disposer d’un accès en lecture/écriture au dossier parent.

## Paramètres {#section-c00d8d89cf114886a535056f2a1bf892}

**Entrée (createFolder)**

| Nom | Type | Obligatoire | Description |
|---|---|---|---|
| companyHandle | `xsd:string` | Oui | La poignée de la société |
| folderPath | `xsd:string` | Oui | Le dossier racine utilisé pour récupérer les dossiers et tous les sous-dossiers au niveau feuille. S’il est exclu, la racine d’entreprise est utilisée. |

**Output (createFolderParam)**

| Nom | Type | Obligatoire | Description |
|---|---|---|---|
| folderHandle | `xsd:string` | Oui | Gestionnaire du nouveau dossier. |

## Exemples {#section-e596fbdb44fd43c8b30005cb2a2fdf26}

Cet exemple de code crée un dossier à la racine d’une entreprise. La réponse renvoie l’identificateur du dossier nouvellement créé.

**Requête**

```java
<ns1:createFolderParam xmlns:ns1="http://www.scene7.com/IpsApi/xsd">
   <ns1:companyHandle>47</ns1:companyHandle>
   <ns1:folderPath>/SpinSets</ns1:folderPath>
</ns1:createFolderParam>
```

**Réponse**

```java
<ns1:createFolderReturn xmlns:ns1="http://www.scene7.com/IpsApi/xsd">
   <folderHandle xmlns="http://www.scene7.com/IpsApi/xsd">MyCompany/SpinSets/</folderHandle>
</ns1:createFolderReturn>
```
