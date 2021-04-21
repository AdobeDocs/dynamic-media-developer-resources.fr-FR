---
description: Ajoute un utilisateur à une ou plusieurs sociétés.
solution: Experience Manager
title: addCompanyMembership
feature: Dynamic Media Classic,SDK/API
role: Developer,Administrator
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '90'
ht-degree: 13%

---


# addCompanyMembership{#addcompanymembership}

Ajoute un utilisateur à une ou plusieurs sociétés.

Syntaxe

## Types d’utilisateur autorisés {#section-ae926c7672984be79f6102748accab72}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `TrialSiteAdmin`
* `ImagePortalAdmin`

## Paramètres {#section-0e925b91d63e48aa91f0b0014e6a0cab}

**Entrée (addCompanyMembershipParam)**

| Nom | Type | Obligatoire | Description |
|---|---|---|---|
| `*`userHandle`*` | `xsd:string` | Non | Nom d’utilisateur dont vous souhaitez ajouter l’adhésion. |
| `*`membershipArray`*` | `types:CompanyMembershipUpdateArray` | Oui | Tableau de sociétés auxquelles vous ajoutez l’utilisateur. |

**Output (addCompanyMembershipReturn)**

L&#39;API IPS ne renvoie pas de réponse pour cette opération.

## Exemples {#section-5469f88bac7047cca131faa6b021e437}

Cet exemple utilise `*`companyHandleArray`*` pour ajouter un utilisateur à une seule société.

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
