---
description: Renvoie les membres d’un groupe.
seo-description: Renvoie les membres d’un groupe.
seo-title: getGroupMembership
solution: Experience Manager
title: getGroupMembership
uuid: 5ec48e8c-378b-43a3-b3dc-aa21dbf339b5
feature: Dynamic Media Classic, SDK/API
role: Développeur, Administrateur
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '94'
ht-degree: 17%

---


# getGroupMembership{#getgroupmembership}

Renvoie les membres d’un groupe.

Syntaxe

## Types d’utilisateur autorisés {#section-35d070e5c4d74ca69df508368953cfb8}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`
* `ImagePortalUser`
* `ImagePortalContrib`
* `ImagePortalContribUser`

## Paramètres {#section-2e92f850254e46e48403acaa215341a5}

**Entrée (getGroupMembershipParam)**

| Nom | Type | Obligatoire | Description |
|---|---|---|---|
| `*`userHandle`*` | `xsd:string` | Non | Nom d’utilisateur. |
| `*`companyHandle`*` | `xsd:string` | Non | La poignée de la société. |

**Output (getGroupMembershipReturn)**

| Nom | Type | Obligatoire | Description |
|---|---|---|---|
| `*`groupArray`*` | `types:GroupArray` | Oui | Tableau de groupes. |

## Exemples {#section-ebb437369f4f4487b3eb2ef0c078b8ae}

Cet exemple de code renvoie tous les membres d&#39;un groupe. La société et les poignées utilisateur étant facultatives, l’opération peut renvoyer tous les membres de tous les groupes.

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

