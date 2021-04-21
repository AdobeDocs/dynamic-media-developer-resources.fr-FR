---
description: Définit l’appartenance au groupe des utilisateurs appartenant à une société spécifique.
solution: Experience Manager
title: setGroupMembers
feature: Dynamic Media Classic,SDK/API
role: Developer,Administrator
translation-type: tm+mt
source-git-commit: 052bfcbcf1bd4ccf60afa7e3325bf58dd07cba85
workflow-type: tm+mt
source-wordcount: '133'
ht-degree: 9%

---


# setGroupMembers{#setgroupmembers}

Définit l’appartenance au groupe des utilisateurs appartenant à une société spécifique.

L&#39;opération déclenche une erreur d&#39;authentification si vous ne disposez pas de privilèges pour effectuer cette opération. Cela est également vrai si l&#39;un des utilisateurs du tableau de pseudo n&#39;appartient pas à la société spécifiée dans le descripteur de société,

## Types d’utilisateur autorisés {#section-4523594039c24aa29c8d0d5c9c415391}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`

## Paramètres {#section-6a18562fc8e942af94be10bbb8c51151}

**Entrée (setGroupMembersParam)**

| Nom | Type | Obligatoire | Description |
|---|---|---|---|
| `*`companyHandle`*` | `xsd:string` | Oui | Poignée de société. |
| `*`groupHandle`*` | `xsd:string` | Oui | Poignée de groupe. |
| `*`userHandleArray`*` | `types:HandleArray` | Oui | Tableau de poignées pour les utilisateurs dont vous souhaitez définir l’appartenance au groupe. |

**Output (setGroupMembesReturn)**

L&#39;API IPS ne renvoie pas de réponse pour cette opération.

## Exemples {#section-9c528c3f44a141ce9eaddf634f26c487}

Cet exemple de code définit l&#39;appartenance à un groupe pour un seul utilisateur.

**Request**

```java
<ns1:setGroupMembersParam xmlns:ns1="http://www.scene7.com/IpsApi/xsd">
   <ns1:companyHandle>47</ns1:companyHandle>
   <ns1:groupHandle>225</ns1:groupHandle>
   <ns1:userHandleArray>
      <ns1:items>70|kmagnusson@adobe.com</ns1:items>
   </ns1:userHandleArray>
</ns1:setGroupMembersParam>
```

**Réponse**

Aucune
