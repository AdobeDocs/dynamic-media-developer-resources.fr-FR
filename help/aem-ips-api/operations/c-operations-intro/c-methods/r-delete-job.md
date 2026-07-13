---
description: Supprime une tâche en cours ou planifiée.
solution: Experience Manager
title: deleteJob
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: d38dd1e2-668e-4956-b854-54bf466d6d45
TQID: 'https://experienceleague.adobe.com/rcnHChrY2u5J1-ipPlJ7JilCfbsTHDNDHhqJlLZuWIQ'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
topic_v2:
  - id: bce87dde-a4ab-44c9-8a18-ad66e4ddb377
source-git-commit: ba0745708154402d9b6c7ebf0554deb366dde11b
workflow-type: tm+mt
source-wordcount: 90
ht-degree: 11%

---

# deleteJob{#deletejob}

Supprime une tâche en cours ou planifiée.

Syntaxe

## Types d’utilisateurs autorisés {#section-1b959679dc8147c291126ddf7e061742}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `TrialSiteAdmin`
* `TrialSiteUser`
* `ImagePortalAdmin`
* `ImagePortalContrib`
* `ImagePortalContribUser`

## Paramètres {#section-000c42bc93744b1a8e777f3ec3c272b0}

**Input (deleteJobParam)**

| Nom | Type | Obligatoire | Description |
|---|---|---|---|
| companyHandle | `xsd:string` | Oui | Identifiant de la société à laquelle appartient la tâche. |
| jobHandle | `xsd:string` | Oui | Poignée de la tâche à supprimer. |

**Output**

L’API IPS ne renvoie pas de réponse pour cette opération.

## Exemples {#section-732d21d4dad04337b7a5ae1a0cc00eba}

Cet exemple de code supprime une tâche en cours d’exécution ou planifiée dans IPS. Elle nécessite une gestion de tâche, que vous devez obtenir à partir d’une autre opération.

**Requête**

```java
<deleteJobParam xmlns="http://www.scene7.com/IpsApi/xsd">
   <companyHandle>47</companyHandle>
   <jobHandle>47|My Test Job|</jobHandle>
</deleteJobParam>
```

**Réponse**

Aucune

