---
description: style
solution: Experience Manager
title: style
feature: Dynamic Media Classic,Viewers,SDK/API
role: Developer,Business Practitioner
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '106'
ht-degree: 7%

---


# style{#style}

Vous pouvez appliquer la commande suivante à partir de la chaîne de requête d’URL et de la configuration. La commande appliquée dans la chaîne de requête d’URL est toujours prioritaire sur la même commande que celle présente dans la configuration.

`style= *`cssPath`*`

<table id="table_F800F787CF0342749B934DAEB600C0EB"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> cssPath</span> </span> </p> </td> 
   <td colname="col2"> <p> Emplacement CSS relatif ou absolu. </p> <p>Indique l’emplacement du fichier CSS personnalisé. Si <span class="codeph"><span class="varname"> cssPath</span></span> est relatif, il est résolu par rapport à l’emplacement de la page HTML de la visionneuse et à la valeur du paramètre <span class="codeph"> contentUrl=</span>. </p> </td> 
  </tr> 
 </tbody> 
</table>

Toutes les références de fichier dans le fichier CSS sont résolues par rapport à l’emplacement du fichier CSS, et non par rapport à l’emplacement de la page HTML appelante.

## Propriétés {#section-8ce2a4493d454d97a9975fc7f9f4eb2c}

Facultatif.

## Par défaut {#section-79a827f7a3bb4f36b3d72c309155059e}

Aucune

## Exemples {#section-f8a0c032979047a38041abfce3f7a70b}

`style=/skins/customStyle.css`

`style=etc/dam/presets/css/html5_interactiveimage.css`

`style=etc/dam/presets/css/html5_interactivevideo.css`

`style=etc/dam/presets/css/html5_carouselviewer_dotted_light.css`
