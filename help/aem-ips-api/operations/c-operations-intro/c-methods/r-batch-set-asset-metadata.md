---
description: Définit les métadonnées des fichiers à l’aide du mode trait.
solution: Experience Manager
title: Métadonnées de lot
feature: Dynamic Media Classic,SDK/API,Metadata,Asset Management
role: Developer,Admin
exl-id: 7393fa4f-71fb-48a5-a7f3-91eec82c88c1
source-git-commit: b89ca96947f751b750623e1f18d2a5d86f0cd759
workflow-type: tm+mt
source-wordcount: '145'
ht-degree: 12%

---

# Métadonnées de lot{#batchsetassetmetadata}

Définit les métadonnées des fichiers à l’aide du mode trait.

Syntaxe

## Types d’utilisateurs autorisés {#section-5310d9fd00604cbf9756944900378855}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`
* `ImagePortalContrib`
* `ImagePortalContribUser`

## Paramètres {#section-7111ac93bc7747f69ba14db4ac3912b0}

**Entrée (batchSetAssetMetadataParam)**

| Nom | Type | Obligatoire | Description |
|---|---|---|---|
| CompanyHandle | `xsd:string` | Oui | Poignée de la société dont vous souhaitez définir les métadonnées dans une opération par lot. |
| Mettre à jour le tableau | `types:BatchMetadataUpdateArray` | Oui | Tableau des mises à jour de métadonnées appliquées aux ressources. |

**Output (batchSetAssetMetadataParam)**

| Nom | Type | Obligatoire | Description |
|---|---|---|---|
| Compte de succès | `xsd:int` | Oui | Nombre de métadonnées correctement définies. |
| Nombre d’avertissements | `xsd:int` | Oui | Nombre d’avertissements générés lorsque l’opération a tenté de définir des métadonnées. |
| Nombre d’erreurs | `xsd:int` | Oui | Nombre d’erreurs générées lorsque l’opération a tenté de définir des métadonnées. |
| Tableau des détails de l’avertissement | `types:AssetOperationFaultArray` | Non | Tableau de détails associé aux ressources générant des avertissements lorsque l’opération a tenté de définir par lots les métadonnées des ressources. |
| Tableau errorDetailArray | `types:AssetOperationFaultArray` | Non | Tableau de détails associé aux ressources qui génèrent des erreurs lorsque l’opération a tenté de définir par lot les métadonnées des ressources. |

## Exemples {#section-2de798ac920e4b47b971b1729a64395b}

**Demander**

```java {.line-numbers}
<batchSetAssetMetadataParam xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
<companyHandle>c|6</companyHandle>
<updateArray>
   <items>
      <assetHandleArray>
         <items>a|743|1|538</items>
         <items>a|744|1|539</items>
      </assetHandleArray>
      <updateArray>
         <items>
            <fieldHandle>m|6|IMAGE|saveMetadataField</fieldHandle>
            <value>400</value>
         </items>
      </updateArray>
   </items>
   <items>
      <assetHandleArray>
         <items>a|732|1|535</items>
         <items>a|739|1|537</items>
      </assetHandleArray>
      <updateArray>
         <items>
            <fieldHandle>m|6|IMAGE|saveMetadataField</fieldHandle>
            <value>300</value>
         </items>
      </updateArray>
   </items>
</updateArray>
</batchSetAssetMetadataParam>
```

**Réponse**

```java {.line-numbers}
<batchSetAssetMetadataReturn xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
   <successCount>4</successCount>
   <warningCount>0</warningCount>
   <errorCount>0</errorCount>
</batchSetAssetMetadataReturn>
```
