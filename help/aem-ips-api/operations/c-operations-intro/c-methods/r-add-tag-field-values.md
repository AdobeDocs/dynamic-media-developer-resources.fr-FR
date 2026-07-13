---
description: Ajoute de nouvelles valeurs de balise au dictionnaire d’un champ de balise existant.
solution: Experience Manager
title: addTagFieldValues
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 099263e4-8214-46eb-898e-7a28c4f25598
TQID: 'https://experienceleague.adobe.com/-DA9IYswE5Mfflys-Cn0Gi62OsMU3O1QYIIKYJNq9QU'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: c66ffd68-0f65-42bb-aa23-b4020f12e0bdid: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 4185012f22b173b569d11ea4d350763a82f98710
workflow-type: tm+mt
source-wordcount: 90
ht-degree: 12%

---

# addTagFieldValues{#addtagfieldvalues}

Ajoute de nouvelles valeurs de balise au dictionnaire d’un champ de balise existant.

Syntaxe

## Types d’utilisateurs autorisés {#section-ba1d7040661e48b7a6b035494e065c91}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`

## Paramètres {#section-abe8893038bb4ddfaccc11a8c75e6bd0}

**Input (addTagFieldValuesParam)**

| Nom | Type | Obligatoire | Description |
|---|---|---|---|
| companyHandle | `xsd:string` | Oui | Identifiant de la société contenant le champ de balise. |
| fieldHandle | `xsd:string` | Oui | Identifiant du champ de balise à modifier. |
| valueArray | `xsd:string` | Oui | Tableau de valeurs de balise à ajouter au dictionnaire existant du champ. |

**Output (addTagFieldValuesParam)**

L’API IPS ne renvoie pas de réponse pour cette opération.

## Exemples {#section-c4049392f1c548f883b8b1f8f167bada}

**Requête**

```java {.line-numbers}
<addTagFieldValuesParam xmlns="http://www.scene7.com/IpsApi/xsd/2010-01-31">
   <companyHandle>c|3</companyHandle>
   <fieldHandle>m|3|ASSET|SingleFixedTag</fieldHandle>
   <valueArray>
      <items>Pineapple</items>
      <items>Banana</items>
   </valueArray>
</addTagFieldValuesParam>
```

**Réponse**

Aucune

