---
description: Renvoie 2 types d’informations différents en fonction des paramètres transmis. originatorHandle renvoie des informations sur les ressources générées à partir de la ressource spécifiée. generateHandle renvoie des informations sur les étapes utilisées pour générer la ressource ou le fichier spécifié.
solution: Experience Manager
title: getGenerationInfo
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: fa098e3c-8145-4238-a84c-c545f1c53341
source-git-commit: 77c88d5fe20e048f6fad2bb23cb1abe090793acf
workflow-type: tm+mt
source-wordcount: '198'
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
| Expression de code | `xsd:string` | Oui | La poignée de l’entreprise. |
| Code Phrase | `xsd:string` | Non | Le moteur utilisé dans la génération. Voir Styles de police. |
| Code Phrase | `xsd:string` | Non | Handle de la ressource à interroger pour les ressources générées. |
| Code Phrase | `xsd:string` | Non | Le handle de la ressource pour interroger les ressources et les moteurs utilisés dans sa génération. |
| Code Phrase | `xsd:StringArray` | Non | Propriétés incluses dans l’opération. |
| Code Phrase | `xsd:StringArray` | Non | Propriétés exclues de l’opération. |

**Output (getGenerationInfoReturn)**

| Nom | Type | Obligatoire | Description |
|---|---|---|---|
| Tableau de génération | `types:GenerationInfoArray` | Oui | Tableau d’informations sur la génération. |

## Exemples {#section-fdffe6ed82d94c7aa90e47f7ce889403}

Cet exemple de code renvoie des informations sur les ressources générées à partir d’une ressource spécifique. Il ne récupère pas d’informations sur les étapes utilisées pour générer la ressource spécifiée. La réponse est tronquée par souci de concision.

**Demander**

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
