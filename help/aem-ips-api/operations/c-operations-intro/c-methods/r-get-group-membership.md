---
description: Renvoie les membres d’un groupe.
seo-description: Renvoie les membres d’un groupe.
seo-title: getGroupMember
solution: Experience Manager
title: getGroupMember
topic: Scene7 Image Production System API
uuid: 5ec48e8c-378b-43a3-b3dc-aa21dbf339b5
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# getGroupMember{#getgroupmembership}

Renvoie les membres d’un groupe.

Syntaxe

## Types d’utilisateurs autorisés {#section-35d070e5c4d74ca69df508368953cfb8}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`
* `ImagePortalUser`
* `ImagePortalContrib`
* `ImagePortalContribUser`

## Paramètres {#section-2e92f850254e46e48403acaa215341a5}

**Entrée (getGroupMembshipParam)**

| Nom | Type | Obligatoire | Description |
|---|---|---|---|
| ` *`userHandle`*` | `xsd:string` | Non | Identifiant de l’utilisateur. |
| ` *`companyHandle`*` | `xsd:string` | Non | La poignée du. |

**Output (getGroupMembshipReturn)**

| Nom | Type | Obligatoire | Description |
|---|---|---|---|
| ` *`groupArray`*` | `types:GroupArray` | Oui | Tableau de groupes. |

## Exemples {#section-ebb437369f4f4487b3eb2ef0c078b8ae}

Cet exemple de code renvoie tous les membres d’un groupe. Comme les  et les poignées utilisateur sont facultatives, l’opération peut renvoyer tous les membres de tous les groupes.

**Request**

```java
<ns1:getGroupMembershipParam xmlns:ns1="http://www.scene7.com/IpsApi/xsd">
   <ns1:companyHandle>47</ns1:companyHandle>
</ns1:getGroupMembershipParam>
```

**Réponse**

```java
<getGroupMembershipReturn xmlns="http://www.scene7.com/IpsApi/xsd">
   <groupArray>
      <items>
         <groupHandle>225</groupHandle><companyHandle>47</companyHandle><name>MyGroup</name><isSystemDefined>false</isSystemDefined></items></groupArray></getGroupMembershipReturn>
```

