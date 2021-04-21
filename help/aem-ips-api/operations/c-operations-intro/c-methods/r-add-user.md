---
description: Crée un compte utilisateur et l’ajoute à une ou plusieurs sociétés.
solution: Experience Manager
title: addUser
feature: Dynamic Media Classic,SDK/API
role: Developer,Administrator
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '183'
ht-degree: 12%

---


# addUser{#adduser}

Crée un compte utilisateur et l’ajoute à une ou plusieurs sociétés.

Lors de l’ajout d’un utilisateur à plusieurs sociétés, spécifiez ces sociétés en fonction de leurs poignées de société dans `companyHandleArray`. Cette opération retourne le handle à l&#39;utilisateur que vous venez d&#39;ajouter.

## Types d’utilisateur autorisés {#section-126ad42f844444fea11ecf8ad01fe1ec}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `TrialSiteAdmin`
* `ImagePortalAdmin`

## Paramètres {#section-40390a512e314b8d80ecffbb7729f6fb}

**Entrée (addUserParam)**

| Nom | Type | Obligatoire | Description |
|---|---|---|---|
| `*`firstName`*` | `xsd:string` | Oui | Prénom de l’utilisateur. |
| `*`lastName`*` | `xsd:string` | Oui | Nom de l’utilisateur. |
| `*`e-mail`*` | `xsd:string` | Oui | Adresse électronique de l’utilisateur. |
| `*`defaultRole`*` | `xsd:string` | Oui | Définit le rôle d’un utilisateur dans chaque société à laquelle il appartient. Notez toutefois que le rôle `IpsAdmin` remplace d’autres paramètres par société. |
| `*`mot de passe`*` | `xsd:string` | Oui | Définit le mot de passe de l’utilisateur. |
| `*`passwordExpires`*` | `xsd:dateTime` | Non | Définit la période d’expiration du mot de passe. Indiquez le fuseau horaire lors de la transmission de la demande. Les fuseaux horaires sont ajustés à l’heure centrale. |
| `*`isValid`*` | `xsd:boolean` | Oui | Détermine si l’utilisateur est valide. |
| `*`membershipArray`*` | `xsd:CompanyMembershipUpdateArray` | Oui | Tableau de poignées de société. |

**Output (addUserParam)**

| Nom | Type | Obligatoire | Description |
|---|---|---|---|
| `*`userHandle`*` | `xsd:string` | Oui | Nom d’utilisateur. |

## Exemples {#section-2547cef622734b71919eef849960b5cb}

L&#39;API IPS renvoie un élément d&#39;identificateur d&#39;utilisateur qui spécifie le nouvel utilisateur.

**Request**

```java
<ns1:addUserParam xmlns:ns1="http://www.scene7.com/IpsApi/xsd">
   <ns1:firstName>Joe</ns1:firstName>
   <ns1:lastName>User</ns1:lastName>
   <ns1:email>juser@adobe.com</ns1:email>
   <ns1:defaultRole>TrialSiteUser</ns1:role>
   <ns1:password>passw0rd</ns1:password>
   <ns1:isValid>true</ns1:isValid>
   <ns1:companyHandleArray>
      <ns1:items>47</ns1:items>
   </ns1:companyHandleArray>
</ns1:addUserParam>
```

**Réponse**

```java
<ns1:addUserReturn xmlns:ns1="http://www.scene7.com/IpsApi/xsd">
   <ns1:userHandle>525s|juser@scene7.com</ns1:userHandle>
</ns1:addUserReturn>
```

