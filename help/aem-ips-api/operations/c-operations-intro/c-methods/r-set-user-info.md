---
description: Définit les attributs utilisateur (par exemple, nom, adresse électronique, rôle, etc.)
solution: Experience Manager
title: setUserInfo
feature: Dynamic Media Classic, SDK/API
role: Développeur, Administrateur
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '114'
ht-degree: 20%

---


# setUserInfo{#setuserinfo}

Définit les attributs utilisateur (par exemple, nom, adresse électronique, rôle, etc.)

Syntaxe

## Types d’utilisateur autorisés {#section-6c28db5d15b3449492a73749e4f981ac}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `TrialSiteAdmin`
* `ImagePortalAdmin`

## Paramètres {#section-71b457921fe74acb862a1e112e550211}

**Entrée (setUserInfoParam)**

| Nom | Type | Obligatoire | Description |
|---|---|---|---|
| `*`userHandle`*` | `xsd:string` | Non | Identifiant utilisateur. |
| `*`firstName`*` | `xsd:string` | Oui | Prénom. |
| `*`lastName`*` | `xsd:string` | Oui | Nom. |
| `*`e-mail`*` | `xsd:string` | Oui | Courriel de l’utilisateur. |
| `*`defaultRole`*` | `xsd:string` | Oui | Définit le rôle d’un utilisateur dans chaque société à laquelle il appartient. Notez toutefois que le rôle `IpsAdmin` remplace d’autres paramètres par société. |
| `*`passwordExpires`*` | `xsd:dateTime` | Non | Définissez la date d’expiration du mot de passe. |
| `*`isValid`*` | `xsd:boolean` | Oui | Détermine si l&#39;utilisateur est un utilisateur IPS valide. |
| `*`membershipArray`*` | `types:CompanyMembershipUpdateArray` | Oui | Tableau de poignées de société. |

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
