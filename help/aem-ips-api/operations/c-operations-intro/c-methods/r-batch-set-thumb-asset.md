---
description: Définit l’image miniature d’une ou de plusieurs ressources.
solution: Experience Manager
title: batchSetThumbAsset
feature: Dynamic Media Classic,SDK/API,Asset Management
role: Developer,Admin
exl-id: f7d7ddd9-a3c3-47c4-8da6-d693851d0d7f
source-git-commit: 77c88d5fe20e048f6fad2bb23cb1abe090793acf
workflow-type: tm+mt
source-wordcount: '171'
ht-degree: 11%

---

# batchSetThumbAsset{#batchsetthumbasset}

Définit l’image miniature d’une ou de plusieurs ressources.

Syntaxe

## Types de ressources de miniature {#section-4edc2a6a8f824213b0aaddb1d437268c}

Les types de ressources miniatures autorisés sont les suivants :

* Image
* AdjustedView
* Masque
* Modèle
* PsdTemplate

## Types d’utilisateurs autorisés {#section-5fc988e3d6384968b86fd9fe363658c0}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`
* `ImagePortalContrib`
* `ImagePortalContribUser`

>[!NOTE]
>
>L’utilisateur doit disposer d’un accès en lecture/écriture à la ressource cible et d’un accès en lecture à la ressource de pouces.

## Paramètres {#section-9c6efa000b384b3db6c013def20cf40b}

**Input (batchSetThumbAssetParam)**

| Nom | Type | Obligatoire | Description |
|---|---|---|---|
| companyHandle | `xsd:string` | Oui | Identifiant de la société qui contient les ressources. |
| updateArray | `types:ThumbAssetUpdateArray` | Oui | Tableau de mises à jour. |

**Output (batchSetThumbAssetParam)**

| Nom | Type | Obligatoire | Description |
|---|---|---|---|
| successCount | `xsd:int` | Oui | Nombre de miniatures définies avec succès. |
| warningCount | `xsd:int` | Oui | Nombre d’avertissements générés lorsque l’opération a tenté de définir les miniatures. |
| errorCount | `xsd:int` | Oui | Nombre d’erreurs générées lorsque l’opération a tenté de définir les miniatures. |
| warningDetailArray | `types:AssetOperationFaultArray` | Non | Tableau de détails associés aux ressources qui ont généré des avertissements lorsque l’opération a tenté d’appliquer les mises à jour. |
| errorDetailArray | `types:AssetOperationFaultArray` | Non | Tableau de détails associés aux ressources qui ont généré des erreurs lorsque l’opération a tenté d’appliquer les mises à jour. |

## Exemples {#section-6de69a8680c24c1486c5f01488393381}

**Requête**

```java
<batchSetThumbAssetParam xmlns="http://www.scene7.com/IpsApi/xsd/2010-01-31">
   <companyHandle>c|3</companyHandle>
   <updateArray>
      <items>
         <assetHandle>a|234</assetHandle>
         <thumbAssetHandle>a|189</thumbAssetHandle>
      </items>
   </updateArray>
```

**Réponse**

```java
<batchSetThumbAssetReturn xmlns="http://www.scene7.com/IpsApi/xsd/2010-01-31">
   <successCount>1</successCount>
   <warningCount>0</warningCount>
   <errorCount>0</errorCount>
</batchSetThumbAssetReturn>
```
