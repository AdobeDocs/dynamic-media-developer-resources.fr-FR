---
title: style
description: style
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API
role: Developer,User
exl-id: a0547ada-3d8f-4ec2-a7e4-424fd1a78a28
source-git-commit: c99aac44711852d8ac661878e11ce0b19d3dbf60
workflow-type: tm+mt
source-wordcount: '97'
ht-degree: 8%

---

# style{#style}

Vous pouvez appliquer la commande suivante à partir de la chaîne de requête de l’URL et de la configuration. La commande appliquée dans la chaîne de requête de l’URL a toujours la priorité sur la même commande présente dans la configuration.

`style= *`cssPath`*`

<table id="table_F800F787CF0342749B934DAEB600C0EB"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> cssPath</span> </span> </p> </td> 
   <td colname="col2"> <p> Emplacement CSS relatif ou absolu. </p> <p>Indique l’emplacement du fichier CSS personnalisé. Si le <span class="codeph"><span class="varname"> cssPath</span></span> est relatif, il est résolu par rapport à l’emplacement de la page HTML de la visionneuse et à la valeur du paramètre <span class="codeph"> contentUrl=</span> . </p> </td> 
  </tr> 
 </tbody> 
</table>

Toutes les références de ressources dans le fichier CSS sont résolues par rapport à l’emplacement du fichier CSS, et non par rapport à l’emplacement de la page HTML appelant.

## Propriétés {#section-8ce2a4493d454d97a9975fc7f9f4eb2c}

Facultatif.

## Par défaut {#section-79a827f7a3bb4f36b3d72c309155059e}

Aucune

## Exemples {#section-f8a0c032979047a38041abfce3f7a70b}

`style=/skins/customStyle.css`

`style=etc/dam/presets/css/html5_interactiveimage.css`

`style=etc/dam/presets/css/html5_interactivevideo.css`

`style=etc/dam/presets/css/html5_carouselviewer_dotted_light.css`
