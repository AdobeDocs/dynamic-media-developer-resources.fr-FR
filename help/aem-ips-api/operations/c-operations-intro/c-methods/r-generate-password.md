---
description: Génère un nouveau mot de passe.
solution: Experience Manager
title: generatePassword
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 80e7642f-4aec-4ff0-a090-e59b7a065c39
source-git-commit: 77c88d5fe20e048f6fad2bb23cb1abe090793acf
workflow-type: tm+mt
source-wordcount: '59'
ht-degree: 16%

---

# generatePassword{#generatepassword}

Génère un nouveau mot de passe.

Syntaxe

## Types d’utilisateurs autorisés {#section-88f7dc11e5c74be281399d8f2e3c9555}

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

**Sortie (generatePasswordParam)**

| Nom | Type | Obligatoire | Description |
|---|---|---|---|
| mot de passe | `xsd:string` | Oui | Un nouveau mot de passe. |

## Exemples {#section-f580fefdccec46fe95359e3aef0ed17f}

Cet exemple de code génère un mot de passe. C’est inhabituel, car la requête est simplement un paramètre sans éléments ni valeurs inclus. IPS renvoie un mot de passe fort.

**Requête**

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
