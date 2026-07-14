---
title: rotation
description: Angle de rotation du matériau. Définit l'angle de rotation des matériaux.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 355d9691-c04b-44a6-9563-5bef185cfa7e
TQID: 'https://experienceleague.adobe.com/prSGGMuV4SpFfhd8uCVzMRGpr-VBpowxE-UagKtpnqI'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 70c478ebbe0b38d9e35c1bb26074a458c0197b2b
workflow-type: tm+mt
source-wordcount: 125
ht-degree: 4%

---

# rotation{#rotate}

Angle de rotation du matériau. Définit l&#39;angle de rotation des matériaux.

` rotate= *` angle `*`

<table id="simpletable_F1A87ECD86E8429788825374A6882CB9"> 
 <tr class="strow"> 
  <td class="stentry"> <p> </span> d'angle de <span class="varname"> </p> </td> 
  <td class="stentry"> <p>Angle de rotation en degrés (réel). </p> </td> 
 </tr> 
</table>

Faire pivoter les matériaux de texture répétables (à l&#39;exclusion des fonds d&#39;écran) de multiples de 45° lorsqu&#39;ils sont appliqués à des objets plats ou des objets plans.

Faire pivoter des matériaux de texture répétables par des angles arbitraires lorsqu&#39;ils sont appliqués aux objets Flowline et Sketch.

Faire pivoter les matériaux de décalcomanie selon des angles arbitraires.

Les angles positifs tournent dans le sens des aiguilles d&#39;une montre. La texture ou la décalcomanie pivote autour du point d&#39;ancrage ( `anchor=`) ; le point d&#39;ancrage reste aligné avec l&#39;origine de l&#39;objet cible.

## Propriétés {#section-ad4d07897ca24f63af1a4062f8618e36}

Attribut Material. Ignoré par la couleur unie, le papier peint, l&#39;armoire et les matériaux de traitement de fenêtre. *`angle`* Doit être un multiple de 45 pour les textures répétables, sauf si elles sont appliquées à des objets Flowline ou Sketch.

## Par défaut {#section-14c991e71b74449db8ff18a775949b28}

`rotate=0`, pas de rotation.

## Voir aussi {#section-f73c00e9368b478dac1fd15bb4367a12}

[anchor=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-http-anchor.md#reference-d53923d785c9442997dc7f2199524c26)

