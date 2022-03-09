---
description: Ajoute un utilisateur à une ou plusieurs sociétés.
solution: Experience Manager
title: addCompanyMembership
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 6efef4fb-f2e5-4c41-b739-a36ac2f17884
source-git-commit: 77c88d5fe20e048f6fad2bb23cb1abe090793acf
workflow-type: tm+mt
source-wordcount: '83'
ht-degree: 14%

---

# addCompanyMembership{#addcompanymembership}

Ajoute un utilisateur à une ou plusieurs sociétés.

Syntaxe

## Types d’utilisateurs autorisés {#section-ae926c7672984be79f6102748accab72}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `TrialSiteAdmin`
* `ImagePortalAdmin`

## Paramètres {#section-0e925b91d63e48aa91f0b0014e6a0cab}

**Entrée (addCompanyMembershipParam)**

| Nom | Type | Obligatoire | Description |
|---|---|---|---|
| userHandle | `xsd:string` | Non | Gestionnaire de l’utilisateur dont vous souhaitez ajouter l’adhésion. |
| membershipArray | `types:CompanyMembershipUpdateArray` | Oui | Un ensemble d’entreprises auxquelles vous ajoutez l’utilisateur. |

**Sortie (addCompanyMembershipReturn)**

L’API IPS ne renvoie pas de réponse pour cette opération.

## Exemples {#section-5469f88bac7047cca131faa6b021e437}

Cet exemple utilise companyHandleArray pour ajouter un utilisateur à une seule société.

**Request**

```java
<ns1:addCompanyMembershipParam xmlns:ns1="http://www.scene7.com/IpsApi/xsd">
   <ns1:userHandle>621|jduvar@adobe.com</ns1:userHandle>
   <ns1:companyHandleArray>
      </ns1:items>47</ns1:items>
   </ns1:companyHandleArray>
</ns1:addCompanyMembershipParam>
```

**Réponse**

Aucune
