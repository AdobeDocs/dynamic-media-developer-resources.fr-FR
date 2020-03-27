---
description: ' hauteur. Indique la hauteur de l’image de réponse.'
seo-description: ' hauteur. Indique la hauteur de l’image de réponse.'
seo-title: hei
solution: Experience Manager
title: hei
topic: Scene7 Image Serving - Image Rendering API
uuid: 6f7e580b-6399-4661-b5d9-8044574ba124
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# hei{#hei}

 hauteur. Indique la hauteur de l’image de réponse.

`hei= *`val`*`

<table id="simpletable_627E67D201744588815325F3C55F76A5"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> val</span></span> </p> </td> 
  <td class="stentry"> <p>Hauteur de l’image en pixels (int supérieur à 0). </p></td> 
 </tr> 
</table>

Les formats de pixellisation sont rendus à l’aide de la taille de  par défaut (ou du paramètre DefaultPix). Cliquez sur Configuration **[!UICONTROL de l’]** application > Configuration de la **[!UICONTROL publication]** > Serveur **** d’images, puis entrez vos valeurs Largeur et Hauteur. Des tailles plus petites offrent de meilleures performances. Vous devez enregistrer vos paramètres et effectuer une publication Image Serving pour appliquer une modification.

Si vous appliquez une `scale=1` commande, une demande de format de pixellisation est générée à la taille spécifiée dans le fichier FXG.

## Par défaut {#section-76ee3daa77cb468ab310821357cc9404}

Si ni `wid=`, `hei=`, ni `scale=` ne sont spécifiés, l’image de réponse est la taille de  par défaut spécifiée dans le fichier FXG.

## Exemple {#section-a91c14d31e71481ba054412d9f642885}

[!DNL http://server/is/agm/myRootId/myImageId?hei=200]

A moins qu’un format ne soit spécifié, l’image est générée sous la forme d’un fichier SWF. Dans ce cas, la hauteur et la largeur n’ont aucune signification, car le fichier SWF s’étend généralement à la taille de la fenêtre du navigateur. Par conséquent, il s’applique uniquement aux formats pixellisés ou PDF. Les formats de pixellisation sont les suivants :

* GIF
* TIF
* PNG
* JPG
* JPEG
* GIF-alpha
* TIF-alpha
* PNG-alpha

