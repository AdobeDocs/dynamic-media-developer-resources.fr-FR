---
description: PageView.fmt
solution: Experience Manager
title: PageView.fmt
topic: Dynamic Media
uuid: bbae406c-9169-4944-8e91-f2d7c8011520
translation-type: tm+mt
source-git-commit: e4695cc4e882351ec3f2c55fd8a3cfca455bd79d
workflow-type: tm+mt
source-wordcount: '72'
ht-degree: 5%

---


# PageView.fmt{#pageview-fmt}

[!DNL `[PageView.|<containerId>_pageView.]fmt=jpg|jpeg|png|png-alpha|gif|gif-alpha`]

<table id="table_8629FDB399124A57B8026E46687D0BC2"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> jpg|jpeg|png|png-alpha|gif|gif-alpha</span> </p> </td> 
   <td colname="col2"> <p> Indique le format d’image utilisé par le composant pour le chargement des images à partir du serveur Image Server. Si le format spécifié se termine par <span class="codeph"> -alpha</span>, le composant effectue le rendu des images sous forme de contenu transparent. Pour tous les autres formats d’image, le composant traite les images comme opaques. Par défaut, le composant possède un arrière-plan blanc. Par conséquent, pour le rendre transparent, définissez la propriété CSS <span class="codeph"> Background-color</span> sur <span class="codeph"> transparent</span>. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Propriétés {#section-12a6fb2fcbc1476b95bd53ce880dc185}

Facultatif.

## Par défaut {#section-4b6a350501124ffa9a6b1b71b32eff5d}

[!DNL `jpeg`]

## Exemple {#section-7de29e43bb3640e4aa1f8984b4afddad}

[!DNL `fmt=png-alpha`]
