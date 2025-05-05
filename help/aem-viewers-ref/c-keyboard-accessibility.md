---
title: Accessibilité du clavier et navigation
description: Toutes les fonctionnalités exposées dans l’interface de la visionneuse à 360°, Zoom de base, Catalogue électronique, Recherche catalogue électronique, Fenêtre déroulante, Zoom intégré, Média mixte, Rotation, Vidéo, Zoom, Dimensionnel (3D), Carrousel, Image interactive, Vidéo interactive et Vidéo360 sont accessibles au clavier.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API
role: Developer,User
exl-id: 0bdf172a-0bde-42d2-900f-f207538fe588
source-git-commit: 11acb9151d3ea247eecde3cfbbd295a95c10829c
workflow-type: tm+mt
source-wordcount: '578'
ht-degree: 0%

---

# Accessibilité du clavier et navigation{#keyboard-accessibility-and-navigation}

Toutes les fonctionnalités exposées dans l’interface de la visionneuse à 360°, Zoom de base, Catalogue électronique, Recherche catalogue électronique, Fenêtre déroulante, Zoom intégré, Média mixte, Rotation, Vidéo, Zoom, Carrousel, Dimensionnel (3D), Image interactive, Vidéo interactive et Vidéo 360 sont accessibles au clavier.

<!-- Updated June 1, 2020 from https://wiki.corp.adobe.com/pages/viewpage.action?spaceKey=scene7qa&title=s7Viewers%2C+S7SDK%2C+S7OnDemand+Release+Notes - Contact is Sasha -->

## Accessibilité du clavier et navigation {#topic-f5650e9493404e55a3627c8d1366b861}

Toutes les fonctionnalités exposées dans l’interface de la visionneuse à 360°, Zoom de base, Catalogue électronique, Recherche catalogue électronique, Fenêtre déroulante, Zoom intégré, Média mixte, Rotation, Vidéo, Zoom, Carrousel, Dimensionnel (3D), Image interactive, Vidéo interactive et Vidéo 360 sont accessibles au clavier.

Un utilisateur final peut naviguer entre les éléments de l’interface utilisateur de la visionneuse à l’aide des touches **[!UICONTROL Tab]** et **[!UICONTROL Maj+Tab]**. L’utilisation de **[!UICONTROL Tab]** permet d’activer la cible d’action sur l’élément d’interface utilisateur suivant dans l’ordre de tabulation ; l’utilisation de **[!UICONTROL Maj+Tab]** rétablit la cible d’action sur l’élément d’interface utilisateur précédent. La traversée de sélection suit l’emplacement de l’élément d’interface utilisateur naturel à l’écran et se déplace de gauche à droite, puis de haut en bas.

Selon les paramètres du système d’exploitation et du navigateur web, l’élément d’interface utilisateur qui a le focus d’entrée reçoit une indication visuelle de focus. Par exemple, l’indicateur visuel peut être une bordure mince générée autour de l’élément d’interface utilisateur.

Il est possible de désactiver ou de personnaliser cette mise en surbrillance dans le CSS de la visionneuse. Dans la table des matières de ce système d’aide, sous un nom de visionneuse spécifique (par exemple, Zoom de base ou Vidéo interactive), cliquez sur **Personnaliser *nom de la visionneuse*** >**&#x200B; Mise en évidence du focus &#x200B;**.

Les touches prises en charge par les éléments de l’interface utilisateur de la visionneuse individuelle sont, dans la plupart des cas, évidentes et faciles à découvrir.

<table id="table_8C49100412224324BF1DBF7FDFDCCBF8"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>Action </p> </th> 
   <th colname="col2" class="entry"> <p>Keystroke </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>Activation des composants de bouton </p> </td> 
   <td colname="col2"> <p>Appuyez ou appuyez sur la touche Entrée. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Zoom avant ou arrière </p> </td> 
   <td colname="col2"> <p> <span class="uicontrol"> + </span> ou <span class="uicontrol"> - </span>, respectivement. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Réinitialisation du zoom </p> </td> 
   <td colname="col2"> <p>Échap. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Panoramique </p> </td> 
   <td colname="col2"> <p>Touche fléchée Haut, Bas, Gauche ou Droite. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Rotation d’une image à 360 degrés </p> </td> 
   <td colname="col2"> <p>Utilisez les touches fléchées lorsque l’image est à l’état réinitialisé. </p> <p>Utilisez la touche fléchée Haut ou Bas lorsque vous utilisez des visionneuses à 360° multidimensionnelles. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Sélection de l’échantillon de produit </p> </td> 
   <td colname="col2"> <p>Touche fléchée Haut, Bas, Gauche ou Droite ; touche Accueil ou Fin. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Activation de l’échantillon de produit </p> </td> 
   <td colname="col2"> <p>Appuyez ou appuyez sur la touche Entrée. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Vidéo et vidéo interactive, retour progressif </p> </td> 
   <td colname="col2"> <p>Touche fléchée gauche ou haut. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Vidéo et vidéo interactive, avance rapide </p> </td> 
   <td colname="col2"> <p>Flèche vers la droite ou vers le bas. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Vidéo et vidéo interactive, accédez au début ou à la fin </p> </td> 
   <td colname="col2"> <p>Clé d’accueil ou de fin, respectivement. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Vidéo et vidéo interactive, contrôle le niveau du volume lorsque la sélection est effectuée sur le curseur </p> </td> 
   <td colname="col2"> <p>Touche fléchée Haut, Bas, Gauche ou Droite ; touche Accueil ou Fin. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Vidéo et vidéo interactive, volume modifiable </p> </td> 
   <td colname="col2"> <p>Touches fléchées, Accueil et Fin pour contrôler le niveau de volume lorsque le focus est sur sa partie inférieure. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Vidéo : lorsque la boîte de dialogue modale s’affiche, la traversée de la sélection se limite uniquement aux commandes de boîte de dialogue. </p> </td> 
   <td colname="col2"> <p>Touche Échap pour fermer la boîte de dialogue. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Carrousel, modification de l’image de bannière dans la vue principale </p> </td> 
   <td colname="col2"> <p>Flèche vers la gauche ou la droite. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Activation du carrousel, de la sélection de zones réactives et de la zone réactive </p> </td> 
   <td colname="col2"> <p>Sélection de zones réactives : touche fléchée haut, bas, gauche ou droite </p> <p>Activation des zones réactives : touche Space ou Enter . </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Catalogue électronique, modifiez l’image de la page dans la vue principale. </p> </td> 
   <td colname="col2"> <p> Touches fléchées gauche ou droite. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Catalogue électronique, sélection de miniatures </p> </td> 
   <td colname="col2"> <p>Touches fléchées, touches Accueil et Fin. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Catalogue électronique, activation d’échantillon </p> </td> 
   <td colname="col2"> <p>Appuyez ou appuyez sur la touche Entrée. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Catalogue électronique, sélection des zones réactives </p> </td> 
   <td colname="col2"> <p>Touches fléchées. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Catalogue électronique, activation </p> </td> 
   <td colname="col2"> <p>Appuyez ou appuyez sur les touches Entrée. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Catalogue électronique, activation des composants déroulants </p> </td> 
   <td colname="col2"> <p> Touche Flèche vers le bas, espace ou touche Entrée. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Catalogue électronique, lorsque la cible d’action se trouve dans le panneau déroulant </p> </td> 
   <td colname="col2"> <p>Utilisez les touches fléchées pour sélectionner un élément spécifique du panneau avant de l’activer. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Dans le catalogue électronique, lorsqu’une boîte de dialogue modale s’affiche, la traversée de la cible d’action se limite uniquement aux commandes de boîte de dialogue. </p> </td> 
   <td colname="col2"> <p>Touche Échap pour fermer la boîte de dialogue. </p> </td> 
  </tr> 
 </tbody> 
</table>
