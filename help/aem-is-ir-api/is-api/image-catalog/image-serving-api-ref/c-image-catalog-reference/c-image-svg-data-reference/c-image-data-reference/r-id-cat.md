---
description: Identifiant de l’enregistrement de catalogue
solution: Experience Manager
title: ID
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 37945115-c93d-4f59-b3d3-a2c4ee7fc990
TQID: 'https://experienceleague.adobe.com/M3stRhM1PHUVUFXTKj-KERQVMOGVolpxUuyNUrRzado'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 99
ht-degree: 7%

---

# ID {#id}

Valeur de clé d’index selon laquelle les enregistrements du fichier de données d’image sont recherchés par le [!DNL Platform Server].

En règle générale, un identifiant d’image court et unique, tel qu’un numéro de SKU, éventuellement avec un certain type de suffixe d’image, si un SKU comporte plusieurs images. Il peut également s’agir d’une chaîne plus complexe qui s’apparente davantage à un chemin de fichier, pour prendre en charge la réadaptation facile des sites web avec la diffusion d’images.

## Propriétés {#id-properties}

Chaîne de texte. Obligatoire. Clé d’index de Principal pour le tableau de données d’image. Chaque valeur catalog::Id doit être unique dans la table.

## Par défaut {#id-default}

Aucune

## Voir aussi {#id-seealso}

[attribute::RootId](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-rootid.md)
