---
description: Crée un format d’image.
solution: Experience Manager
title: saveImageFormat
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: cafbd715-237b-4454-920e-643f0c84e208
TQID: 'https://experienceleague.adobe.com/kP25DoK-SIRIYh69I8tE07KH4dI-GFZf9JjUZjG-lFw'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 146
ht-degree: 10%

---

# saveImageFormat{#saveimageformat}

Crée un format d’image.

>[!NOTE]
>
>La valeur du champ `urlModifier` doit être composée d’un XML valide. Par exemple, remplacez `&` par `&`. Obtenez la valeur `urlModfier` à partir de l’interface utilisateur IPS.

## Types d’utilisateurs autorisés {#section-12c9d8d5933f4692bafb194060b4f882}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`

## Paramètres {#section-b1fc2fe8d606490ba3a2c979ab8bbd78}

**Input (saveImageFormatParam)**

| Nom | Type | Obligatoire | Description |
|---|---|---|---|
| companyHandle | `xsd:string` | Oui | La poignée de la société avec le format d’image que vous souhaitez utiliser. |
| imageFormatHandle | `xsd:string` | Non | Identifiant du format d’image à enregistrer. |
| nom | `xsd:string` | Oui | Nom du format de l’image. |
| urlModifier | `xsd:string` | Oui | Il peut s’agir de n’importe quelle chaîne de requête de protocole IPS. Le moyen le plus simple de générer un modificateur d’URL consiste à en créer un avec l’interface utilisateur IPS, puis à couper et coller la chaîne de requête. |

**Output (saveImageFormatReturn)**

| Nom | Type | Obligatoire | Description |
|---|---|---|---|
| imageFormatHandle | `xsd:string` | Oui | Gérer au format de l’image. |

## Exemples {#section-c7bd733212ef494297a97093f3af193f}

Cet exemple de code crée un format d’image. Dans cet exemple, `urlModifier` a été déterminé par sa valeur dans l’interface utilisateur IPS avec un format HTML valide.

**Requête**

```java
<saveImageFormatParam xmlns="http://www.scene7.com/IpsApi/xsd"> 
   <companyHandle>47</companyHandle> 
   <name>My Image Format Name</name> 
   <urlModifier>wid=400&amp;hei=400&amp;fmt=jpeg&amp;qlt=750&amp;op_sharpen=0&amp; 
   resMode=bicub&amp;op_usm=0.0,0.0,0,0&amp;iccEmbed=0 
   </urlModifier> 
</saveImageFormatParam>
```

**Réponse**

```java
<saveImageFormatReturn xmlns="http://www.scene7.com/IpsApi/xsd"> 
   <imageFormatHandle>47|301</imageFormatHandle> 
</saveImageFormatReturn>
```
