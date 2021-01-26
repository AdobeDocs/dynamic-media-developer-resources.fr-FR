---
description: Réglage du contraste. Ajuste le contraste de l’image en augmentant la luminosité des pixels avec plus de 50 % de luminosité et en réduisant la luminosité des pixels avec moins de 50 % de luminosité.
seo-description: Réglage du contraste. Ajuste le contraste de l’image en augmentant la luminosité des pixels avec plus de 50 % de luminosité et en réduisant la luminosité des pixels avec moins de 50 % de luminosité.
seo-title: op_contraste
solution: Experience Manager
title: op_contraste
topic: Dynamic Media Image Serving - Image Rendering API
uuid: d17b0b49-792b-41ce-a154-5e7635c9ab43
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '165'
ht-degree: 1%

---


# op_contraste{#op-contrast}

Réglage du contraste. Ajuste le contraste de l’image en augmentant la luminosité des pixels avec plus de 50 % de luminosité et en réduisant la luminosité des pixels avec moins de 50 % de luminosité.

`op_contrast= *`adj`*`

<table id="simpletable_8246802C74424A68A7A2EA5B50A89D42"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> adj</span> </p> </td> 
  <td class="stentry"> <p>Ajustement de contraste en pourcentage (-100...100 int). </p></td> 
 </tr> 
</table>

## Propriétés {#section-d319ed55057344eab0a3c93f720acdbf}

Calque, commande. S’applique au calque actif ou à l’image composite si `layer=comp`. Ignoré par les calques d’effet.

## Par défaut {#section-896d1b1f7f084e929355a4684f3e833b}

`op_contrast=0`, sans changement de contraste. Les images ou calques CMJN sont convertis en RVB avant l’application de l’opération.

## Exemple {#section-94bc4348b4bc4f0e9768ea1c45ca8340}

Réduisez le contraste et la netteté d’un calque d’image de qualité supérieure pour l’associer visuellement à une photo d’arrière-plan de qualité inférieure :

... `&op_blur=3&op_contrast=-12&`

Une version ultérieure peut utiliser la luminosité médiane de l’image plutôt qu’une luminosité fixe de 50 %.
