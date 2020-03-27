---
description: Crée un dossier.
seo-description: Crée un dossier.
seo-title: createFolder
solution: Experience Manager
title: createFolder
topic: Scene7 Image Production System API
uuid: e3a4eed3-966d-4435-bfeb-3ead4bf523cd
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# createFolder{#createfolder}

Crée un dossier.

>[!NOTE]
>
>Le nouveau dossier est subordonné au dossier Images, même si vous spécifiez un `/` pour indiquer la racine du .

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
| ` *`companyHandle`*` | `xsd:string` | Oui | La poignée du |
| ` *`folderPath`*` | `xsd:string` | Oui | Dossier racine utilisé pour récupérer les dossiers et tous les sous-dossiers au niveau de la feuille. Si elle est exclue, la racine du  est utilisée. |

**Output (createFolderParam)**

| Nom | Type | Obligatoire | Description |
|---|---|---|---|
| ` *`folderHandle`*` | `xsd:string` | Oui | Gestion du nouveau dossier. |

## Exemples {#section-e596fbdb44fd43c8b30005cb2a2fdf26}

Cet exemple de code crée un dossier à la racine d’un  de. La réponse renvoie le nom d’utilisateur du dossier nouvellement créé.

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

