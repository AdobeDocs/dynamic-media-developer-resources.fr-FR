---
title: op_noise
description: Ajoutez du bruit. Ajoute un bruit aléatoire aux données d’image de premier plan ou au premier plan d’un calque d’effets.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: eeadd3ab-80ff-4f9b-b5b7-4f3da6feebde
source-git-commit: 7a07ec9550c0685c908191dd6806d5b84678820d
workflow-type: tm+mt
source-wordcount: '93'
ht-degree: 1%

---

# op_noise{#op-noise}

Ajoutez du bruit. Ajoute un bruit aléatoire aux données d’image de premier plan ou au premier plan d’un calque d’effets.

`op_noise= *``*[,uniform|gaussian[, *`Val monochrome`*]]`

<table id="table_40675464E5824D52BF392ECCE2DDC03C"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> Val</span> </p> </td> 
   <td colname="col2"> <p>Quantité de bruit en pourcentage (0... 100 int). </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> uniforme</span> </p> </td> 
   <td colname="col2"> <p>Sélectionnez une répartition uniforme du bruit. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> gaussien</span> </p> </td> 
   <td colname="col2"> <p>Sélectionnez la répartition gaussienne du bruit. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="varname"> monochrome</span> </p> </td> 
   <td colname="col2"> <p>Défini sur 0 pour le bruit de couleur et sur 1 pour le bruit gris. </p> </td> 
  </tr> 
 </tbody> 
</table>

*`monochrome`* est ignorée pour les images en niveaux de gris.

## Propriétés {#section-1f1a64c791f545a3bf1abd0b0e575d87}

Calque, commande S’applique au calque actif ou à l’image composite si `layer=comp`.

## Par défaut {#section-d548868fa4b64a60bcb481cad1f8113e}

`op_noise=0,uniform,0`, sans bruit.
