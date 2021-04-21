---
description: Les documents Armoires spécifient un fichier de style Armoire (extension de fichier .vnc), un fichier de données spécial contenant des représentations photographiques des armoires, ainsi que des définitions de disposition paramétriques et d'autres informations requises pour le rendu des façades de l'armoire.
solution: Experience Manager
title: Meubles
feature: Dynamic Media Classic,SDK/API
role: Developer,Business Practitioner
translation-type: tm+mt
source-git-commit: d0bc88f55f857762b3bab4c76d1e3f3dd2733d60
workflow-type: tm+mt
source-wordcount: '163'
ht-degree: 5%

---


# Meubles{#cabinets}

Les documents Armoires spécifient un fichier de style Armoire (extension de fichier .vnc), un fichier de données spécial contenant des représentations photographiques des armoires, ainsi que des définitions de disposition paramétriques et d&#39;autres informations requises pour le rendu des façades de l&#39;armoire.

[!DNL vnc] les fichiers peuvent inclure soit une texture répétable du grain de bois, soit la texture peut être fournie à l&#39;extérieur par l&#39;intermédiaire d&#39;un deuxième argument à  `src=`. Certains fichiers [!DNL vnc] permettent de coloriser ou de texturer des zones sélectionnées de façades d&#39;armoire (généralement utilisées pour les styles d&#39;armoire laminée).

Les documents d&#39;armoire ne peuvent être appliqués qu&#39;aux objets d&#39;armoire.

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
   <td colname="col1"> <p> <a href="../../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-src.md#reference-62c98abad22149d68d405ed6aaff8272" type="reference" format="dita" scope="local"> <span class="codeph"> src=  </span> </a> </p> </td> 
   <td colname="col2"> <p>fichier de style d'armoire ; obligatoire. </p> </td> 
   <td colname="col3"> <p>Aucune </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <a href="../../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-src.md#reference-62c98abad22149d68d405ed6aaff8272" type="reference" format="dita" scope="local"> <span class="codeph"> src=  </span> </a> </p> </td> 
   <td colname="col2"> <p>Fichier image de texture facultatif (seconde valeur pour <span class="codeph"> src= </span>). </p> </td> 
   <td colname="col3"> <p>Aucune </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <a href="../../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-res.md#reference-0ad9de8887144c83a6db97b4994f7c04" type="reference" format="dita" scope="local"> <span class="codeph"> res=  </span> </a> </p> </td> 
   <td colname="col2"> <p>Résolution de texture facultative. </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> attribut::Résolution  </span> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <a href="../../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-http-color.md#reference-ea3cba9edfe94dbab86d8f123a9ed0aa" type="reference" format="dita" scope="local"> <span class="codeph"> color=  </span> </a> </p> </td> 
   <td colname="col2"> <p>Colorise l'armoire et/ou la texture. </p> </td> 
   <td colname="col3"> <p>Aucune </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <a href="../../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-http-sharp.md#reference-acdd87f6b5de4e3a85e5d3c03022a35a" type="reference" format="dita" scope="local"> <span class="codeph"> sharp=  </span> </a> </p> </td> 
   <td colname="col2"> <p>Accentuation. </p> </td> 
   <td colname="col3"> <p>0 (aucune accentuation) </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <a href="../../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-flags.md#reference-3a4844f0f21346d79e6508aaad9a9ac9" type="reference" format="dita" scope="local"> <span class="codeph"> flags=  </span> </a> </p> </td> 
   <td colname="col2"> <p>Indicateurs de rendu spéciaux. </p> </td> 
   <td colname="col3"> <p>0 (aucun indicateur) </p> </td> 
  </tr> 
 </tbody> 
</table>

