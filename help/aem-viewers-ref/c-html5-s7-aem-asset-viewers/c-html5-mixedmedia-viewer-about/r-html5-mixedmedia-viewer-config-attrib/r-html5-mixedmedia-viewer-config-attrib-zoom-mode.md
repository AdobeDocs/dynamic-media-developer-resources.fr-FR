---
description: Définit le type d’interaction du zoom.
solution: Experience Manager
title: zoomMode
feature: Dynamic Media Classic,Visionneuses,SDK/API,Visionneuses de médias mixtes
role: Developer,Business Practitioner
exl-id: a399ed5e-acc3-4c45-9c84-9fa572667489
source-git-commit: bfb350e68d9b7e86cec5ee75fe9280b12ce0e54e
workflow-type: tm+mt
source-wordcount: '141'
ht-degree: 2%

---

# zoomMode{#zoommode}

Définit le type d’interaction du zoom.

`zoomMode=continuous|inline|auto`

<table id="table_E314540D347D47699C04EB80D20C0721"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> continue|inline|auto  </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> L’option continue  </span> active le zoom classique où l’image s’affiche progressivement lorsque vous cliquez, appuyez deux fois ou appuyez longuement dans la vue principale. Vous devez effectuer un zoom arrière ou réinitialiser explicitement l’état du zoom pour revenir à la vue initiale. </p> <p> <span class="codeph"> l’option en ligne  </span> permet un zoom instantané, où l’image agrandie s’affiche instantanément lorsque vous survolez la vue principale sur le bureau ou lorsque vous appuyez ou maintenez la touche enfoncée sur un appareil tactile. l’image revient automatiquement à l’état initial lorsque vous déplacez la souris de la vue ou relâchez votre doigt. Notez que dans le mode <span class="codeph"> intégré </span>, les visionneuses d’images imbriquées sont aplaties et affichées sous forme de miniatures individuelles. <span class="codeph"> auto  </span> active le mode intégré sur l’ordinateur de bureau et le mode continu sur les appareils tactiles. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Propriétés {#section-65be9301796240e38f31818229da7acc}

Facultatif.

## Par défaut {#section-bd374ffc5182484faa77a7a3c8fa70f2}

`continuous`

## Exemple {#section-bd6c4249bccf44aab13fee8552f5a8b3}

`zoomMode=auto`
