---
description: Récupère toutes les propriétés système dans une seule requête.
seo-description: Récupère toutes les propriétés système dans une seule requête.
seo-title: getSystemProperties
solution: Experience Manager
title: getSystemProperties
uuid: 08ea86ba-bde5-45a1-920a-04f784395e6a
feature: Dynamic Media Classic, SDK/API
role: Développeur, Administrateur
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '71'
ht-degree: 15%

---


# getSystemProperties{#getsystemproperties}

Récupère toutes les propriétés système dans une seule requête.

Syntaxe

## Types d’utilisateur autorisés {#section-fc311ce90a54400fa95b9dd36b756e23}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`
* `ImagePortalContrib`
* `ImagePortalContribUser`
* `ImagePortalUser`
* `TrialSiteAdmin`
* `TrialSiteUser`

## Paramètres {#section-b2a4fb7068424223aec87c50f0586d73}

**Entrée (getSystemPropertiesParam)**

Aucune

**Output (getSystemPropertiesReturn)**

| Nom | Type | Obligatoire | Description |
|---|---|---|---|
| `*`propertyArray`*` | `types:PropertyArray` | Oui | Tableau de propriétés système. |

## Exemples {#section-728cc16fe9954b2daa035b4d4d4b4ce6}

Cet exemple de code renvoie un tableau de propriétés système. Réponse tronquée pour la brièveté.

**Request**

```java
<getSystemPropertiesParam xmlns="http://www.scene7.com/IpsApi/xsd/2008-09-10"/>
```

**Réponse**

```java
<getSystemPropertiesReturn xmlns="http://www.scene7.com/IpsApi/xsd/2008-09-10"> 
   <propertyArray> 
      <items> 
         <name>SvgRenderEnabled</name> 
         <value>true</value> 
      </items> 
      <items> 
         <name>SwfRootUrl</name> 
         <value>/SWFs/</value> 
      </items> 
      ... 
   </propertyArray> 
</getSystemPropertiesReturn>
```

