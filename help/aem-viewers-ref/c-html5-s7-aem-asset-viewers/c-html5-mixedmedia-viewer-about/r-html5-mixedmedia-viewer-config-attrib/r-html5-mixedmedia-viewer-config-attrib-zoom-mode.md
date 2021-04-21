---
description: Définit le type d’interaction de zoom.
solution: Experience Manager
title: zoomMode
feature: Dynamic Media Classic,Viewers,SDK/API,Mix Media Sets
role: Developer,Business Practitioner
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '144'
ht-degree: 2%

---


# zoomMode{#zoommode}

Définit le type d’interaction de zoom.

`zoomMode=continuous|inline|auto`

<table id="table_E314540D347D47699C04EB80D20C0721"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> continue|inline|auto  </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> continue  </span> permet un zoom classique lorsque l’image est progressivement zoomée lorsque vous cliquez, appuyez sur le doublon ou appuyez sur la vue principale. Vous devez effectuer un zoom arrière explicite ou réinitialiser l’état de zoom pour revenir à la vue initiale. </p> <p> <span class="codeph"> l’option Inline  </span> permet un zoom instantané, où l’image agrandie s’affiche instantanément lorsque vous passez la vue principale sur le bureau ou lorsque vous appuyez sur un périphérique tactile ; l’image revient automatiquement à l’état initial lorsque vous déplacez la souris de la vue ou relâchez votre doigt. Notez que dans le mode <span class="codeph"> intégré </span>, les visionneuses d’images imbriquées sont aplaties et affichées sous forme de miniatures individuelles. <span class="codeph"> auto  </span> active le mode en ligne sur le bureau et le mode continu sur les périphériques tactiles. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Propriétés {#section-65be9301796240e38f31818229da7acc}

Facultatif.

## Par défaut {#section-bd374ffc5182484faa77a7a3c8fa70f2}

`continuous`

## Exemple {#section-bd6c4249bccf44aab13fee8552f5a8b3}

`zoomMode=auto`
