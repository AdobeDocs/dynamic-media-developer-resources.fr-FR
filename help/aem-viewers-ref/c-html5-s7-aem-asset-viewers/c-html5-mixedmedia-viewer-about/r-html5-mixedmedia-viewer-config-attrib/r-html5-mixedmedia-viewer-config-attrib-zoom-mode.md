---
title: zoomMode
description: Définit le type d’interaction du zoom.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Mixed Media Sets
role: Developer,User
exl-id: a399ed5e-acc3-4c45-9c84-9fa572667489
source-git-commit: 6f838470a7bdea8e8c0219e59746ec82ecd802a8
workflow-type: tm+mt
source-wordcount: '131'
ht-degree: 2%

---

# zoomMode{#zoommode}

Définit le type d’interaction du zoom.

`zoomMode=continuous|inline|auto`

<table id="table_E314540D347D47699C04EB80D20C0721"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> continuous|inline|auto </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> En continu </span> active un zoom classique où l’image s’agrandit progressivement lorsque vous cliquez, appuyez deux fois ou effectuez un pincement dans la vue principale. Pour revenir à la vue initiale, effectuez un zoom arrière ou réinitialisez l’état du zoom. La classe </p> <p> <span class="codeph"> La ligne d’entrée </span> permet un zoom instantané, où l’image agrandie s’affiche instantanément lorsque vous passez la souris sur la vue principale de l’ordinateur ou lorsque vous appuyez et maintenez le bouton de la souris sur un appareil tactile. L’image revient automatiquement à l’état initial une fois que vous déplacez la souris de la vue ou relâchez votre doigt. En mode <span class="codeph"> intégré </span>, les visionneuses d’images imbriquées sont aplaties et affichées sous forme de miniatures individuelles. La classe <span class="codeph"> auto </span> active le mode en ligne sur le bureau et le mode continu sur les appareils tactiles. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Propriétés {#section-65be9301796240e38f31818229da7acc}

Facultatif.

## Par défaut {#section-bd374ffc5182484faa77a7a3c8fa70f2}

`continuous`

## Exemple {#section-bd6c4249bccf44aab13fee8552f5a8b3}

`zoomMode=auto`
