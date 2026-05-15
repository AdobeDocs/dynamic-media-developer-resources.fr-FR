---
title: initialFrame
description: Paramètre commun à tous les observateurs.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API
role: Developer,User
exl-id: db77edf0-e223-4f44-b83b-b6dbe5c1abd6
TQID: 'https://experienceleague.adobe.com/v4kG-OcDN3wmdHDClJHeLR8d2SNcMa5sRQo89Qwig4I'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 108
ht-degree: 2%

---

# initialFrame{#initialframe}

Paramètre commun à tous les observateurs.

>[!NOTE]
>
>Cette commande ne concerne pas la visionneuse d’images vidéo.

` initialFrame= *`frameIdx`*[ *`,pageIdx`*]`

<table id="table_9B98C97485DD4DEB8A6ECBCE8DF6B886"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> frameIdx</span> </span> </p> </td> 
   <td colname="col2"> <p> Indique un index d’image de base zéro que la visionneuse affiche lors du chargement. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"><span class="varname"> pageIdx</span></span> </p> </td> 
   <td colname="col2"> <p>Index de base zéro de la page dans la planche lorsque l’appareil est en orientation portrait. Pour un environnement « de gauche à droite », la <span class="codeph"> 0 </span> signifie « page de gauche » et la <span class="codeph"> 1 </span> signifie « page de droite ». Pour un environnement « de droite à gauche », c'est le contraire : <span class="codeph"> 0</span> signifie « page de droite » et <span class="codeph"> 1</span> signifie « page de gauche ». </p> <p>S’il n’est pas spécifié, la <span class="codeph"> 0</span> est prise par défaut. Ignoré lorsque l’appareil est en orientation paysage. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Propriétés {#section-10ee45d637134e0fbcd943c62578cb78}

Facultatif.

## Par défaut {#section-d411e450028c460392cb8508f8ccc5d9}

Pas de valeur par défaut.

## Exemple {#section-a8afbf76f8384aa0a83ed1feeccd5b9a}

```
initialFrame=2
```
