---
description: Supprime un groupe.
solution: Experience Manager
title: deleteGroup
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 0de188de-b4b6-4f48-9918-bcf962fa9482
source-git-commit: 77c88d5fe20e048f6fad2bb23cb1abe090793acf
workflow-type: tm+mt
source-wordcount: '86'
ht-degree: 11%

---

# deleteGroup{#deletegroup}

Supprime un groupe.

Syntaxe

## Types d’utilisateurs autorisés {#section-ebcc67723663494db0562275b1873460}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`

## Paramètres {#section-42775102ec724c36ae5241eea1a00b8e}

**Entrée (deleteGroupParam)**

| Nom | Type | Obligatoire | Description |
|---|---|---|---|
| companyHandle | `xsd:string` | Oui | Gestionnaire de la société qui appartient au groupe que vous souhaitez supprimer. |
| groupHandle | `xsd:string` | Oui | Gestionnaire du groupe que vous souhaitez supprimer. |

**Output (deleteGroupParam)**

L’API IPS ne renvoie pas de réponse pour cette opération.

## Exemples {#section-8f8501af3b3348a1b5701cf9622bf6e4}

Cet exemple de code supprime un groupe d’une société. Elle nécessite un gestionnaire de groupe, que vous devez obtenir d’une autre opération.

**Requête**

```java
<ns1:deleteGroupParam xmlns:ns1="http://www.scene7.com/IpsApi/xsd">
   <ns1:companyHandle>47</ns1:companyHandle>
   <ns1:groupHandle>241</ns1:groupHandle>
</ns1:deleteGroupParam>
```

**Réponse**

Aucune
