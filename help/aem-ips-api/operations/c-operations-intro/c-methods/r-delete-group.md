---
description: Supprime un groupe.
seo-description: Supprime un groupe.
seo-title: deleteGroup
solution: Experience Manager
title: deleteGroup
topic: Scene7 Image Production System API
uuid: 04934b16-b7ef-4657-9f63-c91fcc741ca4
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '90'
ht-degree: 13%

---


# deleteGroup{#deletegroup}

Supprime un groupe.

Syntaxe

## Types d’utilisateur autorisés {#section-ebcc67723663494db0562275b1873460}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`

## Paramètres {#section-42775102ec724c36ae5241eea1a00b8e}

**Entrée (deleteGroupParam)**

| Nom | Type | Obligatoire | Description |
|---|---|---|---|
| ` *`companyHandle`*` | `xsd:string` | Oui | Identifiant de la société qui appartient au groupe que vous souhaitez supprimer. |
| ` *`groupHandle`*` | `xsd:string` | Oui | Identifiant du groupe à supprimer. |

**Output (deleteGroupParam)**

L&#39;API IPS ne renvoie pas de réponse pour cette opération.

## Exemples {#section-8f8501af3b3348a1b5701cf9622bf6e4}

Cet exemple de code supprime un groupe d&#39;une société. Il nécessite un descripteur de groupe, que vous devez obtenir d&#39;une autre opération.

**Request**

```java
<ns1:deleteGroupParam xmlns:ns1="http://www.scene7.com/IpsApi/xsd">
   <ns1:companyHandle>47</ns1:companyHandle>
   <ns1:groupHandle>241</ns1:groupHandle>
</ns1:deleteGroupParam>
```

**Réponse**

Aucune
