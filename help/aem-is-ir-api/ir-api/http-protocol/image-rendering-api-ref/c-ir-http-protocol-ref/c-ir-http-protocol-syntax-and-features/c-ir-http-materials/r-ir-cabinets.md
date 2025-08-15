---
title: Armoires
description: Les matériaux d’armoires spécifient un fichier de style d’armoire (extension de fichier .vnc), un fichier de données spécial contenant des représentations photographiques d’armoires ainsi que des définitions de mise en page paramétriques et d’autres informations requises pour le rendu des façades d’armoires.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: cdb3ed5e-c396-483d-aea0-2b3f24efe56e
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '159'
ht-degree: 3%

---

# Armoires{#cabinets}

Les matériaux d’armoires spécifient un fichier de style d’armoire (extension de fichier .vnc), un fichier de données spécial contenant des représentations photographiques d’armoires ainsi que des définitions de mise en page paramétriques et d’autres informations requises pour le rendu des façades d’armoires.

[!DNL vnc] Les fichiers peuvent soit inclure une texture de grain de bois reproductible, soit la texture peut être fournie à l’extérieur au moyen d’un deuxième argument à `src=`. Certains [!DNL vnc] fichiers permettent de coloriser ou de texturer des zones sélectionnées des façades d’armoires (généralement utilisées pour les styles d’armoires stratifiées).

Les matériaux d’armoire ne peuvent être appliqués qu’aux objets d’armoire.

<table id="table_0B16200886FE4DFEBB1E4BE8FBA67EE4"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>Attribut </p> </th> 
   <th colname="col2" class="entry"> <p>Description </p> </th> 
   <th colname="col3" class="entry"> <p>Par défaut </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <a href="../../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-src.md#reference-62c98abad22149d68d405ed6aaff8272" type="reference" format="dita" scope="local"><span class="codeph"> src= </span> </a> </p> </td> 
   <td colname="col2"> <p>Fichier de style d’armoire ; Obligatoire. </p> </td> 
   <td colname="col3"> <p>Aucune </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <a href="../../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-src.md#reference-62c98abad22149d68d405ed6aaff8272" type="reference" format="dita" scope="local"><span class="codeph"> src= </span> </a> </p> </td> 
   <td colname="col2"> <p>Fichier image de texture facultatif (deuxième valeur pour <span class="codeph"> src= </span>). </p> </td> 
   <td colname="col3"> <p>Aucune </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <a href="../../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-res.md#reference-0ad9de8887144c83a6db97b4994f7c04" type="reference" format="dita" scope="local"><span class="codeph"> res= </span> </a> </p> </td> 
   <td colname="col2"> <p>Résolution de texture en option. </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> attribut ::Résolution </span> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <a href="../../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-http-color.md#reference-ea3cba9edfe94dbab86d8f123a9ed0aa" type="reference" format="dita" scope="local"><span class="codeph"> couleur= </span> </a> </p> </td> 
   <td colname="col2"> <p>Colorise l’armoire et/ou la texture. </p> </td> 
   <td colname="col3"> <p>Aucune </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <a href="../../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-http-sharp.md#reference-acdd87f6b5de4e3a85e5d3c03022a35a" type="reference" format="dita" scope="local"><span class="codeph"> sharp= </span> </a> </p> </td> 
   <td colname="col2"> <p>Affilage. </p> </td> 
   <td colname="col3"> <p>0 (pas d’accentuation) </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <a href="../../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-flags.md#reference-3a4844f0f21346d79e6508aaad9a9ac9" type="reference" format="dita" scope="local"><span class="codeph"> flags= </span> </a> </p> </td> 
   <td colname="col2"> <p>Indicateurs de rendu spéciaux. </p> </td> 
   <td colname="col3"> <p>0 (sans indicateur) </p> </td> 
  </tr> 
 </tbody> 
</table>
