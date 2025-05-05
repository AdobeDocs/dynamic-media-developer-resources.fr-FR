---
title: réseau
description: Découvrez comment utiliser l’optimisation de la bande passante du réseau pour ajuster la qualité de l’image diffusée en fonction de la bande passante du réseau.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 7df6eeed-1856-40e1-bd5d-8f06efc7f700
source-git-commit: 63c0e3b494b6d583117dad01643946900855802e
workflow-type: tm+mt
source-wordcount: '148'
ht-degree: 4%

---

# réseau{#network}

L’activation de la bande passante réseau ajuste automatiquement la qualité de l’image diffusée en fonction de la bande passante réseau réelle. Pour une bande passante réseau médiocre, l’optimisation de [DPR (Device Pixel Ratio)](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-dpr.md) est automatiquement désactivée, même si elle est déjà activée.

Si vous le souhaitez, votre entreprise peut se désabonner de l’optimisation de la bande passante du réseau au niveau de l’image individuelle en ajoutant `network=off` à l’URL de l’image.

`network=on|off`

<table id="simpletable_2D23B1B282CD4216AB5BE7E7430D1B3F"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> on|off </span> </p> </td> 
  <td class="stentry"> <p>Indique si la bande passante réseau ajuste la qualité de l’image diffusée en fonction de la bande passante réseau réelle (activée) ou si l’optimisation de la bande passante réseau est désactivée pour aucun ajustement de la qualité de l’image.</p> </td> 
 </tr> 
</table>

Les valeurs de bande passante réseau sont basées sur les valeurs côté client détectées du réseau de diffusion de contenu groupé.

## Propriétés

Attribut de requête. Cela n’a aucun effet si les conditions de réseau sont excellentes.

## Par défaut

`network=off`

## Exemple

`https://smartimaging.scene7.com/is/image/ADBE/AdobeStock_409826521?dpr=on,3&network=on`

## Voir aussi

[bfc](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-bfc.md), [drp](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-dpr.md), [Smart Imaging](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/assets/dynamicmedia/imaging-faq.html?lang=fr)
