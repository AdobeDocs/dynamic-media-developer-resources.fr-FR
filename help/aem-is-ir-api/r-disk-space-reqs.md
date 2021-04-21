---
description: 'Outre l’espace nécessaire à l’installation du logiciel, Image Serving dispose de l’espace disque requis suivant : '
solution: Experience Manager
title: Configuration requise et recommandations concernant l'espace disque
feature: Dynamic Media Classic,SDK/API
role: Developer,Business Practitioner
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '512'
ht-degree: 0%

---


# Configuration requise et recommandations relatives à l&#39;espace disque{#disk-space-requirements-and-recommendations}

Outre l’espace nécessaire à l’installation du logiciel, Image Serving dispose de l’espace disque requis suivant :

<table id="table_0AE363AB76304F258A19E43500FE8423"> 
 <thead> 
  <tr> 
   <th class="entry"> <b>Description/ Emplacement par défaut/ Jeu avec</b> </th> 
   <th class="entry"> <b>Calcul/Recommandation</b> </th> 
   <th class="entry"> <b>Commentaires</b> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td> <p><b>Images source, polices, profils ICC</b> </p> <p> <span class="filepath"> <span class="varname"> install_folder  </span>/images  </span> <span class="codeph"></span> </p> <p> <span class="codeph"> IS::RootPaths  </span> </p> </td> 
   <td> <p>Varie ; voir les commentaires ci-dessous. </p> </td> 
   <td> <p>Seuls doivent être accessibles au serveur Image Server ; les serveurs ne modifient jamais les données. </p> </td> 
  </tr> 
  <tr> 
   <td> <p><b>Cache de données de réponse HTTP</b> </p> <p> <span class="filepath"> <span class="varname"> install_folder  </span>/cache/is-response  </span> </p> <p> <span class="codeph"> PS::ResponseCacheFolders  </span> </p> </td> 
   <td> <p> <span class="codeph"> PlatformServer::cache.maxSize  </span> x 2; au moins 2 Go recommandés. </p> </td> 
   <td> <p>Ce cache stocke également les données imbriquées/incorporées et les images source étrangères. </p> </td> 
  </tr> 
  <tr> 
   <td> <p><b>Cache de données du catalogue d’images</b> </p> <p> <span class="filepath"> <span class="varname"> install_folder  </span>/cache/catalog  </span> </p> <p> <span class="codeph"> CS::CatalogCacheFolder  </span> </p> </td> 
   <td> <p>Autorisez le dossier de catalogue à utiliser 1,5 fois l’espace. </p> </td> 
   <td> <p>Renseigné lors du chargement initial des catalogues. </p> </td> 
  </tr> 
  <tr> 
   <td> <p><b>Données du journal</b> </p> <p> <span class="filepath"> <span class="varname"> install_folder  </span>/logs  </span> </p> <p> <span class="codeph"> PS::LogFolder  </span> </p> <p> <span class="codeph"> IS::LogFile  </span> </p> <p> <span class="codeph"> SV::LogFile  </span> </p> </td> 
   <td> <p>100 Mo ou plus. </p> </td> 
   <td> <p>Varie selon la configuration de journalisation et l’utilisation du serveur. </p> </td> 
  </tr> 
  <tr> 
   <td> <p><b>Fichiers temporaires Image Server</b> </p> <p> <span class="filepath"> <span class="varname"> install_folder  </span>/temp  </span> </p> <p> <span class="codeph"> IS::TempDirectory  </span> </p> <p> <span class="codeph"> SV::TempDirectory  </span> </p> </td> 
   <td> <p>100 Moytes est suffisant pour la plupart des utilisations. </p> </td> 
   <td> <p>les données de courte durée ; peut être nécessaire pour les images source autres que les fichiers PTIFF et certains formats d’image de réponse. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Espace disque requis pour les images source {#section-317da75099ad480d9a461c7e706d4f1c}

Il est recommandé de convertir toutes les images source au format PTIFF (pyramid TIFF file format) à l’aide de l’outil de ligne de commande Image Converter (IC). Cette conversion garantit des performances d’exécution optimales de la diffusion d’images pour toutes les applications. Bien que le serveur Image Server puisse traiter tous les formats de fichiers source acceptés par IC, Dynamic Media ne prend pas en charge ces utilisations.

Lorsque vous utilisez des fichiers PTIFF, les règles générales suivantes peuvent vous aider à déterminer l’espace requis.

*`total_space`* (octets) =  *`number_of_images`* x(2000 +  *`avg_pixel_count`* x  *`avg_num_components`* x  *`p_factor`*)

* *`avg_pixel_count`* Taille moyenne en pixels (largeur x hauteur) de toutes les images source d’origine. Par exemple, si les images d’origine font généralement environ 2 k x 2 k de pixels, il s’agit de 4 M de pixels.
* *`avg_num_components`* Dépend du type d’image. Pour la plupart des images RVB, il s’agit de 3, pour la plupart des images CMJN ou RGBA, il s’agit de 4. Utilisez la version 3.5 si la moitié des images est RVB et l’autre moitié RVB.
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
   <td> <p>Déflure-Compression </p> </td> 
   <td> <p> 25-0,75, selon l’image </p> </td> 
  </tr> 
  <tr> 
   <td> <p>Compression JPEG </p> </td> 
   <td> <p> 1 (standard pour la qualité JPEG 95) </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>Cette approximation ne tient pas compte des frais généraux du système de fichiers. L&#39;espace réel sur le disque peut être considérablement plus grand.

**Exemple**

Un déploiement de la diffusion d’images prévoit d’utiliser 30 000 images héritées basse résolution, d’une taille moyenne de 500 x 500 pixels RVB. Les nouvelles données d&#39;image imprimées devraient être ajoutées au taux de 10 000 par année. La taille d’image CMJN type sera de 4 k x 6 k octets. Toutes les données seront compressées au format JPEG en haute qualité. La quantité totale d&#39;espace disque après 3 ans d&#39;utilisation est estimée comme suit :

*`total_space`* = 30 000 x (2 k + 0,5 k x 0,5 k x 3 x 0,1) + 3 x 10 000 x (2 k + 4 k x 6 k x 4 x 0,1) = 2,2 G + 268 Go = environ 270 Go

Pour une qualité garantie optimale, la compression déflate (zip) peut être utilisée. En supposant un *`p_factor`* de 0,4, la quantité totale d&#39;espace disque requise est environ 4 fois supérieure. Dans ce cas, un peu plus de 1 To.
