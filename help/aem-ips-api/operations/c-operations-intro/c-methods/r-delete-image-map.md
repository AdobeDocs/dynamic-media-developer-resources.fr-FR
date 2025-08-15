---
description: Supprime une zone cliquable
solution: Experience Manager
title: deleteImageMap
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: f9942a4a-d258-4e2a-8910-44fa502d97bd
source-git-commit: 77c88d5fe20e048f6fad2bb23cb1abe090793acf
workflow-type: tm+mt
source-wordcount: '93'
ht-degree: 10%

---

# deleteImageMap{#deleteimagemap}

Supprime une zone cliquable

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
>L’utilisateur doit disposer d’un accès en lecture et écriture à la ressource.

## Paramètres {#section-28de12bab79045a5977c68855e37ae3d}

**Input (deleteImageMapParam)**

| Nom | Type | Obligatoire | Description |
|---|---|---|---|
| companyHandle | `xsd:string` | Oui | Descripteur de la société contenant la zone cliquable à supprimer. |
| imageMapHandle | `xsd:string` | Oui | Poignée de la zone cliquable à supprimer. |

**Output (deleteImageMapParam)**

L’API IPS ne renvoie pas de réponse pour cette opération.

## Exemples {#section-b238da3332fb4e3eb3f8bda0bd6a2035}

Cet exemple de code supprime une zone cliquable d’une entreprise. Vous devez obtenir l’identificateur de zone cliquable à partir d’une autre opération.

**Requête**

```java
<deleteImageMapParam xmlns="http://www.scene7.com/IpsApi/xsd">
   <companyHandle>47</companyHandle>
   <imageMapHandle>34191|8|554</imageMapHandle>
</deleteImageMapParam>
```

**Réponse**

Aucun
