---
description: Renvoie tous les dossiers et sous-dossiers, en commençant par le chemin du dossier. La réponse getFolders renvoie un maximum de 100 000 dossiers.
solution: Experience Manager
title: getFolders
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 71fe3343-2560-4d74-8ec3-1229d83a62e1
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '237'
ht-degree: 8%

---

# getFolders{#getfolders}

Renvoie tous les dossiers et sous-dossiers, en commençant par le chemin du dossier. La réponse getFolders renvoie un maximum de 100 000 dossiers.

## Objectif des dossiers {#section-66e344d5333f42f1b060a0cba25935c3}

Un dossier permet d’organiser les sous-dossiers et les ressources. Tous les noms de dossier et de ressource doivent être uniques. Les dossiers et les ressources portant le même nom provoquent un conflit d’espace de noms, même s’ils se trouvent dans des hiérarchies de dossiers différentes.
Syntaxe

## Types d’utilisateurs autorisés {#section-0dc7e17cb60f4cf7bcdb76648e5d2f8e}

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
| companyHandle | `xsd:string` | Oui | La poignée de la société. |
| accessUserHandle | `xsd:string` | Non | Utilisé par les administrateurs pour emprunter l’identité d’un utilisateur spécifique. |
| accessGroupHandle | `xsd:string` | Non | Filtrez selon un groupe spécifique. |
| folderPath | `xsd:string` | Non | Le dossier racine pour récupérer les dossiers et tous les sous-dossiers au niveau de la feuille. Si elle est exclue, la racine de l’entreprise est utilisée. |
| assetTypeArray | `types:StringArray` | Non | Renvoie les dossiers contenant uniquement des types de ressources spécifiés. |
| responseFieldArray | `types:StringArray` | Non | Contient la liste des champs que vous souhaitez inclure dans la réponse. |
| excludeFieldArray | `types:StringArray` | Non | Contient une liste des champs que vous souhaitez exclure de la réponse. |

**Sortie (getFoldersReturn)**

| Nom | Type | Obligatoire | Description |
|---|---|---|---|
| folderArray | `types:FolderArray` | Non | Tableau de dossiers correspondant aux critères de filtrage. La réponse est limitée à 100 000 dossiers au maximum. |
| permissionsSetArray | `types:PermissionSetArray` |  |  |

## Exemples {#section-b5cb06e9fb9945ad898dbdc3692b754e}

Cet exemple de code renvoie un tableau qui contient tous les dossiers d’une entreprise avec des informations spécifiques sur chaque dossier.

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
