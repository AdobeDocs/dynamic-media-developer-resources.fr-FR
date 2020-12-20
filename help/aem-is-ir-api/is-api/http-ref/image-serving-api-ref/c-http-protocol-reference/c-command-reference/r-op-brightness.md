---
description: Réglage de la luminosité. Diminue ou augmente la luminosité de l’image.
seo-description: Réglage de la luminosité. Diminue ou augmente la luminosité de l’image.
seo-title: op_brightness
solution: Experience Manager
title: op_brightness
topic: Scene7 Image Serving - Image Rendering API
uuid: 751ec9e5-4a70-438d-950c-deff4db034b1
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '85'
ht-degree: 3%

---


# op_brightness{#op-brightness}

Réglage de la luminosité. Diminue ou augmente la luminosité de l’image.

`op_brightness= *`adj`*`

<table id="simpletable_2B5DB95B1FF044C8BD226D4F8311E806"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> adj</span> </p> </td> 
  <td class="stentry"> <p>Réglage de la luminosité (-100...+100 int). </p></td> 
 </tr> 
</table>

## Propriétés {#section-c7e757f63b2c4b5ebaacbadb51c72ce4}

Calque, commande. S’applique au calque actif ou à l’image composite si `layer=comp`. Ignoré par les calques d’effet. Les images ou calques CMJN sont convertis en RVB avant l’application de l’opération.

## Par défaut {#section-be56be0759634c79b4f264f194a94dbc}

`op_brightness=0`, sans changement de luminosité.

## Exemple {#section-c25f952f1b77409abb9ccf885862d75c}

Assommez légèrement l’arrière-plan d’une image pour mettre en évidence le contenu de premier plan :

`http://server/myRootId/myImageId?wid=500&layer=0&maskUse=invert&op_brightness=-10&layer=1&src=myRootId/myImageId`
