---
description: Réglez la saturation. Modifie la saturation de chaque pixel visible du calque ou de l’image composite.
solution: Experience Manager
title: op_saturation
feature: Dynamic Media Classic, SDK/API
role: Developer,User
exl-id: cd71e27e-6ccc-4ade-9bcf-af8e41bcf381
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '95'
ht-degree: 3%

---

# op_saturation{#op-saturation}

Réglez la saturation. Modifie la saturation de chaque pixel visible du calque ou de l’image composite.

`op_saturation= *`adj`*`

<table id="simpletable_5F118A28FE674B06A16F6F19C56B4594"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> adj</span> </p> </td> 
  <td class="stentry"> <p>Ajustement de la saturation (-100..+100 int). </p></td> 
 </tr> 
</table>

`op_saturation=-100` dénature complètement l’image.

## Propriétés {#section-9a3cc9ff060049449554dfa69d92fd53}

Couche, commande. S’applique au calque actif ou à l’image composite si `layer=comp`. Ignoré par les calques d’effet.

## Par défaut {#section-ef0e78f55c8b4d22aee09104dad6410a}

`op_saturation=0`, pour aucune modification de la saturation. Les images ou calques CMJN sont convertis en RVB avant l’application de l’opération.

## Exemple {#section-033b272f1b7e4efeb94e841fd8095357}

Manipuler une photo en couleur pour obtenir un aspect &quot;haute touche&quot; :

`http://server/myRootId/myImageId?op_saturation=-60&op_brightness=45&op_contrast=-35`
