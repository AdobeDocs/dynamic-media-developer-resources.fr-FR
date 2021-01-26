---
description: Renvoie les utilisateurs d’une société spécifiée par une poignée de société.
seo-description: Renvoie les utilisateurs d’une société spécifiée par une poignée de société.
seo-title: getCompanyMembers
solution: Experience Manager
title: getCompanyMembers
topic: Dynamic Media Image Production System API
uuid: 45e2d040-a70a-46f4-863a-633ddabcbcf6
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '101'
ht-degree: 15%

---


# getCompanyMembers{#getcompanymembers}

Renvoie les utilisateurs d’une société spécifiée par une poignée de société.

Syntaxe

## Types d’utilisateur autorisés {#section-b2bc2fa0cc944cea8be82524838307cc}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `TrialSiteAdmin`
* `ImagePortalAdmin`

## Paramètres {#section-5602e4d6f2214e398e6a804e61f1a088}

**Entrée (getCompanyMembersParam)**

| Nom | Type | Obligatoire | Description |
|---|---|---|---|
| `*`companyHandle`*` | `xsd:string` | Oui | Poignée de la société dont vous souhaitez obtenir les membres. |
| `*`includeInvalid`*` | `xsd:boolean` | Oui | Incluez des sociétés non valides. |

**Output (getCompanyMembersReturn)**

| Nom | Type | Obligatoire | Description |
|---|---|---|---|
| `*`MemberArray`*` | `types:CompanyMemberArray` | Oui | Tableau des adhésions des utilisateurs. |

## Exemples {#section-39d8cf3653fd4fe8b842caabac9dedfc}

Cet exemple de code renvoie tous les membres d&#39;une société dans un tableau d&#39;utilisateurs. La réponse a été tronquée pour la brièveté.

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

