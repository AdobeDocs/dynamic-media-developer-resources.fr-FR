---
description: Réglage de la luminosité. Diminue ou augmente la luminosité de l’image.
solution: Experience Manager
title: op_brightness
feature: Dynamic Media Classic,SDK/API
role: Developer,Business Practitioner
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '83'
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
