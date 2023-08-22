---
title: op_brightness
description: Ajustez la luminosité. Diminue ou augmente la luminosité de l’image.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 390ed812-87ae-41e7-8021-65dd95915ae8
source-git-commit: 7a07ec9550c0685c908191dd6806d5b84678820d
workflow-type: tm+mt
source-wordcount: '75'
ht-degree: 2%

---

# op_brightness{#op-brightness}

Ajustez la luminosité. Diminue ou augmente la luminosité de l’image.

`op_brightness= *`adj`*`

<table id="simpletable_2B5DB95B1FF044C8BD226D4F8311E806"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> adj</span> </p> </td> 
  <td class="stentry"> <p>Ajustement de la luminosité (-100...+100 int). </p></td> 
 </tr> 
</table>

## Propriétés {#section-c7e757f63b2c4b5ebaacbadb51c72ce4}

Couche, commande. S’applique au calque actif ou à l’image composite si `layer=comp`. Ignoré par les calques d’effet. Les images ou calques CMJN sont convertis en RGB avant l’application de l’opération.

## Par défaut {#section-be56be0759634c79b4f264f194a94dbc}

`op_brightness=0`, pour aucun changement de luminosité.

## Exemple {#section-c25f952f1b77409abb9ccf885862d75c}

Obscurcissez légèrement l’arrière-plan d’une image pour mettre l’accent sur le contenu de premier plan :

`http://server/myRootId/myImageId?wid=500&layer=0&maskUse=invert&op_brightness=-10&layer=1&src=myRootId/myImageId`
