---
description: FlyoutZoomView.overlay
solution: Experience Manager
title: FlyoutZoomView.overlay
feature: Dynamic Media Classic,Visionneuses,SDK/API,Fenêtre déroulante
role: Developer,User
exl-id: 7fbf24c6-900f-4e94-b879-3a8f95dc5c08
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '111'
ht-degree: 4%

---

# FlyoutZoomView.overlay{#flyoutzoomview-overlay}

`[FlyoutZoomView.|<containerId>_flyout.]overlay=0|1`

<table id="table_D052090D052D4273B37872C0C7E09E4B"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> 0 | 1</span> </p> </td> 
   <td colname="col2"> <p> Contrôle l’aspect de mise en surbrillance de la vue principale lorsque la fenêtre déroulante est principale. Lorsqu’elle est définie sur <span class="codeph"> 0</span>, la zone actuellement visible dans la fenêtre déroulante est mise en surbrillance à l’aide des styles fournis par les noms de classe CSS <span class="codeph"> .s7highlight</span> ou <span class="codeph"> .s7cursor</span> (selon la valeur du modificateur <span class="codeph"> surlignage </span>). Lorsqu’il est défini sur <span class="codeph"> 1</span> , le composant passe en mode "inverse" où la zone actuellement consultée est entièrement transparente (au cas où <span class="codeph"> surlignage mode</span> est défini sur <span class="codeph"> surligner</span>) ou stylisée avec <span class="codeph"> .s7cursor</span> nom de classe CSS (au cas où <span class="codeph"> surlignage</span> est défini sur <span class="codeph"> cursor</span>), mais les zones environnantes sont remplies à l’aide des styles fournis par <span class="codeph"> .s7overlay</span> nom de classe CSS. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Propriétés {#section-5526a5d19e7e4ee2a35b1c4816ed4202}

Facultatif.

## Par défaut {#section-a08032f0fcf041c09e63c0238a339fc9}

`0`

## Exemple {#section-0338be21edd04ff1a3bed5c8319b61a4}

`overlay=1`
