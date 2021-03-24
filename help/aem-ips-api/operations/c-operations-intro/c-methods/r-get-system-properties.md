---
description: Récupère toutes les propriétés système dans une seule requête.
solution: Experience Manager
title: getSystemProperties
feature: Dynamic Media Classic, SDK/API
role: Développeur, Administrateur
translation-type: tm+mt
source-git-commit: 052bfcbcf1bd4ccf60afa7e3325bf58dd07cba85
workflow-type: tm+mt
source-wordcount: '62'
ht-degree: 17%

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

