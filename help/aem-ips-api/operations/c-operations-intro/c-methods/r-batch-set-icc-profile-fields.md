---
description: Définit les champs de métadonnées du profil ICC.
solution: Experience Manager
title: Champs batchSetIccProfile
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: d10a30ca-afa7-4ef0-8cef-0329b0068bf3
source-git-commit: b89ca96947f751b750623e1f18d2a5d86f0cd759
workflow-type: tm+mt
source-wordcount: '137'
ht-degree: 13%

---

# Champs batchSetIccProfile{#batchseticcprofilefields}

Définit les champs de métadonnées du profil ICC.

Syntaxe

## Types d’utilisateurs autorisés {#section-f6f7caf9434b4f469518dab64b76c0f4}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`
* `ImagePortalContrib`
* `ImagePortalContribUser`

## Paramètres {#section-75a02b55ae0d444ca26b59aac6e86d6f}

**Entrée (batchSetIccProfileFields)**

| Nom | Type | Obligatoire | Description |
|---|---|---|---|
| CompanyHandle | `xsd:string` | Oui | Gérez vers la société qui contient les profils ICC. |
| Mettre à jour la matrice | `xsd:string` | Oui | Tableau de mises à jour de profil ICC. |

**Output (batchSetIccProfileFields)**

| Nom | Type | Obligatoire | Description |
|---|---|---|---|
| Compte de succès | `xsd:int` | Oui | Nombre de champs de profil ICC correctement définis. |
| Nombre d’avertissements | `xsd:int` | Oui | Nombre d’avertissements générés lorsque l’opération a tenté de définir les champs de profil ICC. |
| Nombre d’erreurs | `xsd:int` | Oui | Nombre d’erreurs générées lorsque l’opération a tenté de définir les champs de profil ICC. |
| Tableau des détails de l’avertissement | `types:AssetOperationFaultArray` | Non | Tableau de détails associé aux ressources qui ont généré des avertissements lorsque l’opération a tenté d’appliquer les mises à jour. |
| Tableau errorDetailArray | `types:AssetOperationFaultArray` | Non | Tableau de détails associé aux ressources qui ont généré des erreurs lorsque l’opération a tenté d’appliquer les mises à jour. |

## Exemples {#section-5dc90cfbd9b1411485b44859032f7cb9}

**Demander**

```java {.line-numbers}
<batchSetIccProfileFieldsParam xmlns="http://www.scene7.com/IpsApi/xsd/2009-07-31">
   <companyHandle>c|1</companyHandle>
   <updateArray>
      <items>
         <assetHandle>a|1808|13|169</assetHandle>
         <class>Output</class>
         <colorSpace>CMYK</colorSpace>
         <pcsType>Luv</pcsType>
      </items>
   </updateArray>
</batchSetIccProfileFieldsParam>
```

**Réponse**

```java {.line-numbers}
<batchSetIccProfileFieldsReturn xmlns="http://www.scene7.com/IpsApi/xsd/2009-07-31">
   <successCount>1</successCount>
   <warningCount>0</warningCount>
   <errorCount>0</errorCount>
</batchSetIccProfileFieldsReturn>
```
