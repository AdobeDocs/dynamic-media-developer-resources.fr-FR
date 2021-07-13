---
description: Orientation du rendu du texte. Indique l’angle à partir duquel le texte spécifié avec textPs= est disposé et rendu dans la zone de texte (définie avec size= ou textFlowPath=).
solution: Experience Manager
title: textAngle
feature: Dynamic Media Classic, SDK/API
role: Developer,User
exl-id: 102dbdc0-77b8-4c60-b456-6cf693e0b38b
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '106'
ht-degree: 5%

---

# textAngle{#textangle}

Orientation du rendu du texte. Indique l’angle à partir duquel le texte spécifié avec textPs= est disposé et rendu dans la zone de texte (définie avec size= ou textFlowPath=).

` textAngle= *`Angle`*`

<table id="simpletable_40832AC4B43A458CA69B225768124F58"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="varname"> Angle </span> </p> </td> 
  <td class="stentry"> <p>Angle de direction (degrés). </p> </td> 
 </tr> 
</table>

Les valeurs positives font pivoter le texte dans le sens des aiguilles d’une montre ; `textAngle=90` trace le texte de haut en bas.

## Propriétés {#section-6d586a632daa4261a8ce62db56140b36}

Attribut de calque. S’applique à `layer=0` si `layer=comp`. Ignoré si `textPs=` n’est pas spécifié pour ce calque ou si `textPath=` est spécifié.

## Par défaut {#section-49a9f5819c994c27928282c14b2bb2a7}

`textAngle=0` sans rotation.

## Voir aussi {#section-dccc29ff33704061b2519b56b7be45fd}

[Formatage de texte](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-text-formatting/c-text-formatting.md#concept-0d3136db7f6f49668274541cd4b6364c),  [positionnement de texte](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-text-formatting/r-text-positioning.md#reference-f647443d92914f4b89a7cc5a83267d87),  [textPs=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-textps.md#reference-4209a2a6169f44278da2647cfb0cd767),  [textFlowPath=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-textflowpath.md#reference-0b8d9493d71342f0b6a64a6d221584ef),  [textPath=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-textpath.md#reference-b09cc0902dff4725bdb54d5da4076ccd)
