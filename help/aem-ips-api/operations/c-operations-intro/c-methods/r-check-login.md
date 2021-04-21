---
description: Vérifie si un utilisateur disposant d’une société spécifique (identifiée par son nom d’utilisateur), son adresse électronique et son mot de passe peut se connecter.
solution: Experience Manager
title: checkLogin
feature: Dynamic Media Classic,SDK/API
role: Developer,Administrator
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '152'
ht-degree: 12%

---


# checkLogin{#checklogin}

Vérifie si un utilisateur disposant d’une société spécifique (identifiée par son nom d’utilisateur), son adresse électronique et son mot de passe peut se connecter.

>[!NOTE]
>
>Si l’identificateur de société est omis, cette méthode vérifie la connexion de l’utilisateur par défaut.

## Types d’utilisateur autorisés {#section-df8b26b550854f899948276adaca083a}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `TrialSiteAdmin`
* `TrialSiteUser`
* `ImagePortalAdmin`
* `ImagePortalUser`
* `ImagePortalContrib`
* `ImagePortalContribUser`

## Paramètres {#section-1ad4c0b4803b4388aedd655030676cb3}

**Entrée (checkLoginParam)**

| Nom | Type | Obligatoire | Description |
|---|---|---|---|
| `*`companyHandle`*` | `xsd:string` | Non | Identifiant de la société contenant l’utilisateur. |
| `*`e-mail`*` | `xsd:string` | Oui | Adresse électronique de l’utilisateur. |
| `*`mot de passe`*` | `xsd:string` | Oui | Mot de passe de l’utilisateur. |

**Output (checkLoginParam)**

| Nom | Type | Obligatoire | Description |
|---|---|---|---|
| `*`état`*` | `xsd:string` | Oui | Etat de connexion de l’utilisateur. |

## Exemples {#section-23f90100a9d94bc7b4045634cccd1b98}

Cet exemple de code utilise un paramètre de nom d&#39;utilisateur de société, une adresse électronique et un mot de passe pour déterminer si un utilisateur peut se connecter à IPS. Si l&#39;utilisateur *peut* se connecter, cette méthode renvoie la chaîne `ValidLogin`. Si l&#39;utilisateur *ne peut pas se connecter*, cette méthode renvoie la chaîne `InvalidLogin`.

**Request**

```java
<ns1:checkLoginParam xmlns:ns1="http://www.scene7.com/IpsApi/xsd">
   <ns1:companyHandle>137</ns1:companyHandle>
   <ns1:email>juser3@scene7.com</ns1:email>
   <ns1:password>welcome</ns1:password>
</ns1:checkLoginParam>
```

**Réponse**

```java
<ns1:checkLoginReturn xmlns:ns1="http://www.scene7.com/IpsApi/xsd">
   <ns1:status>InvalidLogin</ns1:status>
</ns1:checkLoginReturn>
```

