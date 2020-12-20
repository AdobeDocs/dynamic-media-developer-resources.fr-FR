---
description: Supprime un type de jeu de propriétés et son jeu de propriétés et ses propriétés associés.
seo-description: Supprime un type de jeu de propriétés et son jeu de propriétés et ses propriétés associés.
seo-title: deletePropertySetType
solution: Experience Manager
title: deletePropertySetType
topic: Scene7 Image Production System API
uuid: 7a5232cc-fa3a-4dac-bf88-8b954dd37c87
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '106'
ht-degree: 10%

---


# deletePropertySetType{#deletepropertysettype}

Supprime un type de jeu de propriétés et son jeu de propriétés et ses propriétés associés.

Syntaxe

## Types d’utilisateur autorisés {#section-16a17b4ebf9a4639bdb2784a2e9fe00d}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `TrialSiteAdmin`
* `ImagePortalAdmin`

## Paramètres {#section-1c8973f5d35f44b4a6a483a41609e455}

**Entrée (deletePropertySetTypeParam)**

| Nom | Type | Obligatoire | Description |
|---|---|---|---|
| ` *`typeHandle`*` | `xsd:string` | Oui | Poignée du type de jeu de propriétés à supprimer. |

**Output (deletePropertySetTypeParam)**

L&#39;API IPS ne renvoie pas de réponse pour cette opération.

## Exemples {#section-85faa2e3411a4e23aa6489037f7ce078}

Cet exemple de code utilise l&#39;identificateur du type comme champ dans le `deletePropertySetTypeParam` envoyé au serveur de services Web IPS afin de supprimer le type de jeu de propriétés.

**Request**

```java
<deletePropertySetTypeParam xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
   <typeHandle>pt|10801</typeHandle>
</deletePropertySetTypeParam>
```

**Réponse**

Aucune
