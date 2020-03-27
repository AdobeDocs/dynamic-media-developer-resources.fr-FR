---
description: Définit les attributs de l’utilisateur (nom, adresse électronique, rôle, etc.)
seo-description: Définit les attributs de l’utilisateur (nom, adresse électronique, rôle, etc.)
seo-title: setUserInfo
solution: Experience Manager
title: setUserInfo
topic: Scene7 Image Production System API
uuid: 52e3a21e-1dd5-4f9d-b460-506d280fff47
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# setUserInfo{#setuserinfo}

Définit les attributs de l’utilisateur (nom, adresse électronique, rôle, etc.)

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
| ` *`userHandle`*` | `xsd:string` | Non | Identifiant utilisateur. |
| ` *`firstName`*` | `xsd:string` | Oui | Prénom. |
| ` *`lastName`*` | `xsd:string` | Oui | Nom. |
| ` *`e-mail`*` | `xsd:string` | Oui | Adresse électronique de l’utilisateur. |
| ` *`defaultRole`*` | `xsd:string` | Oui | Définit le rôle d’un utilisateur dans chaque auquel il appartient. Notez toutefois que le `IpsAdmin` rôle remplace d’autres paramètres  par. |
| ` *`passwordExpires`*` | `xsd:dateTime` | Non | Définissez la date d’expiration du mot de passe. |
| ` *`isValid`*` | `xsd:boolean` | Oui | Détermine si l&#39;utilisateur est un utilisateur IPS valide. |
| ` *`membershipArray`*` | `types:CompanyMembershipUpdateArray` | Oui | Un tableau de  poignées. |

**Output (setUserInfoReturn)**

L&#39;API IPS ne renvoie pas de réponse pour cette opération.

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
