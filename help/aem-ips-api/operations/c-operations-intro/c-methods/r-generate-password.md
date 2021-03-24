---
description: Génère un nouveau mot de passe.
solution: Experience Manager
title: generatePassword
feature: Dynamic Media Classic, SDK/API
role: Développeur, Administrateur
translation-type: tm+mt
source-git-commit: 052bfcbcf1bd4ccf60afa7e3325bf58dd07cba85
workflow-type: tm+mt
source-wordcount: '66'
ht-degree: 18%

---


# generatePassword{#generatepassword}

Génère un nouveau mot de passe.

Syntaxe

## Types d’utilisateur autorisés {#section-88f7dc11e5c74be281399d8f2e3c9555}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `TrialSiteAdmin`
* `TrialSiteUser`
* `ImagePortalAdmin`
* `ImagePortalUser`
* `ImagePortalContrib`
* `ImagePortalContribUser`

## Paramètres {#section-d516615c906240819a284786efb19863}

**Entrée (generatePasswordParam)**

Aucune

**Output (generatePasswordParam)**

| Nom | Type | Obligatoire | Description |
|---|---|---|---|
| `*`mot de passe`*` | `xsd:string` | Oui | Nouveau mot de passe. |

## Exemples {#section-f580fefdccec46fe95359e3aef0ed17f}

Cet exemple de code génère un mot de passe. Il est inhabituel, car la requête est simplement un paramètre sans éléments ou valeurs placés entre eux. IPS renvoie un mot de passe fort.

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

