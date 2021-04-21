---
description: Ajoutez du bruit. Ajoute le bruit aléatoire aux données de l’image de premier plan ou au premier plan d’un calque d’effet.
solution: Experience Manager
title: op_noise
feature: Dynamic Media Classic,SDK/API
role: Developer,Business Practitioner
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '99'
ht-degree: 2%

---


# op_noise{#op-noise}

Ajoutez du bruit. Ajoute le bruit aléatoire aux données de l’image de premier plan ou au premier plan d’un calque d’effet.

`op_noise= *``*[,uniform|gaussian[, *`valmonochrome`*]]`

<table id="table_40675464E5824D52BF392ECCE2DDC03C"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> val</span> </p> </td> 
   <td colname="col2"> <p>Quantité de bruit en pourcentage (0...100 int). </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> uniforme</span> </p> </td> 
   <td colname="col2"> <p>Sélectionnez une répartition uniforme du bruit. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> gaussien</span> </p> </td> 
   <td colname="col2"> <p>Sélectionnez la distribution du bruit gaussien. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="varname"> monochrome</span> </p> </td> 
   <td colname="col2"> <p>Définissez sur 0 pour le bruit de couleur, 1 pour le bruit gris. </p> </td> 
  </tr> 
 </tbody> 
</table>

*`monochrome`* est ignorée pour les images en niveaux de gris.

## Propriétés {#section-1f1a64c791f545a3bf1abd0b0e575d87}

Calque, commande. S’applique au calque actif ou à l’image composite si `layer=comp`.

## Par défaut {#section-d548868fa4b64a60bcb481cad1f8113e}

`op_noise=0,uniform,0`, sans bruit.
