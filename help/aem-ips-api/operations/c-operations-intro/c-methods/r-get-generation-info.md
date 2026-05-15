---
description: Renvoie 2 types d’informations différents en fonction des paramètres transmis. originatorHandle renvoie des informations sur les ressources générées à partir de la ressource spécifiée. generateHandle renvoie des informations sur les étapes utilisées pour générer la ressource ou le fichier spécifié.
solution: Experience Manager
title: getGenerationInfo
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: fa098e3c-8145-4238-a84c-c545f1c53341
TQID: 'https://experienceleague.adobe.com/MA0SJinQzPjDFkSXVRhH2e7A3Ry6HXoW--K-elv028M'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: c66ffd68-0f65-42bb-aa23-b4020f12e0bdid: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 198
ht-degree: 9%

---

# getGenerationInfo{#getgenerationinfo}

Renvoie 2 types d’informations différents en fonction des paramètres transmis. originatorHandle renvoie des informations sur les ressources générées à partir de la ressource spécifiée. generateHandle renvoie des informations sur les étapes utilisées pour générer la ressource ou le fichier spécifié.

Syntaxe

## Types d’utilisateurs autorisés {#section-9cc2216b32c74107be07aeacecc11401}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `TrialSiteAdmin`
* `TrialSiteUser`
* `ImagePortalAdmin`
* `ImagePortalUser`
* `ImagePortalContrib`
* `ImagePortalContribUser`

## Paramètres {#section-b7fa94c82147455888e8469fa5f6922b}

**Input (getGenerationInfoParam)**

| Nom | Type | Obligatoire | Description |
|---|---|---|---|
| Expression de code | `xsd:string` | Oui | La poignée de la société. |
| Expression de code | `xsd:string` | Non | Moteur utilisé pour la génération. Voir Styles de polices. |
| Expression de code | `xsd:string` | Non | Descripteur de la ressource à interroger pour les ressources générées. |
| Expression de code | `xsd:string` | Non | Le handle de la ressource pour interroger les ressources et les moteurs utilisés dans sa génération. |
| Expression de code | `xsd:StringArray` | Non | Propriétés incluses dans l’opération. |
| Expression de code | `xsd:StringArray` | Non | Propriétés exclues de l’opération. |

**Output (getGenerationInfoReturn)**

| Nom | Type | Obligatoire | Description |
|---|---|---|---|
| generateArray | `types:GenerationInfoArray` | Oui | Tableau d’informations de génération. |

## Exemples {#section-fdffe6ed82d94c7aa90e47f7ce889403}

Cet exemple de code renvoie des informations sur les ressources générées à partir d’une ressource spécifique. Elle ne récupère pas d’informations sur les étapes utilisées pour générer la ressource spécifiée. La réponse est tronquée à des fins de concision.

**Requête**

```java
<getGenerationInfoParam xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
   <companyHandle>c|6</companyHandle>
   <originatorHandle>a|716|25|160</originatorHandle>
</getGenerationInfoParam>
```

**Réponse**

```java
<getGenerationInfoReturn xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
   <generationArray>
      <items>
         <engine>PostScriptRip</engine>
         <originator>
         ...
         </generated>
         <attributeArray/>
      </items>
   </generationArray>
</getGenerationInfoReturn>
```
