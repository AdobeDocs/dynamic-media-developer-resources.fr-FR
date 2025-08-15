---
description: Obtient les projets d’un groupe de ressources connexes.
solution: Experience Manager
title: getProjects
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: d7262ed7-7419-4d6b-86ed-f3ad4657d654
source-git-commit: 77c88d5fe20e048f6fad2bb23cb1abe090793acf
workflow-type: tm+mt
source-wordcount: '66'
ht-degree: 19%

---

# getProjects{#getprojects}

Obtient les projets d’un groupe de ressources connexes.

Syntaxe

## Types d’utilisateurs autorisés {#section-337649866b1f4098844d1974ed7ab5d0}

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
| CompanyHandle | `xsd:string` | Oui | La poignée de l’entreprise. |

**Output (getProjectsReturn)**

| Nom | Type | Obligatoire | Description |
|---|---|---|---|
| Réseau de projet | `types:ProjectArray` | Oui | L’éventail des projets associés à l’entreprise. |

## Exemples {#section-8b12d0b948f644f68bf9a16060d3849a}

Cet exemple de code renvoie tous les indicateurs de projet d’un tableau de projet.

**Demander**

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
