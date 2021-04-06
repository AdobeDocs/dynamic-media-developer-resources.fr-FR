---
description: Toutes les fonctionnalités exposées dans l’interface de la visionneuse de zoom de base, catalogue électronique, recherche de catalogue électronique, fenêtre déroulante, zoom en ligne, supports variés, à 360°, vidéo, zoom, dimension (3D), carrousel, image interactive, vidéo interactive et vidéo360 sont accessibles au clavier.
solution: Experience Manager
title: Accessibilité et navigation du clavier
feature: Dynamic Media Classic, Visionneuses, SDK/API
role: Développeur, Professionnel
exl-id: 0bdf172a-0bde-42d2-900f-f207538fe588
translation-type: tm+mt
source-git-commit: 62234233bb1a5bcbd0eac5d281b42ed785c0c169
workflow-type: tm+mt
source-wordcount: '587'
ht-degree: 0%

---

# Accessibilité du clavier et navigation{#keyboard-accessibility-and-navigation}

Toutes les fonctionnalités exposées dans l’interface de la visionneuse de zoom de base, catalogue électronique, recherche de catalogue électronique, fenêtre déroulante, zoom en ligne, supports variés, à 360°, vidéo, zoom, carrousel, dimension (3D), image interactive, vidéo interactive et vidéo360 sont accessibles au clavier.

<!-- Updated June 1, 2020 from https://wiki.corp.adobe.com/pages/viewpage.action?spaceKey=scene7qa&title=s7Viewers%2C+S7SDK%2C+S7OnDemand+Release+Notes - Contact is Sasha -->

## Accessibilité du clavier et navigation {#topic-f5650e9493404e55a3627c8d1366b861}

Toutes les fonctionnalités exposées dans l’interface de la visionneuse de zoom de base, catalogue électronique, recherche de catalogue électronique, fenêtre déroulante, zoom en ligne, supports variés, à 360°, vidéo, zoom, carrousel, dimension (3D), image interactive, vidéo interactive et vidéo360 sont accessibles au clavier.

Un utilisateur final peut naviguer entre les éléments de l’interface utilisateur de la visionneuse à l’aide des touches **[!UICONTROL Tabulation]** et **[!UICONTROL Maj+Tabulation]**. L’utilisation de l’onglet **[!UICONTROL Tab]** permet d’activer la cible d’action sur l’élément d’interface utilisateur suivant dans l’ordre de tabulation ; l’utilisation de **[!UICONTROL Maj+Tab]** rétablit la cible d’action sur l’élément d’interface utilisateur précédent. La traversée de la cible d’action suit l’emplacement de l’élément d’interface utilisateur naturel à l’écran et se déplace de gauche à droite, puis de haut en bas.

En fonction des paramètres du système d’exploitation et du navigateur Web, l’élément d’interface utilisateur qui a la cible d’action reçoit une indication de la cible d’action visuelle. Par exemple, l’indicateur visuel peut être une bordure mince rendue autour de l’élément d’interface utilisateur.

Il est possible de désactiver ou de personnaliser cette mise en surbrillance dans la page CSS de la visionneuse. Dans la table des matières de ce système d’aide, sous un nom de visionneuse spécifique (par exemple, Zoom de base ou Vidéo interactive), cliquez sur **Personnalisation de *nom de la visionneuse*** >** Mise en surbrillance de la mise au point **.

Les touches prises en charge par les éléments de l’interface utilisateur du lecteur individuel sont, dans la plupart des cas, évidentes et faciles à découvrir.

<table id="table_8C49100412224324BF1DBF7FDFDCCBF8"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>Action </p> </th> 
   <th colname="col2" class="entry"> <p>Keystroke </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>Activer les composants de bouton </p> </td> 
   <td colname="col2"> <p>Appuyez sur la touche Espace ou Entrée. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Zoom avant ou arrière </p> </td> 
   <td colname="col2"> <p> <span class="uicontrol"> +  </span> ou  <span class="uicontrol"> -  </span>, respectivement. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Réinitialisation du zoom </p> </td> 
   <td colname="col2"> <p>Touche Echap. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Panoramique </p> </td> 
   <td colname="col2"> <p>Touche fléchée vers le haut, le bas, la gauche ou la droite. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Rotation d’une image à 360 degrés </p> </td> 
   <td colname="col2"> <p>Utilisez les touches fléchées lorsque l’image est à l’état de réinitialisation. </p> <p>Utilisez la touche fléchée Haut ou Bas lorsque vous utilisez des visionneuses à 360° multidimensionnelles. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Sélection de l’échantillon de produit </p> </td> 
   <td colname="col2"> <p>Touche flèche vers le haut, le bas, la gauche ou la droite ; Clé d’accueil ou de fin. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Activation d’échantillon de produit </p> </td> 
   <td colname="col2"> <p>Appuyez sur la touche Espace ou Entrée. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Vidéo et vidéo interactive, rembobinage progressif </p> </td> 
   <td colname="col2"> <p>Touche flèche vers la gauche ou vers le haut. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Vidéo et vidéo interactive, avance rapide </p> </td> 
   <td colname="col2"> <p>Touche fléchée droite ou descendante. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Vidéo et vidéo interactive, accédez au début ou à la fin </p> </td> 
   <td colname="col2"> <p>Clé d’accueil ou de fin, respectivement. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Vidéo et vidéo interactive, contrôler le niveau de volume lorsque la mise au point est effectuée sur le curseur </p> </td> 
   <td colname="col2"> <p>Touche flèche vers le haut, le bas, la gauche ou la droite ; Clé d’accueil ou de fin. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Vidéo et vidéo interactive, volume mutable </p> </td> 
   <td colname="col2"> <p>Touches fléchées, Origine et Fin pour contrôler le niveau de volume lorsque la mise au point est effectuée sur la partie de réglette. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Vidéo : lorsque la boîte de dialogue modale est affichée, la traversée de la cible d’action devient limitée aux commandes de boîte de dialogue uniquement. </p> </td> 
   <td colname="col2"> <p>Touche Echap pour fermer la boîte de dialogue. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Carrousel, modifier l’image de la bannière dans la vue principale </p> </td> 
   <td colname="col2"> <p>Touche fléchée gauche ou droite. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Carrousel, sélection des zones réactives et activation des zones réactives </p> </td> 
   <td colname="col2"> <p>Sélection de zones réactives : touche fléchée vers le haut, le bas, la gauche ou la droite </p> <p>Activation de zone réactive : Appuyez sur la touche Espace ou Entrée. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Catalogue électronique, modifier l’image de la page dans la vue principale </p> </td> 
   <td colname="col2"> <p> Touches fléchées gauche ou droite. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Catalogue électronique, sélection de miniatures </p> </td> 
   <td colname="col2"> <p>Touches fléchées ; Clé d’accueil et de fin. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>activation de catalogue électronique, échantillon </p> </td> 
   <td colname="col2"> <p>Appuyez sur la touche Espace ou Entrée. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Catalogue électronique, sélection de zones réactives </p> </td> 
   <td colname="col2"> <p>Touches fléchées. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Catalogue électronique, activation </p> </td> 
   <td colname="col2"> <p>Appuyez sur la touche Espace ou sur les touches Entrée. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Catalogue électronique, activation des composants déroulants </p> </td> 
   <td colname="col2"> <p> Touche fléchée vers le bas ; Espace ou touche Entrée. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Catalogue électronique, lorsque la cible d’action se trouve dans le panneau déroulant </p> </td> 
   <td colname="col2"> <p>Utilisez les touches fléchées pour sélectionner un élément spécifique du panneau avant de l’activer. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Lorsqu’une boîte de dialogue modale s’affiche, la traversée de la cible d’action devient limitée aux commandes de boîte de dialogue uniquement. </p> </td> 
   <td colname="col2"> <p>Touche Echap pour fermer la boîte de dialogue. </p> </td> 
  </tr> 
 </tbody> 
</table>
