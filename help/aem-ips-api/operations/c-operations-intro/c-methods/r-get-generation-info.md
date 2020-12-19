---
description: Renvoie 2 types d’informations différents en fonction des paramètres transmis. originatorHandle renvoie des informations sur les ressources générées à partir de la ressource spécifiée. generateHandle renvoie des informations sur les étapes utilisées pour générer la ressource ou le fichier spécifié.
seo-description: Renvoie 2 types d’informations différents en fonction des paramètres transmis. originatorHandle renvoie des informations sur les ressources générées à partir de la ressource spécifiée. generateHandle renvoie des informations sur les étapes utilisées pour générer la ressource ou le fichier spécifié.
seo-title: getGenerationInfo
solution: Experience Manager
title: getGenerationInfo
topic: Scene7 Image Production System API
uuid: 4310a702-c08b-4479-9f57-9f2bc1d6b032
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '231'
ht-degree: 8%

---


# getGenerationInfo{#getgenerationinfo}

Renvoie 2 types d’informations différents en fonction des paramètres transmis. originatorHandle renvoie des informations sur les ressources générées à partir de la ressource spécifiée. generateHandle renvoie des informations sur les étapes utilisées pour générer la ressource ou le fichier spécifié.

Syntaxe

## Types d’utilisateur autorisés {#section-9cc2216b32c74107be07aeacecc11401}

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

**Entrée (getGenerationInfoParam)**

| Nom | Type | Obligatoire | Description |
|---|---|---|---|
| ` *`Expression de code`*` | `xsd:string` | Oui | La poignée de la société. |
| ` *`Expression de code`*` | `xsd:string` | Non | Moteur utilisé dans la génération. Voir Styles des polices. |
| ` *`Expression de code`*` | `xsd:string` | Non | Poignée de la ressource à requête pour les ressources générées. |
| ` *`Expression de code`*` | `xsd:string` | Non | Poignée de la ressource à la requête pour les ressources et les moteurs utilisés dans sa génération. |
| ` *`Expression de code`*` | `xsd:StringArray` | Non | Propriétés incluses dans l’opération. |
| ` *`Expression de code`*` | `xsd:StringArray` | Non | Propriétés exclues de l’opération. |

**Output (getGenerationInfoReturn)**

| Nom | Type | Obligatoire | Description |
|---|---|---|---|
| ` *`generateArray`*` | `types:GenerationInfoArray` | Oui | Tableau des informations de génération. |

## Exemples {#section-fdffe6ed82d94c7aa90e47f7ce889403}

Cet exemple de code renvoie des informations sur les ressources générées à partir d’une ressource spécifique. Il ne récupère pas les informations sur les étapes utilisées pour générer la ressource spécifiée. La réponse est tronquée pour la brièveté.

**Request**

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

