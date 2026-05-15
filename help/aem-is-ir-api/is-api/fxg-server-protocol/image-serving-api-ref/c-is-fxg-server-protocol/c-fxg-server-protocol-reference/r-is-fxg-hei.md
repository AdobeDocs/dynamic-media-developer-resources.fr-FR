---
title: établissement d'enseignement supérieur
description: Hauteur de la vue. Indique la hauteur de l’image de réponse.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: dcc9311d-4157-490b-9fc4-47060ddb0e37
TQID: 'https://experienceleague.adobe.com/Tpl8zVXQVzs3isa26A3YvnOzs6gqpz3-4L-qDBx-eK0'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 174
ht-degree: 1%

---

# établissement d&#39;enseignement supérieur{#hei}

Hauteur de la vue. Indique la hauteur de l’image de réponse.

`hei= *`val`*`

<table id="simpletable_627E67D201744588815325F3C55F76A5"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> val</span></span> </p> </td> 
  <td class="stentry"> <p>Hauteur de l’image en pixels (nombre entier supérieur à 0). </p></td> 
 </tr> 
</table>

Les formats de trame sont rendus à l’aide de la Taille d’affichage par défaut (ou du paramètre DefaultPix). Sélectionnez **[!UICONTROL Configuration de l’application]** > **[!UICONTROL Configuration de la publication]** > **[!UICONTROL Serveur d’images]**, puis saisissez vos valeurs de largeur et de hauteur. Des tailles plus petites offrent de meilleures performances. Enregistrez vos paramètres et effectuez une publication d’image pour appliquer une modification.

Si vous appliquez une commande `scale=1`, une demande de format de trame est générée à la taille spécifiée dans le FXG.

## Par défaut {#section-76ee3daa77cb468ab310821357cc9404}

Si `wid=`, `hei=` ou `scale=` ne sont pas spécifiés, l’image de réponse correspond à la taille d’affichage par défaut spécifiée dans le fichier FXG.

## Exemple {#section-a91c14d31e71481ba054412d9f642885}

[!DNL `http://server/is/agm/myRootId/myImageId?hei=200`]

Sauf si un format est spécifié, l’image est rendue sous la forme d’un fichier SWF. Dans ce cas, hauteur et largeur n’ont aucune signification, car le SWF s’étend généralement à la taille de la fenêtre du navigateur. Par conséquent, les formats hei et wid ne s’appliquent qu’aux formats matriciels ou PDF. Les formats de trame sont les suivants :

* GIF
* TIF
* PNG
* JPG
* JPEG
* GIF-alpha
* TIF-alpha
* PNG-alpha
