---
description: Le kit de développement de visionneuse fournit un ensemble de composants JavaScript pour le développement de lecteurs personnalisés. Les visionneuses sont des applications Web qui permettent d’incorporer du contenu multimédia enrichi fourni par Adobe Scene7 dans des pages Web.
seo-description: Le kit de développement de visionneuse fournit un ensemble de composants JavaScript pour le développement de lecteurs personnalisés. Les visionneuses sont des applications Web qui permettent d’incorporer du contenu multimédia enrichi fourni par Adobe Scene7 dans des pages Web.
seo-title: Didacticiel du kit SDK du lecteur de contenu
solution: Experience Manager
title: Didacticiel du kit SDK du lecteur de contenu
topic: Dynamic media
uuid: ea331f05-0c58-4e6b-b5a1-d9b8372d8e94
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# Didacticiel du kit SDK du lecteur de contenu{#viewer-sdk-tutorial}

Le kit de développement de visionneuse fournit un ensemble de composants JavaScript pour le développement de lecteurs personnalisés. Les visionneuses sont des applications Web qui permettent d’incorporer du contenu multimédia enrichi fourni par Adobe Scene7 dans des pages Web.

Par exemple, le kit SDK propose un zoom et un panoramique interactifs. Il permet également d’ et de lecture vidéo à 360° des fichiers téléchargés vers Adobe Scene7 via l’application principale SPS (Scene7 Publishing System).

Bien que les composants reposent sur la fonctionnalité HTML5, ils sont conçus pour fonctionner sur les périphériques Android et Apple iOS, ainsi que sur les ordinateurs de bureau, notamment Internet Explorer et versions ultérieures. Ce type d’expérience signifie que vous pouvez fournir un flux de travail unique pour toutes les plateformes prises en charge.

Le SDK est constitué de composants de l’interface qui constituent le contenu du lecteur de contenu. Vous pouvez mettre en forme ces composants par le biais de CSS et de composants non-UI qui ont un rôle de prise en charge, tel que l’extraction et l’analyse des définitions ou le suivi. Tous les comportements de composant sont personnalisables à l’aide de modificateurs que vous pouvez spécifier de différentes manières, par exemple sous forme de `name=value` paires dans l’URL.

Ce didacticiel comprend l’ordre suivant de  de pour vous aider à créer une visionneuse de zoom de base :

* [Téléchargez le dernier SDK du lecteur de contenu à partir d’Adobe Developer Connection](c-tutorial.md#section-84dc74c9d8e24a2380b6cf8fc28d7127)
* [Chargement du SDK du lecteur de contenu](c-tutorial.md#section-98596c276faf4cf79ccf558a9f4432c6)
* [Ajout d’un style à la visionneuse](c-tutorial.md#section-3783125360a1425eae5a5a334867cc32)
* [Inclusion des  de et ZoomView](c-tutorial.md#section-1a01730663154a508b88cc40c6f35539)
* [Ajout des composants MediaSet et Swatches à votre lecteur de contenu](c-tutorial.md#section-02b8c21dd842400e83eae2a48ec265b7)
* [Ajout de boutons à la visionneuse](c-tutorial.md#section-1fc334fa0d2b47eb9cdad461725c07be)
* [Configuration verticale des échantillons](c-tutorial.md#section-91a8829d5b5a4d45a35b7faeb097fcc9)

## Téléchargez le dernier SDK du lecteur de contenu à partir d’Adobe Developer Connection {#section-84dc74c9d8e24a2380b6cf8fc28d7127}

1. Téléchargez la dernière version du kit de développement de visionneuse depuis Adobe Developer Connection [ici](https://marketing.adobe.com/developer/devcenter/scene7/show).

   >[!NOTE]
   >
   >Vous pouvez suivre ce didacticiel sans avoir à télécharger le package du SDK de lecteur, car le SDK est en fait chargé à distance. Cependant, le package du lecteur de contenu contient des exemples supplémentaires et un guide de référence API que vous trouverez utile lors de la création de vos propres lecteurs.

## Chargement du SDK du lecteur de contenu {#section-98596c276faf4cf79ccf558a9f4432c6}

1. en configurant une nouvelle page pour développer la visionneuse de zoom de base que vous allez créer.

   Prenons le code d’amorçage (ou chargeur) pour configurer une application SDK vide. Ouvrez votre éditeur de texte préféré et collez-y le balisage HTML suivant :

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
               can use a relative path if the viewer is deployed on one of the Adobe Scene7 servers and it is served  
               from the same domain. Otherwise, specify a full path to one of Adobe Scene7 servers that have the SDK  
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

   Ajouter le code JavaScript suivant dans la `script` balise pour initialiser le `ParameterManager`. Cela vous permet de vous préparer à créer et à instancier des composants SDK dans la `initViewer` fonction :

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

   Vous utiliserez ce fichier de modèle vide comme référence lors de la création future de nouvelles visionneuses. Ce modèle fonctionne localement et lorsqu’il est diffusé à partir d’un serveur Web.

Vous allez maintenant ajouter un style à votre lecteur.

## Ajout d’un style à la visionneuse {#section-3783125360a1425eae5a5a334867cc32}

1. Pour ce lecteur de page complète que vous êtes en train de créer, vous pouvez ajouter des styles de base.

   Ajouter le `style` bloc suivant au bas de la `head`:

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

## Inclusion des  de et ZoomView {#section-1a01730663154a508b88cc40c6f35539}

1. Créez une visionneuse réelle en incluant les composants `Container` et `ZoomView`.

   Insérez les `include` instructions suivantes au bas de l’ `<head>` élément, une fois le [!DNL Utils.js] script chargé :

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

   Ajouter les variables suivantes en haut de la fonction anonyme principale, juste au-dessus `s7sdk.Util.init()`:

   ```
   var container, zoomView;
   ```

1. Insérez les éléments suivants dans la `initViewer` fonction pour définir certains modificateurs et instancier les composants respectifs :

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

1. Pour que le code ci-dessus s’exécute correctement, ajoutez un gestionnaire de  `containerResize` et une fonction d’aide :

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

1. de la page afin que vous puissiez voir ce que vous avez créé. La page se présente comme suit :

   ![](assets/viewer-1.jpg)

Vous allez maintenant ajouter les composants `MediaSet` et `Swatches` à votre lecteur de contenu.

## Ajout des composants MediaSet et Swatches à votre lecteur de contenu {#section-02b8c21dd842400e83eae2a48ec265b7}

1. Pour permettre aux utilisateurs de sélectionner des images d’une visionneuse, vous pouvez ajouter les composants `MediaSet` et `Swatches`.

   Ajouter SDK suivant inclut :

   ```
   s7sdk.Util.lib.include('s7sdk.set.MediaSet'); 
   s7sdk.Util.lib.include('s7sdk.set.Swatches');
   ```

1. Mettez à jour le  de variable avec ce qui suit :

   ```
   var mediaSet, container, zoomView, swatches;
   ```

1. Instanciez `MediaSet` et `Swatches` les composants dans la `initViewer` fonction.

   Veillez à instancier l’ `Swatches` instance une fois que les composants `ZoomView` et `Container` sont masqués, sinon l’ordre d’empilement masque le `Swatches`:

   ```
   // Create MediaSet to manage assets and add event listener to the NOTF_SET_PARSED event 
   mediaSet = new s7sdk.set.MediaSet(null, params, "mediaSet"); 
   
   // Add MediaSet event listener 
   mediaSet.addEventListener(s7sdk.event.AssetEvent.NOTF_SET_PARSED, onSetParsed, false); 
   
   /* create Swatches component and associate event handler for swatch selection notification */ 
   swatches = new s7sdk.set.Swatches("s7container", params, "mySwatches");   
   swatches.addEventListener(s7sdk.event.AssetEvent.SWATCH_SELECTED_EVENT, swatchSelected, false);
   ```

1. Ajoutez maintenant les fonctions de gestionnaire de  de suivantes :

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

1. Positionnez les échantillons au bas de la visionneuse en ajoutant le fichier CSS suivant à l’ `style` élément :

   ```
   /* Align swatches to bottom of viewer */ 
   .s7swatches { 
       bottom: 0; 
       left: 0; 
       right: 0; 
       height: 150px; 
   }
   ```

1.  votre lecteur.

   Notez que les échantillons se trouvent dans le coin inférieur gauche du lecteur. Pour que les nuances prennent toute la largeur de la visionneuse, ajoutez un appel pour redimensionner manuellement les nuances chaque fois que l’utilisateur redimensionne son navigateur. Ajouter les éléments suivants à la `resizeViewer` fonction :

   ```
   swatches.resize(width, swatches.getHeight());
   ```

   Votre lecteur ressemble désormais à l’image suivante. Essayez de redimensionner la fenêtre du navigateur de la visionneuse et notez le comportement qui en résulte.

   ![](assets/viewer-2.jpg)

Vous allez maintenant ajouter des boutons de zoom avant, de zoom arrière et de réinitialisation du zoom à votre visionneuse.

## Ajout de boutons à la visionneuse {#section-1fc334fa0d2b47eb9cdad461725c07be}

1. Actuellement, l’utilisateur ne peut effectuer un zoom qu’à l’aide de mouvements de clic ou de toucher. Par conséquent, ajoutez quelques boutons de commande de zoom de base à la visionneuse.

   Ajouter les composants de bouton suivants :

   ```
   s7sdk.Util.lib.include('s7sdk.common.Button');
   ```

1. Mettez à jour le  de variable avec ce qui suit :

   ```
   var mediaSet, container, zoomView, swatches, zoomInButton, zoomOutButton, zoomResetButton;
   ```

1. Instancier les boutons au bas de la `initViewer` fonction.

   N’oubliez pas que l’ordre est important, sauf si vous spécifiez l’ordre `z-index` dans CSS :

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

1. Définissez maintenant certains styles de base pour les boutons en ajoutant ce qui suit au `style` bloc situé en haut de votre fichier :

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

1.  votre lecteur. Il ressemblera à ce qui suit :

   ![](assets/viewer-3.jpg)

   Vous allez maintenant configurer les échantillons de sorte qu’ils soient alignés verticalement à droite.

## Configuration verticale des échantillons {#section-91a8829d5b5a4d45a35b7faeb097fcc9}

1. Vous pouvez configurer les modificateurs directement sur l’ `ParameterManager` instance.

   Ajouter les éléments suivants en haut de la `initViewer` fonction pour configurer la disposition `Swatches` du curseur en tant que ligne unique :

   ```
   params.push("Swatches.tmblayout", "1,0");
   ```

1. Mettez à jour l’appel de redimensionnement suivant à l’intérieur `resizeViewer`:

   ```
   swatches.resize(swatches.getWidth(), height);
   ```

1. Modifiez la `s7swatches` règle suivante dans `ZoomViewer.css`:

   ```
   .s7swatches { 
       top:0 ; 
       bottom: 0; 
       right: 0; 
       width: 150px; 
   }
   ```

1.  votre lecteur. Il ressemblera à ce qui suit :

   ![](assets/viewer-4.jpg)

   La visionneuse de zoom de base est maintenant terminée.

   Ce didacticiel de la visionneuse décrit les fondamentaux du kit de développement de visionneuse Scene7. Lorsque vous travaillez avec le kit SDK, vous pouvez utiliser les différents composants standard pour créer et mettre en forme facilement des expériences d’affichage riches pour vos   .

