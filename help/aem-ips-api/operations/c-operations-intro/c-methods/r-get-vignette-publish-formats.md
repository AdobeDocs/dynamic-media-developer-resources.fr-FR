---
description: 'null'
seo-description: 'null'
seo-title: getVideoPublishFormats
solution: Experience Manager
title: getVideoPublishFormats
topic: Scene7 Image Production System API
uuid: 2cf58002-5c4a-4391-85d4-4a67cb085afa
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# getVideoPublishFormats{#getvignettepublishformats}

Syntaxe

## Types d’utilisateur autorisés {#section-1f5e2f74aef8408e89ed9ccac8b5b9bc}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `TrialSiteAdmin`
* `ImagePortalAdmin`

## Paramètres {#section-ba28150e6d8c4aa0b4ec72451ba7bc71}

**Input (getVideoPublishFormatsParam)**

| Nom | Type | Obligatoire | Description |
|---|---|---|---|
| ` *`companyHandle`*` | `xsd:string` | Oui | La poignée du. |

**Output (getViewettePublishFormatsReturn)**

| Nom | Type | Obligatoire | Description |
|---|---|---|---|
| ` *`vignetteFormatArray`*` | `types:VignettePublishFormatArray` | Oui | Tableau des formats de publication de vignettes. |

## Exemples {#section-2cc32b27cc6243b7b3e273cc05996226}

Cet exemple de code renvoie deux formats de publication de vignettes associés à un  spécifique. Les informations sont renvoyées dans un tableau, qui est tronqué pour être concis.

**Request**

```java
<getVignettePublishFormatsParam xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
   <companyHandle>c|21</companyHandle>
</getVignettePublishFormatsParam>
```

**Réponse**

```java
<getVignettePublishFormatsReturn xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
   <vignetteFormatArray>
      <items>
         <companyHandle>c|21</companyHandle>
         <vignetteFormatHandle>v|21|281</vignetteFormatHandle>
         <name>APIcreateVignettePublishFormat</name>
         ...
      </items>
   </vignetteFormatArray>
</getVignettePublishFormatsReturn>
```

