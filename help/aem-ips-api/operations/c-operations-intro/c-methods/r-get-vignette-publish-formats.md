---
description: getVideoPublishFormats
solution: Experience Manager
title: getVideoPublishFormats
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 6e56d68e-b5cf-4044-9c58-f8221fa4490f
source-git-commit: 77c88d5fe20e048f6fad2bb23cb1abe090793acf
workflow-type: tm+mt
source-wordcount: '61'
ht-degree: 21%

---

# getVideoPublishFormats{#getvignettepublishformats}

Syntaxe

## Types d’utilisateurs autorisés {#section-1f5e2f74aef8408e89ed9ccac8b5b9bc}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `TrialSiteAdmin`
* `ImagePortalAdmin`

## Paramètres {#section-ba28150e6d8c4aa0b4ec72451ba7bc71}

**Entrée (getVignettePublishFormatsParam)**

| Nom | Type | Obligatoire | Description |
|---|---|---|---|
| companyHandle | `xsd:string` | Oui | La poignée de la société. |

**Sortie (getVignettePublishFormatsReturn)**

| Nom | Type | Obligatoire | Description |
|---|---|---|---|
| vignetteFormatArray | `types:VignettePublishFormatArray` | Oui | Tableau des formats de publication de vignettes. |

## Exemples {#section-2cc32b27cc6243b7b3e273cc05996226}

Cet exemple de code renvoie deux formats de publication de vignettes associés à une société spécifique. Les informations sont renvoyées dans un tableau, qui est tronqué pour plus de concision.

**Requête**

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
