---
description: Créez ou modifiez un groupe.
solution: Experience Manager
title: saveGroup
feature: Dynamic Media Classic, SDK/API
role: Developer,Admin
exl-id: 1dd980e7-eb38-4c90-b4fc-83327d4a95f5
source-git-commit: fcda99340a18d5037157723bb3bdca5fa9df3277
workflow-type: tm+mt
source-wordcount: '97'
ht-degree: 19%

---

# saveGroup{#savegroup}

Créez ou modifiez un groupe.

Syntaxe

## Types d’utilisateurs autorisés {#section-a6c1ce4c69f44ad0bcd41bbf3893bc45}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`

## Paramètres {#section-743610e98dd5494baffcbad6401038eb}

**Entrée (saveGroupParam)**

| Nom | Type | Obligatoire | Description |
|---|---|---|---|
| `*`companyHandle`*` | `xsd:string` | Oui | Gestionnaire de l’entreprise avec le groupe que vous souhaitez enregistrer. |
| `*`groupHandle`*` | `xsd:string` | Non | La poignée du groupe. |
| `*`name`*` | `xsd:string` | Oui | Nom du groupe. |
| `*`isSystemDefined`*` | `xsd:boolean` | Oui | `false` est la valeur par défaut. |

**Sortie (saveGroupReturn)**

| Nom | Type | Obligatoire | Description |
|---|---|---|---|
| `*`groupHandle`*` | `xsd:string` | Oui | Poignée de groupe. |

## Exemples {#section-26eee227ff1f4edabb7fa1240b4d9999}

Cet exemple de code crée un groupe qui appartient à une société spécifique. Si le groupe existe déjà, il est enregistré avec les valeurs de paramètre que vous indiquez.

**Request**

```java
<ns1:saveGroupParam xmlns:ns1="http://www.scene7.com/IpsApi/xsd">
   <ns1:companyHandle>47</ns1:companyHandle>
   <ns1:name>My Other Group</ns1:name>
   <ns1:isSystemDefined>false</ns1:isSystemDefined>
</ns1:saveGroupParam>
```

**Réponse**

```java
<saveGroupReturn xmlns="http://www.scene7.com/IpsApi/xsd">
   <groupHandle>281</groupHandle>
</saveGroupReturn>
```
