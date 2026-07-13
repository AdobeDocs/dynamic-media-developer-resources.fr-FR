---
title: UseLastModified
description: Activez les en-têtes de réponse de dernière modification. Active ou désactive l’inclusion de l’en-tête Last-Modified dans les réponses HTTP pouvant être mises en cache émises par le rendu des images.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 31dfbc55-0efd-417b-be4a-67c878772388
TQID: 'https://experienceleague.adobe.com/X-d-02WckbxVyDxRvZDIcOghkk8Z8yYbGOZ3Aigx4ts'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 49c3ac586f6fb17608838f8dcf2c637822314fc7
workflow-type: tm+mt
source-wordcount: 237
ht-degree: 1%

---

# UseLastModified{#uselastmodified}

Activez les en-têtes de réponse de dernière modification. Active ou désactive l’inclusion de l’en-tête Last-Modified dans les réponses HTTP pouvant être mises en cache émises par le rendu des images.

Le serveur utilise la valeur d’`vignette::TimeStamp` et de `catalog::TimeStamp` la plus récente de toutes les vignettes et de tous les catalogues de matières/enregistrements de catalogue impliqués dans une réponse comme valeur d’en-tête Dernière modification .

Ne doit être activé que si un réseau de mise en cache distribué, tel qu’Akamai, est utilisé et ne prend pas en charge les en-têtes etag.

>[!NOTE]
>
>Des précautions doivent être prises lors de l’utilisation d’en-têtes Dernière modification dans un environnement à charge équilibrée impliquant plusieurs hôtes de diffusion/rendu d’images. La mise en cache client peut être annulée et la charge du serveur augmentée si, pour une raison quelconque, les serveurs ont des horodatages différents pour les mêmes entrées de catalogue. Une telle situation peut se produire comme suit :

* `catalog::TimeStamp`, `vignette::TimeStamp` ou `attribute::TimeStamp` n’est pas défini, de sorte que l’heure de modification du fichier [!DNL catalog.ini] est utilisée par défaut pour `catalog::TimeStamp`.

* Au lieu de partager les fichiers de catalogue de ressources par le biais d’un montage réseau, chaque serveur dispose de sa propre instance des fichiers de catalogue sur un système de fichiers local.
* Plusieurs instances d’un même fichier [!DNL catalog.ini] ont des dates de modification de fichier différentes, probablement en raison d’une copie incorrecte des fichiers.

## Propriétés {#section-453952244193452caccfaf7f601007c1}

Drapeau. 0 pour désactiver, 1 pour activer les en-têtes HTTP de dernière modification.

## Par défaut {#section-ec8fae847ca2421d8cdcde324e5a2d76}

Hérité de `default::UseLastModified` si non défini ou si vide.

## Voir aussi {#section-1536715169da48b0aecc4ab7326c86db}

[catalog::TimeStamp](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-material-data-reference/r-ir-timestamp-dataref.md#reference-6daf7973dc4f4b4e9e8165756db7c319) , [vignette::TimeStamp](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-vignette-map-reference/r-ir-timestamp-vignette.md#reference-d57cdd40a6a645d199dbb1d56cc85bc1)

