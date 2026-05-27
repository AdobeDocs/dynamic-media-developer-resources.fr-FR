---
description: Obtient des informations sur un utilisateur. Utilisez l’adresse e-mail et le mot de passe d’un utilisateur système comme informations d’identification pour autoriser la requête. Sinon, l’opération obtient des informations sur l’utilisateur ou l’utilisatrice par défaut.
solution: Experience Manager
title: getUserInfo
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 1981f25f-779e-4434-ab6b-0debb40521fe
TQID: 'https://experienceleague.adobe.com/4FEwXXgelDJ5CDf4FhaE11GS3vsnZi6wjY7HproyCIw'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: c66ffd68-0f65-42bb-aa23-b4020f12e0bdid: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 139
ht-degree: 10%

---

# getUserInfo{#getuserinfo}

Obtient des informations sur un utilisateur. Utilisez l’adresse e-mail et le mot de passe d’un utilisateur système comme informations d’identification pour autoriser la requête. Sinon, l’opération obtient des informations sur l’utilisateur ou l’utilisatrice par défaut.

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
| userHandle | `xsd:string` | Non | Gérez vers l’utilisateur dont vous souhaitez renvoyer les informations. |
| e-mail | `xsd:string` | Non | Adresse e-mail de l’utilisateur. |

**Output (getUserInfoReturn)**

| Nom | Type | Obligatoire | Description |
|---|---|---|---|
| userInfo | `types:User` | Oui | Prénom, nom, adresse e-mail et rôle d’un utilisateur, ainsi que la validité de l’utilisateur et l’expiration de son mot de passe. |

## Exemples {#section-98d77a2e360a438dbe240099bea26a65}

Cet exemple de code renvoie des informations pour l’utilisateur IPS par défaut.

**Requête**

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
