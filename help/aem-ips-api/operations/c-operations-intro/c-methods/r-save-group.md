---
description: Créez ou modifiez un groupe.
solution: Experience Manager
title: saveGroup
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 1dd980e7-eb38-4c90-b4fc-83327d4a95f5
TQID: 'https://experienceleague.adobe.com/VTDPxH7rjfnALgRNc-Md6NLKZfOrRk6CqQhGi0JNZs4'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 92
ht-degree: 18%

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
| companyHandle | `xsd:string` | Oui | Le handle de la société avec le groupe que vous souhaitez enregistrer. |
| groupHandle | `xsd:string` | Non | La poignée du groupe. |
| nom | `xsd:string` | Oui | Nom du groupe. |
| isSystemDefined | `xsd:boolean` | Oui | `false` est la valeur par défaut. |

**Output (saveGroupReturn)**

| Nom | Type | Obligatoire | Description |
|---|---|---|---|
| groupHandle | `xsd:string` | Oui | Identifiant du groupe. |

## Exemples {#section-26eee227ff1f4edabb7fa1240b4d9999}

Cet exemple de code crée un groupe qui appartient à une société spécifique. Si le groupe existe déjà, il est enregistré avec les valeurs de paramètre que vous spécifiez.

**Requête**

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
