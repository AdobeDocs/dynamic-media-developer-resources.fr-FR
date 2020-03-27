---
description: Génère un nouveau mot de passe.
seo-description: Génère un nouveau mot de passe.
seo-title: generatePassword
solution: Experience Manager
title: generatePassword
topic: Scene7 Image Production System API
uuid: e3367bfc-d437-4a61-83e8-69830154dc61
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# generatePassword{#generatepassword}

Génère un nouveau mot de passe.

Syntaxe

## Types d’utilisateurs autorisés {#section-88f7dc11e5c74be281399d8f2e3c9555}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `TrialSiteUser`
* `ImagePortalAdmin`
* `ImagePortalUser`
* `ImagePortalContrib`
* `ImagePortalContribUser`

## Paramètres {#section-d516615c906240819a284786efb19863}

**Input (generatePasswordParam)**

Aucune

**Output (generatePasswordParam)**

| Nom | Type | Obligatoire | Description |
|---|---|---|---|
| ` *`mot de passe`*` | `xsd:string` | Oui | Un nouveau mot de passe. |

## Exemples {#section-f580fefdccec46fe95359e3aef0ed17f}

Cet exemple de code génère un mot de passe. C’est inhabituel, car la requête est simplement un paramètre sans éléments ou valeurs placés entre eux. IPS renvoie un mot de passe fort.

**Request**

```java
<generatePasswordParam xmlns="http://www.scene7.com/IpsApi/xsd">
</generatePasswordParam>
```

**Réponse**

```java
<generatePasswordReturn xmlns="http://www.scene7.com/IpsApi/xsd">
   <password>1\7aQRn]</password>
</generatePasswordReturn>
```

