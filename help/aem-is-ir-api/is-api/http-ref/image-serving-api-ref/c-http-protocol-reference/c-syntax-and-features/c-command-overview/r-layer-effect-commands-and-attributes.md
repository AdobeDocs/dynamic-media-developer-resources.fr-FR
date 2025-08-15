---
description: Ces commandes peuvent être utilisées pour définir des effets de calque, tels que les effets d’ombre portée ou d’éclat. Les calques d’effet ignorent toutes les autres commandes.
solution: Experience Manager
title: Commandes d’effet de calque
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 483b1f24-9cd2-45e0-9d18-0dc0fbe8abcf
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '116'
ht-degree: 0%

---

# Commandes d’effet de calque{#layer-effect-commands}

Ces commandes peuvent être utilisées pour définir des effets de calque, tels que les effets d’ombre portée ou d’éclat. Les calques d’effet ignorent toutes les autres commandes.

<table id="simpletable_3094B9783772437FAACF9B382F7A32EE"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <a href="../../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-blendmode.md#reference-8be10dde1d584429966cb61ac8e7d172" type="reference" format="dita" scope="local"> Mode de fusion</a> </p></td> 
  <td class="stentry"> <p>Spécifie le mode de fusion des calques. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <a href="/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-data-types/r-is-http-color.md" type="reference" format="dita" scope="local"> Couleur</a> </p></td> 
  <td class="stentry"> <p>Indique la couleur et l’opacité de l’effet principal. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <a href="../../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-effect.md#reference-b1296c4afed047fb921bbc1e33752135" type="reference" format="dita" scope="local"> effet</a> </p></td> 
  <td class="stentry"> <p>Démarre le segment de calque d’effet et indique l’ordre z. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <a href="../../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-maskuse.md#reference-9bb1fb5eee4a4bd38f33dadc1a752464" type="reference" format="dita" scope="local"> Utilisation du masque</a> </p></td> 
  <td class="stentry"> <p>Spécifie la méthode d’utilisation du masque de fusion du parent (couche alpha). </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><a href="../../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-op-blur.md#reference-00638f29e59b49c99f6bba27daf24668" type="reference" format="dita" scope="local"> op_blur</a> </p></td> 
  <td class="stentry"> <p>Plumes l’effet. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><a href="../../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-op-grow.md#reference-f95f3291c78c42b9a34b1b7e177e739a" type="reference" format="dita" scope="local"> op_grow</a> </p></td> 
  <td class="stentry"> <p>Augmente ou réduit l’effet de calque. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><a href="../../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-op-noise.md#reference-763c4a890fe24bb6bb5ae9dad4e2da94" type="reference" format="dita" scope="local"> op_noise</a> </p></td> 
  <td class="stentry"> <p>Ajoute du bruit à l’effet. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <a href="../../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-opac.md#reference-d2269b51aca34599a08d0a46ee5c27e5" type="reference" format="dita" scope="local"> opac</a> </p></td> 
  <td class="stentry"> <p>Réduit l’opacité du calque. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <a href="../../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-pos.md#reference-65de948f4b404f1182b22119ca332143" type="reference" format="dita" scope="local"> Pos</a> </p></td> 
  <td class="stentry"> <p>Place le calque d’effet par rapport à son calque parent. </p></td> 
 </tr> 
</table>
