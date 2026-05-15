---
title: InteractiveSwatches.maxloadradius
description: Attribut de configuration pour la visionneuse de vidéos interactives.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Interactive Videos
role: Developer,User
exl-id: 16c9c70a-352d-4a21-bb14-2f9e266a83e8
TQID: 'https://experienceleague.adobe.com/BhsXOdgu2cCLX9hJEzn6PgW-aRjAZUybM4c891T7gZs'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 71
ht-degree: 4%

---

# InteractiveSwatches.maxloadradius{#interactiveswatches-maxloadradius}

Attribut de configuration pour la visionneuse de vidéos interactives.

` [InteractiveSwatches.|<containerId>_interactiveSwatches.]maxloadradius=-1|0| *`preloadnbr`*`

<table id="table_441553CD34C94A58A9D7CBF772DEDDB6"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">1|0|<span class="varname"> preloadnbr</span></span> </p> </td> 
   <td colname="col2"> <p> Indique le comportement de préchargement du composant. </p> <p>Lorsque la valeur est définie sur <span class="codeph"> -1</span> tous les échantillons sont chargés simultanément lorsque le composant est initialisé ou que la ressource est modifiée. </p> <p>Lorsque cette valeur est définie sur <span class="codeph"> 0</span> seuls les échantillons visibles sont chargés. </p> <p>Définissez sur <span class="codeph"><span class="varname"> preloadnbr</span></span> pour définir le nombre de lignes/colonnes invisibles autour de la zone visible qui sont préchargées. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Propriétés {#section-1e637b22e8a44d759d588e47576891e6}

Facultatif.

## Par défaut {#section-71fb773f814649b2885aefee68073641}

`1`

## Exemple {#section-bce98c31f08a4a0ab262fab7f95ba020}

```
maxloadradius=-1
```
