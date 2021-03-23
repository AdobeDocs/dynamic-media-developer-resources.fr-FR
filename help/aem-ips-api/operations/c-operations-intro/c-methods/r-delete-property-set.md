---
description: Supprime un jeu de propriétés et toutes les propriétés associées.
seo-description: Supprime un jeu de propriétés et toutes les propriétés associées.
seo-title: deletePropertySet
solution: Experience Manager
title: deletePropertySet
uuid: b4fdf51f-89ec-4a69-9179-078ee8e1937f
feature: Dynamic Media Classic, SDK/API
role: Développeur, Administrateur
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '99'
ht-degree: 11%

---


# deletePropertySet{#deletepropertyset}

Supprime un jeu de propriétés et toutes les propriétés associées.

Syntaxe

## Types d’utilisateur autorisés {#section-b54aa8c854de400a989b4957412ff42c}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `TrialSiteAdmin`
* `ImagePortalAdmin`

## Paramètres {#section-e5fc868f69494cf6858e03027db09101}

**Entrée (deletePropertySetParam)**

| Nom | Type | Obligatoire | Description |
|---|---|---|---|
| `*`setHandle`*` | `xsd:string` | Oui | Poignée de la propriété à supprimer. |

**Output (deletePropertySetParam)**

L&#39;API IPS ne renvoie pas de réponse pour cette opération.

## Exemples {#section-cf319fc8f86a40ab9cbd838b031973fe}

Cet exemple de code utilise le nom d&#39;utilisateur de la visionneuse comme champ dans le `deletePropertySetParam` envoyé au serveur de services Web IPS pour supprimer la visionneuse de propriétés.

**Request**

```java
<deletePropertySetParam xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
   <setHandle>ps|941</setHandle>
</deletePropertySetParam>
```

**Réponse**

Aucune
