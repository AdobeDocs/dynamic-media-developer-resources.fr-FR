---
description: Crée un dossier.
seo-description: Crée un dossier.
seo-title: createFolder
solution: Experience Manager
title: createFolder
topic: Dynamic Media Image Production System API
uuid: e3a4eed3-966d-4435-bfeb-3ead4bf523cd
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '122'
ht-degree: 20%

---


# [!DNL createFolder]{#createfolder}

Crée un dossier.

>[!NOTE]
>
>Le nouveau dossier est Secondaire au dossier Images, même si vous spécifiez `/` pour indiquer la racine de la société.

Syntaxe

## Types d’utilisateur autorisés {#section-14ef6368056b4e8f96198c20b6d93b9b}

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
| `*`companyHandle`*` | `xsd:string` | Oui | Le Handle à la société |
| `*`folderPath`*` | `xsd:string` | Oui | Dossier racine utilisé pour récupérer les dossiers et tous les sous-dossiers au niveau feuille. Si elle est exclue, la racine de la société est utilisée. |

**Output (createFolderParam)**

| Nom | Type | Obligatoire | Description |
|---|---|---|---|
| `*`folderHandle`*` | `xsd:string` | Oui | Gestionnaire du nouveau dossier. |

## Exemples {#section-e596fbdb44fd43c8b30005cb2a2fdf26}

Cet exemple de code crée un dossier à la racine d&#39;une société. La réponse renvoie le nom d&#39;utilisateur du dossier que vous venez de créer.

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

