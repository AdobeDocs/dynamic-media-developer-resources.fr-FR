---
description: Définit les attributs de l’utilisateur (par exemple, nom, adresse électronique, rôle, etc.)
solution: Experience Manager
title: setUserInfo
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: d8f8fe53-a874-4b77-9084-9a369862a672
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '113'
ht-degree: 18%

---

# setUserInfo{#setuserinfo}

Définit les attributs de l’utilisateur (par exemple, nom, adresse électronique, rôle, etc.)

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
| Poignée utilisateur | `xsd:string` | Non | Pseudo utilisateur. |
| prénom | `xsd:string` | Oui | Prénom. |
| Nom de famille | `xsd:string` | Oui | Nom. |
| e-mail | `xsd:string` | Oui | Adresse électronique de l’utilisateur. |
| Rôle par défaut | `xsd:string` | Oui | Définit le rôle d’un utilisateur dans chaque entreprise à laquelle il appartient. Notez toutefois que le rôle remplace les `IpsAdmin` autres paramètres par société. |
| expirations du mot de passe | `xsd:dateTime` | Non | Date d’expiration du mot de passe de l’éditeur. |
| est valide | `xsd:boolean` | Oui | Détermine si l’utilisateur est un utilisateur IPS valide. |
| Tableau d’adhérents | `types:CompanyMembershipUpdateArray` | Oui | Tableau de poignées d’entreprise. |

**Output (setUserInfoReturn)**

L’API IPS ne renvoie pas de réponse pour cette opération.

## Exemples {#section-272c103076fb4de0a53729e2f6bfb895}

**Demander**

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
