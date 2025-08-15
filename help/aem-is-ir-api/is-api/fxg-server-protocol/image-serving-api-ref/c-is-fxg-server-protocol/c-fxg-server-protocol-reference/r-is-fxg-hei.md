---
title: Hei
description: Hauteur de la vue. Spécifie la hauteur de l’image de réponse.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: dcc9311d-4157-490b-9fc4-47060ddb0e37
source-git-commit: 38f3e425be0ce3e241fc18b477e3f68b7b763b51
workflow-type: tm+mt
source-wordcount: '171'
ht-degree: 1%

---

# Hei{#hei}

Hauteur de la vue. Spécifie la hauteur de l’image de réponse.

`hei= *`Val`*`

<table id="simpletable_627E67D201744588815325F3C55F76A5"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"><span class="varname"> Val</span></span> </p> </td> 
  <td class="stentry"> <p>Hauteur d’image en pixels (int supérieur à 0). </p></td> 
 </tr> 
</table>

Les formats raster sont rendus à l’aide de la taille d’affichage par défaut (ou du paramètre DefaultPix). Sélectionnez **[!UICONTROL Configuration de]** l’application > **[!UICONTROL Configuration Publish Configuration]** > **[!UICONTROL Image Server]**, puis entrez vos valeurs Largeur et Hauteur. Des tailles plus petites offrent de meilleures performances. Enregistrez vos paramètres et effectuez une Publish de diffusion d’images pour appliquer une modification.

Si vous appliquez une `scale=1` commande, une demande de format raster est rendue à la taille spécifiée dans le FXG.

## Par défaut {#section-76ee3daa77cb468ab310821357cc9404}

Si `wid=`, `hei=`ou `scale=` ne sont pas spécifiées, l’image de réponse correspond à la taille d’affichage par défaut spécifiée dans le fichier FXG.

## Exemple {#section-a91c14d31e71481ba054412d9f642885}

[!DNL `http://server/is/agm/myRootId/myImageId?hei=200`]

À moins qu’un format ne soit spécifié, l’image est rendue au format SWF. Dans ce cas, la hauteur et la largeur n’ont aucune signification, car le SWF s’étend généralement à la taille de la fenêtre du navigateur. Par conséquent, hei et wid ne s’appliquent qu’aux formats raster ou PDF. Les formats de raster incluent :

* GIF
* FIT
* PNG
* JPG (en anglais)
* JPEG
* GIF alpha
* TIF-alpha
* PNG-alpha
