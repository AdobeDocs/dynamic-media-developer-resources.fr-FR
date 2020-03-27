---
description: Renvoie les utilisateurs d’un  spécifié par un pseudo de.
seo-description: Renvoie les utilisateurs d’un  spécifié par un pseudo de.
seo-title: getCompanyMembers
solution: Experience Manager
title: getCompanyMembers
topic: Scene7 Image Production System API
uuid: 45e2d040-a70a-46f4-863a-633ddabcbcf6
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# getCompanyMembers{#getcompanymembers}

Renvoie les utilisateurs d’un  spécifié par un pseudo de.

Syntaxe

## Types d’utilisateurs autorisés {#section-b2bc2fa0cc944cea8be82524838307cc}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `TrialSiteAdmin`
* `ImagePortalAdmin`

## Paramètres {#section-5602e4d6f2214e398e6a804e61f1a088}

**Entrée (getCompanyMembersParam)**

| Nom | Type | Obligatoire | Description |
|---|---|---|---|
| ` *`companyHandle`*` | `xsd:string` | Oui | Poignée du dont vous voulez obtenir les membres. |
| ` *`includeInvalid`*` | `xsd:boolean` | Oui | Incluez des  non valides. |

**Output (getCompanyMembersReturn)**

| Nom | Type | Obligatoire | Description |
|---|---|---|---|
| ` *`MemberArray`*` | `types:CompanyMemberArray` | Oui | Tableau des adhésions des utilisateurs. |

## Exemples {#section-39d8cf3653fd4fe8b842caabac9dedfc}

Cet exemple de code renvoie tous les membres d’un  d’dans un tableau d’utilisateurs. La réponse a été tronquée pour la brièveté.

**Request**

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

