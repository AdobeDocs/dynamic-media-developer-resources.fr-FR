---
description: Utilisez ces paramètres de serveur pour les dossiers de données de contenu.
solution: Experience Manager
title: Dossiers de données de contenu
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin,User
exl-id: 9aa4121f-25f8-49d0-a304-7ae756c046f5
TQID: 'https://experienceleague.adobe.com/IM1zNaaqC0zD36pUobHIL0Z-rlcrZoujnPbpBtOXq1Y'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
topic_v2:
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 226
ht-degree: 0%

---

# Dossiers de données de contenu{#content-data-folders}

Utilisez ces paramètres de serveur pour les dossiers de données de contenu.

## IS::RootPath - Dossiers racine des données d’image {#section-5c57569514bb4d00b19de31d2e137e3b}

L’emplacement de toutes les données sources, y compris les images, les polices et les profils ICC. Il peut s’agir d’un ou plusieurs chemins d’accès absolus aux fichiers ou chemins d’accès relatifs à *[!DNL install_folder]*, séparés par des points-virgules. Si vide, *[!DNL install_folder]* est la racine par défaut. Plusieurs valeurs peuvent être spécifiées pour distribuer les données d’image sur plusieurs systèmes de fichiers. Le serveur d’images tente d’accéder aux chemins d’accès racine dans l’ordre spécifié jusqu’à ce que le fichier demandé soit trouvé.

## PS::staticContent.rootPath - Dossiers racine de données de contenu statique {#section-a4f5b6942b7b4abdbf825b1f2e932cfe}

Emplacement des données sources de contenu statique destinées à être diffusées par le biais du contexte de [!DNL /is/static]. Il peut s’agir d’un ou plusieurs chemins d’accès absolus au fichier ou de chemins relatifs à *[!DNL install_folder]*, séparés par des points-virgules. Si vide, *[!DNL install_folder]* est la racine par défaut.

Plusieurs valeurs peuvent être spécifiées et séparées par des points-virgules pour distribuer le contenu statique sur plusieurs systèmes de fichiers. Généralement définie sur les mêmes valeurs que `IS::RootPath`.

Le [!DNL Platform Server] tente d’accéder aux chemins d’accès racine dans l’ordre spécifié jusqu’à ce que le fichier demandé soit trouvé.

>[!NOTE]
>
>Par défaut, ce champ est délibérément défini sur un emplacement non existant ( [!DNL *[!DNL install_folder]*/static]), ce qui désactive le service de contenu statique.

## IS::SaveDirectory - Fichier Enregistrer le dossier racine {#section-1c517f8d49ce4cb8b9013e520bf309c9}

Chemin d’accès racine de `attribute::SavePath` (utilisé par `req=saveToFile`). Le serveur d’images doit disposer des autorisations d’accès en création pour le sous-dossier dans lequel il crée les fichiers image.
