---
description: Hauteur de la vue. Indique la hauteur de l’image de réponse.
solution: Experience Manager
title: hei
feature: Dynamic Media Classic,SDK/API
role: Developer,Business Practitioner
translation-type: tm+mt
source-git-commit: d0bc88f55f857762b3bab4c76d1e3f3dd2733d60
workflow-type: tm+mt
source-wordcount: '180'
ht-degree: 3%

---


# hei{#hei}

Hauteur de la vue. Indique la hauteur de l’image de réponse.

`hei= *`val`*`

<table id="simpletable_627E67D201744588815325F3C55F76A5"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> val</span></span> </p> </td> 
  <td class="stentry"> <p>Hauteur de l’image en pixels (int supérieur à 0). </p></td> 
 </tr> 
</table>

Les formats de pixellisation sont rendus à l’aide de la taille de Vue par défaut (ou du paramètre DefaultPix). Cliquez sur **[!UICONTROL Configuration de l’application]** > **[!UICONTROL Configuration de la publication]** > **[!UICONTROL Image Server]**, puis entrez vos valeurs Largeur et Hauteur. Des tailles plus petites offrent de meilleures performances. Vous devez enregistrer vos paramètres et effectuer une publication Image Serving pour appliquer une modification.

Si vous appliquez une commande `scale=1`, une demande de format de pixellisation est générée à la taille spécifiée dans le fichier FXG.

## Par défaut {#section-76ee3daa77cb468ab310821357cc9404}

Si aucun élément `wid=`, `hei=` ou `scale=` n’est spécifié, l’image de réponse correspond à la taille de vue par défaut spécifiée dans le fichier FXG.

## Exemple {#section-a91c14d31e71481ba054412d9f642885}

[!DNL http://server/is/agm/myRootId/myImageId?hei=200]

A moins qu’un format ne soit spécifié, l’image est rendue sous la forme d’un fichier SWF. Dans ce cas, la hauteur et la largeur n’ont aucune signification, car le fichier SWF s’étend généralement à la taille de la fenêtre du navigateur. Par conséquent, hei et widgets s’appliquent uniquement aux formats pixellisés ou PDF. Les formats de pixellisation sont les suivants :

* GIF
* TIF
* PNG
* JPG
* JPEG
* GIF-alpha
* TIF-alpha
* PNG-alpha

