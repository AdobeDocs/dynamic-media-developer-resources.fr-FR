---
description: Crée un dossier.
solution: Experience Manager
title: createFolder
feature: Dynamic Media Classic, SDK/API
role: Developer,Admin
exl-id: 569130ae-5515-4b14-a410-2bd6f9fc7638
source-git-commit: fcda99340a18d5037157723bb3bdca5fa9df3277
workflow-type: tm+mt
source-wordcount: '123'
ht-degree: 17%

---

# [!DNL createFolder]{#createfolder}

Crée un dossier.

>[!NOTE]
>
>Le nouveau dossier est Secondaire au dossier Images , même si vous spécifiez une balise `/` pour indiquer la racine de l’entreprise.

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

**Input (createFolder)**

| Nom | Type | Obligatoire | Description |
|---|---|---|---|
| `*`companyHandle`*` | `xsd:string` | Oui | La gestion de la société |
| `*`folderPath`*` | `xsd:string` | Oui | Dossier racine utilisé pour récupérer les dossiers et tous les sous-dossiers au niveau de la feuille. Si elle est exclue, la racine de l’entreprise est utilisée. |

**Output (createFolderParam)**

| Nom | Type | Obligatoire | Description |
|---|---|---|---|
| `*`folderHandle`*` | `xsd:string` | Oui | Gestion du nouveau dossier. |

## Exemples {#section-e596fbdb44fd43c8b30005cb2a2fdf26}

Cet exemple de code crée un dossier à la racine d’une entreprise. La réponse renvoie le gestionnaire du dossier nouvellement créé.

**Request**

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
