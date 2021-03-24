---
description: Largeur de la vue. Indique la largeur de l’image de réponse (image de vue).
solution: Experience Manager
title: wid
feature: Dynamic Media Classic, SDK/API
role: Développeur, Professionnel
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '184'
ht-degree: 3%

---


# wid{#wid}

Largeur de la vue. Indique la largeur de l’image de réponse (image de vue).

`wid= *`val`*`

<table id="simpletable_8229FEFB366F4A799C206FD3E3C601BA"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> val</span></span> </p> </td> 
  <td class="stentry"> <p>Largeur de l’image en pixels (int supérieur à 0), </p></td> 
 </tr> 
</table>

## Par défaut {#section-830bae0b6bac440098444d7cdcb23e2e}

Si aucun élément `wid=`, `hei=` ou `scale=` n’est spécifié, l’image de réponse correspond à la taille de vue par défaut spécifiée dans le fichier FXG.

Les formats de pixellisation sont rendus à l’aide de la taille de Vue par défaut (ou du paramètre DefaultPix). Cliquez sur **[!UICONTROL Configuration de l’application]** > **[!UICONTROL Configuration de la publication]** > **[!UICONTROL Image Server]**, puis entrez vos valeurs Largeur et Hauteur. Des tailles plus petites offrent de meilleures performances. Vous devez enregistrer vos paramètres et effectuer une publication Image Serving pour appliquer une modification.

Si vous appliquez une commande `scale=1`, une demande de format de pixellisation est générée à la taille spécifiée dans le fichier FXG.

## Exemple {#section-2f72cb2653d54c6aaacf0d97521fb72c}

[!DNL http://server/is/agm/myRootId/myImageId?wid=200]

A moins qu’un format ne soit spécifié, l’image est rendue sous la forme d’un fichier SWF. Dans ce cas, la hauteur et la largeur n’ont aucune signification, car le fichier SWF s’étend généralement à la taille de la fenêtre du navigateur. Par conséquent, hei et widgets s’appliquent uniquement aux formats pixellisés ou PDF. Les formats de pixellisation sont les suivants :

* GIF
* TIF
* PNG
* JPG
* JPEG
* GIF-alpha
* TIF-alpha
* PNG-alpha

