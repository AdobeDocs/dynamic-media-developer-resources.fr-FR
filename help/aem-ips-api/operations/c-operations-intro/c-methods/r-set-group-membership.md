---
description: Définit l’appartenance à un groupe pour un utilisateur.
solution: Experience Manager
title: setGroupMembership
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 0a355a34-1c2d-48c1-ba12-7d07d1673d09
source-git-commit: 77c88d5fe20e048f6fad2bb23cb1abe090793acf
workflow-type: tm+mt
source-wordcount: '96'
ht-degree: 11%

---

# setGroupMembership{#setgroupmembership}

Définit l’appartenance à un groupe pour un utilisateur.

Syntaxe

## Types d’utilisateurs autorisés {#section-3d6308a8a5694ed085e04d1c37982b9e}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`

## Paramètres {#section-6aeda13b26af4796aad1306ac7a9ad17}

**Input (setGroupMembershipParam)**

| Nom | Type | Obligatoire | Description |
|---|---|---|---|
| userHandle | `xsd:string` | Non | Gestionnaire de l’utilisateur dont vous souhaitez définir l’appartenance à un groupe. |
| companyHandle | `xsd:string` | Non | Poignée de la société. |
| groupHandleArray | `types:HandleArray` | Oui | Le tableau de gestionnaires aux groupes auxquels l’utilisateur doit appartenir. |

**Sortie (setGroupMembershipReturn)**

L’API IPS ne renvoie pas de réponse pour cette opération.

## Exemples {#section-67b86d259df24938896fe19061845811}

Cet exemple de code fait de l’utilisateur un membre d’un groupe. Ajoutez un utilisateur à plusieurs groupes à l’aide du tableau de gestion des groupes.

**Requête**

```java
<ns1:setGroupMembershipParam xmlns:ns1="http://www.scene7.com/IpsApi/xsd">
   <ns1:userHandle>70|kmagnusson@adobe.com</ns1:userHandle>
   <ns1:companyHandle>47</ns1:companyHandle>
   <ns1:groupHandleArray>
      <ns1:items>225</ns1:items>
   </ns1:groupHandleArray>
</ns1:setGroupMembershipParam>
```

**Réponse**

Aucune
