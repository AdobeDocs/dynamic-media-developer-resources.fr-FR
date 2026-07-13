---
title: IccProfileSrcCmyk
description: Profil colorimétrique d’entrée CMJN par défaut. Indique le nom du profil de couleurs ICC à utiliser pour les images en matériau CMJN qui n’incorporent pas de profil de couleurs.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 09be34c8-facc-40c3-ba15-c48bd93b3be1
TQID: 'https://experienceleague.adobe.com/AX-NqS0F7TjgfLR2S8xyrJukDlB8-n-d17Bcn--AFrg'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 4339f336345d7d7f3c05c7f5a18fbd28bcfd382b
workflow-type: tm+mt
source-wordcount: 125
ht-degree: 2%

---

# IccProfileSrcCmyk{#iccprofilesrccmyk}

Profil colorimétrique d’entrée CMJN par défaut. Indique le nom du profil de couleurs ICC à utiliser pour les images en matériau CMJN qui n’incorporent pas de profil de couleurs.

## Propriétés {#section-0cee77438d914c319ec876edb3490821}

Chaîne de texte. Si spécifié, doit être une valeur de `icc::Name` valide de la carte de profil ICC de ce catalogue d’images ou du catalogue par défaut, ou un chemin d’accès au fichier relatif à `attribute::RootPath`. Le profil ICC référencé doit être un profil CMJN.

## Par défaut {#section-11f6239e0dd14827abf4a95c1b30161c}

Hérité de `default::IccProfileSrcCmyk` si non défini ou si vide. Si `attribute::IccProfileSrcCmyk` ne correspond pas à un profil valide, `attribute::IccProfileCmyk` est utilisé à la place.

## Voir aussi {#section-88adddd70265459a9a5d2f50829a4ba7}

[icc::Name](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-icc-profile-map-reference/r-ir-name-icc.md#reference-7a293ede360e433782575f8f6a562ac2) , [attribute::IccRenderIntent](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-iccrenderintent.md#reference-3b80b7a4c25545a593c5076f318b5c40), [attribute::IccProfileCmyk](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-iccprofilecmyk.md#reference-55aead2d924847ffbd1be4c46add7127), [attribute::RootPath](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-rootpath.md#reference-a4d7c96b62e14fcbad1740c702f160f3)

