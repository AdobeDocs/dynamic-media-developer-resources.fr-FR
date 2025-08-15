---
description: Renvoie les dossiers et sous-dossiers sous la forme d’une arborescence hiérarchique. La réponse getFolderTree est limitée à un maximum de 100 000 dossiers
solution: Experience Manager
title: getFolderTree
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 1afe63ca-d11a-4fa5-a26b-90a23bee1b68
source-git-commit: 77c88d5fe20e048f6fad2bb23cb1abe090793acf
workflow-type: tm+mt
source-wordcount: '261'
ht-degree: 8%

---

# getFolderTree{#getfoldertree}

Renvoie les dossiers et sous-dossiers sous la forme d’une arborescence hiérarchique. La réponse getFolderTree est limitée à un maximum de 100 000 dossiers

Syntaxe

## Types d’utilisateurs autorisés {#section-66ef19149f4d4123a3a99004b5a2743e}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `TrialSiteAdmin`
* `TrialSiteUser`
* `ImagePortalContrib`
* `ImagePortalContribUser`

>[!NOTE]
>
>L’utilisateur doit disposer d’un accès en lecture au dossier pour y renvoyer des données.

## Paramètres {#section-0c2b30513f1e439cbd840e8cc6465b3a}

**Input (getFolderTreeParam)**

| Nom | Type | Obligatoire | Description |
|---|---|---|---|
| companyHandle | `xsd:string` | Oui | La poignée de la société. |
| accessUserHandle | `xsd:string` | Non | Utilisé uniquement par les administrateurs pour emprunter l’identité d’un utilisateur spécifique. |
| accessGroupHandle | `xsd:string` | Non | Utilisé pour filtrer par groupe spécifique, y compris ceux auxquels la société appartient. |
| folderPath | `xsd:string` | Non | Le dossier racine pour récupérer les dossiers et tous les sous-dossiers au niveau feuille. S’il est exclu, la racine d’entreprise est utilisée. |
| profondeur | `xsd:int` | Oui | Une valeur égale à zéro permet d’obtenir le dossier de niveau supérieur. Toute autre valeur indique la profondeur à descendre dans l’arborescence. |
| assetTypeArray | `types:StringArray` | Non | Renvoie les dossiers qui contiennent uniquement des types de ressources spécifiés. |
| responseFieldArray | `types:StringArray` | Non | Contient une liste de champs que vous souhaitez inclure dans la réponse. |
| excludeFieldArray | `types:StringArray` | Non | Contient une liste de champs que vous souhaitez exclure de la réponse. |

**Output (getFolderTreeReturn)**

| Nom | Type | Obligatoire | Description |
|---|---|---|---|
| dossiers | `types:folders` | Non | Hiérarchie des dossiers dans une arborescence. La réponse est limitée à un maximum de 100 000 dossiers. |
| permissionSetArray | `types:PermissionSetArray` |  |  |

## Exemples {#section-a9fd2edb56574dd9bf8b0f2fd89367e4}

Cet exemple de code utilise un handle d’entreprise et un paramètre de profondeur pour déterminer le niveau de profondeur que la réponse doit renvoyer. La réponse contient des dossiers et des tableaux de sous-dossiers avec des associés. Définissez la valeur de profondeur sur un nombre plus petit pour effectuer une recherche plus approfondie dans l’arborescence de dossiers.

**Requête**

```java
<ns1:getFolderTreeParam xmlns:ns1="http://www.scene7.com/IpsApi/xsd">
   <ns1:companyHandle>47</ns1:companyHandle>
   <ns1:depth>-1</ns1:depth>
</ns1:getFolderTreeParam>
```

**Réponse**

```java
<getFolderTreeReturn xmlns="http://www.scene7.com/IpsApi/xsd/">
  <folders>
    <items>
      <folderHandle>f|sampleFolder/uploadTestDir/</folderHandle>
      <path>MyCompany/uploadTestDir/</path>
      <lastModified>2011-11-14T11:19:59.031-08:00</lastModified>
      <childLastModified>2011-11-14T11:19:59.031-08:00</childLastModified>
      <permissionSetHandle>pm|2</permissionSetHandle>
      <hasSubfolders>true</hasSubfolders>
      <subfolderArray>
        <items>
          <folderHandle>f|MyCompany/uploadTestDir/SubFolder/</folderHandle>
          <path>DevanCo/uploadTestDir/SubFolder/</path>
          <lastModified>2011-11-14T11:19:59.032-08:00</lastModified>
          <childLastModified>2011-11-14T11:19:59.032-08:00</childLastModified>
          <permissionSetHandle>pm|2</permissionSetHandle>
          <hasSubfolders>true</hasSubfolders>
          <subfolderArray>
            <items>
              <folderHandle>f|MyCompany/uploadTestDir/SubFolder/10/</folderHandle>
              <path>DevanCo/uploadTestDir/SubFolder/10/</path>
              <lastModified>2011-11-14T11:19:59.033-08:00</lastModified>
              <childLastModified>2011-11-14T15:06:58.563-08:00</childLastModified>
              <permissionSetHandle>pm|2</permissionSetHandle>
              <hasSubfolders>false</hasSubfolders>
            </items>
          </subfolderArray>
        </items>
      </subfolderArray>
    </items>
  </folders>
  <permissionSetArray>
    <items>
      <permissionSetHandle>pm|2</permissionSetHandle>
      <permissionArray>
        <items>
          <groupHandle>g|1</groupHandle>
          <groupName>Asset Download Group</groupName>
          <permissionType>Read</permissionType>
          <isAllowed>true</isAllowed>
          <isOverride>false</isOverride>
        </items>
        <items>
          <groupHandle>g|2</groupHandle>
          <groupName>Asset Upload Group</groupName>
          <permissionType>Read</permissionType>
          <isAllowed>true</isAllowed>
          <isOverride>true</isOverride>
        </items>
        <items>
          <groupHandle>g|2</groupHandle>
          <groupName>Asset Upload Group</groupName>
          <permissionType>Write</permissionType>
          <isAllowed>true</isAllowed>
          <isOverride>true</isOverride>
        </items>
      </permissionArray>
    </items>
  <permissionSetArray>
</getFolderTreeReturn>
```
