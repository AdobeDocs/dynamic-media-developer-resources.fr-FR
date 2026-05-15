---
title: Accessibilité clavier et navigation
description: Toutes les fonctionnalités exposées dans les interfaces Zoom de base, Catalogue électronique, Recherche catalogue électronique, Fenêtre déroulante, Zoom intégré, Médias mixtes, Spin, Vidéo, Zoom, Dimensionnel (3D), Carrousel, Image interactive, Vidéo interactive et Visionneuse Video360 sont accessibles à l’aide du clavier.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API
role: Developer,User
exl-id: 0bdf172a-0bde-42d2-900f-f207538fe588
TQID: 'https://experienceleague.adobe.com/Yo1xl9U8Ld3nzbeHm6pQxAncRKQIXEWimijQM4FjLtc'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
topic_v2: id: cc72dcf1-72e1-48cc-b434-e7c27d62d67c
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 588
ht-degree: 0%

---

# Accessibilité clavier et navigation{#keyboard-accessibility-and-navigation}

Toutes les fonctionnalités exposées dans les interfaces Zoom de base, Catalogue électronique, Recherche catalogue électronique, Fenêtre déroulante, Zoom intégré, Médias mixtes, Spin, Vidéo, Zoom, Carrousel, Dimensionnel (3D), Image interactive, Vidéo interactive et Visionneuse Video360 sont accessibles à l’aide du clavier.

<!-- Updated June 1, 2020 from https://wiki.corp.adobe.com/pages/viewpage.action?spaceKey=scene7qa&title=s7Viewers%2C+S7SDK%2C+S7OnDemand+Release+Notes - Contact is Sasha -->

## Accessibilité clavier et navigation {#topic-f5650e9493404e55a3627c8d1366b861}

Toutes les fonctionnalités exposées dans les interfaces Zoom de base, Catalogue électronique, Recherche catalogue électronique, Fenêtre déroulante, Zoom intégré, Médias mixtes, Spin, Vidéo, Zoom, Carrousel, Dimensionnel (3D), Image interactive, Vidéo interactive et Visionneuse Video360 sont accessibles à l’aide du clavier.

Un utilisateur final peut naviguer entre les éléments de l’interface utilisateur de la visionneuse à l’aide des touches **[!UICONTROL Tab]** et **[!UICONTROL Maj+Tab]**. L’utilisation de **[!UICONTROL Tab]** fait passer le focus de saisie à l’élément d’interface utilisateur suivant dans l’ordre de tabulation ; l’utilisation de **[!UICONTROL Maj+Tab]** ramène le focus de saisie à l’élément d’interface utilisateur précédent. Le parcours de sélection suit l’emplacement naturel de l’élément d’interface utilisateur à l’écran et se déplace de gauche à droite, puis de haut en bas.

Selon le système d’exploitation et les paramètres du navigateur web, l’élément d’interface utilisateur avec le focus reçoit une indication de focus visuelle. Par exemple, l’indicateur visuel peut être une bordure fine affichée autour de l’élément d’interface utilisateur.

Il est possible de désactiver ou de personnaliser cette mise en surbrillance dans le CSS de la visionneuse. Dans la table des matières de ce système d’aide, sous un nom de visionneuse spécifique (par exemple, Zoom de base ou Vidéo interactive), cliquez sur **Personnalisation *nom de la visionneuse*** >** Mettre en surbrillance **.

Les touches prises en charge par les éléments individuels de l’interface utilisateur de la visionneuse sont, dans la plupart des cas, évidentes et faciles à découvrir.

<table id="table_8C49100412224324BF1DBF7FDFDCCBF8"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>Action </p> </th> 
   <th colname="col2" class="entry"> <p>Touche </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>Activer les composants de bouton </p> </td> 
   <td colname="col2"> <p>Espace ou touche Entrée. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Zoom avant ou arrière </p> </td> 
   <td colname="col2"> <p> <span class="uicontrol"> + </span> ou <span class="uicontrol"> - </span>, respectivement. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Réinitialisation du Zoom </p> </td> 
   <td colname="col2"> <p>Touche Échap. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Panoramique </p> </td> 
   <td colname="col2"> <p>Touche fléchée haut, bas, gauche ou droite. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Rotation d’une image à 360 degrés </p> </td> 
   <td colname="col2"> <p>Utilisez les touches fléchées lorsque l’image est à l’état réinitialisé. </p> <p>Utilisez les touches fléchées vers le haut ou vers le bas lorsque vous utilisez des visionneuses à 360° multidimensionnelles. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Sélection de l’échantillon de produit </p> </td> 
   <td colname="col2"> <p>Touche fléchée vers le haut, le bas, à gauche ou à droite ; touche Début ou Fin. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Activation de l’échantillon de produit </p> </td> 
   <td colname="col2"> <p>Espace ou touche Entrée. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Vidéo et vidéo interactive, retour progressif </p> </td> 
   <td colname="col2"> <p>Touche fléchée vers la gauche ou vers le haut. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Vidéo et vidéo interactive, avance rapide </p> </td> 
   <td colname="col2"> <p>Touche fléchée droite ou vers le bas. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Vidéo et vidéo interactive, aller au début ou à la fin </p> </td> 
   <td colname="col2"> <p>Touche Début ou Fin, respectivement. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Vidéo et vidéo interactive, contrôlez le niveau de volume lorsque le focus est sur le curseur. </p> </td> 
   <td colname="col2"> <p>Touche fléchée vers le haut, le bas, à gauche ou à droite ; touche Début ou Fin. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Vidéo et vidéo interactive, volume mutable </p> </td> 
   <td colname="col2"> <p>Touches fléchées, Début et Fin pour contrôler le niveau de volume lorsque le focus se trouve sur sa partie curseur. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Vidéo : lorsque la boîte de dialogue modale s’affiche, la traversée de focus se limite uniquement aux commandes de boîte de dialogue. </p> </td> 
   <td colname="col2"> <p>Appuyez sur Échap pour fermer la boîte de dialogue. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Carrousel, modifier l’image de la bannière dans la vue principale </p> </td> 
   <td colname="col2"> <p>Touche fléchée gauche ou droite. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Carrousel, sélection de zones réactives et activation de zones réactives </p> </td> 
   <td colname="col2"> <p>Sélection de zone réactive : touche fléchée vers le haut, le bas, à gauche ou à droite </p> <p>Activation de la zone réactive : espace ou touche Entrée. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Catalogue électronique, modifier l’image de la page dans la vue principale </p> </td> 
   <td colname="col2"> <p> Touches fléchées gauche ou droite. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Catalogue électronique, sélection de miniatures </p> </td> 
   <td colname="col2"> <p>Touches fléchées ; Touches Début et Fin. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Catalogue électronique, activation de l’échantillon </p> </td> 
   <td colname="col2"> <p>Espace ou touche Entrée. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Catalogue électronique, sélection de zones réactives </p> </td> 
   <td colname="col2"> <p>Touches fléchées. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Catalogue électronique, activation </p> </td> 
   <td colname="col2"> <p>Touches Espace ou Entrée. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Catalogue électronique, activation des composants déroulants </p> </td> 
   <td colname="col2"> <p> Touche fléchée vers le bas ; touche Espace ou Entrée. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Catalogue électronique, lorsque le focus se trouve dans le panneau déroulant </p> </td> 
   <td colname="col2"> <p>Utilisez les touches fléchées pour sélectionner un élément spécifique dans le panneau avant de l’activer. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Dans eCatalog, lorsqu’une boîte de dialogue modale s’affiche, la traversée de focus se limite uniquement aux contrôles de boîte de dialogue. </p> </td> 
   <td colname="col2"> <p>Appuyez sur Échap pour fermer la boîte de dialogue. </p> </td> 
  </tr> 
 </tbody> 
</table>
