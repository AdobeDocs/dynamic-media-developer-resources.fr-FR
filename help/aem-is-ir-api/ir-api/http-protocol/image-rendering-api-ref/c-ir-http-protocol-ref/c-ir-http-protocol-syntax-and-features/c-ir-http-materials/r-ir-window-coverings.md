---
description: Les matériaux utilisés pour couvrir les fenêtres comprennent à la fois des tentures douces (tentures, valises, rideaux de café) et des garnitures de fenêtres dures (teintes et stores).
seo-description: Les matériaux utilisés pour couvrir les fenêtres comprennent à la fois des tentures douces (tentures, valises, rideaux de café) et des garnitures de fenêtres dures (teintes et stores).
seo-title: Recouvrements de fenêtre
solution: Experience Manager
title: Recouvrements de fenêtre
topic: Scene7 Image Serving - Image Rendering API
uuid: 3d74466a-b7c3-43b0-9b0b-f8bb809e2773
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# Window coverings{#window-coverings}

Les matériaux utilisés pour couvrir les fenêtres comprennent à la fois des tentures douces (tentures, valises, rideaux de café) et des garnitures de fenêtres dures (teintes et stores).

Les matériaux de recouvrement de fenêtre spécifient un fichier *de style de* fenêtre (extension de [!DNL .vnw] fichier), un fichier de données spécial similaire à une vignette, contenant des données de masque, d’éclairage, de mise en page et de texture définissant le recouvrement de la fenêtre.

[!DNL vnw] n’incluent pas la couleur et la texture (tissu) de la garniture de fenêtre. Ces informations sont spécifiées séparément, de la même manière que les textures répétables.

Les matériaux de recouvrement de fenêtre ne peuvent être appliqués qu’aux objets de cadre de recouvrement de fenêtre, qui se chevauchent.

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
   <td colname="col1"> <p> <a href="../../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-src.md#reference-62c98abad22149d68d405ed6aaff8272" type="reference" format="dita" scope="local"> <span class="codeph"> src= </span></a> </p> </td> 
   <td colname="col2"> <p>Fenêtre recouvrant le fichier de style ; obligatoire. </p> </td> 
   <td colname="col3"> <p>Aucune </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <a href="../../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-src.md#reference-62c98abad22149d68d405ed6aaff8272" type="reference" format="dita" scope="local"> <span class="codeph"> src= </span></a> </p> </td> 
   <td colname="col2"> <p>Fichier image de texture (seconde valeur pour <span class="codeph"> src= </span>). </p> </td> 
   <td colname="col3"> <p>Aucune </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <a href="../../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-res.md#reference-0ad9de8887144c83a6db97b4994f7c04" type="reference" format="dita" scope="local"> <span class="codeph"> res= </span></a> </p> </td> 
   <td colname="col2"> <p>Résolution de la texture. </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> attribut:Resolution </span> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <a href="../../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-http-repeat.md#reference-37749da8233f42599ecf4731055fb7d8" type="reference" format="dita" scope="local"> <span class="codeph"> repeat= </span></a> </p> </td> 
   <td colname="col2"> <p>Mode Répétition. </p> </td> 
   <td colname="col3"> <p>0 (répétition droite) </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <a href="../../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-http-color.md#reference-ea3cba9edfe94dbab86d8f123a9ed0aa" type="reference" format="dita" scope="local"> <span class="codeph"> color= </span></a> </p> </td> 
   <td colname="col2"> <p>Couleur unie (ou colore la texture). </p> </td> 
   <td colname="col3"> <p>128 (gris neutre) </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <a href="../../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-http-sharp.md#reference-acdd87f6b5de4e3a85e5d3c03022a35a" type="reference" format="dita" scope="local"> <span class="codeph"> sharp= </span></a> </p> </td> 
   <td colname="col2"> <p>Accentuation. </p> </td> 
   <td colname="col3"> <p>0 (aucun accentuation) </p> </td> 
  </tr> 
 </tbody> 
</table>

