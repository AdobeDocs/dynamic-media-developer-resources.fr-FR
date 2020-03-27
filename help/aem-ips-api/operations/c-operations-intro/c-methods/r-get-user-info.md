---
description: Obtient des informations sur un utilisateur. Utilisez l’adresse électronique et le mot de passe d’un utilisateur système comme informations d’identification pour autoriser la requête. Sinon, l’opération obtient des informations sur l’utilisateur par défaut.
seo-description: Obtient des informations sur un utilisateur. Utilisez l’adresse électronique et le mot de passe d’un utilisateur système comme informations d’identification pour autoriser la requête. Sinon, l’opération obtient des informations sur l’utilisateur par défaut.
seo-title: getUserInfo
solution: Experience Manager
title: getUserInfo
topic: Scene7 Image Production System API
uuid: b305c108-22e9-4268-a5b3-25fddd844c24
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# getUserInfo{#getuserinfo}

Obtient des informations sur un utilisateur. Utilisez l’adresse électronique et le mot de passe d’un utilisateur système comme informations d’identification pour autoriser la requête. Sinon, l’opération obtient des informations sur l’utilisateur par défaut.

Syntaxe

## Types d’utilisateurs autorisés {#section-1c42d78e914a4b84a946b3480f29b36a}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `TrialSiteAdmin`
* `TrialSiteUser`
* `ImagePortalAdmin`
* `ImagePortalUser`
* `ImagePortalContrib`
* `ImagePortalContribUser`

## Paramètres {#section-e87b3cb743494719925c9458eed433b6}

**Input (getUserInfoParam)**

| Nom | Type | Obligatoire | Description |
|---|---|---|---|
| ` *`userHandle`*` | `xsd:string` | Non | Traitez l’utilisateur dont vous souhaitez retourner les informations. |
| ` *`e-mail`*` | `xsd:string` | Non | Adresse électronique de l’utilisateur. |

**Output (getUserInfoReturn)**

| Nom | Type | Obligatoire | Description |
|---|---|---|---|
| ` *`userInfo`*` | `types:User` | Oui | Prénom, nom, adresse électronique et rôle d’un utilisateur, ainsi que la validité et l’expiration du mot de passe de l’utilisateur. |

## Exemples {#section-98d77a2e360a438dbe240099bea26a65}

Cet exemple de code renvoie des informations pour l&#39;utilisateur IPS par défaut.

**Request**

```java
<getUserInfoParam xmlns="http://www.scene7.com/IpsApi/xsd" /></getUserInfoParam>
```

**Réponse**

```java
<ns1:getUserInfoReturn xmlns:ns1="http://www.scene7.com/IpsApi/xsd"> 
   <ns1:userInfo> 
      <ns1:userHandle>3261|user@scene7.com</ns1:userHandle> 
      <ns1:firstName>FirstName</ns1:firstName> 
      <ns1:lastName>LastName</ns1:lastName> 
      <ns1:email>user@scene7.com</ns1:email> 
      <ns1:role>IpsAdmin</ns1:role> 
      <ns1:isValid>true</ns1:isValid> 
      <ns1:passwordExpires>2107-04-22T18:35:41.995Z</ns1:passwordExpires> 
   </ns1:userInfo> 
</ns1:getUserInfoReturn>
```

