---
title: op_saturation
description: Régler la saturation. Modifie la saturation de chaque pixel visible du calque ou de l’image composite.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: cd71e27e-6ccc-4ade-9bcf-af8e41bcf381
TQID: 'https://experienceleague.adobe.com/lTgjlQNmfVcS1XswABjicGEHjDUO1PVjM7wD1Zi6o2M'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 93
ht-degree: 2%

---

# op_saturation{#op-saturation}

Régler la saturation. Modifie la saturation de chaque pixel visible du calque ou de l’image composite.

`op_saturation= *`adj`*`

<table id="simpletable_5F118A28FE674B06A16F6F19C56B4594"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> adj</span> </p> </td> 
  <td class="stentry"> <p>Réglage de la saturation (-100...+100 int). </p></td> 
 </tr> 
</table>

`op_saturation=-100` désature complètement l’image.

## Propriétés {#section-9a3cc9ff060049449554dfa69d92fd53}

Commande Calque. S’applique au calque actif ou à l’image composite, le cas `layer=comp`. Ignoré par les calques d’effet.

## Par défaut {#section-ef0e78f55c8b4d22aee09104dad6410a}

`op_saturation=0`, pas de changement de saturation. Les images ou calques CMJN sont convertis en RGB avant l’application de l’opération.

## Exemple {#section-033b272f1b7e4efeb94e841fd8095357}

Manipulez une photographie en couleurs afin d’obtenir un aspect « high-key » :

`http://server/myRootId/myImageId?op_saturation=-60&op_brightness=45&op_contrast=-35`
