---
description: Définit des attributs utilisateur (par exemple, nom, courrier électronique, rôle, etc.)
solution: Experience Manager
title: setUserInfo
feature: Dynamic Media Classic, SDK/API
role: Developer,Admin
exl-id: d8f8fe53-a874-4b77-9084-9a369862a672
source-git-commit: fcda99340a18d5037157723bb3bdca5fa9df3277
workflow-type: tm+mt
source-wordcount: '112'
ht-degree: 20%

---

# setUserInfo{#setuserinfo}

Définit des attributs utilisateur (par exemple, nom, courrier électronique, rôle, etc.)

Syntaxe

## Types d’utilisateurs autorisés {#section-6c28db5d15b3449492a73749e4f981ac}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `TrialSiteAdmin`
* `ImagePortalAdmin`

## Paramètres {#section-71b457921fe74acb862a1e112e550211}

**Input (setUserInfoParam)**

| Nom | Type | Obligatoire | Description |
|---|---|---|---|
| `*`userHandle`*` | `xsd:string` | Non | Identifiant utilisateur. |
| `*`firstName`*` | `xsd:string` | Oui | Prénom. |
| `*`lastName`*` | `xsd:string` | Oui | Nom. |
| `*`e-mail`*` | `xsd:string` | Oui | Adresse électronique de l’utilisateur. |
| `*`defaultRole`*` | `xsd:string` | Oui | Définit le rôle d’un utilisateur dans chaque société à laquelle il appartient. Notez toutefois que le rôle `IpsAdmin` remplace d’autres paramètres par entreprise. |
| `*`passwordExpires`*` | `xsd:dateTime` | Non | Définissez la date d’expiration du mot de passe. |
| `*`isValid`*` | `xsd:boolean` | Oui | Détermine si l’utilisateur est un utilisateur IPS valide. |
| `*`membershipArray`*` | `types:CompanyMembershipUpdateArray` | Oui | Un tableau de gestionnaires de société. |

**Sortie (setUserInfoReturn)**

L’API IPS ne renvoie pas de réponse pour cette opération.

## Exemples {#section-272c103076fb4de0a53729e2f6bfb895}

**Request**

```java
<setUserInfoParam xmlns="http://www.scene7.com/IpsApi/xsd">
   <firstName>test</firstName>
   <lastName>test</lastName>
   <email>test@test.test</email>
   <defaultRole>IpsAdmin</defaultRole>
   <isValid>true</isValid>
</setUserInfoParam>
```

**Réponse**

Aucune
