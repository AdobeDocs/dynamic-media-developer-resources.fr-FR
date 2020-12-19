---
description: Récupère les adhésions d’un utilisateur dans un tableau de sociétés.
seo-description: Récupère les adhésions d’un utilisateur dans un tableau de sociétés.
seo-title: getCompanyMembership
solution: Experience Manager
title: getCompanyMembership
topic: Scene7 Image Production System API
uuid: fb3dfe29-4292-4ab2-8015-36c4930a9c05
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '90'
ht-degree: 16%

---


# getCompanyMembership{#getcompanymembership}

Récupère les adhésions d’un utilisateur dans un tableau de sociétés.

Syntaxe

## Types d’utilisateur autorisés {#section-f8bba547e1f648648be99dc48fd72b5d}

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

**Entrée (getCompanyMembershipParam)**

| Nom | Type | Obligatoire | Description |
|---|---|---|---|
| ` *`userHandle`*` | `xsd:string` | Non | Identifiant de l’utilisateur dont vous souhaitez obtenir les adhésions. |

**Output (getCompanyMembershipReturn)**

| Nom | Type | Obligatoire | Description |
|---|---|---|---|
| ` *`membershipArray`*` | `types:CompanyMembershipArray` | Oui | Tableau des adhésions aux sociétés. |

## Exemples {#section-e4958d104ea344a4a79f57d07b46eba7}

Cet exemple de code prend un nom d&#39;utilisateur et récupère tous les membres de société de l&#39;utilisateur dans un tableau. La réponse a été tronquée pour la brièveté.

**Request**

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

