---
description: Supprime un type de jeu de propriétés, ainsi que le jeu de propriétés et les propriétés qui lui sont associés.
solution: Experience Manager
title: deletePropertySetType
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 97ec0f41-794f-4340-b86d-ab07a742d447
source-git-commit: 77c88d5fe20e048f6fad2bb23cb1abe090793acf
workflow-type: tm+mt
source-wordcount: '93'
ht-degree: 9%

---

# deletePropertySetType{#deletepropertysettype}

Supprime un type de jeu de propriétés, ainsi que le jeu de propriétés et les propriétés qui lui sont associés.

Syntaxe

## Types d’utilisateurs autorisés {#section-16a17b4ebf9a4639bdb2784a2e9fe00d}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `TrialSiteAdmin`
* `ImagePortalAdmin`

## Paramètres {#section-1c8973f5d35f44b4a6a483a41609e455}

**Entrée (deletePropertySetTypeParam)**

| Nom | Type | Obligatoire | Description |
|---|---|---|---|
| typeHandle | `xsd:string` | Oui | La gestion du type de jeu de propriétés à supprimer. |

**Sortie (deletePropertySetTypeParam)**

L’API IPS ne renvoie pas de réponse pour cette opération.

## Exemples {#section-85faa2e3411a4e23aa6489037f7ce078}

Cet exemple de code utilise la poignée du type comme champ dans le `deletePropertySetTypeParam` envoyé au serveur des services Web IPS pour supprimer le type de jeu de propriétés.

**Requête**

```java
<deletePropertySetTypeParam xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
   <typeHandle>pt|10801</typeHandle>
</deletePropertySetTypeParam>
```

**Réponse**

Aucune
