---
description: Supprime un utilisateur d’une ou de plusieurs sociétés.
solution: Experience Manager
title: removeCompanyMembership
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 1cb9a286-48a0-4542-a80a-c97fd973474e
TQID: 'https://experienceleague.adobe.com/5jjL8MnUtL046oSej3HErZB9hrD-ueEBC5-h9vD92HM'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: ba0745708154402d9b6c7ebf0554deb366dde11b
workflow-type: tm+mt
source-wordcount: 100
ht-degree: 10%

---

# removeCompanyMembership{#removecompanymembership}

Supprime un utilisateur d’une ou de plusieurs sociétés.

Syntaxe

## Types d’utilisateurs autorisés {#section-e9a16c8a7d8d4845989a1488c9ca9c98}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `TrialSiteAdmin`
* `ImagePortalAdmin`

## Paramètres {#section-6dfce5e44d8a4799afd0c231a0b10463}

**Input (removeCompanyMembershipParam)**

| Nom | Type | Obligatoire | Description |
|---|---|---|---|
| userHandle | `xsd:string` | Non | La poignée de l’utilisateur avec l’abonnement que vous souhaitez supprimer. |
| companyHandleArray | `types:HandleArray` | Oui | Poignée de la société dont vous supprimez l’utilisateur. |

**Output (removeCompanyMembershipReturn)**

L’API IPS ne renvoie pas de réponse pour cette opération.

## Exemples {#section-6b7903195e8647a1bd0502f87387ca62}

Cet exemple de code supprime un utilisateur d’une entreprise. Omettez le handle d’utilisateur facultatif pour supprimer tous les utilisateurs des sociétés spécifiées dans le tableau handle d’entreprise .

**Requête**

```java
<ns1:removeCompanyMembershipParam xmlns:ns1="http://www.scene7.com/IpsApi/xsd">
   <ns1:userHandle>621|jduvar@adobe.com</ns1:userHandle>
   <ns1:companyHandleArray>
      <ns1:items>47</ns1:items>
   </ns1:companyHandleArray>
</ns1:removeCompanyMembershipParam>
```

**Réponse**

Aucune

