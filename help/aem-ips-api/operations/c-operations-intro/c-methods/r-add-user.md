---
description: Crée un compte utilisateur et l’ajoute à un ou plusieurs  d’.
seo-description: Crée un compte utilisateur et l’ajoute à un ou plusieurs  d’.
seo-title: addUser
solution: Experience Manager
title: addUser
topic: Scene7 Image Production System API
uuid: b8c5ada6-470e-4795-a4f3-20750da709a9
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# addUser{#adduser}

Crée un compte utilisateur et l’ajoute à un ou plusieurs  d’.

Lors de l’ajout d’un utilisateur à plusieurs  de, spécifiez les  par les poignées de leurs  de `companyHandleArray`la page. Cette opération renvoie le pseudo à l’utilisateur que vous venez d’ajouter.

## Types d’utilisateurs autorisés {#section-126ad42f844444fea11ecf8ad01fe1ec}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `TrialSiteAdmin`
* `ImagePortalAdmin`

## Paramètres {#section-40390a512e314b8d80ecffbb7729f6fb}

**Input (addUserParam)**

| Nom | Type | Obligatoire | Description |
|---|---|---|---|
| ` *`firstName`*` | `xsd:string` | Oui | Prénom de l’utilisateur. |
| ` *`lastName`*` | `xsd:string` | Oui | Nom de l’utilisateur. |
| ` *`e-mail`*` | `xsd:string` | Oui | Adresse électronique de l’utilisateur. |
| ` *`defaultRole`*` | `xsd:string` | Oui | Définit le rôle d’un utilisateur dans chaque auquel il appartient. Notez toutefois que le `IpsAdmin` rôle remplace d’autres paramètres  par. |
| ` *`mot de passe`*` | `xsd:string` | Oui | Définit le mot de passe de l’utilisateur |
| ` *`passwordExpires`*` | `xsd:dateTime` | Non | Définit la période d’expiration du mot de passe. Indiquez le fuseau horaire lors de la transmission de la requête. Les fuseaux horaires sont ajustés à l’heure centrale. |
| ` *`isValid`*` | `xsd:boolean` | Oui | Détermine si l’utilisateur est valide. |
| ` *`membershipArray`*` | `xsd:CompanyMembershipUpdateArray` | Oui | Un tableau de  poignées. |

**Output (addUserParam)**

| Nom | Type | Obligatoire | Description |
|---|---|---|---|
| ` *`userHandle`*` | `xsd:string` | Oui | Identifiant de l’utilisateur. |

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

