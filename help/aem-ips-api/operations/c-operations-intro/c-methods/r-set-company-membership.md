---
description: Définit l’appartenance d’un utilisateur à une ou plusieurs sociétés.
solution: Experience Manager
title: setCompanyMembership
feature: Dynamic Media Classic, SDK/API
role: Developer,Admin
exl-id: 43144c75-1d83-4e1d-8319-c3275d349a2f
source-git-commit: fcda99340a18d5037157723bb3bdca5fa9df3277
workflow-type: tm+mt
source-wordcount: '81'
ht-degree: 14%

---

# setCompanyMembership{#setcompanymembership}

Définit l’appartenance d’un utilisateur à une ou plusieurs sociétés.

Syntaxe

## Types d’utilisateurs autorisés {#section-0cbcc78cfee64c2baf66f29cce6d0a65}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `TrialSiteAdmin`
* `ImagePortalAdmin`

## Paramètres {#section-3930dc6a016140178631083563598104}

**Entrée (setCompanyMembershipParam)**

| Nom | Type | Obligatoire | Description |
|---|---|---|---|
| `*`userHandle`*` | `xsd:sting` | Non | Identifiant utilisateur. |
| `*`membershipArray`*` | `types:CompanyMembershipUpdateArray` | Oui | Tableau d&#39;entreprises. |

**Sortie (setCompanyMembershipParam)**

L’API IPS ne renvoie pas de réponse pour cette opération.

## Exemples {#section-862c0cc32ce0407ab248028e690a8386}

Cet exemple de code ajoute un utilisateur à une société. Si nécessaire, indiquez plusieurs sociétés dans le tableau de gestion de l’entreprise.

**Request**

```java
<ns1:setCompanyMembershipParam xmlns:ns1="http://www.scene7.com/IpsApi/xsd">
   <ns1:userHandle>3341|juser@scene7.com</ns1:userHandle>
   <ns1:companyHandleArray>
      <ns1:items>137</ns1:items>
   </ns1:companyHandleArray>
</ns1:setCompanyMembershipParam>
```

**Réponse**

Aucune
