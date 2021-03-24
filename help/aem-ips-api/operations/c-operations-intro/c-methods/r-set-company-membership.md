---
description: Définit l’appartenance d’un utilisateur à une ou plusieurs sociétés.
solution: Experience Manager
title: setCompanyMembership
feature: Dynamic Media Classic, SDK/API
role: Développeur, Administrateur
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '83'
ht-degree: 14%

---


# setCompanyMembership{#setcompanymembership}

Définit l’appartenance d’un utilisateur à une ou plusieurs sociétés.

Syntaxe

## Types d’utilisateur autorisés {#section-0cbcc78cfee64c2baf66f29cce6d0a65}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `TrialSiteAdmin`
* `ImagePortalAdmin`

## Paramètres {#section-3930dc6a016140178631083563598104}

**Entrée (setCompanyMembershipParam)**

| Nom | Type | Obligatoire | Description |
|---|---|---|---|
| `*`userHandle`*` | `xsd:sting` | Non | Identifiant utilisateur. |
| `*`membershipArray`*` | `types:CompanyMembershipUpdateArray` | Oui | Tableau de sociétés. |

**Output (setCompanyMembershipParam)**

L&#39;API IPS ne renvoie pas de réponse pour cette opération.

## Exemples {#section-862c0cc32ce0407ab248028e690a8386}

Cet exemple de code ajoute un utilisateur à une société. Si nécessaire, spécifiez plusieurs sociétés dans le tableau des poignées de société.

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
