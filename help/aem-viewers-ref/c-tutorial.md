---
description: Le kit de développement de visionneuse fournit un ensemble de composants basés sur JavaScript pour le développement de lecteurs personnalisés. Les lecteurs de contenu sont des applications Web qui permettent à l’Adobe Dynamic Media d’incorporer du contenu multimédia enrichi dans des pages Web.
solution: Experience Manager
title: Didacticiel sur le SDK du lecteur de contenu
feature: Dynamic Media Classic,Viewers,SDK/API
role: Developer,Business Practitioner
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '974'
ht-degree: 0%

---


# Didacticiel SDK du lecteur{#viewer-sdk-tutorial}

Le kit de développement de visionneuse fournit un ensemble de composants basés sur JavaScript pour le développement de lecteurs personnalisés. Les lecteurs de contenu sont des applications Web qui permettent à l’Adobe Dynamic Media d’incorporer du contenu multimédia enrichi dans des pages Web.

Par exemple, le SDK fournit un zoom et un panoramique interactifs. Il permet également une vue à 360° et la lecture vidéo des fichiers qui ont été téléchargés vers Adobe Dynamic Media via l’application principale Dynamic Media Classic.

Bien que les composants reposent sur la fonctionnalité HTML5, ils sont conçus pour fonctionner sur les périphériques Android et Apple iOS, ainsi que sur les ordinateurs de bureau, y compris Internet Explorer et les versions ultérieures. Ce type d’expérience signifie que vous pouvez fournir un flux de travail unique pour toutes les plates-formes prises en charge.

Le SDK est constitué de composants d’interface qui constituent le contenu de la visionneuse. Vous pouvez mettre en forme ces composants par le biais de CSS et de composants non-UI qui ont un rôle de prise en charge, tel que l’extraction et l’analyse des définitions ou le suivi. Tous les comportements de composant sont personnalisables à l’aide de modificateurs que vous pouvez spécifier de différentes manières, par exemple sous la forme de paires `name=value` dans l’URL.

Ce didacticiel comprend les tâches suivantes pour vous aider à créer une visionneuse de zoom de base :

* [Téléchargement du dernier SDK de visionneuse à partir de Adobe Developer Connection](c-tutorial.md#section-84dc74c9d8e24a2380b6cf8fc28d7127)
* [Chargement du SDK du lecteur de contenu](c-tutorial.md#section-98596c276faf4cf79ccf558a9f4432c6)
* [Ajouter le style à votre lecteur](c-tutorial.md#section-3783125360a1425eae5a5a334867cc32)
* [Inclusion de l’affichage Conteneur et zoom](c-tutorial.md#section-1a01730663154a508b88cc40c6f35539)
* [Ajouter les composants MediaSet et Swatches à votre visionneuse](c-tutorial.md#section-02b8c21dd842400e83eae2a48ec265b7)
* [Ajouter des boutons à votre lecteur](c-tutorial.md#section-1fc334fa0d2b47eb9cdad461725c07be)
* [Configuration verticale des échantillons](c-tutorial.md#section-91a8829d5b5a4d45a35b7faeb097fcc9)

## Téléchargez le dernier SDK de visionneuse à partir de Adobe Developer Connection {#section-84dc74c9d8e24a2380b6cf8fc28d7127}

1. Téléchargez le dernier SDK de visionneuse à partir de Adobe Developer Connection [ici](https://marketing.adobe.com/developer/devcenter/scene7/show).

   >[!NOTE]
   >
   >Vous pouvez suivre ce didacticiel sans avoir à télécharger le package du SDK de visionneuse, car le SDK est en fait chargé à distance. Cependant, le package Viewer contient d’autres exemples et un guide de référence d’API que vous trouverez utile lors de la création de vos propres visionneuses.

## Charger le kit de développement de visionneuse {#section-98596c276faf4cf79ccf558a9f4432c6}

1. Début en configurant une nouvelle page pour développer la visionneuse de zoom de base que vous allez créer.

   Prenons le code d’amorçage (ou chargeur) pour configurer une application SDK vide. Ouvrez l’éditeur de texte favori et collez-y les balises HTML suivantes :

   ```
   <!DOCTYPE html> 
   <html> 
       <head> 
           <meta http-equiv="Content-Type" content="text/html; charset=utf-8" /> 
           <meta name="viewport" content="user-scalable=no, height=device-height, width=device-width, initial-scale=1.0, maximum-scale=1.0"/> 
   
           <!-- Hiding the Safari on iPhone OS UI components --> 
           <meta name="apple-mobile-web-app-capable" content="yes"/> 
           <meta name="apple-mobile-web-app-status-bar-style" content="black"/> 
           <meta name="apple-touch-fullscreen" content="no"/> 
   
           <title>Custom Viewer</title> 
   
           <!-- 
               Include Utils.js before you use any of the SDK components. This file  
               contains SDK utilities and global functions that are used to initialize the viewer and load viewer  
               components. The path to the Utils.js determines which version of the SDK that the viewer uses. You  
               can use a relative path if the viewer is deployed on one of the Adobe Dynamic Media servers and it is served  
               from the same domain. Otherwise, specify a full path to one of Adobe Dynamic Media servers that have the SDK  
               installed.  
           --> 
           <script language="javascript" type="text/javascript"      
                   src="http://s7d1.scene7.com/s7sdk/2.8/js/s7sdk/utils/Utils.js"></script> 
   
       </head> 
       <body> 
           <script language="javascript" type="text/javascript"> 
           </script>  
       </body> 
   </html>
   ```

   Ajoutez le code JavaScript suivant dans la balise `script` pour initialiser `ParameterManager`. Cela vous permet de vous préparer à créer et à instancier des composants SDK dans la fonction `initViewer` :

   ```
   /* We create a self-running anonymous function to encapsulate variable scope. Placing code inside such 
      a function is optional, but this prevents variables from polluting the global object.  */ 
   (function () { 
   
       // Initialize the SDK   
       s7sdk.Util.init(); 
   
       /* Create an instance of the ParameterManager component to collect components' configuration 
          that can come from a viewer preset, URL, or the HTML page itself. The ParameterManager  
          component also sends a notification s7sdk.Event.SDK_READY when all needed files are loaded 
          and the configuration parameters are processed. The other components should never be initialized 
          outside this handler. After defining the handler for the s7sdk.Event.SDK_READY event, it 
          is safe to initiate configuration initialization by calling ParameterManager.init(). */ 
       var params = new s7sdk.ParameterManager(); 
   
       /* Event handler for s7sdk.Event.SDK_READY dispatched by ParameterManager to initialize various components of  
          this viewer. */ 
       function initViewer() { 
   
       }  
   
       /* Add event handler for the s7sdk.Event.SDK_READY event dispatched by the ParameterManager when all modifiers 
          are processed and it is safe to initialize the viewer. */ 
       params.addEventListener(s7sdk.Event.SDK_READY, initViewer, false); 
   
       /* Initiate configuration initialization of ParameterManager. */ 
       params.init(); 
   
   }());
   ```

1. Enregistrez le fichier en tant que modèle vide. Vous pouvez utiliser n’importe quel nom de fichier.

   Vous utiliserez ce fichier de modèle vide comme référence lors de la création de nouvelles visionneuses à l’avenir. Ce modèle fonctionne localement et lorsqu’il est diffusé à partir d’un serveur Web.

Vous allez maintenant ajouter un style à votre lecteur de contenu.

## Ajouter le style à votre visionneuse {#section-3783125360a1425eae5a5a334867cc32}

1. Pour cette visionneuse de pages complètes que vous créez, vous pouvez ajouter quelques styles de base.

   Ajoutez le bloc `style` suivant au bas du `head` :

   ```
   <style> 
       html, body { 
           width: 100%; 
           height: 100%; 
       } 
       body { 
           /* Remove any padding and margin around the edges of the browser window */ 
           padding: 0; 
           margin: 0; 
   
           /* We set overflow to hidden so that scroll bars do not flicker when resizing the window */ 
           overflow: hidden; 
       } 
   </style>
   ```

Vous allez maintenant inclure les composants `Container` et `ZoomView`.

## Inclusion du Conteneur et de la vue Zoom {#section-1a01730663154a508b88cc40c6f35539}

1. Créez une visionneuse réelle en incluant les composants `Container` et `ZoomView`.

   Insérez les instructions `include` suivantes au bas de l’élément `<head>`, après le chargement du script [!DNL Utils.js] :

   ```
   <!-- 
       Add an "include" statement with a related module for each component that is needed for that particular  
       viewer. Check API documentation to see a complete list of components and their modules. 
   --> 
   <script language="javascript" type="text/javascript"> 
       s7sdk.Util.lib.include('s7sdk.common.Container');  
       s7sdk.Util.lib.include('s7sdk.image.ZoomView');  
   </script>
   ```

1. Créez maintenant des variables pour référencer les différents composants du SDK.

   Ajoutez les variables suivantes en haut de la fonction anonyme principale, juste au-dessus de `s7sdk.Util.init()` :

   ```
   var container, zoomView;
   ```

1. Insérez les éléments suivants dans la fonction `initViewer` pour définir certains modificateurs et instancier les composants respectifs :

   ```
   /* Modifiers can be added directly to ParameterManager instance */ 
   params.push("serverurl", "http://s7d1.scene7.com/is/image"); 
   params.push("asset", "Scene7SharedAssets/ImageSet-Views-Sample"); 
   
   /* Create a viewer container as a parent component for other user interface components that  
      are part of the viewer application and associate event handlers for resize and  
      full screen notification. The advantage of using Container as the parent is the  
      component's ability to resize and bring itself and its children to full screen. */ 
   container = new s7sdk.common.Container(null, params, "s7container"); 
   container.addEventListener(s7sdk.event.ResizeEvent.COMPONENT_RESIZE, containerResize, false); 
   
   /* Create ZoomView component */ 
   zoomView = new s7sdk.image.ZoomView("s7container", params, "myZoomView");  
   
   /* We call this to ensure all SDK components are scaled to initial conditions when viewer loads */ 
   resizeViewer(container.getWidth(), container.getHeight());
   ```

1. Pour que le code ci-dessus s&#39;exécute correctement, ajoutez un gestionnaire de événement `containerResize` et une fonction d&#39;assistance :

   ```
   /* Event handler for s7sdk.event.ResizeEvent.COMPONENT_RESIZE events dispatched by Container to resize 
      various view components included in this viewer. */ 
   function containerResize(event) { 
       resizeViewer(event.s7event.w, event.s7event.h); 
   } 
   
   /* Resize viewer components */ 
   function resizeViewer(width, height) { 
       zoomView.resize(width, height); 
   }
   ```

1. Prévisualisation de la page afin que vous puissiez voir ce que vous avez créé. La page se présente comme suit :

   ![](assets/viewer-1.jpg)

Vous allez maintenant ajouter les composants `MediaSet` et `Swatches` à votre visionneuse.

## Ajouter les composants MediaSet et Swatches à votre visionneuse {#section-02b8c21dd842400e83eae2a48ec265b7}

1. Pour permettre aux utilisateurs de sélectionner des images à partir d’une visionneuse, vous pouvez ajouter les composants `MediaSet` et `Swatches`.

   Ajoutez le SDK suivant :

   ```
   s7sdk.Util.lib.include('s7sdk.set.MediaSet'); 
   s7sdk.Util.lib.include('s7sdk.set.Swatches');
   ```

1. Mettez à jour la liste de variables avec ce qui suit :

   ```
   var mediaSet, container, zoomView, swatches;
   ```

1. Instanciez les composants `MediaSet` et `Swatches` dans la fonction `initViewer`.

   Veillez à instancier l&#39;instance `Swatches` après les composants `ZoomView` et `Container`, sinon l&#39;ordre d&#39;empilement masque `Swatches` :

   ```
   // Create MediaSet to manage assets and add event listener to the NOTF_SET_PARSED event 
   mediaSet = new s7sdk.set.MediaSet(null, params, "mediaSet"); 
   
   // Add MediaSet event listener 
   mediaSet.addEventListener(s7sdk.event.AssetEvent.NOTF_SET_PARSED, onSetParsed, false); 
   
   /* create Swatches component and associate event handler for swatch selection notification */ 
   swatches = new s7sdk.set.Swatches("s7container", params, "mySwatches");   
   swatches.addEventListener(s7sdk.event.AssetEvent.SWATCH_SELECTED_EVENT, swatchSelected, false);
   ```

1. Ajoutez maintenant les fonctions de gestionnaire de événements suivantes :

   ```
   /* Event handler for the s7sdk.event.AssetEvent.NOTF_SET_PARSED event dispatched by MediaSet to 
      assign the asset to the Swatches when parsing is complete. */ 
   function onSetParsed(e) { 
   
       // set media set for Swatches to display  
       var mediasetDesc = e.s7event.asset;  
       swatches.setMediaSet(mediasetDesc); 
   
       // select the first swatch by default  
       swatches.selectSwatch(0, true);      
   } 
   
   /* Event handler for s7sdk.event.AssetEvent.SWATCH_SELECTED_EVENT events dispatched by Swatches to switch 
      the image in the ZoomView when a different swatch is selected. */ 
   function swatchSelected(event) {     
       zoomView.setItem(event.s7event.asset);  
   }
   ```

1. Positionnez les nuances au bas de la visionneuse en ajoutant le CSS suivant à l’élément `style` :

   ```
   /* Align swatches to bottom of viewer */ 
   .s7swatches { 
       bottom: 0; 
       left: 0; 
       right: 0; 
       height: 150px; 
   }
   ```

1. Prévisualisation votre lecteur.

   Notez que les nuances se trouvent dans le coin inférieur gauche du lecteur. Pour que les nuances puissent prendre toute la largeur de la visionneuse, ajoutez un appel pour redimensionner manuellement les nuances chaque fois que l’utilisateur redimensionne son navigateur. Ajoutez les éléments suivants à la fonction `resizeViewer` :

   ```
   swatches.resize(width, swatches.getHeight());
   ```

   Votre lecteur ressemble désormais à l’image suivante. Essayez de redimensionner la fenêtre du navigateur de la visionneuse et notez le comportement qui en résulte.

   ![](assets/viewer-2.jpg)

Vous allez maintenant ajouter des boutons de zoom avant, de zoom arrière et de réinitialisation du zoom à votre visionneuse.

## Ajouter des boutons à votre lecteur {#section-1fc334fa0d2b47eb9cdad461725c07be}

1. Actuellement, l’utilisateur ne peut effectuer un zoom qu’à l’aide de mouvements de clic ou de toucher. Par conséquent, ajoutez quelques boutons de commande de zoom de base à la visionneuse.

   Ajoutez les composants de bouton suivants :

   ```
   s7sdk.Util.lib.include('s7sdk.common.Button');
   ```

1. Mettez à jour la liste de variables avec ce qui suit :

   ```
   var mediaSet, container, zoomView, swatches, zoomInButton, zoomOutButton, zoomResetButton;
   ```

1. Instancier les boutons au bas de la fonction `initViewer`.

   N’oubliez pas que l’ordre est important, sauf si vous spécifiez `z-index` dans CSS :

   ```
   /* Create Zoom In, Zoom Out and Zoom Reset buttons */ 
   zoomInButton  = new s7sdk.common.ZoomInButton("s7container", params, "zoomInBtn"); 
   zoomOutButton = new s7sdk.common.ZoomOutButton("s7container", params, "zoomOutBtn"); 
   zoomResetButton = new s7sdk.common.ZoomResetButton("s7container", params, "zoomResetBtn"); 
   
   /* Add handlers for zoom in, zoom out and zoom reset buttons inline. */ 
   zoomInButton.addEventListener("click", function() { zoomView.zoomIn(); }); 
   zoomOutButton.addEventListener("click", function() { zoomView.zoomOut(); }); 
   zoomResetButton.addEventListener("click", function() { zoomView.zoomReset(); });
   ```

1. Désormais, définissez certains styles de base pour les boutons en ajoutant ce qui suit au bloc `style` situé en haut de votre fichier :

   ```
   /* define styles common to all button components and their sub-classes */ 
   .s7button { 
       position:absolute; 
       width: 28px; 
       height: 28px; 
       z-index:100; 
   } 
   
   /* position individual buttons*/ 
   .s7zoominbutton  { 
       top: 50px; 
       left: 50px; 
    } 
   .s7zoomoutbutton  { 
       top: 50px; 
       left: 80px; 
    } 
   .s7zoomresetbutton  { 
       top: 50px; 
       left: 110px; 
    }
   ```

1. Prévisualisation votre lecteur. Il ressemblera à ce qui suit :

   ![](assets/viewer-3.jpg)

   Vous allez maintenant configurer les nuances de sorte qu’elles soient alignées verticalement sur la droite.

## Configuration verticale des échantillons {#section-91a8829d5b5a4d45a35b7faeb097fcc9}

1. Vous pouvez configurer les modificateurs directement sur l&#39;instance `ParameterManager`.

   Ajoutez les éléments suivants en haut de la fonction `initViewer` pour configurer la mise en page du miniature `Swatches` en une seule ligne :

   ```
   params.push("Swatches.tmblayout", "1,0");
   ```

1. Mettez à jour l’appel de redimensionnement suivant dans `resizeViewer` :

   ```
   swatches.resize(swatches.getWidth(), height);
   ```

1. Modifiez la règle `s7swatches` suivante dans `ZoomViewer.css` :

   ```
   .s7swatches { 
       top:0 ; 
       bottom: 0; 
       right: 0; 
       width: 150px; 
   }
   ```

1. Prévisualisation votre lecteur. Il ressemblera à ce qui suit :

   ![](assets/viewer-4.jpg)

   La visionneuse de zoom de base est maintenant terminée.

   Ce didacticiel du lecteur de contenu décrit les fondamentaux du kit de développement de visionneuse Dynamic Media. Lorsque vous travaillez avec le SDK, vous pouvez utiliser les différents composants standard pour créer et mettre en forme facilement des expériences d’affichage riches pour vos audiences de cible.

