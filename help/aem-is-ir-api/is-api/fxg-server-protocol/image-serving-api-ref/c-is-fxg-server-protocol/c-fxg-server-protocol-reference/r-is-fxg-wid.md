---
description: Largeur  du. Indique la largeur de l’image de réponse (image de ).
seo-description: Largeur  du. Indique la largeur de l’image de réponse (image de ).
seo-title: wid
solution: Experience Manager
title: wid
topic: Scene7 Image Serving - Image Rendering API
uuid: b59b936c-abab-4f9d-95ca-0a09743ba0fb
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# wid{#wid}

Largeur  du. Indique la largeur de l’image de réponse (image de ).

`wid= *`val`*`

<table id="simpletable_8229FEFB366F4A799C206FD3E3C601BA"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> val</span></span> </p> </td> 
  <td class="stentry"> <p>Largeur de l'image en pixels (int supérieur à 0), </p></td> 
 </tr> 
</table>

## Par défaut {#section-830bae0b6bac440098444d7cdcb23e2e}

Si ni `wid=`, `hei=`, ni `scale=` ne sont spécifiés, l’image de réponse est la taille de  par défaut spécifiée dans le fichier FXG.

Les formats de pixellisation sont rendus à l’aide de la taille de  par défaut (ou du paramètre DefaultPix). Cliquez sur Configuration **[!UICONTROL de l’]** application > Configuration de la **[!UICONTROL publication]** > Serveur **** d’images, puis entrez vos valeurs Largeur et Hauteur. Des tailles plus petites offrent de meilleures performances. Vous devez enregistrer vos paramètres et effectuer une publication Image Serving pour appliquer une modification.

Si vous appliquez une `scale=1` commande, une demande de format de pixellisation est générée à la taille spécifiée dans le fichier FXG.

## Exemple {#section-2f72cb2653d54c6aaacf0d97521fb72c}

[!DNL http://server/is/agm/myRootId/myImageId?wid=200]

A moins qu’un format ne soit spécifié, l’image est générée sous la forme d’un fichier SWF. Dans ce cas, la hauteur et la largeur n’ont aucune signification, car le fichier SWF s’étend généralement à la taille de la fenêtre du navigateur. Par conséquent, il s’applique uniquement aux formats pixellisés ou PDF. Les formats de pixellisation sont les suivants :

* GIF
* TIF
* PNG
* JPG
* JPEG
* GIF-alpha
* TIF-alpha
* PNG-alpha

