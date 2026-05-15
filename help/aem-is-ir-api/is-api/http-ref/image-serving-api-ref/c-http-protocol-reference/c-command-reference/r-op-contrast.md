---
title: op_contraste
description: Ajustez le contraste. Ajuste le contraste de l’image en augmentant la luminosité des pixels avec plus de 50 % de luminosité et en réduisant la luminosité des pixels avec moins de 50 % de luminosité.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 0216f22e-a3b3-4dda-89c2-9c6c2c81cab3
TQID: 'https://experienceleague.adobe.com/Ob098G38TFXX0HzB3JQOCcdD9ZnrYWrMum6XEQSmGRU'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 143
ht-degree: 1%

---

# op_contraste{#op-contrast}

Ajustez le contraste. Ajuste le contraste de l’image en augmentant la luminosité des pixels avec plus de 50 % de luminosité et en réduisant la luminosité des pixels avec moins de 50 % de luminosité.

`op_contrast= *`adj`*`

<table id="simpletable_8246802C74424A68A7A2EA5B50A89D42"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> adj</span> </p> </td> 
  <td class="stentry"> <p>Ajustement du contraste en pourcentage (-100...100 int). </p></td> 
 </tr> 
</table>

## Propriétés {#section-d319ed55057344eab0a3c93f720acdbf}

Commande Calque. S’applique au calque actif ou à l’image composite, le cas `layer=comp`. Ignoré par les calques d’effet.

## Par défaut {#section-896d1b1f7f084e929355a4684f3e833b}

`op_contrast=0`, pas de changement de contraste. Les images ou calques CMJN sont convertis en RGB avant l’application de l’opération.

## Exemple {#section-94bc4348b4bc4f0e9768ea1c45ca8340}

Réduisez le contraste et la netteté d’un calque d’image de qualité supérieure pour le faire correspondre visuellement à une photo d’arrière-plan de faible qualité :

... `&op_blur=3&op_contrast=-12&`

Dans une version ultérieure, il est possible d’utiliser la luminosité médiane de l’image plutôt qu’une luminosité fixe de 50 %.
