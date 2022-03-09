---
description: Supprime un projet d’une entreprise. Les liens entre les ressources et le projet sont rompus, mais les ressources ne sont pas supprimées d’IPS.
solution: Experience Manager
title: deleteProject
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: b42be3ef-c935-4548-8f92-4fc33af321b5
source-git-commit: 77c88d5fe20e048f6fad2bb23cb1abe090793acf
workflow-type: tm+mt
source-wordcount: '128'
ht-degree: 9%

---

# deleteProject{#deleteproject}

Supprime un projet d’une entreprise. Les liens entre les ressources et le projet sont rompus, mais les ressources ne sont pas supprimées d’IPS.

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
| companyName | `xsd:string` | Oui | Nom de la société associée au projet. |
| projectHandle | `xsd:string` | Oui | Gestionnaire du projet à supprimer. |

**Sortie (deleteProjectReturn)**

L’API IPS ne renvoie pas de réponse pour cette opération.

## Exemples {#section-e38507f1f7ec41b9a625f47390490254}

Cet exemple de code utilise le nom d’entreprise et le nom d’utilisateur du projet comme champs dans le paramètre deleteProjectParam envoyé au serveur des services Web IPS pour supprimer le projet.

**Request**

```java
<deleteProjectParam xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
   <companyHandle>c|6</companyHandle>
<projectHandle>p|6|ProjectTestAPI</projectHandle></deleteProjectParam>
```

**Réponse**

Aucune
