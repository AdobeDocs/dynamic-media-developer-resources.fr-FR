---
description: Définit les champs spécifiques à l’image pour un ou plusieurs fichiers d’image.
solution: Experience Manager
title: batchSetImageFields
feature: Dynamic Media Classic, SDK/API
role: Développeur, Administrateur
exl-id: 8ea6dbb8-4d32-43e5-961f-31110f983663
translation-type: tm+mt
source-git-commit: b4344397f82eb7d2d61020909f4acc7fddea210b
workflow-type: tm+mt
source-wordcount: '199'
ht-degree: 10%

---

# batchSetImageFields{#batchsetimagefields}

Définit les champs spécifiques à l’image pour un ou plusieurs fichiers d’image.

Syntaxe

## Types d’utilisateur autorisés {#section-6b087bdcb7874c13acf76e113a093054}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`
* `ImagePortalContrib`
* `ImagePortalContribUser`

## Paramètres {#section-4969815cf67c4d11b13bb2017b3604e8}

**Entrée (batchSetImageFields)**

| Nom | Type | Obligatoire | Description |
|---|---|---|---|
| `*`companyHandle`*` | `xsd:string` | Oui | Poignée de la société contenant les fichiers d’image. |
| `*`updateArray`*` | `types:ImageFieldUpdateArray` | Oui | Tableau des mises à jour des champs d’image. |

**Output (batchSetImageFields)**

| Nom | Type | Obligatoire | Description |
|---|---|---|---|
| `*`successCount`*` | `xsd:int` | Oui | Nombre de champs d’image définis avec succès. |
| `*`warningCount`*` | `xsd:int` | Oui | Nombre d’avertissements générés lorsque l’opération tentait de définir les champs d’image. |
| `*`errorCount`*` | `xsd:int` | Oui | Nombre d’erreurs générées lorsque l’opération tentait de définir les champs d’image. |
| `*`warningDetailArray`*` | `types:AssetOperationFaultArray` | Non | Tableau des détails associés aux ressources qui ont généré des avertissements lorsque l’opération tentait d’appliquer les mises à jour. |
| `*`errorDetailArray`*` | `types:AssetOperationFaultArray` | Non | Tableau des détails associés aux ressources qui ont généré des erreurs lorsque l’opération a tenté d’appliquer les mises à jour. |

## Exemples {#section-0476e3d6516a4f8bbaac9de983bc6d1e}

Cet exemple montre comment définir les données dans les champs de deux images d&#39;un tableau de mise à jour. Dans le tableau, les images sont spécifiées par leurs poignées de ressources et contiennent une résolution en pixels, des coordonnées d’ancrage de position x et y, ainsi que des données utilisateur. La réponse indique que les champs des deux images ont été définis avec succès.

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
