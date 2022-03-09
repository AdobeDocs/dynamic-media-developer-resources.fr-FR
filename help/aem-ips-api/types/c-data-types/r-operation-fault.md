---
description: Message détaillé répondant à l’une des URL fournies dans la requête d’invalidation du réseau CDN.
solution: Experience Manager
title: OperationFault
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: e1fa7f66-f9d9-45cd-a9b3-d0ff344b137d
source-git-commit: 77c88d5fe20e048f6fad2bb23cb1abe090793acf
workflow-type: tm+mt
source-wordcount: '49'
ht-degree: 12%

---

# OperationFault{#operationfault}

Message détaillé répondant à l’une des URL fournies dans la requête d’invalidation du réseau CDN.

**Pris en charge depuis**

4.5.0, correctif 2011-02

## Paramètres {#section-cf4b0c923cef4c14869319af73ace58b}

| ** Nom** | ** Type** | ** Description** |
|---|---|---|
| code | `xsd:int` | Code d’erreur fourni à partir du CDN |
| motif | `xsd:string` | Message d’erreur fourni par le réseau de diffusion de contenu |
