---
description: Mode de répétition de la texture. Indique le mode de mosaïque des images de texture pour remplir la surface  du.
seo-description: Mode de répétition de la texture. Indique le mode de mosaïque des images de texture pour remplir la surface  du.
seo-title: Repeat
solution: Experience Manager
title: Repeat
topic: Scene7 Image Serving - Image Rendering API
uuid: bd15a573-9902-4672-992d-90d171160a46
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# Repeat{#repeat}

Mode de répétition de la texture. Indique le mode de mosaïque des images de texture pour remplir la surface  du.

## Propriétés {#section-cef4109cddf54ce095c3293d85bc412d}

Enum. Utilisé uniquement pour les textures répétables. Ignoré pour tous les autres matériaux.

Les valeurs suivantes sont autorisées pour les matériaux de texture répétables :

<table id="simpletable_C24FDA80A8AC431DA3FC86188E3774E1" class="- topic/simpletable "> 
 <tr class="- topic/strow strow"> 
  <td class="- topic/stentry stentry"> <p>01 </p></td> 
  <td class="- topic/stentry stentry"> <p>Répétez. </p></td> 
 </tr> 
 <tr class="- topic/strow strow"> 
  <td class="- topic/stentry stentry"> <p>1 </p></td> 
  <td class="- topic/stentry stentry"> <p>Carrelage aléatoire à 4 voies. </p></td> 
 </tr> 
 <tr class="- topic/strow strow"> 
  <td class="- topic/stentry stentry"> <p>2 </p></td> 
  <td class="- topic/stentry stentry"> <p>Mosaïque aléatoire à 8 voies. </p></td> 
 </tr> 
 <tr class="- topic/strow strow"> 
  <td class="- topic/stentry stentry"> <p>3 </p></td> 
  <td class="- topic/stentry stentry"> <p>Carrelage en losange. </p></td> 
 </tr> 
 <tr class="- topic/strow strow"> 
  <td class="- topic/stentry stentry"> <p>4 </p></td> 
  <td class="- topic/stentry stentry"> <p>Le papier peint à un quart de goutte est accroché. </p></td> 
 </tr> 
 <tr class="- topic/strow strow"> 
  <td class="- topic/stentry stentry"> <p>5 </p></td> 
  <td class="- topic/stentry stentry"> <p>Le papier peint à la troisième goutte est suspendu. </p></td> 
 </tr> 
 <tr class="- topic/strow strow"> 
  <td class="- topic/stentry stentry"> <p>6 </p></td> 
  <td class="- topic/stentry stentry"> <p>Le papier peint à demi-goutte est suspendu. </p></td> 
 </tr> 
 <tr class="- topic/strow strow"> 
  <td class="- topic/stentry stentry"> <p>7 </p></td> 
  <td class="- topic/stentry stentry"> <p>Le papier peint à la cinquième goutte est suspendu. </p></td> 
 </tr> 
 <tr class="- topic/strow strow"> 
  <td class="- topic/stentry stentry"> <p>8 </p></td> 
  <td class="- topic/stentry stentry"> <p>Le papier peint est suspendu. </p></td> 
 </tr> 
 <tr class="- topic/strow strow"> 
  <td class="- topic/stentry stentry"> <p>9 </p></td> 
  <td class="- topic/stentry stentry"> <p>Du papier peint aléatoire. </p></td> 
 </tr> 
 <tr class="- topic/strow strow"> 
  <td class="- topic/stentry stentry"> <p>10 </p></td> 
  <td class="- topic/stentry stentry"> <p>Une goutte aléatoire. </p></td> 
 </tr> 
 <tr class="- topic/strow strow"> 
  <td class="- topic/stentry stentry"> <p>11 </p></td> 
  <td class="- topic/stentry stentry"> <p>Au hasard. </p></td> 
 </tr> 
 <tr class="- topic/strow strow"> 
  <td class="- topic/stentry stentry"> <p>12 </p></td> 
  <td class="- topic/stentry stentry"> <p>À moitié. </p></td> 
 </tr> 
 <tr class="- topic/strow strow"> 
  <td class="- topic/stentry stentry"> <p>13 </p></td> 
  <td class="- topic/stentry stentry"> <p>Miroir (correspondance de bibliothèque). </p></td> 
 </tr> 
 <tr class="- topic/strow strow"> 
  <td class="- topic/stentry stentry"> <p>14 </p></td> 
  <td class="- topic/stentry stentry"> <p>Générateur aléatoire standard. </p></td> 
 </tr> 
 <tr class="- topic/strow strow"> 
  <td class="- topic/stentry stentry"> <p>15 </p></td> 
  <td class="- topic/stentry stentry"> <p>Optimisateur de fréquence élevée. </p></td> 
 </tr> 
 <tr class="- topic/strow strow"> 
  <td class="- topic/stentry stentry"> <p>16 </p></td> 
  <td class="- topic/stentry stentry"> <p>Optimiseur aléatoire basse fréquence. </p></td> 
 </tr> 
 <tr class="- topic/strow strow"> 
  <td class="- topic/stentry stentry"> <p>17 </p></td> 
  <td class="- topic/stentry stentry"> <p>Caractère aléatoire horizontal. </p></td> 
 </tr> 
 <tr class="- topic/strow strow"> 
  <td class="- topic/stentry stentry"> <p>18 </p></td> 
  <td class="- topic/stentry stentry"> <p>Caractère aléatoire vertical. </p></td> 
 </tr> 
 <tr class="- topic/strow strow"> 
  <td class="- topic/stentry stentry"> <p>19 </p></td> 
  <td class="- topic/stentry stentry"> <p>Séparateur de bord. </p></td> 
 </tr> 
</table>

## Par défaut {#section-23fba3bd1f3544c7913d12f2ca148517}

0 (répétition droite).

## Voir aussi {#section-a08887a91db34ed3b183899c69c9f74f}

[répéter=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-http-repeat.md#reference-37749da8233f42599ecf4731055fb7d8)
