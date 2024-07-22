---
description: Met une tâche active en pause.
solution: Experience Manager
title: pauseJob
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 010e969a-911e-49fc-8577-66c18cd4329c
source-git-commit: 77c88d5fe20e048f6fad2bb23cb1abe090793acf
workflow-type: tm+mt
source-wordcount: '61'
ht-degree: 16%

---

# pauseJob{#pausejob}

Met une tâche active en pause.

Syntaxe

## Types d’utilisateurs autorisés {#section-f2bf306ab4574871bd21f9f7dd681033}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `TrialSiteAdmin`
* `TrialSiteUser`
* `ImagePortalAdmin`
* `ImagePortalContrib`
* `ImagePortalContribUser`

## Paramètres {#section-7aedb924cf8b4e05a0dc927636d537a0}

**Entrée (pauseJobParam)**

| Nom | Type | Obligatoire | Description |
|---|---|---|---|
| companyHandle | `xsd:string` | Oui | Traitez la société. |
| jobHandle | `xsd:string` | Oui | Gérez la tâche que vous souhaitez mettre en pause. |

**Sortie (PauseJobReturn)**

L’API IPS ne renvoie pas de réponse pour cette opération.

## Exemples {#section-ee4914f9496f4bd88556728a48fb22c1}

Cet exemple de code met une tâche active en pause.

**Requête**

```java
<pauseJobParam xmlns="http://www.scene7.com/IpsApi/xsd">
   <companyHandle>47</companyHandle>
   <jobHandle>47|My Test Job|</jobHandle>
</pauseJobParam>
```

**Réponse**

Aucune
