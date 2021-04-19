---
description: Définit les métadonnées des fichiers en mode batch.
solution: Experience Manager
title: batchSetAssetMetadata
feature: Dynamic Media Classic, SDK/API, Métadonnées, Gestion des ressources
role: Developer,Administrator
exl-id: 7393fa4f-71fb-48a5-a7f3-91eec82c88c1
translation-type: tm+mt
source-git-commit: f464a7adcb8035a5bdebf1a6c9b647ba04535431
workflow-type: tm+mt
source-wordcount: '153'
ht-degree: 13%

---

# batchSetAssetMetadata{#batchsetassetmetadata}

Définit les métadonnées des fichiers en mode batch.

Syntaxe

## Types d’utilisateur autorisés {#section-5310d9fd00604cbf9756944900378855}

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
| `*`companyHandle`*` | `xsd:string` | Oui | Poignée de la société dont vous souhaitez définir les métadonnées dans une opération de traitement par lot. |
| `*`updateArray`*` | `types:BatchMetadataUpdateArray` | Oui | Tableau de mises à jour des métadonnées appliquées aux ressources. |

**Output (batchSetAssetMetadataParam)**

| Nom | Type | Obligatoire | Description |
|---|---|---|---|
| `*`successCount`*` | `xsd:int` | Oui | Nombre de métadonnées définies avec succès. |
| `*`warningCount`*` | `xsd:int` | Oui | Nombre d’avertissements générés lorsque l’opération tentait de définir des métadonnées. |
| `*`errorCount`*` | `xsd:int` | Oui | Nombre d’erreurs générées lorsque l’opération tentait de définir des métadonnées. |
| `*`warningDetailArray`*` | `types:AssetOperationFaultArray` | Non | Tableau des détails associés aux ressources générant des avertissements lorsque l’opération tentait de définir par lot des métadonnées pour les ressources. |
| `*`errorDetailArray`*` | `types:AssetOperationFaultArray` | Non | Tableau des détails associés aux fichiers qui génèrent des erreurs lorsque l’opération tentait de définir par lot des métadonnées pour les fichiers. |

## Exemples {#section-2de798ac920e4b47b971b1729a64395b}

**Request**

```java
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

```java
<batchSetAssetMetadataReturn xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
   <successCount>4</successCount>
   <warningCount>0</warningCount>
   <errorCount>0</errorCount>
</batchSetAssetMetadataReturn>
```
