---
description: Supprime un utilisateur d’une ou de plusieurs sociétés.
solution: Experience Manager
title: removeCompanyMembership
feature: Dynamic Media Classic,SDK/API
role: Developer,Administrator
translation-type: tm+mt
source-git-commit: 052bfcbcf1bd4ccf60afa7e3325bf58dd07cba85
workflow-type: tm+mt
source-wordcount: '107'
ht-degree: 11%

---


# removeCompanyMembership{#removecompanymembership}

Supprime un utilisateur d’une ou de plusieurs sociétés.

Syntaxe

## Types d’utilisateur autorisés {#section-e9a16c8a7d8d4845989a1488c9ca9c98}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `TrialSiteAdmin`
* `ImagePortalAdmin`

## Paramètres {#section-6dfce5e44d8a4799afd0c231a0b10463}

**Entrée (removeCompanyMembershipParam)**

| Nom | Type | Obligatoire | Description |
|---|---|---|---|
| `*`userHandle`*` | `xsd:string` | Non | Nom d’utilisateur associé à l’adhésion que vous souhaitez supprimer. |
| `*`companyHandleArray`*` | `types:HandleArray` | Oui | Poignée de la société à partir de laquelle vous supprimez l’utilisateur. |

**Output (removeCompanyMembershipReturn)**

L&#39;API IPS ne renvoie pas de réponse pour cette opération.

## Exemples {#section-6b7903195e8647a1bd0502f87387ca62}

Cet exemple de code supprime un utilisateur d’une société. Omettez la poignée d&#39;utilisateur facultative pour supprimer tous les utilisateurs des sociétés spécifiées dans le tableau de poignée de société.

**Request**

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
