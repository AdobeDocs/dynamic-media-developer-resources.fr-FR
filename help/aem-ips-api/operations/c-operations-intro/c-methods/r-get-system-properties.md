---
description: Récupère toutes les propriétés système dans une seule requête.
solution: Experience Manager
title: getSystemProperties
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: b0ef16fd-1645-4e22-99bb-8c9269623168
TQID: 'https://experienceleague.adobe.com/h-TDyXxJuCL9gRQPTO2bxonLxUgS27L8xh6-2P6I1ZA'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: c66ffd68-0f65-42bb-aa23-b4020f12e0bdid: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: ba0745708154402d9b6c7ebf0554deb366dde11b
workflow-type: tm+mt
source-wordcount: 55
ht-degree: 16%

---

# getSystemProperties{#getsystemproperties}

Récupère toutes les propriétés système dans une seule requête.

Syntaxe

## Types d’utilisateurs autorisés {#section-fc311ce90a54400fa95b9dd36b756e23}

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

**Input (getSystemPropertiesParam)**

Aucune

**Output (getSystemPropertiesReturn)**

| Nom | Type | Obligatoire | Description |
|---|---|---|---|
| propertyArray | `types:PropertyArray` | Oui | Tableau de propriétés système. |

## Exemples {#section-728cc16fe9954b2daa035b4d4d4b4ce6}

Cet exemple de code renvoie un tableau de propriétés système. Réponse tronquée pour des raisons de concision.

**Requête**

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

