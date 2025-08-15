---
description: Renvoie tous les dossiers et sous-dossiers, en commençant par le chemin du dossier. La réponse getFolders renvoie un maximum de 100 000 dossiers.
solution: Experience Manager
title: getFolders
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 71fe3343-2560-4d74-8ec3-1229d83a62e1
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '240'
ht-degree: 7%

---

# getFolders{#getfolders}

Renvoie tous les dossiers et sous-dossiers, en commençant par le chemin du dossier. La réponse getFolders renvoie un maximum de 100 000 dossiers.

## Rôle des dossiers {#section-66e344d5333f42f1b060a0cba25935c3}

Un dossier permet d’organiser des sous-dossiers et des ressources. Tous les noms de dossiers et de ressources doivent être uniques. Les dossiers et les ressources qui partagent le même nom provoquent un conflit d’espace de noms, même s’ils se trouvent dans des hiérarchies de dossiers différentes.
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
>L’utilisateur doit disposer d’un accès en lecture au dossier pour renvoyer les données qu’il contient.

## Paramètres {#section-0c1976503eaa418a9226b51667901176}

**Entrée (getFoldersParam)**

| Nom | Type | Obligatoire | Description |
|---|---|---|---|
| CompanyHandle | `xsd:string` | Oui | La poignée de l’entreprise. |
| AccessUserHandle | `xsd:string` | Non | Utilisé par les administrateurs pour emprunter l’identité d’un utilisateur spécifique. |
| Poignée accessGroupHandle | `xsd:string` | Non | Filtrer par groupe spécifique. |
| chemin d’accès au dossier | `xsd:string` | Non | Dossier racine pour récupérer les dossiers et tous les sous-dossiers au niveau feuille. Si elle est exclue, la racine de l’entreprise est utilisée. |
| assetTypeArray | `types:StringArray` | Non | Renvoie les dossiers qui contiennent uniquement les types de ressource spécifiés. |
| Réseau responseFieldArray | `types:StringArray` | Non | Contient la liste des champs à inclure dans la réponse. |
| excludeFieldArray | `types:StringArray` | Non | Contient la liste des champs à exclure de la réponse. |

**Output (getFoldersReturn)**

| Nom | Type | Obligatoire | Description |
|---|---|---|---|
| Tableau de dossiers | `types:FolderArray` | Non | Tableau de dossiers répondant aux critères de filtrage. La réponse est limitée à 100 000 dossiers maximum. |
| permissionsSetArray | `types:PermissionSetArray` |  |  |

## Exemples {#section-b5cb06e9fb9945ad898dbdc3692b754e}

Cet exemple de code renvoie un tableau qui contient tous les dossiers d’une société ainsi que des informations spécifiques sur chaque dossier.

**Demander**

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
