---
description: Supprime une zone cliquable.
solution: Experience Manager
title: deleteImageMap
feature: Dynamic Media Classic, SDK/API
role: Developer,Admin
exl-id: f9942a4a-d258-4e2a-8910-44fa502d97bd
source-git-commit: fcda99340a18d5037157723bb3bdca5fa9df3277
workflow-type: tm+mt
source-wordcount: '98'
ht-degree: 12%

---

# deleteImageMap{#deleteimagemap}

Supprime une zone cliquable.

Syntaxe

## Types d’utilisateurs autorisés {#section-41fd188af16a40d4b07923165bcf15d8}

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
| `*`companyHandle`*` | `xsd:string` | Oui | Gestionnaire de la société qui contient la zone cliquable à supprimer. |
| `*`imageMapHandle`*` | `xsd:string` | Oui | Poignée de la zone cliquable à supprimer. |

**Sortie (deleteImageMapParam)**

L’API IPS ne renvoie pas de réponse pour cette opération.

## Exemples {#section-b238da3332fb4e3eb3f8bda0bd6a2035}

Cet exemple de code supprime une zone cliquable d’une société. Vous devez obtenir la gestion de la zone cliquable à partir d’une autre opération.

**Request**

```java
<deleteImageMapParam xmlns="http://www.scene7.com/IpsApi/xsd">
   <companyHandle>47</companyHandle>
   <imageMapHandle>34191|8|554</imageMapHandle>
</deleteImageMapParam>
```

**Réponse**

Aucun
