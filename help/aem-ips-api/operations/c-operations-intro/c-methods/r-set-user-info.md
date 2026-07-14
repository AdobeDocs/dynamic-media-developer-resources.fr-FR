---
description: Définit des attributs utilisateur (par exemple, nom, e-mail, rôle, etc.).
solution: Experience Manager
title: setUserInfo
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: d8f8fe53-a874-4b77-9084-9a369862a672
TQID: 'https://experienceleague.adobe.com/JzJv4nEeWfbY-Wp-qkEq883dlTqaRm9Fc-UvDa70dOg'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 6762cee83f1b7c970ed6353450c2ae6c602e7f3a
workflow-type: tm+mt
source-wordcount: 114
ht-degree: 18%

---

# setUserInfo{#setuserinfo}

Définit des attributs utilisateur (par exemple, nom, e-mail, rôle, etc.).

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
| userHandle | `xsd:string` | Non | Handle utilisateur. |
| firstName | `xsd:string` | Oui | Prénom. |
| lastName | `xsd:string` | Oui | Nom. |
| e-mail | `xsd:string` | Oui | Adresse e-mail de l’utilisateur. |
| defaultRole | `xsd:string` | Oui | Définit le rôle d’un utilisateur dans chaque société à laquelle il appartient. Notez toutefois que le rôle `IpsAdmin` remplace d’autres paramètres par société. |
| passwordExpires | `xsd:dateTime` | Non | Définissez la date d’expiration du mot de passe de . |
| isValid | `xsd:boolean` | Oui | Détermine si l’utilisateur est un utilisateur IPS valide. |
| membershipArray | `types:CompanyMembershipUpdateArray` | Oui | Tableau d’identifiants d’entreprise. |

**Output (setUserInfoReturn)**

L’API IPS ne renvoie pas de réponse pour cette opération.

## Exemples {#section-272c103076fb4de0a53729e2f6bfb895}

**Requête**

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

