---
description: Affectation ou mise à jour de fichiers dans un projet.
solution: Experience Manager
title: Définir les ressources du projet
feature: Dynamic Media Classic,SDK/API,Asset Management
role: Developer,Admin
exl-id: b6e6e9bd-5ee2-4750-9182-49e7a3e3486c
source-git-commit: 77c88d5fe20e048f6fad2bb23cb1abe090793acf
workflow-type: tm+mt
source-wordcount: '83'
ht-degree: 18%

---

# Définir les ressources du projet{#setprojectassets}

Affectation ou mise à jour de fichiers dans un projet.

Syntaxe

## Types d’utilisateurs autorisés {#section-8d87939db6d547b48ca6d71771bbefa8}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`
* `ImagePortalContrib`
* `ImagePortalContribUser`

## Paramètres {#section-bd51ef23deaf434ba2efb8cef2a8b4a5}

**Entrée (setProjectAssetsParam)**

| Nom | Type | Obligatoire | Description |
|---|---|---|---|
| Nom de la société | `xsd:string` | Oui | Pseudo de l’entreprise. |
| Poignée de projet | `xsd:string` | Oui | Pseudo de projet. |
| assetHandleArray | `types:HandleArray` | Oui | Tableau de descripteurs de ressources que vous souhaitez associer au projet. |

**Output (setProjectAssetsReturn)**

| Nom | Type | Obligatoire | Description |
|---|---|---|---|
| Compte de succès | `xsd:int` | Oui | Nombre de ressources ajoutées avec succès. |

## Exemples {#section-33c1a909c3dc4aa98da474c23a036596}

Cet exemple de code affecte une ressource à un projet. La requête renvoie un nombre de réussite de un.

**Demander**

```java
<setProjectAssetsParam xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
   <companyHandle>c|6</companyHandle>
   <projectHandle>p|6|ProjectTestAPI</projectHandle>
   <assetHandleArray>
      <items>a|739|1|537</items>
   </assetHandleArray>
</setProjectAssetsParam>
```

**Réponse**

```java
<setProjectAssetsReturn xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
   <successCount>1</successCount>
   <warningCount>0</warningCount>
   <errorCount>0</errorCount>
</setProjectAssetsReturn>
```
