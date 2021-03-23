---
description: Supprime un projet d’une société. Les liens entre les ressources et le projet sont rompus, mais les ressources ne sont pas supprimées d'IPS.
seo-description: Supprime un projet d’une société. Les liens entre les ressources et le projet sont rompus, mais les ressources ne sont pas supprimées d'IPS.
seo-title: deleteProject
solution: Experience Manager
title: deleteProject
uuid: 0915066f-2106-4cbc-a68a-f149810c24f8
feature: Dynamic Media Classic, SDK/API
role: Développeur, Administrateur
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '160'
ht-degree: 7%

---


# deleteProject{#deleteproject}

Supprime un projet d’une société. Les liens entre les ressources et le projet sont rompus, mais les ressources ne sont pas supprimées d&#39;IPS.

Syntaxe

## Types d’utilisateur autorisés {#section-d8a70e23c68d426e9af1357b978ae2f0}

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
| `*`companyName`*` | `xsd:string` | Oui | Nom de la société associée au projet. |
| `*`projectHandle`*` | `xsd:string` | Oui | Identifiant du projet à supprimer. |

**Output (deleteProjectReturn)**

L&#39;API IPS ne renvoie pas de réponse pour cette opération.

## Exemples {#section-e38507f1f7ec41b9a625f47390490254}

Cet exemple de code utilise le nom d&#39;utilisateur de la société et le nom d&#39;utilisateur du projet en tant que champs dans deleteProjectParam envoyé au serveur des services Web IPS pour supprimer le projet.

**Request**

```java
<deleteProjectParam xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
   <companyHandle>c|6</companyHandle>
<projectHandle>p|6|ProjectTestAPI</projectHandle></deleteProjectParam>
```

**Réponse**

Aucune
