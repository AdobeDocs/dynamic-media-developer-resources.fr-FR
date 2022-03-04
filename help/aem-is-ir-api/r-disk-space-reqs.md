---
description: 'Outre l’espace nécessaire à l’installation du logiciel, le serveur d’images a les exigences suivantes en termes d’espace disque : '
solution: Experience Manager
title: Exigences et recommandations relatives à l’espace disque
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 35486f3f-f0aa-4b69-a1d2-4bc6b5e41c43
source-git-commit: 790ce3aa4e9aadc019d17e663fc93d7c69772b23
workflow-type: tm+mt
source-wordcount: '502'
ht-degree: 0%

---

# Exigences et recommandations relatives à l’espace disque{#disk-space-requirements-and-recommendations}

En plus de l’espace nécessaire à l’installation du logiciel, Image Serving a les exigences suivantes en termes d’espace disque :

<table id="table_0AE363AB76304F258A19E43500FE8423"> 
 <thead> 
  <tr> 
   <th class="entry"> <b>Description/ Emplacement par défaut/ Défini avec</b> </th> 
   <th class="entry"> <b>Calcul/recommandation</b> </th> 
   <th class="entry"> <b>Commentaires</b> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td> <p><b>Images sources, polices, profils ICC</b> </p> <p> <span class="filepath"> <span class="varname"> install_folder </span>/images </span> <span class="codeph"></span> </p> <p> <span class="codeph"> IS::RootPaths </span> </p> </td> 
   <td> <p>Varie; voir les commentaires ci-dessous. </p> </td> 
   <td> <p>doit uniquement être accessible au serveur d’images ; les serveurs ne modifient jamais les données. </p> </td> 
  </tr> 
  <tr> 
   <td> <p><b>Cache de données de réponse HTTP</b> </p> <p> <span class="filepath"> <span class="varname"> install_folder </span>/cache/is-response </span> </p> <p> <span class="codeph"> PS::ResponseCacheFolders </span> </p> </td> 
   <td> <p> <span class="codeph"> PlatformServer::cache.maxSize </span> x 2; au moins 2 Go recommandé. </p> </td> 
   <td> <p>Ce cache stocke également les données imbriquées/incorporées et les images sources étrangères. </p> </td> 
  </tr> 
  <tr> 
   <td> <p><b>Cache de données du catalogue d’images</b> </p> <p> <span class="filepath"> <span class="varname"> install_folder </span>/cache/catalog </span> </p> <p> <span class="codeph"> CS::CatalogCacheFolder </span> </p> </td> 
   <td> <p>Autorisez le dossier de catalogue à utiliser 1.5x l’espace. </p> </td> 
   <td> <p>Renseigné lorsque les catalogues sont initialement chargés. </p> </td> 
  </tr> 
  <tr> 
   <td> <p><b>Données du journal</b> </p> <p> <span class="filepath"> <span class="varname"> install_folder </span>/logs </span> </p> <p> <span class="codeph"> PS::LogFolder </span> </p> <p> <span class="codeph"> IS::LogFile </span> </p> <p> <span class="codeph"> SV::LogFile </span> </p> </td> 
   <td> <p>100 Mo ou plus. </p> </td> 
   <td> <p>Varie en fonction de la configuration de journalisation et de l’utilisation du serveur. </p> </td> 
  </tr> 
  <tr> 
   <td> <p><b>Fichiers temporaires du serveur d’images</b> </p> <p> <span class="filepath"> <span class="varname"> install_folder </span>/temp </span> </p> <p> <span class="codeph"> IS::TempDirectory </span> </p> <p> <span class="codeph"> SV::TempDirectory </span> </p> </td> 
   <td> <p>100 Mo sont suffisants pour la plupart des utilisations. </p> </td> 
   <td> <p>les données de courte durée; peut être nécessaire pour les images source autres que les fichiers PTIFF et certains formats d’image de réponse. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Exigences d’espace disque pour les images sources {#section-317da75099ad480d9a461c7e706d4f1c}

Il est recommandé de convertir toutes les images source au format de fichier de TIFF pyramid (PTIFF) à l’aide de l’outil de ligne de commande du convertisseur d’images (IC). Cette conversion garantit des performances d’exécution optimales du serveur d’images pour toutes les applications. Bien que le serveur d’images puisse traiter tous les formats de fichiers source acceptés par IC, Dynamic Media ne prend pas en charge ces utilisations.

Lorsque vous utilisez des fichiers PTIFF, les règles de base suivantes peuvent vous aider à déterminer les exigences d’espace.

*`total_space`* (octets) = *`number_of_images`* x(2000 + *`avg_pixel_count`* x *`avg_num_components`* x *`p_factor`*)

* *`avg_pixel_count`* Taille moyenne en pixels (largeur x hauteur) de toutes les images sources originales. Par exemple, si les images d’origine font généralement environ 2 000 x 2 000 pixels, il s’agit de 4 millions de pixels.
* *`avg_num_components`* Dépend du type d’image. Pour les images principalement RGB, il est 3, pour les images CMJN ou RGBA, il est 4. Utilisez la version 3.5 si la moitié des images est RGB et que l’autre moitié est RGBA.
* *`p_factor`* Dépend du type de compression et du jeu de qualité lorsque les images sont converties avec IC.

<table id="table_89995BECF30243569954819D07DA2A2F"> 
 <thead> 
  <tr> 
   <th class="entry"> <b>Compression PTIFF</b> </th> 
   <th class="entry"> <b><i>p_factor</i></b> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td> <p>Non compressé </p> </td> 
   <td> <p> 33 </p> </td> 
  </tr> 
  <tr> 
   <td> <p>Compression de la déflation </p> </td> 
   <td> <p> 25 à 0,75, selon l’image </p> </td> 
  </tr> 
  <tr> 
   <td> <p>Compression JPEG </p> </td> 
   <td> <p> 1 (standard pour la qualité de JPEG 95) </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>Cette approximation ne prend pas en compte les frais généraux du système de fichiers. L’espace réel sur le disque peut être considérablement plus grand.

**Exemple**

Un déploiement de diffusion d’images prévoit d’utiliser 30 000 images héritées basse résolution, avec une taille moyenne de 500 x 500 pixels de RGB. De nouvelles données d’image de qualité imprimée devraient être ajoutées au taux de 10 000 par an. La taille d’image CMJN type est de 4 Ko x 6 Ko. Toutes les données sont compressées en JPEG à haute qualité. La quantité totale d’espace disque après 3 ans d’utilisation est estimée comme suit :

*`total_space`* = 30 000 x (2k + 0,5k x 0,5k x 3 x 0,1) + 3 x 10 000 x (2k + 4k x 6k x 4 x 0,1) = 2,2 G + 268 Go = environ 270 Go

Pour garantir une qualité optimale, la compression déflée (zip) peut être utilisée. En supposant une *`p_factor`* de 0,4, la quantité totale d’espace disque requise est environ 4 fois plus grande. Dans ce cas, un peu plus de 1 To.
