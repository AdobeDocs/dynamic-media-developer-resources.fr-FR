---
description: Crée un format d’image.
solution: Experience Manager
title: saveImageFormat
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: cafbd715-237b-4454-920e-643f0c84e208
source-git-commit: 77c88d5fe20e048f6fad2bb23cb1abe090793acf
workflow-type: tm+mt
source-wordcount: '146'
ht-degree: 10%

---

# saveImageFormat{#saveimageformat}

Crée un format d’image.

>[!NOTE]
>
>La valeur du champ `urlModifier` doit être composée de code XML valide. Par exemple, remplacez `&` par `&`. Obtenez la valeur `urlModfier` à partir de l’interface utilisateur d’IPS.

## Types d’utilisateurs autorisés {#section-12c9d8d5933f4692bafb194060b4f882}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`

## Paramètres {#section-b1fc2fe8d606490ba3a2c979ab8bbd78}

**Entrée (saveImageFormatParam)**

| Nom | Type | Obligatoire | Description |
|---|---|---|---|
| companyHandle | `xsd:string` | Oui | Gestion de l’entreprise avec le format d’image que vous souhaitez utiliser. |
| imageFormatHandle | `xsd:string` | Non | Gestionnaire du format d’image que vous souhaitez enregistrer. |
| nom | `xsd:string` | Oui | Nom du format d’image. |
| urlModifier | `xsd:string` | Oui | Il peut s’agir de n’importe quelle chaîne de requête de protocole IPS. Le moyen le plus simple de générer un modificateur d’URL consiste à en créer un avec l’interface utilisateur d’IPS, puis à couper et coller la chaîne de requête. |

**Sortie (saveImageFormatReturn)**

| Nom | Type | Obligatoire | Description |
|---|---|---|---|
| imageFormatHandle | `xsd:string` | Oui | Gérer au format d’image. |

## Exemples {#section-c7bd733212ef494297a97093f3af193f}

Cet exemple de code crée un format d’image. Dans cet exemple, `urlModifier` a été déterminé par sa valeur dans l’interface utilisateur d’IPS avec un format d’HTML valide.

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
