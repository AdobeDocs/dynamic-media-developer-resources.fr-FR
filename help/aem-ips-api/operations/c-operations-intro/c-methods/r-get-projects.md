---
description: Obtient des projets pour un groupe d’actifs connexes.
solution: Experience Manager
title: getProjects
feature: Dynamic Media Classic,SDK/API
role: Developer,Administrator
translation-type: tm+mt
source-git-commit: 052bfcbcf1bd4ccf60afa7e3325bf58dd07cba85
workflow-type: tm+mt
source-wordcount: '73'
ht-degree: 20%

---


# getProjects{#getprojects}

Obtient des projets pour un groupe d’actifs connexes.

Syntaxe

## Types d’utilisateur autorisés {#section-337649866b1f4098844d1974ed7ab5d0}

* `IpsUser`
* `IpsAdmin`
* `TrialSiteAdmin`
* `TrialSiteUser`
* `ImagePortalContrib`
* `ImagePortalContribUser`

## Paramètres {#section-8d549237b8c440b4872a0a086ddc00a1}

**Entrée (getProjectsParam)**

| Nom | Type | Obligatoire | Description |
|---|---|---|---|
| `*`companyHandle`*` | `xsd:string` | Oui | La poignée de la société. |

**Sortie (getProjectsReturn)**

| Nom | Type | Obligatoire | Description |
|---|---|---|---|
| `*`projectArray`*` | `types:ProjectArray` | Oui | Tableau de projets associés à la société. |

## Exemples {#section-8b12d0b948f644f68bf9a16060d3849a}

Cet exemple de code renvoie toutes les poignées de projet dans un tableau de projet.

**Request**

```java
<ns1:getProjectsParam xmlns:ns1="http://www.scene7.com/IpsApi/xsd">
   <ns1:companyHandle>47</ns1:companyHandle>
</ns1:getProjectsParam>
```

**Réponse**

```java
<getProjectsReturn xmlns="http://www.scene7.com/IpsApi/xsd">
   <projectArray>
      <items>
         <projectHandle>47|My Project 1</projectHandle>
         <name>My Project 1</name>
      </items>
      <items>
         <projectHandle>47|My Project 2</projectHandle>
         <name>My Project 2</name>
      </items>
   </projectArray>
</getProjectsReturn>
```

