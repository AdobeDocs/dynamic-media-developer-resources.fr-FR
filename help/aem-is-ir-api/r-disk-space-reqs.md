---
title: Exigences et recommandations en matière d’espace disque
description: Outre l’espace nécessaire à l’installation du logiciel, la diffusion d’images requiert l’espace disque suivant.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 35486f3f-f0aa-4b69-a1d2-4bc6b5e41c43
source-git-commit: 6a4c1f4425199cfa6088fc42137552748c1a9dcf
workflow-type: tm+mt
source-wordcount: '503'
ht-degree: 0%

---

# Exigences et recommandations en matière d’espace disque{#disk-space-requirements-and-recommendations}

Outre l’espace nécessaire à l’installation du logiciel, la diffusion d’images requiert l’espace disque suivant :

<table id="table_0AE363AB76304F258A19E43500FE8423"> 
 <thead> 
  <tr> 
   <th class="entry"> <b>Description/ Emplacement Par Défaut/ Défini Avec</b> </th> 
   <th class="entry"> <b>Calcul/Recommandation</b> </th> 
   <th class="entry"> <b>Commentaires</b> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td> <p><b>Images Source, polices, profils ICC</b> </p> <p> <span class="filepath"> <span class="varname"> install_folder </span>/images </span> <span class="codeph"></span> </p> <p> <span class="codeph"> IS::RootPaths </span> </p> </td> 
   <td> <p>Varie ; voir les commentaires ci-dessous. </p> </td> 
   <td> <p>Seuls doivent être accessibles au serveur d’images, qui ne modifie jamais les données. </p> </td> 
  </tr> 
  <tr> 
   <td> <p><b>Cache de données de réponse HTTP</b> </p> <p> <span class="filepath"> <span class="varname"> install_folder </span>/cache/is-response </span> </p> <p> <span class="codeph"> PS::ResponseCacheFolders </span> </p> </td> 
   <td> <p> <span class="codeph"> PlatformServer::cache.maxSize </span> x 2 ; au moins 2 Go recommandé. </p> </td> 
   <td> <p>Ce cache stocke également les données imbriquées/incorporées et les images sources étrangères. </p> </td> 
  </tr> 
  <tr> 
   <td> <p><b>Cache de données de catalogue d’images</b> </p> <p> <span class="filepath"> <span class="varname"> install_folder </span>/cache/catalog </span> </p> <p> <span class="codeph"> CS::CatalogCacheFolder </span> </p> </td> 
   <td> <p>Autorisez le dossier de catalogue à utiliser 1,5 fois l’espace. </p> </td> 
   <td> <p>Renseigné lors du chargement initial des catalogues. </p> </td> 
  </tr> 
  <tr> 
   <td> <p><b>Consigner les données</b> </p> <p> <span class="filepath"> <span class="varname"> install_folder </span>/logs </span> </p> <p> <span class="codeph"> PS::LogFolder </span> </p> <p> <span class="codeph"> IS::LogFile </span> </p> <p> <span class="codeph"> SV::LogFile </span> </p> </td> 
   <td> <p>100 Mo ou plus. </p> </td> 
   <td> <p>Elle varie en fonction de la configuration de journalisation et de l’utilisation du serveur. </p> </td> 
  </tr> 
  <tr> 
   <td> <p><b>Fichiers temporaires du serveur d’images</b> </p> <p> <span class="filepath"> <span class="varname"> install_folder </span>/temp </span> </p> <p> <span class="codeph"> IS::TempDirectory </span> </p> <p> <span class="codeph"> SV::TempDirectory </span> </p> </td> 
   <td> <p>100 Mo sont suffisants pour la plupart des utilisations. </p> </td> 
   <td> <p>Données de courte durée ; peuvent être nécessaires pour les images sources autres que les PTIFF et certains formats d’image de réponse. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Espace disque requis pour les images sources {#section-317da75099ad480d9a461c7e706d4f1c}

Adobe vous recommande de convertir toutes les images sources au format de fichier pyramid TIFF (PTIFF) à l’aide de l’outil de ligne de commande Convertisseur d’images (IC). Cette conversion garantit des performances d’exécution optimales de la diffusion d’images pour toutes les applications. Bien que le serveur d’images puisse traiter tous les formats de fichiers sources acceptés par IC, Dynamic Media ne prend pas en charge ces utilisations.

Lorsque vous utilisez des fichiers PTIFF, les règles de base suivantes peuvent vous aider à déterminer l’espace requis.

*`total_space`* (octets) = *`number_of_images`* × (2 000 + *`avg_pixel_count`* x *`avg_num_components`* × *`p_factor`*)

* *`avg_pixel_count`* Taille moyenne en pixels (largeur x hauteur) de toutes les images source d’origine. Par exemple, si les images d’origine font généralement environ 2 000 × 2 000 pixels, il s’agit de 4 mégapixels.
* *`avg_num_components`* Dépend du type d’images. Pour la plupart des images RGB, elle est de 3 ; pour la plupart des images CMJN ou RGBA, elle est de 4. Utilisez la version 3.5 si la moitié des images est RGB et l’autre moitié est RGBA.
* *`p_factor`* Dépend du type de compression et du jeu de qualité lorsque les images sont converties avec IC.

<table id="table_89995BECF30243569954819D07DA2A2F"> 
 <thead> 
  <tr> 
   <th class="entry"> <b>compression PTIFF</b> </th> 
   <th class="entry"> <b><i>p_factor</i></b> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td> <p>Non compressé </p> </td> 
   <td> <p> 33 </p> </td> 
  </tr> 
  <tr> 
   <td> <p>Compression-Dégonflage </p> </td> 
   <td> <p> 25-0,75, selon l'image </p> </td> 
  </tr> 
  <tr> 
   <td> <p>Compression JPEG </p> </td> 
   <td> <p> 1 (standard pour la qualité JPEG 95) </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>Cette approximation ne tient pas compte de la surcharge du système de fichiers. L&#39;espace réel sur le disque peut être sensiblement plus grand.

**Exemple**

Un déploiement de diffusion d’images s’attend à utiliser 30 000 images héritées basse résolution, avec une taille moyenne de 500 × 500 pixels RGB. De nouvelles données d’image de qualité d’impression sont ajoutées à raison de 10 000 par an. La taille standard de l’image CMJN est de 4 Ko × 6 Ko. Toutes les données sont compressées sous JPEG et de haute qualité. La quantité totale d’espace disque après trois ans d’utilisation est estimée comme suit :

*`total_space`* = 30 000 × (2k + 0,5k × 0,5k × 3 × 0,1) + 3 × 10 000 × (2k + 4k × 6k × 4 × 0,1) = 2,2 G + 268 Go = environ 270 Go

Pour garantir la meilleure qualité, une compression telle qu&#39;une fermeture éclair pourrait être employée. En supposant une *`p_factor`* de 0,4, la quantité totale d’espace disque requise est environ quatre fois plus importante. Dans ce cas, légèrement plus de 1 téraoctet.
