---
title: Accessibilité clavier et navigation
description: Toutes les fonctions exposées dans l’interface de visionneuse Zoom de base, Catalogue électronique, Search catalogue électronique, Fenêtre déroulante, Zoom intégré, Supports variés, Rotation, Vidéo, Zoom, Dimensionnel (3D), Carrousel, Image interactive, Vidéo interactive et Video360 sont accessibles au clavier.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API
role: Developer,User
exl-id: 0bdf172a-0bde-42d2-900f-f207538fe588
source-git-commit: 11acb9151d3ea247eecde3cfbbd295a95c10829c
workflow-type: tm+mt
source-wordcount: '578'
ht-degree: 0%

---

# Accessibilité clavier et navigation{#keyboard-accessibility-and-navigation}

Toutes les fonctions exposées dans l’interface de visionneuse Zoom de base, Catalogue électronique, Search catalogue électronique, Fenêtre déroulante, Zoom intégré, Supports variés, Rotation, Vidéo, Zoom, Carrousel, Dimensionnel (3D), Image interactive, Vidéo interactive et Video360 sont accessibles à l’aide du clavier.

<!-- Updated June 1, 2020 from https://wiki.corp.adobe.com/pages/viewpage.action?spaceKey=scene7qa&title=s7Viewers%2C+S7SDK%2C+S7OnDemand+Release+Notes - Contact is Sasha -->

## Accessibilité clavier et navigation {#topic-f5650e9493404e55a3627c8d1366b861}

Toutes les fonctions exposées dans l’interface de visionneuse Zoom de base, Catalogue électronique, Search catalogue électronique, Fenêtre déroulante, Zoom intégré, Supports variés, Rotation, Vidéo, Zoom, Carrousel, Dimensionnel (3D), Image interactive, Vidéo interactive et Video360 sont accessibles à l’aide du clavier.

Un utilisateur final peut naviguer entre les éléments de l’interface utilisateur de la visionneuse à l’aide des **[!UICONTROL touches de tabulation]** et **[!UICONTROL Maj + tabulation]** . L’utilisation **[!UICONTROL de l’option Tab]** fait passer le focus d’entrée à l’élément d’interface utilisateur suivant dans l’ordre de tabulation ; l’utilisation **[!UICONTROL de Maj+Tab]** ramène le focus d’entrée à l’élément d’interface utilisateur précédent. La traversée de focus suit l’emplacement naturel de l’élément de l’interface utilisateur à l’écran et se déplace de gauche à droite, puis de haut en bas.

Selon les paramètres du système d’exploitation et du navigateur Web, l’élément d’interface utilisateur qui a le focus d’entrée reçoit une indication de focus visuel. Par exemple, l’indicateur visuel peut être une bordure mince rendue autour de l’élément d’interface utilisateur.

Il est possible de désactiver ou de personnaliser cette mise au point dans le fichier CSS de la visionneuse. Dans la table des matières de ce système d’aide, sous un nom de visionneuse spécifique (par exemple, zoom de base ou vidéo interactive), cliquez sur **Personnalisation *du nom de la visionneuse*** >**&#x200B; mise en surbrillance &#x200B;** de focus.

Les frappes prises en charge par des éléments individuels de l’interface utilisateur de la visionneuse sont, dans la plupart des cas, évidentes et faciles à découvrir.

<table id="table_8C49100412224324BF1DBF7FDFDCCBF8"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>Action </p> </th> 
   <th colname="col2" class="entry"> <p>Frappe </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>Activer les composants de bouton </p> </td> 
   <td colname="col2"> <p>Espace ou touche Entrée. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Zoom avant ou arrière </p> </td> 
   <td colname="col2"> <p> <span class="uicontrol"></span>+ ou <span class="uicontrol"> - </span>, respectivement. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Réinitialisation du zoom </p> </td> 
   <td colname="col2"> <p>Clé Échap. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Pan </p> </td> 
   <td colname="col2"> <p>Touche fléchée Haut, Bas, Gauche ou Droite. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Rotation d’une image à 360 degrés </p> </td> 
   <td colname="col2"> <p>Utilisez les touches fléchées lorsque l’image est dans un état de réinitialisation. </p> <p>Utilisez la touche fléchée Haut ou Bas lorsque vous travaillez avec des visionneuses à 360° multidimensionnelles. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Sélection de la nuance de produits </p> </td> 
   <td colname="col2"> <p>Touche fléchée Haut, Bas, Gauche ou Droite ; Touche Accueil ou Fin. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Activation de la nuance de produit </p> </td> 
   <td colname="col2"> <p>Espace ou touche Entrée. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Vidéo et vidéo interactive, rembobinage progressif </p> </td> 
   <td colname="col2"> <p>Touche fléchée Haut ou gauche. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Vidéo et vidéo interactive, avance rapide </p> </td> 
   <td colname="col2"> <p>Touche fléchée droite ou flèche bas. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Vidéo et vidéo interactive, aller au début ou à la fin </p> </td> 
   <td colname="col2"> <p>Touche d’accueil ou de fin, respectivement. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Vidéo et vidéo interactive, contrôler le niveau de volume lorsque la mise au point est sur le curseur </p> </td> 
   <td colname="col2"> <p>Touche fléchée Haut, Bas, Gauche ou Droite ; Touche Accueil ou Fin. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Vidéo et vidéo interactive, volume mutable </p> </td> 
   <td colname="col2"> <p>Touches fléchées, d’accueil et de fin pour contrôler le niveau de volume lorsque la mise au point est sur sa partie curseur. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Vidéo, lorsque la boîte de dialogue modale est affichée, la traversée de la mise au point devient limitée aux contrôles de boîte de dialogue uniquement. </p> </td> 
   <td colname="col2"> <p>Touche Échap pour fermer la boîte de dialogue. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Carrousel, changer l’image de la bannière dans la vue principale </p> </td> 
   <td colname="col2"> <p>Touche fléchée droite ou gauche. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Carrousel, sélection de zone réactive et activation de zone réactive </p> </td> 
   <td colname="col2"> <p>Sélection de la zone réactive : touche fléchée Haut, Bas, Gauche ou Droite </p> <p>Activation de la zone réactive : touche Espace ou Entrée. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Catalogue électronique, modifier l’image de la page dans la vue principale </p> </td> 
   <td colname="col2"> <p> Touches fléchées droite ou gauche. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Catalogue électronique, sélection de miniatures </p> </td> 
   <td colname="col2"> <p>Flèches; Touche d’accueil et de fin. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>catalogue électronique, activation de l’échantillon </p> </td> 
   <td colname="col2"> <p>Espace ou touche Entrée. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>catalogue électronique, sélection des zones réactives </p> </td> 
   <td colname="col2"> <p>Flèches. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>eCatalog, activation </p> </td> 
   <td colname="col2"> <p>Touche Espace ou Entrée. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>catalogue électronique, activation des composants déroulants </p> </td> 
   <td colname="col2"> <p> Touche fléchée vers le bas ; Espace, ou touche Entrée. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Catalogue électronique, lorsque le focus est sur le panneau Drop-Drown </p> </td> 
   <td colname="col2"> <p>Utilisez les touches fléchées pour sélectionner un élément spécifique dans le panneau avant de l’activer. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Catalogue électronique, lorsqu’une boîte de dialogue modale est affichée, la traversée de focus devient limitée aux contrôles de boîte de dialogue uniquement. </p> </td> 
   <td colname="col2"> <p>Touche Échap pour fermer la boîte de dialogue. </p> </td> 
  </tr> 
 </tbody> 
</table>
