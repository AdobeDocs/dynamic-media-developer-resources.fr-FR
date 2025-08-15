---
description: Supprime un groupe.
solution: Experience Manager
title: supprimer le groupe
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 0de188de-b4b6-4f48-9918-bcf962fa9482
source-git-commit: 77c88d5fe20e048f6fad2bb23cb1abe090793acf
workflow-type: tm+mt
source-wordcount: '86'
ht-degree: 11%

---

# supprimer le groupe{#deletegroup}

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
| CompanyHandle | `xsd:string` | Oui | Identifiant de l’entreprise appartenant au groupe que vous souhaitez supprimer. |
| Poignée de groupe | `xsd:string` | Oui | Poignée du groupe à supprimer. |

**Output (deleteGroupParam)**

L’API IPS ne renvoie pas de réponse pour cette opération.

## Exemples {#section-8f8501af3b3348a1b5701cf9622bf6e4}

Cet exemple de code supprime un groupe d’une société. Elle nécessite un descripteur de groupe, que vous devez obtenir à partir d’une autre opération.

**Demander**

```java
<ns1:deleteGroupParam xmlns:ns1="http://www.scene7.com/IpsApi/xsd">
   <ns1:companyHandle>47</ns1:companyHandle>
   <ns1:groupHandle>241</ns1:groupHandle>
</ns1:deleteGroupParam>
```

**Réponse**

Aucune
