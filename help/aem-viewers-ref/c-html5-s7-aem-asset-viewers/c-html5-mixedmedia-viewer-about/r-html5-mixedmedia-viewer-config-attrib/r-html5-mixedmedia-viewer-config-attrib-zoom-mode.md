---
title: zoomMode
description: Définit le type d’interaction de zoom.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Mixed Media Sets
role: Developer,User
exl-id: a399ed5e-acc3-4c45-9c84-9fa572667489
TQID: 'https://experienceleague.adobe.com/Joa1KBx6spGvXsMkjxSCPn-23cICUffLJ9CWOQ-BRwo'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 132
ht-degree: 2%

---

# zoomMode{#zoommode}

Définit le type d’interaction de zoom.

`zoomMode=continuous|inline|auto`

<table id="table_E314540D347D47699C04EB80D20C0721"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> continue|inline|auto </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph">’</span> continue active le zoom classique, où l’image effectue un zoom avant progressif lorsque vous cliquez, appuyez deux fois ou pincez dans la vue principale. Pour revenir à la vue initiale, effectuez un zoom arrière ou réinitialisez l’état de zoom. La classe </p> <p> <span class="codeph">’</span> en ligne active le zoom instantané, où l’image agrandie s’affiche instantanément lorsque vous placez le pointeur de la souris sur la vue principale du bureau ou lorsque vous touchez et maintenez un appareil tactile. L’image revient automatiquement à son état initial lorsque vous déplacez la souris hors de la vue ou relâchez le doigt. En mode de </span> en ligne <span class="codeph">, les visionneuses d’images imbriquées sont aplaties et affichées sous forme de miniatures individuelles. La classe <span class="codeph"> auto </span> active le mode intégré sur les ordinateurs de bureau et le mode continu sur les appareils tactiles. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Propriétés {#section-65be9301796240e38f31818229da7acc}

Facultatif.

## Par défaut {#section-bd374ffc5182484faa77a7a3c8fa70f2}

`continuous`

## Exemple {#section-bd6c4249bccf44aab13fee8552f5a8b3}

`zoomMode=auto`
