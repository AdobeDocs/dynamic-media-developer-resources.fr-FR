---
description: Renvoie tous les dossiers et sous-dossiers, en commençant par le chemin d’accès au dossier. La réponse getFolders renvoie un maximum de 100 000 dossiers.
solution: Experience Manager
title: getFolders
feature: Dynamic Media Classic, SDK/API
role: Développeur, Administrateur
translation-type: tm+mt
source-git-commit: 052bfcbcf1bd4ccf60afa7e3325bf58dd07cba85
workflow-type: tm+mt
source-wordcount: '244'
ht-degree: 8%

---


# getFolders{#getfolders}

Renvoie tous les dossiers et sous-dossiers, en commençant par le chemin d’accès au dossier. La réponse getFolders renvoie un maximum de 100 000 dossiers.

## Objet des dossiers {#section-66e344d5333f42f1b060a0cba25935c3}

Un dossier vous permet d’organiser les sous-dossiers et les fichiers. Tous les noms de dossier et de fichier doivent être uniques. Les dossiers et les fichiers portant le même nom provoqueront un conflit d’espaces de nommage, même s’ils se trouvent dans des hiérarchies de dossiers différentes.
Syntaxe

## Types d’utilisateur autorisés {#section-0dc7e17cb60f4cf7bcdb76648e5d2f8e}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `TrialSiteAdmin`
* `TrialSiteUser`
* `ImagePortalAdmin`
* `ImagePortalUser`
* `ImagePortalContrib`
* `ImagePortalContribUser`

>[!NOTE]
>
>L’utilisateur doit disposer d’un accès en lecture au dossier pour y renvoyer des données.

## Paramètres {#section-0c1976503eaa418a9226b51667901176}

**Entrée (getFoldersParam)**

| Nom | Type | Obligatoire | Description |
|---|---|---|---|
| `*`companyHandle`*` | `xsd:string` | Oui | La poignée de la société. |
| `*`accessUserHandle`*` | `xsd:string` | Non | Utilisé par les administrateurs pour se faire passer pour un utilisateur spécifique. |
| `*`accessGroupHandle`*` | `xsd:string` | Non | Filtrer selon un groupe spécifique. |
| `*`folderPath`*` | `xsd:string` | Non | dossier racine dans lequel récupérer les dossiers et tous les sous-dossiers au niveau feuille. Si elle est exclue, la racine de la société est utilisée. |
| `*`assetTypeArray`*` | `types:StringArray` | Non | Renvoie les dossiers qui contiennent uniquement des types de fichier spécifiés. |
| `*`responseFieldArray`*` | `types:StringArray` | Non | Contient une liste de champs que vous souhaitez inclure dans la réponse. |
| `*`excludeFieldArray`*` | `types:StringArray` | Non | Contient une liste de champs que vous souhaitez exclure de la réponse. |

**Output (getFoldersReturn)**

| Nom | Type | Obligatoire | Description |
|---|---|---|---|
| `*`folderArray`*` | `types:FolderArray` | Non | Tableau de dossiers correspondant aux critères de filtrage. La réponse est limitée à 100 000 dossiers au maximum. |
| `*`permissionsSetArray`*` | `types:PermissionSetArray` |  |  |

## Exemples {#section-b5cb06e9fb9945ad898dbdc3692b754e}

Cet exemple de code renvoie un tableau contenant tous les dossiers d&#39;une société, ainsi que des informations spécifiques sur chaque dossier.

**Request**

```java
<ns1:getFoldersParam xmlns:ns1="http://www.scene7.com/IpsApi/xsd">
   <ns1:companyHandle>47</ns1:companyHandle>
</ns1:getFoldersParam>
```

**Réponse**

```java
<getFoldersReturn xmlns="http://www.scene7.com/IpsApi/xsd">
   <folderArray>
      <items>
         <folderHandle>MyCompany/</folderHandle>
         <path>MyCompany/</path>
         <hasSubfolders>false</hasSubfolders>
      </items>
      <items>
         <folderHandle>MyCompany/eCatalogs/</folderHandle>
         <path>MyCompany/eCatalogs/</path>
         <hasSubfolders>false</hasSubfolders>
      </items>
      <items>
         <folderHandle>MyCompany/PDF/</folderHandle>
         <path>MyCompany/PDF/</path>
         <hasSubfolders>false</hasSubfolders>
      </items>
   </folderArray>
</getFoldersReturn>
```

