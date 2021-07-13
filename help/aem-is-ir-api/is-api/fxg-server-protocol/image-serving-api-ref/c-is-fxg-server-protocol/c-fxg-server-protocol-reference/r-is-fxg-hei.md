---
description: Hauteur d’affichage. Indique la hauteur de l’image de réponse.
solution: Experience Manager
title: hei
feature: Dynamic Media Classic, SDK/API
role: Developer,User
exl-id: dcc9311d-4157-490b-9fc4-47060ddb0e37
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '177'
ht-degree: 3%

---

# hei{#hei}

Hauteur d’affichage. Indique la hauteur de l’image de réponse.

`hei= *`val`*`

<table id="simpletable_627E67D201744588815325F3C55F76A5"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> val</span></span> </p> </td> 
  <td class="stentry"> <p>Hauteur de l’image en pixels (int supérieur à 0). </p></td> 
 </tr> 
</table>

Les formats pixellisés sont rendus à l’aide de la taille d’affichage par défaut (ou du paramètre DefaultPix ). Cliquez sur **[!UICONTROL Configuration de l’application]** > **[!UICONTROL Configuration de la publication]** > **[!UICONTROL Serveur d’images]**, puis saisissez vos valeurs Largeur et Hauteur. Des tailles plus petites offrent de meilleures performances. Vous devez enregistrer vos paramètres et effectuer une publication Image Serving pour appliquer une modification.

Si vous appliquez une commande `scale=1`, une demande de format de pixellisation est rendue à la taille spécifiée dans le FXG.

## Par défaut {#section-76ee3daa77cb468ab310821357cc9404}

Si aucune valeur `wid=`, `hei=` ou `scale=` n’est spécifiée, l’image de réponse est la taille d’affichage par défaut spécifiée dans le fichier FXG.

## Exemple {#section-a91c14d31e71481ba054412d9f642885}

[!DNL http://server/is/agm/myRootId/myImageId?hei=200]

À moins qu’un format ne soit spécifié, l’image est rendue sous la forme d’un fichier SWF. Dans ce cas, la hauteur et la largeur n’ont aucune signification, car le SWF s’étend généralement à la taille de la fenêtre du navigateur. Par conséquent, il s’applique uniquement aux formats pixellisés ou PDF. Les formats de pixellisation incluent :

* GIF
* TIF
* PNG
* JPG
* JPEG
* GIF-alpha
* TIF-alpha
* PNG-alpha
