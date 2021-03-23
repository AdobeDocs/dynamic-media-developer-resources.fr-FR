---
description: Définit les champs de métadonnées de police.
seo-description: Définit les champs de métadonnées de police.
seo-title: batchSetFontFields
solution: Experience Manager
title: batchSetFontFields
uuid: 0209865e-32b3-4bea-a508-05771a0365e1
feature: Dynamic Media Classic, SDK/API
role: Développeur, Administrateur
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '137'
ht-degree: 13%

---


# batchSetFontFields{#batchsetfontfields}

Définit les champs de métadonnées de police.

## Types d’utilisateur autorisés {#section-89eff13b5ed54cddb87b1304ba4eff0e}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalContrib`
* `ImagePortalContribUser`

## Paramètres {#section-836f5948d00a46e98ccb62f0573e4e68}

**Entrée (batchSetFontFieldsParam)**

| Nom | Type | Obligatoire | Description |
|---|---|---|---|
| `*`companyHandle`*` | `xsd:string` | Oui | Accédez à la société contenant les polices. |
| `*`updateArray`*` | `types:FontFieldUpdateArray` | Oui | Tableau des mises à jour des champs de police. |

**Output (batchSetFontFieldsParam)**

| Nom | Type | Obligatoire | Description |
|---|---|---|---|
| `*`successCount`*` | `xsd:int` | Oui | Nombre de champs de police définis avec succès. |
| `*`warningCount`*` | `xsd:int` | Oui | Nombre d’avertissements générés lorsque l’opération tentait de définir des champs de police. |
| `*`errorCount`*` | `xsd:int` | Oui | Nombre d’erreurs générées lorsque l’opération tentait de définir des champs de police. |
| `*`warningDetailArray`*` | `types:AssetOperationFaultArray` | Non | Tableau des détails associés aux ressources qui ont généré des avertissements lorsque l’opération tentait d’appliquer les mises à jour. |
| `*`errorDetailArray`*` | `types:AssetOperationFaultArray` | Non | Tableau des détails associés aux ressources qui ont généré des erreurs lorsque l’opération a tenté d’appliquer les mises à jour. |

## Exemples {#section-0449c2e4ec534f4b8ee849ec4fe12c4e}

**Request**

```java
<batchSetFontFieldsParam xmlns="http://www.scene7.com/IpsApi/xsd/2009-07-31">
   <companyHandle>c|1</companyHandle>
   <updateArray>
      <items>
          <assetHandle>a|450|14|19</assetHandle>
          <fontName>Bookman Old Style Font Name</fontName>
          <postscriptName>Bookman Old Style PostScript</postscriptName>
          <rtfName>Bookman Old Style RTF</rtfName>
          <fontFamily>Bookman Old Style Family</fontFamily>
          <style>BoldItalic</style>
          <typeName>Open Type</typeName><type>OTF</type>
      </items>
   </updateArray>
</batchSetFontFieldsParam>
```

**Réponse**

```java
<batchSetFontFieldsReturn xmlns="http://www.scene7.com/IpsApi/xsd/2009-07-31">
   <successCount>1</successCount>
   <warningCount>0</warningCount>
   <errorCount>0</errorCount>
</batchSetFontFieldsReturn>
```

