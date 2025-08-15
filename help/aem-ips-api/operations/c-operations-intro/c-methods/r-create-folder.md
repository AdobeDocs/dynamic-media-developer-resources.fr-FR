---
title: Créer un dossier
description: Crée un dossier.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 569130ae-5515-4b14-a410-2bd6f9fc7638
source-git-commit: f42378a20b58e4c5ebc961c6526d7cecabc2ae38
workflow-type: tm+mt
source-wordcount: '118'
ht-degree: 16%

---

# [!DNL createFolder]{#createfolder}

Crée un dossier.

>[!NOTE]
>
>Le nouveau dossier est subordonné au dossier Images, même si vous spécifiez un `/` pour indiquer la racine de l’entreprise.

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
| CompanyHandle | `xsd:string` | Oui | La poignée à l’entreprise |
| chemin d’accès au dossier | `xsd:string` | Oui | Dossier racine utilisé pour récupérer les dossiers et tous les sous-dossiers au niveau feuille. Si elle est exclue, la racine de l’entreprise est utilisée. |

**Output (createFolderParam)**

| Nom | Type | Obligatoire | Description |
|---|---|---|---|
| poignée de dossier | `xsd:string` | Oui | Pseudo du nouveau dossier. |

## Exemples {#section-e596fbdb44fd43c8b30005cb2a2fdf26}

Cet exemple de code crée un dossier à la racine d’une société. La réponse renvoie l’identifiant du nouveau dossier créé.

**Demander**

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
