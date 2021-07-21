---
description: Supprime un jeu de propriétés et toutes les propriétés associées.
solution: Experience Manager
title: deletePropertySet
feature: Dynamic Media Classic, SDK/API
role: Developer,Admin
exl-id: 72429030-200d-4e13-a537-10a728998a26
source-git-commit: fcda99340a18d5037157723bb3bdca5fa9df3277
workflow-type: tm+mt
source-wordcount: '88'
ht-degree: 12%

---

# deletePropertySet{#deletepropertyset}

Supprime un jeu de propriétés et toutes les propriétés associées.

Syntaxe

## Types d’utilisateurs autorisés {#section-b54aa8c854de400a989b4957412ff42c}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `TrialSiteAdmin`
* `ImagePortalAdmin`

## Paramètres {#section-e5fc868f69494cf6858e03027db09101}

**Entrée (deletePropertySetParam)**

| Nom | Type | Obligatoire | Description |
|---|---|---|---|
| `*`setHandle`*` | `xsd:string` | Oui | La gestion de la propriété à supprimer. |

**Sortie (deletePropertySetParam)**

L’API IPS ne renvoie pas de réponse pour cette opération.

## Exemples {#section-cf319fc8f86a40ab9cbd838b031973fe}

Cet exemple de code utilise la poignée de l’ensemble comme champ dans la balise `deletePropertySetParam` envoyée au serveur des services Web IPS afin de supprimer l’ensemble de propriétés.

**Request**

```java
<deletePropertySetParam xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
   <setHandle>ps|941</setHandle>
</deletePropertySetParam>
```

**Réponse**

Aucune
