---
title: Domaines de confiance
description: Flash domaines Web d’application. Adobe Flash applications peuvent nécessiter l’accès aux propriétés des images livrées au format SWF. Le fichier SWF doit accorder l’accès explicitement en enregistrant le nom des domaines d’application qu’il approuve.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 41794f62-6140-4e54-9de2-908b20c51b37
source-git-commit: 8454991568374ecd1c4babdd3210250ea7988c4c
workflow-type: tm+mt
source-wordcount: '116'
ht-degree: 2%

---

# Domaines de confiance{#trusteddomains}

Flash domaines Web d’application. Adobe Flash applications peuvent nécessiter l’accès aux propriétés des images livrées au format SWF. Le fichier SWF doit accorder l’accès explicitement en enregistrant le nom des domaines d’application qu’il approuve.

## Propriétés {#section-5d6ecfa431a04abd8628a28e0ab3be83}

Chaîne contenant une liste de noms de domaine Web séparés par des virgules. Si elles sont vides, les applications doivent être traitées à partir du même domaine que Image Rendering pour pouvoir accéder aux propriétés des images dans [!DNL swf]les réponses formatées.

## Par défaut {#section-8fae0c896f7d46e7a61b0fd7e2b34dc3}

Héritée de si elle n’est `default::TrustedDomains` pas présente.

## Voir aussi {#section-2f829671c385411d8e1a7525def5529f}

[src=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-src.md#reference-62c98abad22149d68d405ed6aaff8272) , `mask=`, [attribute ::RootUrl](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-rooturl.md#reference-b8d706a573814802bd6794223cc78402)
