---
description: Ajoutez du bruit. Ajoute du bruit aléatoire aux données de l’image de premier plan ou au premier plan d’une couche d’effet.
solution: Experience Manager
title: op_bruit
feature: Dynamic Media Classic, SDK/API
role: Developer,User
exl-id: eeadd3ab-80ff-4f9b-b5b7-4f3da6feebde
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '96'
ht-degree: 2%

---

# op_bruit{#op-noise}

Ajoutez du bruit. Ajoute du bruit aléatoire aux données de l’image de premier plan ou au premier plan d’une couche d’effet.

`op_noise= *``*[,uniform|gaussian[, *`valmonochrome`*]]`

<table id="table_40675464E5824D52BF392ECCE2DDC03C"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> val</span> </p> </td> 
   <td colname="col2"> <p>Quantité de bruit en pourcentage (0...100 int). </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> uniforme</span> </p> </td> 
   <td colname="col2"> <p>Sélectionnez Répartition uniforme du bruit. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> gausse</span> </p> </td> 
   <td colname="col2"> <p>Sélectionnez la répartition du bruit en gausse. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="varname"> monochrome</span> </p> </td> 
   <td colname="col2"> <p>Définissez cette valeur sur 0 pour le bruit de couleur, 1 pour le bruit gris. </p> </td> 
  </tr> 
 </tbody> 
</table>

*`monochrome`* est ignorée pour les images en niveaux de gris.

## Propriétés {#section-1f1a64c791f545a3bf1abd0b0e575d87}

Couche, commande. S’applique au calque actif ou à l’image composite si `layer=comp`.

## Par défaut {#section-d548868fa4b64a60bcb481cad1f8113e}

`op_noise=0,uniform,0`, sans bruit.
