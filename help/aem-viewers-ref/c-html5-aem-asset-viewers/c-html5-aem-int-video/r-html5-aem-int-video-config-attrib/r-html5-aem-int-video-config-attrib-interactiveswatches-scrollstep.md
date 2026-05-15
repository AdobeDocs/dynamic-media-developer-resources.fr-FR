---
title: InteractiveSwatches.scrollstep
description: Attribut de configuration pour la visionneuse de vidéos interactives.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Interactive Videos
role: Developer,User
exl-id: 15bf7af8-428b-4c1c-b7ad-004563347d7c
TQID: 'https://experienceleague.adobe.com/28KSiSs54nPSMOpQm7thVn5We8EBvmyAN-YHQB-aITA'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 65
ht-degree: 4%

---

# InteractiveSwatches.scrollstep{#interactiveswatches-scrollstep}

Attribut de configuration pour la visionneuse de vidéos interactives.

` [InteractiveSwatches.|<containerId>_interactiveSwatches.]scrollstep= *`étape`*`

<table id="table_441553CD34C94A58A9D7CBF772DEDDB6"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"><span class="varname"> étape</span></span> </p> </td> 
   <td colname="col2"> <p>Indique le nombre d’échantillons à faire défiler pour chaque appui du bouton de défilement correspondant. </p> <p>Si la valeur spécifiée est supérieure au nombre d’échantillons interactifs visibles, chaque appui ne fait défiler que le nombre d’échantillons visibles pour éviter l’omission d’un échantillon. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Propriétés {#section-1e637b22e8a44d759d588e47576891e6}

Facultatif.

## Par défaut {#section-71fb773f814649b2885aefee68073641}

`3`

## Exemple {#section-bce98c31f08a4a0ab262fab7f95ba020}

```
scrollstep=1
```
