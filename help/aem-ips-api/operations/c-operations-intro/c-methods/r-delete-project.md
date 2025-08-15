---
description: Supprime un projet d’une société. Les liens entre les ressources et le projet sont rompus, mais les actifs ne sont pas supprimés d’IPS.
solution: Experience Manager
title: Supprimer le projet
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: b42be3ef-c935-4548-8f92-4fc33af321b5
source-git-commit: 77c88d5fe20e048f6fad2bb23cb1abe090793acf
workflow-type: tm+mt
source-wordcount: '128'
ht-degree: 7%

---

# Supprimer le projet{#deleteproject}

Supprime un projet d’une société. Les liens entre les ressources et le projet sont rompus, mais les actifs ne sont pas supprimés d’IPS.

Syntaxe

## Types d’utilisateurs autorisés {#section-d8a70e23c68d426e9af1357b978ae2f0}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`
* `ImagePortalContrib`
* `ImagePortalContribUser`

## Paramètres {#section-00d1e00dd5014513a52b4e6b4f61de62}

**Entrée (deleteProjectParam)**

| Nom | Type | Obligatoire | Description |
|---|---|---|---|
| Nom de la société | `xsd:string` | Oui | Nom de l’entreprise associée au projet. |
| Poignée de projet | `xsd:string` | Oui | Poignée du projet à supprimer. |

**Output (deleteProjectReturn)**

L’API IPS ne renvoie pas de réponse pour cette opération.

## Exemples {#section-e38507f1f7ec41b9a625f47390490254}

Cet exemple de code utilise le descripteur de société et le descripteur de projet en tant que champs dans le deleteProjectParam envoyé au serveur des services Web IPS afin de supprimer le projet.

**Demander**

```java
<deleteProjectParam xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
   <companyHandle>c|6</companyHandle>
<projectHandle>p|6|ProjectTestAPI</projectHandle></deleteProjectParam>
```

**Réponse**

Aucune
