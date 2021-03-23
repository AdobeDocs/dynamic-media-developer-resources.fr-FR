---
description: Supprime une zone cliquable.
seo-description: Supprime une zone cliquable.
seo-title: deleteImageMap
solution: Experience Manager
title: deleteImageMap
uuid: 0abdf72c-f445-41d0-bd88-63b7ad1359d5
feature: Dynamic Media Classic, SDK/API
role: Développeur, Administrateur
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '105'
ht-degree: 11%

---


# deleteImageMap{#deleteimagemap}

Supprime une zone cliquable.

Syntaxe

## Types d’utilisateur autorisés {#section-41fd188af16a40d4b07923165bcf15d8}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`
* `ImagePortalContrib`
* `ImagePortalContribUser`

>[!NOTE]
>
>L’utilisateur doit disposer d’un accès en lecture et en écriture à la ressource.

## Paramètres {#section-28de12bab79045a5977c68855e37ae3d}

**Entrée (deleteImageMapParam)**

| Nom | Type | Obligatoire | Description |
|---|---|---|---|
| `*`companyHandle`*` | `xsd:string` | Oui | Poignée de la société contenant la zone cliquable à supprimer. |
| `*`imageMapHandle`*` | `xsd:string` | Oui | Poignée de la zone cliquable à supprimer. |

**Output (deleteImageMapParam)**

L&#39;API IPS ne renvoie pas de réponse pour cette opération.

## Exemples {#section-b238da3332fb4e3eb3f8bda0bd6a2035}

Cet exemple de code supprime une zone cliquable d’une société. Vous devez obtenir la poignée de zone cliquable à partir d’une autre opération.

**Request**

```java
<deleteImageMapParam xmlns="http://www.scene7.com/IpsApi/xsd">
   <companyHandle>47</companyHandle>
   <imageMapHandle>34191|8|554</imageMapHandle>
</deleteImageMapParam>
```

**Réponse**

Aucun
