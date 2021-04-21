---
description: Crée un format d’image.
solution: Experience Manager
title: saveImageFormat
feature: Dynamic Media Classic,SDK/API
role: Developer,Administrator
translation-type: tm+mt
source-git-commit: 052bfcbcf1bd4ccf60afa7e3325bf58dd07cba85
workflow-type: tm+mt
source-wordcount: '153'
ht-degree: 11%

---


# saveImageFormat{#saveimageformat}

Crée un format d’image.

>[!NOTE]
>
>La valeur du champ `urlModifier` doit être composée de données XML valides. Par exemple, remplacez `&` par `&`. Récupérez la valeur `urlModfier` de l&#39;interface utilisateur IPS.

## Types d’utilisateur autorisés {#section-12c9d8d5933f4692bafb194060b4f882}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`

## Paramètres {#section-b1fc2fe8d606490ba3a2c979ab8bbd78}

**Entrée (saveImageFormatParam)**

| Nom | Type | Obligatoire | Description |
|---|---|---|---|
| `*`companyHandle`*` | `xsd:string` | Oui | Poignée vers la société avec le format d’image que vous souhaitez utiliser. |
| `*`imageFormatHandle`*` | `xsd:string` | Non | Poignée de format d’image à enregistrer. |
| `*`name`*` | `xsd:string` | Oui | Nom du format d’image. |
| `*`urlModificateur`*` | `xsd:string` | Oui | Il peut s&#39;agir de n&#39;importe quelle chaîne de requête de protocole IPS. Le moyen le plus simple de générer un modificateur d&#39;URL consiste à en créer un avec l&#39;interface utilisateur d&#39;IPS, puis à couper et coller la chaîne de requête. |

**Output (saveImageFormatReturn)**

| Nom | Type | Obligatoire | Description |
|---|---|---|---|
| `*`imageFormatHandle`*` | `xsd:string` | Oui | Passez au format d’image. |

## Exemples {#section-c7bd733212ef494297a97093f3af193f}

Cet exemple de code crée un format d’image. Dans cet exemple, `urlModifier` a été déterminé par sa valeur dans l&#39;interface utilisateur d&#39;IPS avec un format HTML valide.

**Request**

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

