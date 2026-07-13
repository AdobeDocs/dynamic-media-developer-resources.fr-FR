---
description: Supprime un groupe.
solution: Experience Manager
title: deleteGroup
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 0de188de-b4b6-4f48-9918-bcf962fa9482
TQID: 'https://experienceleague.adobe.com/skfJjk-dexrQR94ImWtaWV-1hkPmvrlFVn-EyA5mKtQ'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: c66ffd68-0f65-42bb-aa23-b4020f12e0bdid: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: ba0745708154402d9b6c7ebf0554deb366dde11b
workflow-type: tm+mt
source-wordcount: 86
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

**Input (deleteGroupParam)**

| Nom | Type | Obligatoire | Description |
|---|---|---|---|
| companyHandle | `xsd:string` | Oui | Identifiant de la société qui appartient au groupe que vous souhaitez supprimer. |
| groupHandle | `xsd:string` | Oui | Gestionnaire du groupe que vous souhaitez supprimer. |

**Output (deleteGroupParam)**

L’API IPS ne renvoie pas de réponse pour cette opération.

## Exemples {#section-8f8501af3b3348a1b5701cf9622bf6e4}

Cet exemple de code supprime un groupe d’une entreprise. Elle nécessite un handle de groupe, que vous devez obtenir à partir d&#39;une autre opération.

**Requête**

```java
<ns1:deleteGroupParam xmlns:ns1="http://www.scene7.com/IpsApi/xsd">
   <ns1:companyHandle>47</ns1:companyHandle>
   <ns1:groupHandle>241</ns1:groupHandle>
</ns1:deleteGroupParam>
```

**Réponse**

Aucune

