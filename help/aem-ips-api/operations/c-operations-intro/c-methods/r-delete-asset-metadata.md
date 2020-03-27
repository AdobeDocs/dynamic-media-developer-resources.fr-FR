---
description: Supprime les valeurs de métadonnées d’un fichier. Fonctionne avec un tableau de métadonnées supprimées pour définir des valeurs dans un lot.
seo-description: Supprime les valeurs de métadonnées d’un fichier. Fonctionne avec un tableau de métadonnées supprimées pour définir des valeurs dans un lot.
seo-title: deleteAssetMetadata
solution: Experience Manager
title: deleteAssetMetadata
topic: Scene7 Image Production System API
uuid: 2dc783c6-23da-4a94-8780-3c4ec88ff3f4
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# deleteAssetMetadata{#deleteassetmetadata}

Supprime les valeurs de métadonnées d’un fichier. Fonctionne avec un tableau de métadonnées supprimées pour définir des valeurs dans un lot.

Syntaxe

## Types d’utilisateurs autorisés {#section-e913be43b684491daf02bc73211e4290}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`
* `ImagePortalContrib`
* `ImagePortalContribUser`

>[!NOTE]
>
>L’utilisateur doit avoir accès en lecture et en suppression à la ressource.

## Paramètres {#section-0eed164e278b456fbdfb7a50727a0416}

**Input (deleteAssetMetadataParam)**

<table id="table_A4438E2FE5F245E5B73F46CD887BE70F"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>Nom </p> </th> 
   <th colname="col2" class="entry"> <p>Type </p> </th> 
   <th colname="col3" class="entry"> <p>Obligatoire </p> </th> 
   <th colname="col4" class="entry"> <p>Description </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>companyHandle </p> </td> 
   <td colname="col2"> <p><span class="codeph"> xsd:string</span> </p> </td> 
   <td colname="col3"> <p>Oui </p> </td> 
   <td colname="col4"> <p>Identifiant du auquel appartient le dossier. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>assetHandle </p> </td> 
   <td colname="col2"> <p><span class="codeph"> xsd:string</span> </p> </td> 
   <td colname="col3"> <p>Oui </p> </td> 
   <td colname="col4"> <p>Poignée du fichier à supprimer. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>metadataDelete </p> </td> 
   <td colname="col2"> <p><span class="codeph"> xsd:string</span> </p> </td> 
   <td colname="col3"> <p>Oui </p> </td> 
   <td colname="col4"> <p>Métadonnées à supprimer du fichier. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>deleteArray </p> </td> 
   <td colname="col2"> <p><span class="codeph"> type:MetadataDeleteArray</span> </p> </td> 
   <td colname="col3"> <p>Oui </p> </td> 
   <td colname="col4"> <p>Tableau de métadonnées à supprimer du fichier. </p> </td> 
  </tr> 
 </tbody> 
</table>

**Output (deleteAssetMetadataParam)**

L&#39;API IPS ne renvoie pas de réponse pour cette opération.

## Exemples {#section-d5657289f5234bb0a613dcf691507958}

MetadataDelete

```java
    <complexType name="MetadataDelete">
        <sequence>
            <element name="fieldHandle" type="xsd:string"/>
        </sequence>
    </complexType>
```

Exemple d’appel

```java
<ac:Request id="deleteAssetMetadata">
 <deleteAssetMetadataParam xmlns="http://www.scene7.com/IpsApi/xsd/2013-08-29-beta">
  <companyHandle>c|101</companyHandle>
  <assetHandle>a|202</assetHandle>
  <deleteArray>
   <items>
    <fieldHandle>m|2919|ASSET|UntypedUDFField1395788289789</fieldHandle>
   </items>
  </deleteArray>
 </deleteAssetMetadataParam>
</ac:Request>
```

