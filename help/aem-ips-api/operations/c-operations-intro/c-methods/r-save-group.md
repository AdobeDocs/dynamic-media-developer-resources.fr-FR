---
description: Créez ou modifiez un groupe.
seo-description: Créez ou modifiez un groupe.
seo-title: saveGroup
solution: Experience Manager
title: saveGroup
topic: Scene7 Image Production System API
uuid: d1631a55-7f1d-48b4-8b35-fd5a05277219
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# saveGroup{#savegroup}

Créez ou modifiez un groupe.

Syntaxe

## Types d’utilisateurs autorisés {#section-a6c1ce4c69f44ad0bcd41bbf3893bc45}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`

## Paramètres {#section-743610e98dd5494baffcbad6401038eb}

**Input (saveGroupParam)**

| Nom | Type | Obligatoire | Description |
|---|---|---|---|
| ` *`companyHandle`*` | `xsd:string` | Oui | Le nom d’utilisateur du avec le groupe que vous souhaitez enregistrer. |
| ` *`groupHandle`*` | `xsd:string` | Non | Poignée du groupe. |
| ` *`nom`*` | `xsd:string` | Oui | Nom du groupe. |
| ` *`isSystemDefined`*` | `xsd:boolean` | Oui | `false` est définie par défaut. |

**Output (saveGroupReturn)**

| Nom | Type | Obligatoire | Description |
|---|---|---|---|
| ` *`groupHandle`*` | `xsd:string` | Oui | Poignée du groupe. |

## Exemples {#section-26eee227ff1f4edabb7fa1240b4d9999}

Cet exemple de code crée un groupe qui appartient à un  de spécifique. Si le groupe existe déjà, il est enregistré avec les valeurs de paramètre que vous spécifiez.

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

