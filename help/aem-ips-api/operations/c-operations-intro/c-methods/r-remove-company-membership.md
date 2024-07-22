---
description: Supprime un utilisateur d’une ou de plusieurs entreprises.
solution: Experience Manager
title: removeCompanyMembership
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 1cb9a286-48a0-4542-a80a-c97fd973474e
source-git-commit: 77c88d5fe20e048f6fad2bb23cb1abe090793acf
workflow-type: tm+mt
source-wordcount: '100'
ht-degree: 10%

---

# removeCompanyMembership{#removecompanymembership}

Supprime un utilisateur d’une ou de plusieurs entreprises.

Syntaxe

## Types d’utilisateurs autorisés {#section-e9a16c8a7d8d4845989a1488c9ca9c98}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `TrialSiteAdmin`
* `ImagePortalAdmin`

## Paramètres {#section-6dfce5e44d8a4799afd0c231a0b10463}

**Entrée (removeCompanyMembershipParam)**

| Nom | Type | Obligatoire | Description |
|---|---|---|---|
| userHandle | `xsd:string` | Non | Gestionnaire pour l’utilisateur avec l’appartenance que vous souhaitez supprimer. |
| companyHandleArray | `types:HandleArray` | Oui | Gestionnaire de la société à laquelle vous supprimez l’utilisateur. |

**Sortie (removeCompanyMembershipReturn)**

L’API IPS ne renvoie pas de réponse pour cette opération.

## Exemples {#section-6b7903195e8647a1bd0502f87387ca62}

Cet exemple de code supprime un utilisateur d’une société. Omettez la poignée d’utilisateur facultative pour supprimer tous les utilisateurs de la société spécifiée dans le tableau de gestionnaires de société.

**Requête**

```java
<ns1:removeCompanyMembershipParam xmlns:ns1="http://www.scene7.com/IpsApi/xsd">
   <ns1:userHandle>621|jduvar@adobe.com</ns1:userHandle>
   <ns1:companyHandleArray>
      <ns1:items>47</ns1:items>
   </ns1:companyHandleArray>
</ns1:removeCompanyMembershipParam>
```

**Réponse**

Aucune
