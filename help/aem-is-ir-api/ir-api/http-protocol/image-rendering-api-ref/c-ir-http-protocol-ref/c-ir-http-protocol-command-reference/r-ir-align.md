---
title: aligner
description: Alignement du rendu de la texture. Spécifie le point d'origine défini par l'objet vignette sélectionné à utiliser.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 0b76f173-809b-4b41-bf39-6b85f77ab2db
TQID: 'https://experienceleague.adobe.com/U6V-e23e9ILdnQfTpJzGPzbCTZEICccSpcMebA-NRjA'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 70c478ebbe0b38d9e35c1bb26074a458c0197b2b
workflow-type: tm+mt
source-wordcount: 190
ht-degree: 4%

---

# aligner {#align}

Alignement du rendu de la texture. Spécifie le point d&#39;origine défini par l&#39;objet vignette sélectionné à utiliser.

`align=0|1|2|3|4|5|6`

<table id="simpletable_D15233999E35488EB2F933BD72798E2F"> 
 <tr class="strow"> 
  <td class="stentry"> <p>0 </p></td> 
  <td class="stentry"> <p>Origine par défaut (correspondance centrale). </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>1 </p></td> 
  <td class="stentry"> <p>Origine de correspondance continue. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>2 </p></td> 
  <td class="stentry"> <p>Alignement aléatoire. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>3..6 </p></td> 
  <td class="stentry"> <p>Origine définie par l’utilisateur. </p></td> 
 </tr> 
</table>

Le rendu applique la texture à l’objet de sorte que le point d’ancrage de texture ( `anchor=`) corresponde au point d’origine spécifié.

Chaque objet peut définir jusqu’à six points d’origine (0, 1, 3, 4, 5, 6). Si une valeur `align` est spécifiée mais que le point d’origine correspondant n’est pas défini par l’objet vignette, le point d’origine par défaut (correspondance centrale) est utilisé.

`align=2` Spécifie l&#39;alignement aléatoire des textures, auquel cas `anchor=` est effectivement ignoré.

Principalement utilisé pour les matériaux d&#39;ameublement, éventuellement pour les tissus d&#39;habillement, pour gérer l&#39;alignement de la texture entre les objets adjacents.

## Propriétés {#section-350fadc87dcf4812a8a02d1c3d6697a0}

Attribut Material. Ignoré si un objet de cadre de mur, d&#39;armoire, d&#39;appareil ou de revêtement de fenêtre est sélectionné ou si la matière n&#39;est pas une texture répétable.

## Par défaut {#section-3231c2854bae4477836b626ac208dd34}

`catalog::Alignment`, si le matériau est basé sur une entrée de catalogue, sinon 0 (centré).

## Voir aussi {#section-945d1ce275df487d9d564d4043156c79}

[catalog::Alignment](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-material-data-reference/r-ir-alignment.md#reference-e52152e8dc244d0aa13b40c615d0f399) , [anchor=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-http-anchor.md#reference-d53923d785c9442997dc7f2199524c26)

