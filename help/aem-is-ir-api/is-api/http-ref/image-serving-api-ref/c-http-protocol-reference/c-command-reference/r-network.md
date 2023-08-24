---
title: réseau
description: Découvrez comment utiliser l’optimisation de la bande passante du réseau pour ajuster la qualité de l’image diffusée en fonction de la bande passante du réseau.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
source-git-commit: a6e0db8238ba5f2209089c6eda7b42c42f66b25f
workflow-type: tm+mt
source-wordcount: '157'
ht-degree: 3%

---

# réseau{#network}

L’activation de la bande passante réseau ajuste automatiquement la qualité de l’image diffusée en fonction de la bande passante réseau réelle. Pour une bande passante réseau médiocre, [RGPD (rapport des pixels de l’appareil)](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-dpr.md) l’optimisation est automatiquement désactivée, même si elle est déjà activée.

Si vous le souhaitez, votre entreprise peut exclure l’optimisation de la bande passante du réseau au niveau de l’image individuelle en ajoutant `network=off` à l’URL de l’image.

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

[bfc](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-bfc.md), [drp](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-dpr.md), [Imagerie dynamique](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/assets/dynamicmedia/imaging-faq.html?lang=en)