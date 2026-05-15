---
description: Le serveur surveille en permanence le dossier de catalogue et recharge automatiquement un catalogue d’images, y compris les fichiers de données de catalogue associés, lorsqu’il détecte que le fichier d’attributs de catalogue principal a été modifié.
solution: Experience Manager
title: Mise à jour des catalogues d’images
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: b520b4f3-6717-4768-99e2-78a76d1ede24
TQID: 'https://experienceleague.adobe.com/vnAa-SrnEWsyYW3PuGQT-CjlhGBB9nkQ20hZSKCUuUw'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 307
ht-degree: 0%

---

# Mise à jour des catalogues d’images{#updating-image-catalogs}

Le serveur surveille en permanence le dossier de catalogue et recharge automatiquement un catalogue d’images, y compris les fichiers de données de catalogue associés, lorsqu’il détecte que le fichier d’attributs de catalogue principal a été modifié.

Pour mettre à jour les catalogues d’images sur le serveur, remplacez d’abord tous les fichiers de données de catalogue à modifier, puis remplacez (ou « appuyez » pour mettre à jour la date du fichier) le fichier d’attributs de catalogue pour déclencher le rechargement du catalogue.

## Mises à jour incrémentielles {#section-2c0f2c1b8480486d86920b5f2cfe72d2}

Le chargement et le traitement de catalogues d’images volumineux peuvent placer une charge importante sur le serveur et avoir un impact négatif sur les opérations de diffusion en direct. Pour minimiser cet impact, il est recommandé de mettre en œuvre un mécanisme de mise à jour incrémentielle du catalogue, qui fonctionne comme suit :

Un fichier catalogue principal contenant toutes les images est chargé chaque nuit pendant les heures de faible trafic. S’il est nécessaire d’ajouter ou de modifier des enregistrements dans le catalogue d’images au cours de la journée, un autre fichier de données d’image est créé qui contient uniquement les enregistrements nouveaux ou modifiés. Ce fichier est enregistré en tant que fichier de données d’image secondaire dans `attribute::CatalogFile`. Le serveur détecte que le fichier d’attributs de catalogue a été modifié, puis vérifie quels fichiers de données de catalogue ont été modifiés. Si le fichier de données d’image principal n’a pas été touché, le serveur charge ou recharge uniquement le fichier de données incrémentielles. Ce fichier étant généralement beaucoup plus petit que le fichier de catalogue principal, l’impact sur le serveur est beaucoup plus faible que lors du rechargement du catalogue principal.

Les mises à jour incrémentielles peuvent réduire considérablement l’impact sur le serveur en cas de trafic important. Il est recommandé de fusionner régulièrement le fichier de données de catalogue incrémentiel dans le fichier de données de catalogue principal pendant les heures de faible trafic pour maintenir des performances de serveur optimales.
