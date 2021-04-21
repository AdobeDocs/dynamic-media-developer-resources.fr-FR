---
description: PageView.iscommand
solution: Experience Manager
title: PageView.iscommand
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog Search
role: Developer,Business Practitioner
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '68'
ht-degree: 7%

---


# PageView.iscommand{#pageview-iscommand}

[!DNL `[PageView.|<containerId>_pageView.]iscommand= *`isCommand`*`]

<table id="table_9E7BB12BF371419F88DD4D24EF04632C"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"><span class="varname"> isCommand</span></span> </p> </td> 
   <td colname="col2"> <p> Chaîne de commande Diffusion d’images appliquée à l’image de la page. Si elle est spécifiée dans l’URL, toutes les occurrences de <span class="codeph"> &amp;</span> et <span class="codeph"> =</span> doivent être codées en HTTP sous la forme <span class="codeph"> %26</span> et <span class="codeph"> %3D</span>, respectivement. </p> <p> <p>Remarque :  Les commandes de manipulation de dimensionnement d’image ne sont pas prises en charge. </p> </p> </td> 
  </tr> 
 </tbody> 
</table>

## Propriétés {#section-df5a0604766b4ac2b9a6742b377e427c}

Facultatif.

## Par défaut {#section-9f2bf4c418e5441c9fff3eb755f7bda6}

Aucune

## Exemple {#section-813de2905d6c44c0991cfe0931581462}

Lorsqu’elle est spécifiée dans l’URL de la visionneuse.

[!DNL `iscommand=op_sharpen%3d1%26op_colorize%3d0xff0000`]

Lorsqu’elle est spécifiée dans les données de configuration.

[!DNL `iscommand=op_sharpen=1&op_colorize=0xff0000`]
