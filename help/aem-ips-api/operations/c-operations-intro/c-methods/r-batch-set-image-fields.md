---
description: Définit des champs spécifiques à l’image pour un ou plusieurs fichiers d’image.
seo-description: Définit des champs spécifiques à l’image pour un ou plusieurs fichiers d’image.
seo-title: batchSetImageFields
solution: Experience Manager
title: batchSetImageFields
topic: Scene7 Image Production System API
uuid: e0ad7da4-cb28-4402-8b47-a600916d23b3
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# batchSetImageFields{#batchsetimagefields}

Définit des champs spécifiques à l’image pour un ou plusieurs fichiers d’image.

Syntaxe

## Types d’utilisateurs autorisés {#section-6b087bdcb7874c13acf76e113a093054}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`
* `ImagePortalContrib`
* `ImagePortalContribUser`

## Paramètres {#section-4969815cf67c4d11b13bb2017b3604e8}

**Input (batchSetImageFields)**

| Nom | Type | Obligatoire | Description |
|---|---|---|---|
| ` *`companyHandle`*` | `xsd:string` | Oui | Poignée du  qui contient les fichiers d’image. |
| ` *`updateArray`*` | `types:ImageFieldUpdateArray` | Oui | Le tableau des mises à jour des champs d’image. |

**Output (batchSetImageFields)**

| Nom | Type | Obligatoire | Description |
|---|---|---|---|
| ` *`successCount`*` | `xsd:int` | Oui | Nombre de champs d’image définis avec succès. |
| ` *`warningCount`*` | `xsd:int` | Oui | Nombre d’avertissements générés lorsque l’opération tentait de définir les champs d’image. |
| ` *`errorCount`*` | `xsd:int` | Oui | Nombre d’erreurs générées lorsque l’opération tentait de définir les champs d’image. |
| ` *`warningDetailArray`*` | `types:AssetOperationFaultArray` | Non | Tableau des détails associés aux ressources qui ont généré des avertissements lorsque l’opération tentait d’appliquer les mises à jour. |
| ` *`errorDetailArray`*` | `types:AssetOperationFaultArray` | Non | Tableau des détails associés aux ressources qui ont généré des erreurs lorsque l’opération tentait d’appliquer les mises à jour. |

## Exemples {#section-0476e3d6516a4f8bbaac9de983bc6d1e}

Cet exemple montre comment définir les données dans les champs de deux images d&#39;un tableau de mise à jour. Dans le tableau, les images sont spécifiées par leurs poignées de ressources et contiennent la résolution en pixels, les coordonnées de l’ancre x et y, ainsi que les données utilisateur. La réponse indique que les champs des deux images ont été définis avec succès.

**Request**

```java
<batchSetImageFieldsParam xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
   <companyHandle>c|21</companyHandle>
   <updateArray>
      <items>
         <assetHandle>a|140626|1|102524</assetHandle>
         <resolution>72</resolution>
         <anchorX>50</anchorX>
         <anchorY>100</anchorY>
         <userData>nada1</userData>
      </items>
      <items>
         <assetHandle>a|96680|1|64865</assetHandle>
         <resolution>150</resolution>
         <anchorX>100</anchorX>
         <anchorY>50</anchorY>
         <userData>nada2</userData>
      </items>
   </updateArray>
</batchSetImageFieldsParam>
```

**Réponse**

```java
<batchSetImageFieldsReturn xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
   <successCount>2</successCount>
   <warningCount>0</warningCount>
   <errorCount>0</errorCount>
</batchSetImageFieldsReturn>
```

