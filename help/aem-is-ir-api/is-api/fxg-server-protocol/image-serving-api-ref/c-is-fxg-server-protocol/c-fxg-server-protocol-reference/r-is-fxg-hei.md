---
title: hei
description: Hauteur d’affichage. Indique la hauteur de l’image de réponse.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: dcc9311d-4157-490b-9fc4-47060ddb0e37
source-git-commit: 38f3e425be0ce3e241fc18b477e3f68b7b763b51
workflow-type: tm+mt
source-wordcount: '171'
ht-degree: 1%

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

Les formats pixellisés sont rendus à l’aide de la taille d’affichage par défaut (ou du paramètre DefaultPix ). Sélectionnez **[!UICONTROL Configuration de l’application]** > **[!UICONTROL Configuration de Publish]** > **[!UICONTROL Serveur d’images]**, puis saisissez vos valeurs Largeur et Hauteur. Des tailles plus petites offrent de meilleures performances. Enregistrez vos paramètres et effectuez un Publish de diffusion d’images pour appliquer une modification.

Si vous appliquez une commande `scale=1`, une requête de format de pixellisation est rendue à la taille spécifiée dans le FXG.

## Par défaut {#section-76ee3daa77cb468ab310821357cc9404}

Si `wid=`, `hei=` ou `scale=` ne sont pas spécifiés, l’image de réponse est la taille d’affichage par défaut spécifiée dans le fichier FXG.

## Exemple {#section-a91c14d31e71481ba054412d9f642885}

[!DNL `http://server/is/agm/myRootId/myImageId?hei=200`]

À moins qu’un format ne soit spécifié, l’image est rendue sous la forme d’un fichier de SWF. Dans ce cas, la hauteur et la largeur n’ont aucune signification, car le SWF s’étend généralement à la taille de la fenêtre du navigateur. Par conséquent, sa valeur et s’appliquent uniquement aux formats pixellisés ou PDF. Les formats de pixellisation incluent :

* GIF
* TIF
* PNG
* JPG
* JPEG
* GIF-alpha
* TIF-alpha
* PNG-alpha
