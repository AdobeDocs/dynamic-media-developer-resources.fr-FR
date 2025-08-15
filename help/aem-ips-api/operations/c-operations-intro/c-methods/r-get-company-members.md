---
description: Renvoie les utilisateurs d’une société spécifiée par un nom d’utilisateur de société.
solution: Experience Manager
title: getCompanyMembers
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: da5e5a48-2e0b-4ccc-a71e-b5b746484d4a
source-git-commit: 77c88d5fe20e048f6fad2bb23cb1abe090793acf
workflow-type: tm+mt
source-wordcount: '89'
ht-degree: 15%

---

# getCompanyMembers{#getcompanymembers}

Renvoie les utilisateurs d’une société spécifiée par un nom d’utilisateur de société.

Syntaxe

## Types d’utilisateurs autorisés {#section-b2bc2fa0cc944cea8be82524838307cc}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `TrialSiteAdmin`
* `ImagePortalAdmin`

## Paramètres {#section-5602e4d6f2214e398e6a804e61f1a088}

**Input (getCompanyMembersParam)**

| Nom | Type | Obligatoire | Description |
|---|---|---|---|
| companyHandle | `xsd:string` | Oui | Identifiant de la société dont vous souhaitez obtenir les membres. |
| includeInvalid | `xsd:boolean` | Oui | Inclure les sociétés non valides. |

**Output (getCompanyMembersReturn)**

| Nom | Type | Obligatoire | Description |
|---|---|---|---|
| memberArray | `types:CompanyMemberArray` | Oui | Tableau des appartenances des utilisateurs. |

## Exemples {#section-39d8cf3653fd4fe8b842caabac9dedfc}

Cet exemple de code renvoie tous les membres d’une société dans un tableau utilisateur. La réponse a été tronquée par souci de concision.

**Requête**

```java
<ns1:getCompanyMembersParam xmlns:ns1="http://www.scene7.com/IpsApi/xsd">
   <ns1:companyHandle>47</ns1:companyHandle>
   <ns1:includeInvalid>false</ns1:includeInvalid>
</ns1:getCompanyMembersParam>
```

**Réponse**

```java
<getCompanyMembersReturn xmlns="http://www.scene7.com/IpsApi/xsd">
   <memberArray>
      <items>
         <userHandle>66|pbayol@adobe.com</userHandle>
         <firstName>Peter</firstName>
         <lastName>Bayol</lastName>
         <email>pbayol@adobe.com</email>
         <role>IpsAdmin</role>
         <isValid>true</isValid>
         <passwordExpires>2107-07-25T23:12:49.472-07:00</passwordExpires>
      </items>
      ...
   </memberArray>
</getCompanyMembersReturn>
```
