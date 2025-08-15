---
title: FlyoutZoomView.overlay
description: FlyoutZoomView.overlay
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Flyout
role: Developer,User
exl-id: 7fbf24c6-900f-4e94-b879-3a8f95dc5c08
source-git-commit: 50dddf148345d2ca5243d5d7108fefa56d23dad6
workflow-type: tm+mt
source-wordcount: '103'
ht-degree: 2%

---

# FlyoutZoomView.overlay{#flyoutzoomview-overlay}

`[FlyoutZoomView.|<containerId>_flyout.]overlay=0|1`

<table id="table_D052090D052D4273B37872C0C7E09E4B"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> 0|1</span> </p> </td> 
   <td colname="col2"> <p> Contrôle l’aspect de la surbrillance de la vue principale lorsque la fenêtre déroulante est active. Lorsqu’elle est définie sur <span class="codeph"> 0</span>, la zone actuellement visible dans la fenêtre déroulante est mise en surbrillance à l’aide des styles fournis par <span class="codeph"> .s7highlighter</span> ou par <span class="codeph"> .s7cursor</span> les noms de classe CSS (selon la valeur de <span class="codeph"> highlightmode</span> modificateur). Lorsqu’il est défini sur <span class="codeph"> 1</span> le composant passe en mode « inverse » où la zone actuellement consultée est entièrement transparente (dans le cas où <span class="codeph"> mode de mise en surbrillance</span> est défini sur <span class="codeph"> mise en surbrillance</span>) ou mise en forme avec <span class="codeph"> nom de classe CSS .s7cursor</span> (dans le cas où <span class="codeph"> mode de mise en surbrillance</span> est défini sur <span class="codeph"> cursor</span>), mais où la zone environnante est remplie à l’aide des styles fournis par <span class="codeph"> .s7overlay</span> nom de classe CSS. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Propriétés {#section-5526a5d19e7e4ee2a35b1c4816ed4202}

Facultatif.

## Par défaut {#section-a08032f0fcf041c09e63c0238a339fc9}

`0`

## Exemple {#section-0338be21edd04ff1a3bed5c8319b61a4}

`overlay=1`
