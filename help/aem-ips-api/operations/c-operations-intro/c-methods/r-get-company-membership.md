---
description: Obtient l’appartenance d’un utilisateur à un tableau de la société.
solution: Experience Manager
title: getCompanyMembership
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 53af8a97-208c-4c44-93d6-aa36a459af51
source-git-commit: 77c88d5fe20e048f6fad2bb23cb1abe090793acf
workflow-type: tm+mt
source-wordcount: '81'
ht-degree: 16%

---

# getCompanyMembership{#getcompanymembership}

Obtient l’appartenance d’un utilisateur à un tableau de la société.

Syntaxe

## Types d’utilisateurs autorisés {#section-f8bba547e1f648648be99dc48fd72b5d}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `TrialSiteAdmin`
* `ImagePortalAdmin`
* `TrialSiteUser`
* `ImagePortalAdmin`
* `ImagePortalUser`
* `ImagePortalContrib`
* `ImagePortalContribUser`

## Paramètres {#section-8745c360c3e1400a88e9bdb26bcb93de}

**Input (getCompanyMembershipParam)**

| Nom | Type | Obligatoire | Description |
|---|---|---|---|
| Poignée utilisateur | `xsd:string` | Non | Handle destiné à l’utilisateur dont vous souhaitez obtenir les appartenances. |

**Output (getCompanyMembershipReturn)**

| Nom | Type | Obligatoire | Description |
|---|---|---|---|
| Tableau d’adhérents | `types:CompanyMembershipArray` | Oui | Gamme d’adhésions d’entreprise. |

## Exemples {#section-e4958d104ea344a4a79f57d07b46eba7}

Cet exemple de code prend un pseudonyme d’utilisateur et obtient toutes les appartenances d’entreprise de l’utilisateur dans un tableau. La réponse a été tronquée par souci de concision.

**Demander**

```java
<ns1:getCompanyMembershipParam xmlns:ns1="http://www.scene7.com/IpsApi/xsd">
   <ns1:userHandle>70|kmagnusson@adobe.com</ns1:userHandle>
</ns1:getCompanyMembershipParam>
```

**Réponse**

```java
<getCompanyMembershipReturn xmlns="http://www.scene7.com/IpsApi/xsd">
   <membershipArray>
      <items>
         <companyHandle>48</companyHandle>
         <name>AIR</name>
         <rootPath>AIR/</rootPath>
         <expires>2101-01-31T23:00:00.485-08:00</expires>
      </items>
      ...
    </membershipArray>
</getCompanyMembershipReturn>
```
