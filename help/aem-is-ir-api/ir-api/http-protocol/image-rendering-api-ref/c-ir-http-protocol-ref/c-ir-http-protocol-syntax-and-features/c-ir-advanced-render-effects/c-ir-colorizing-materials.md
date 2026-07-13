---
title: Matériaux colorants
description: La plupart des matériaux peuvent être colorés dynamiquement.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 95b13a57-f10b-4ff2-90fd-507e69cb2b04
TQID: 'https://experienceleague.adobe.com/MGmuOj214tFPKeSGwz33pGn2m0B0fme1Cq-umlxG9v0'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 4339f336345d7d7f3c05c7f5a18fbd28bcfd382b
workflow-type: tm+mt
source-wordcount: 76
ht-degree: 0%

---

# Matériaux colorants{#colorizing-materials}

La plupart des matériaux peuvent être colorés dynamiquement.

L’algorithme de colorisation est simpliste et fonctionne mieux pour les images matérielles qui ont une plage de teintes limitée. Pour colorer un matériau, le moteur de rendu soustrait simplement la valeur `bgc=` et ajoute la valeur `color=` à chaque valeur en pixels.

La colorisation est désactivée si `color=` n’est pas spécifié. L&#39;attribut `bgc=` est ignoré par les matériaux de l&#39;armoire ; la valeur de couleur de base incorporée dans le fichier [!DNL vnc] est utilisée à la place.

