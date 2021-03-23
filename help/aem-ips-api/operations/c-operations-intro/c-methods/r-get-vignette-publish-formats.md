---
description: getVignettePublishFormats
solution: Experience Manager
title: getVignettePublishFormats
uuid: 2cf58002-5c4a-4391-85d4-4a67cb085afa
feature: Dynamic Media Classic, SDK/API
role: Développeur, Administrateur
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '68'
ht-degree: 22%

---


# getVignettePublishFormats{#getvignettepublishformats}

Syntaxe

## Types d&#39;utilisateur autorisés {#section-1f5e2f74aef8408e89ed9ccac8b5b9bc}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `TrialSiteAdmin`
* `ImagePortalAdmin`

## Paramètres {#section-ba28150e6d8c4aa0b4ec72451ba7bc71}

**Entrée (getVignettePublishFormatsParam)**

| Nom | Type | Obligatoire | Description |
|---|---|---|---|
| `*`companyHandle`*` | `xsd:string` | Oui | La poignée de la société. |

**Output (getVignettePublishFormatsReturn)**

| Nom | Type | Obligatoire | Description |
|---|---|---|---|
| `*`vignetteFormatArray`*` | `types:VignettePublishFormatArray` | Oui | Tableau des formats de publication de vignettes. |

## Exemples {#section-2cc32b27cc6243b7b3e273cc05996226}

Cet exemple de code renvoie deux formats de publication de vignettes associés à une société spécifique. Les informations sont renvoyées dans un tableau, tronqué pour être concis.

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

