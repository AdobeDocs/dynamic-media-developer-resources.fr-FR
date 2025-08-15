---
description: Définit des champs spécifiques à une image pour un ou plusieurs fichiers image.
solution: Experience Manager
title: Champs d’image en forme de lot
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 8ea6dbb8-4d32-43e5-961f-31110f983663
source-git-commit: 77c88d5fe20e048f6fad2bb23cb1abe090793acf
workflow-type: tm+mt
source-wordcount: '192'
ht-degree: 9%

---

# Champs d’image en forme de lot{#batchsetimagefields}

Définit des champs spécifiques à une image pour un ou plusieurs fichiers image.

Syntaxe

## Types d’utilisateurs autorisés {#section-6b087bdcb7874c13acf76e113a093054}

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
| CompanyHandle | `xsd:string` | Oui | Poignée de l’entreprise qui contient les ressources image. |
| Mettre à jour le tableau | `types:ImageFieldUpdateArray` | Oui | Tableau des mises à jour des champs d’image. |

**Output (batchSetImageFields)**

| Nom | Type | Obligatoire | Description |
|---|---|---|---|
| Compte de succès | `xsd:int` | Oui | Nombre de champs d’image correctement définis. |
| Nombre d’avertissements | `xsd:int` | Oui | Nombre d’avertissements générés lorsque l’opération a tenté de définir les champs d’image. |
| Nombre d’erreurs | `xsd:int` | Oui | Nombre d’erreurs générées lorsque l’opération a tenté de définir les champs d’image. |
| Tableau des détails de l’avertissement | `types:AssetOperationFaultArray` | Non | Tableau de détails associé aux ressources qui ont généré des avertissements lorsque l’opération a tenté d’appliquer les mises à jour. |
| Tableau errorDetailArray | `types:AssetOperationFaultArray` | Non | Tableau de détails associé aux ressources qui ont généré des erreurs lorsque l’opération a tenté d’appliquer les mises à jour. |

## Exemples {#section-0476e3d6516a4f8bbaac9de983bc6d1e}

Cet exemple définit les données dans les champs de deux images d’un tableau de mises à jour. Dans le tableau, les images sont spécifiées par leurs descripteurs de ressources et contiennent une résolution en pixels, les coordonnées d’ancrage des positions x et y et les données utilisateur. La réponse indique que les champs des deux images ont été correctement définis.

**Demander**

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
