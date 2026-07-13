---
title: Traitement des variables dans les requêtes imbriquées
description: Les références $var$ peuvent se produire n’importe où dans les accolades d’une requête de diffusion d’images ou de rendu d’image imbriquée, y compris à gauche du caractère « ? » séparant le chemin d’accès de la requête.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: fa82ec48-aeec-4cd9-8d2e-cf9c913c67a7
TQID: 'https://experienceleague.adobe.com/m7BlSGU8gSozgp8fvNcWuMz5uvpUrfMi4fV5yCYH5bs'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 4339f336345d7d7f3c05c7f5a18fbd28bcfd382b
workflow-type: tm+mt
source-wordcount: 162
ht-degree: 0%

---

# Traitement des variables dans les requêtes imbriquées{#variable-processing-in-nested-requests}

Les références $var$ peuvent se produire n’importe où dans les accolades d’une requête de diffusion d’images ou de rendu d’image imbriquée, y compris à gauche du caractère « ? » séparant le chemin d’accès de la requête.

Le serveur remplace ces références par des valeurs (provenant de l’URL ou de l’`catalog::Modifier` du catalogue d’images principal) avant d’analyser et de traiter plus en détail la requête imbriquée.

En outre, toutes les définitions de `$ *[!DNL var]*=` de l’URL et du `catalog::Modifier` sont transférées à toutes les requêtes de diffusion d’images et de rendu d’images imbriquées. Cela permet de s’assurer que toutes les définitions de variable sont disponibles pour tous les modèles, quel que soit le niveau d’imbrication.

Quel que soit le niveau d’imbrication, seul le codage HTTP à une seule passe doit être appliqué aux valeurs de variable qui doivent être remplacées n’importe où dans les requêtes de rendu d’image ou de diffusion d’image imbriquées.

