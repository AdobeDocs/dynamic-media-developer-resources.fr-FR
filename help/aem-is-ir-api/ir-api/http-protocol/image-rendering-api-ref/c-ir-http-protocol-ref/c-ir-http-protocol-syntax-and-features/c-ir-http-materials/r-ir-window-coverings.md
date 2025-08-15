---
title: Revêtements de fenêtre
description: Les revêtements de fenêtre comprennent des revêtements de fenêtre souples (draps, valises, rideaux de café) et des revêtements de fenêtre durs (stores et teintes).
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: ce6543a1-2438-4661-95bf-ff3d956013bc
source-git-commit: 790ce3aa4e9aadc019d17e663fc93d7c69772b23
workflow-type: tm+mt
source-wordcount: '153'
ht-degree: 3%

---

# Revêtements de fenêtre{#window-coverings}

Les revêtements de fenêtre comprennent des revêtements de fenêtre souples (draps, valises, rideaux de café) et des revêtements de fenêtre durs (stores et teintes).

Les matériaux de recouvrement de fenêtre spécifient un *fichier de style de recouvrement de fenêtre* (extension de fichier [!DNL .vnw]), un fichier de données spécial similaire à une vignette, contenant des données de masque, d&#39;éclairage, de mise en page et de texture définissant le recouvrement de fenêtre.

Les fichiers [!DNL vnw] n&#39;incluent pas la couleur et la texture (tissu) du couvre-fenêtre. Ces informations sont spécifiées séparément, de la même manière que les textures répétables.

Les matériaux de revêtement de fenêtre ne peuvent être appliqués qu&#39;aux objets de cadre de revêtement de fenêtre, qui sont des objets qui se chevauchent.

<table id="table_545865B054E84592BDAEDA57DBFAE9B3"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>Attribut </p> </th> 
   <th colname="col2" class="entry"> <p>Description </p> </th> 
   <th colname="col3" class="entry"> <p>Par défaut </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <a href="../../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-src.md#reference-62c98abad22149d68d405ed6aaff8272" type="reference" format="dita" scope="local"> <span class="codeph"> src= </span> </a> </p> </td> 
   <td colname="col2"> <p>Fichier de style de recouvrement de fenêtre ; obligatoire. </p> </td> 
   <td colname="col3"> <p>Aucune </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <a href="../../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-src.md#reference-62c98abad22149d68d405ed6aaff8272" type="reference" format="dita" scope="local"> <span class="codeph"> src= </span> </a> </p> </td> 
   <td colname="col2"> <p>Fichier image de la texture (seconde valeur pour <span class="codeph"> src= </span>). </p> </td> 
   <td colname="col3"> <p>Aucune </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <a href="../../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-res.md#reference-0ad9de8887144c83a6db97b4994f7c04" type="reference" format="dita" scope="local"> <span class="codeph"> res= </span> </a> </p> </td> 
   <td colname="col2"> <p>Résolution de la texture. </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> attribute::Resolution </span> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <a href="../../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-http-repeat.md#reference-37749da8233f42599ecf4731055fb7d8" type="reference" format="dita" scope="local"> <span class="codeph"> repeat= </span> </a> </p> </td> 
   <td colname="col2"> <p>Mode de répétition. </p> </td> 
   <td colname="col3"> <p>0 (répétition droite) </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <a href="../../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-http-color.md#reference-ea3cba9edfe94dbab86d8f123a9ed0aa" type="reference" format="dita" scope="local"> <span class="codeph"> color= </span> </a> </p> </td> 
   <td colname="col2"> <p>Couleur unie (ou colore la texture). </p> </td> 
   <td colname="col3"> <p>128 (gris neutre) </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <a href="../../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-http-sharp.md#reference-acdd87f6b5de4e3a85e5d3c03022a35a" type="reference" format="dita" scope="local"> <span class="codeph"> sharp= </span> </a> </p> </td> 
   <td colname="col2"> <p>Accentuation. </p> </td> 
   <td colname="col3"> <p>0 (aucun accentuation) </p> </td> 
  </tr> 
 </tbody> 
</table>
