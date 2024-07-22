---
title: wid
description: Largeur de l’affichage. Spécifie la largeur de l’image de réponse (image d’affichage).
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 5edd045c-600e-4295-9672-04a5c3bc651d
source-git-commit: 6a4c1f4425199cfa6088fc42137552748c1a9dcf
workflow-type: tm+mt
source-wordcount: '173'
ht-degree: 1%

---

# wid{#wid}

Largeur de l’affichage. Spécifie la largeur de l’image de réponse (image d’affichage).

`wid= *`val`*`

<table id="simpletable_8229FEFB366F4A799C206FD3E3C601BA"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> val</span></span> </p> </td> 
  <td class="stentry"> <p>Largeur de l’image en pixels (int supérieur à 0), </p></td> 
 </tr> 
</table>

## Par défaut {#section-830bae0b6bac440098444d7cdcb23e2e}

Si `wid=`, `hei=` et `scale=` ne sont pas spécifiés, l’image de réponse est la taille d’affichage par défaut spécifiée dans le fichier FXG.

Les formats pixellisés sont rendus à l’aide de la taille d’affichage par défaut (ou du paramètre DefaultPix ). Cliquez sur **[!UICONTROL Configuration de l’application]** > **[!UICONTROL Configuration de Publish]** > **[!UICONTROL Serveur d’images]**, puis entrez vos valeurs Largeur et Hauteur. Des tailles plus petites offrent de meilleures performances. Enregistrez vos paramètres et effectuez un Publish de diffusion d’images pour appliquer une modification.

Si vous appliquez une commande `scale=1`, une requête de format de pixellisation est rendue à la taille spécifiée dans le FXG.

## Exemple {#section-2f72cb2653d54c6aaacf0d97521fb72c}

`http://server/is/agm/myRootId/myImageId?wid=200`

À moins qu’un format ne soit spécifié, l’image est rendue sous la forme d’un fichier de SWF. Dans ce cas, la hauteur et la largeur n’ont aucune signification, car le SWF s’étend généralement à la taille de la fenêtre du navigateur. Par conséquent, `hei` et `wid` s’appliquent uniquement aux formats pixellisés ou PDF. Les formats de pixellisation incluent :

* GIF
* TIF
* PNG
* JPG
* JPEG
* GIF-alpha
* TIF-alpha
* PNG-alpha
