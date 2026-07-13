---
description: Définit des champs spécifiques à une image pour une ou plusieurs ressources d’image.
solution: Experience Manager
title: batchSetImageFields
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 8ea6dbb8-4d32-43e5-961f-31110f983663
TQID: 'https://experienceleague.adobe.com/J3mCGBUY4Ws5Wq18tHWrHQJNElW5gYvwSQ2yKF-NhsM'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 4185012f22b173b569d11ea4d350763a82f98710
workflow-type: tm+mt
source-wordcount: 195
ht-degree: 9%

---

# batchSetImageFields{#batchsetimagefields}

Définit des champs spécifiques à une image pour une ou plusieurs ressources d’image.

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
| companyHandle | `xsd:string` | Oui | Identifiant de la société qui contient les ressources d’image. |
| updateArray | `types:ImageFieldUpdateArray` | Oui | Tableau de mises à jour des champs d’image. |

**Output (batchSetImageFields)**

| Nom | Type | Obligatoire | Description |
|---|---|---|---|
| successCount | `xsd:int` | Oui | Nombre de champs d’image définis avec succès. |
| warningCount | `xsd:int` | Oui | Nombre d’avertissements générés lorsque l’opération a tenté de définir les champs d’image. |
| errorCount | `xsd:int` | Oui | Nombre d’erreurs générées lorsque l’opération a tenté de définir les champs d’image. |
| warningDetailArray | `types:AssetOperationFaultArray` | Non | Tableau de détails associés aux ressources qui ont généré des avertissements lorsque l’opération a tenté d’appliquer les mises à jour. |
| errorDetailArray | `types:AssetOperationFaultArray` | Non | Tableau de détails associés aux ressources qui ont généré des erreurs lorsque l’opération a tenté d’appliquer les mises à jour. |

## Exemples {#section-0476e3d6516a4f8bbaac9de983bc6d1e}

Cet exemple montre comment définir des données dans les champs de deux images d’un tableau de mise à jour. Dans le tableau , les images sont spécifiées par leurs poignées de ressource et contiennent la résolution en pixels, les coordonnées d’ancrage des positions x et y et les données utilisateur. La réponse indique que les champs des deux images ont été définis avec succès.

**Requête**

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

