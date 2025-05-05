---
description: Message détaillé répondant à l’une des URL fournies dans la requête d’invalidation du réseau CDN.
solution: Experience Manager
title: OperationFault
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: e1fa7f66-f9d9-45cd-a9b3-d0ff344b137d
source-git-commit: f42378a20b58e4c5ebc961c6526d7cecabc2ae38
workflow-type: tm+mt
source-wordcount: '52'
ht-degree: 5%

---

# [!DNL OperationFault]{#operationfault}

Message détaillé répondant à l’une des URL fournies dans la requête d’invalidation du réseau CDN.

**Pris en charge depuis**

4.5.0, correctif 2011-02

## Paramètres {#section-cf4b0c923cef4c14869319af73ace58b}

| **&#x200B; Nom** | **&#x200B; Type** | **&#x200B; Description** |
|---|---|---|
| code | `xsd:int` | Code d’erreur fourni à partir du réseau de diffusion de contenu |
| motif | `xsd:string` | Message d’erreur fourni par le réseau de diffusion de contenu |
