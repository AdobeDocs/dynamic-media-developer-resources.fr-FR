---
title: FlyoutZoomView.fmt
description: FlyoutZoomView.fmt
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Flyout
role: Developer,User
exl-id: 4e1ce754-6967-492b-a617-764ee3ec3a55
source-git-commit: 50dddf148345d2ca5243d5d7108fefa56d23dad6
workflow-type: tm+mt
source-wordcount: '73'
ht-degree: 4%

---

# FlyoutZoomView.fmt{#flyoutzoomview-fmt}

`[FlyoutZoomView.|<containerId>_flyout.]fmt=jpg|jpeg|png|png-alpha|gif|gif-alpha`

<table id="table_12B0B59D83BC40FCB957F41B331A1EF9"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> jpg|jpeg|png|png-alpha|gif-alpha</span> </p> </td> 
   <td colname="col2"> <p> Spécifie le format d’image à utiliser par le composant pour le chargement des images à partir du serveur d’images. Si le format spécifié se termine par <span class="codeph"> "-alpha"</span>, le composant effectue le rendu des images en tant que contenu transparent. Pour tous les autres formats d’image, le composant traite les images comme opaques. Par défaut, l’arrière-plan du composant est blanc. Par conséquent, pour le rendre transparent, définissez la propriété CSS <span class="codeph"> background-color</span> sur <span class="codeph"> transparent</span>. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Propriétés {#section-5526a5d19e7e4ee2a35b1c4816ed4202}

Facultatif.

## Par défaut {#section-a08032f0fcf041c09e63c0238a339fc9}

`jpeg`

## Exemple {#section-0338be21edd04ff1a3bed5c8319b61a4}

`fmt=png-alpha`
