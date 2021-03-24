---
description: Créez ou modifiez un groupe.
solution: Experience Manager
title: saveGroup
feature: Dynamic Media Classic, SDK/API
role: Développeur, Administrateur
translation-type: tm+mt
source-git-commit: 052bfcbcf1bd4ccf60afa7e3325bf58dd07cba85
workflow-type: tm+mt
source-wordcount: '99'
ht-degree: 19%

---


# saveGroup{#savegroup}

Créez ou modifiez un groupe.

Syntaxe

## Types d’utilisateur autorisés {#section-a6c1ce4c69f44ad0bcd41bbf3893bc45}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`

## Paramètres {#section-743610e98dd5494baffcbad6401038eb}

**Entrée (saveGroupParam)**

| Nom | Type | Obligatoire | Description |
|---|---|---|---|
| `*`companyHandle`*` | `xsd:string` | Oui | Poignée vers la société avec le groupe que vous souhaitez enregistrer. |
| `*`groupHandle`*` | `xsd:string` | Non | Poignée du groupe. |
| `*`name`*` | `xsd:string` | Oui | Nom du groupe. |
| `*`isSystemDefined`*` | `xsd:boolean` | Oui | `false` est définie par défaut. |

**Output (saveGroupReturn)**

| Nom | Type | Obligatoire | Description |
|---|---|---|---|
| `*`groupHandle`*` | `xsd:string` | Oui | Poignée de groupe. |

## Exemples {#section-26eee227ff1f4edabb7fa1240b4d9999}

Cet exemple de code crée un groupe qui appartient à une société spécifique. Si le groupe existe déjà, il est enregistré avec les valeurs de paramètre que vous spécifiez.

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

