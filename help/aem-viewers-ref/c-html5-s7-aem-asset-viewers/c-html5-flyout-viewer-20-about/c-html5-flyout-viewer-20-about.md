---
title: Fenêtre déroulante
description: La visionneuse Fenêtre déroulante est une visionneuse d’images. Elle affiche une image statique avec la version agrandie dans la vue déroulante activée par l’utilisateur. Cette visionneuse fonctionne avec les visionneuses d’images et la navigation s’effectue à l’aide d’échantillons. Il est conçu pour fonctionner sur les ordinateurs de bureau et les appareils mobiles.
keywords: réactif
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Flyout
role: Developer,User
exl-id: 9b60330f-5348-431d-9682-cf97aace3679
source-git-commit: b89ca96947f751b750623e1f18d2a5d86f0cd759
workflow-type: tm+mt
source-wordcount: '2011'
ht-degree: 0%

---

# Fenêtre déroulante{#flyout}

La visionneuse Fenêtre déroulante est une visionneuse d’images. Il affiche une image statique avec la version agrandie affichée dans la vue déroulante activée par un utilisateur. Cette visionneuse fonctionne avec des visionneuses d’images et la navigation est effectuée à l’aide d’échantillons. Il est conçu pour fonctionner sur les ordinateurs de bureau et les appareils mobiles.

>[!NOTE]
>
>Les images qui utilisent IR (Image Rendering) ou UGC (User-Generated Content) ne sont pas prises en charge par cette visionneuse.

Type de visionneuse : 504.

Voir [Configuration requise et conditions préalables](../../c-system-requirements-and-prerequisites.md#concept-9282e5b777de42cdaf72ef7ebd646842).

## URL de démonstration {#section-e1c3106f5b3e445d9b95be337c2f94e2}

[https://s7d9.scene7.com/s7viewers/html5/FlyoutViewer.html?asset=Scene7SharedAssets/ImageSet-Views-Sample](https://s7d9.scene7.com/s7viewers/html5/FlyoutViewer.html?asset=Scene7SharedAssets/ImageSet-Views-Sample)

## Utilisation de la visionneuse de fenêtre déroulante {#section-f21ac23d3f6449ad9765588d69584772}

La visionneuse Fenêtre déroulante représente un fichier JavaScript principal et un ensemble de fichiers d’assistance (une seule JavaScript inclure avec tous les composants du Kit de développement logiciel (SDK) utilisés par cette visionneuse particulière, ressources, CSS) téléchargés par la visionneuse au moment de l’exécution

Flyout Viewer est uniquement destiné à une utilisation intégrée, ce qui signifie qu’il est intégré dans la page Web à l’aide d’une API documentée. Aucune page Web prête pour la production n’est disponible pour la visionneuse déroulante.

La configuration et l’habillage sont similaires à ceux des autres visionneuses. Vous pouvez utiliser un CSS personnalisé pour appliquer un habillage.

Voir [Référence de commande commune à tous les visualiseurs - Attributs](../../r-html5-viewer-20-cmdref-configattrib/r-html5-viewer-20-cmdref-configattrib.md#concept-850e0f2c49b949deb7cfbfd330d329bd) de configuration et [Référence de commande communs à tous les visualiseurs - URL](../../c-html5-viewer-20-cmdref-url/c-html5-viewer-20-cmdref-url.md#concept-9b337f349b7b406b8c33c7ee96b3e226)

## Interaction avec la visionneuse Fenêtre déroulante {#section-ab66eb6955aa4a8aa6d14a3b3acfed3f}

La visionneuse Fenêtre déroulante prend en charge les gestes tactiles uniques et multipoint courants dans d’autres applications mobiles.

<table id="table_ED747CC7178448919C34A4FCD18922D0"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>Mouvement </p> </th> 
   <th colname="col2" class="entry"> <p>Description </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>Robinet unique </p> </td> 
   <td colname="col2"> <p> Active la vue déroulante ou passe du niveau de zoom principal au niveau de zoom secondaire. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Glissement horizontal </p> </td> 
   <td colname="col2"> <p> Fait défiler la liste des nuances dans la barre d’échantillons. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Balayage vertical </p> </td> 
   <td colname="col2"> <p>Si le mouvement est effectué dans la zone d’échantillons, il effectue un défilement natif de la page. </p> </td> 
  </tr> 
 </tbody> 
</table>

La visionneuse prend également en charge l’entrée tactile et l’entrée souris sur les appareils Windows dotés d’un écran tactile et d’une souris. Cette prise en charge se limite toutefois aux navigateurs web Chrome, Internet Explorer 11 et Edge uniquement.

Cette visionneuse est entièrement accessible à partir du clavier.

Voir [Accessibilité clavier et navigation](../../c-keyboard-accessibility.md#topic-f5650e9493404e55a3627c8d1366b861).

## Incorporation de la visionneuse déroulante {#section-6bb5d3c502544ad18a58eafe12a13435}

Les différentes pages web ont des besoins différents en termes de comportement des observateurs. La page web peut avoir une mise en page statique ou utiliser une conception réactive qui s’affiche différemment selon les appareils ou selon la taille des fenêtres du navigateur. Pour répondre à ces besoins, la visionneuse prend en charge deux modes de fonctionnement principaux : l’incorporation de taille fixe et l’incorporation de conception réactive.

Le mode d’incorporation de taille fixe est utilisé lorsque la visionneuse ne change pas de taille après son chargement initial. Ce choix est préférable pour les pages web avec une disposition de page statique.

Le mode d’incorporation de conception réactive suppose que la visionneuse doit être redimensionnée au moment de l’exécution en réponse au changement de taille de son `DIV` de conteneur. Le cas d’utilisation le plus courant consiste à ajouter une visionneuse à une page web qui utilise une disposition de page flexible.

Lors de l’utilisation du mode d’incorporation Responsive Design avec la visionneuse Fenêtre déroulante, veillez à spécifier des points d’arrêt explicites pour l’image d’affichage principal à l’aide du paramètre `imagereload` . Idéalement, faites correspondre vos points d’arrêt avec les points d’arrêt de largeur de la visionneuse dictés par le CSS de la page Web.

En mode d’incorporation de conception réactive, la visionneuse se comporte différemment selon la taille d’un conteneur `DIV` de page Web. Si la page Web définit uniquement la largeur du conteneur `DIV`, en laissant sa hauteur illimitée, le spectateur choisit automatiquement sa hauteur en fonction du format de la ressource utilisée. Cette fonctionnalité signifie que l’actif s’intègre parfaitement dans la vue sans aucun rembourrage sur les côtés. Ce cas d’utilisation particulier est le plus courant pour les pages Web qui utilisent des cadres de mise en page de conception réactive tels que Bootstrap et Foundation.

Sinon, si la page Web définit à la fois la largeur et la hauteur du conteneur `DIV`de l’afficheuse , celle-ci remplit uniquement cette zone et suit la taille fournie par la mise en page Web. Un bon exemple d’utilisation consiste à incorporer la visionneuse dans une superposition modale, où la superposition est dimensionnée en fonction de la taille de la fenêtre du navigateur Web.

**Incorporation de taille fixe**

Ajoutez la visionneuse à une page web en procédant comme suit :

1. Ajout du fichier JavaScript de la visionneuse à votre page web.
1. La définition du `DIV` de conteneur.
1. Définition de la taille de la visionneuse.
1. Création et initialisation de la visionneuse.

1. Ajout du fichier JavaScript de la visionneuse à votre page web.

   La création d’une visionneuse nécessite l’ajout d’une balise de script dans l’en-tête HTML. Avant de pouvoir utiliser l’API de visionneuse, veillez à inclure `FlyoutViewer.js`. `FlyoutViewer.js` se trouve dans le sous-dossier [!DNL html5/js/] suivant de votre déploiement d’observateurs IS standard :

[!DNL <s7viewers_root>/html5/js/FlyoutViewer.js]

Vous pouvez utiliser un chemin d’accès relatif si la visionneuse est déployée sur l’un des serveurs Dynamic Media d’Adobe et qu’elle est diffusée à partir du même domaine. Sinon, vous spécifiez un chemin d’accès complet à l’un des serveurs Dynamic Media Adobe sur lesquels les visionneuses IS sont installées.

Un chemin relatif ressemble à ce qui suit :

```html {.line-numbers}
<script language="javascript" type="text/javascript" src="/s7viewers/html5/js/FlyoutViewer.js"></script>
```

>[!NOTE]
>
>Référencez uniquement le fichier JavaScript `include` de visionneuse principal sur votre page. Ne référencez aucun fichier JavaScript supplémentaire dans le code de page web qui pourrait être téléchargé par la logique de la visionneuse au moment de l’exécution. En particulier, ne référencez pas directement la bibliothèque SDK `Utils.js` HTML5 chargée par la visionneuse à partir du chemin d’accès `/s7viewers` au contexte (SDK `include`consolidé). La raison en est que l’emplacement des bibliothèques d’exécution ou des bibliothèques de `Utils.js` visionneuse similaires est entièrement géré par la logique de la visionneuse et que l’emplacement change entre les versions de la visionneuse. Adobe ne conserve pas les anciennes versions de la visionneuse `includes` secondaire sur le serveur.
>
>
>Par conséquent, le fait de placer une référence directe à une JavaScript `include` secondaire utilisée par l’utilisateur sur la page interrompt la fonctionnalité de la visionneuse à l’avenir lorsqu’une nouvelle version du produit est déployée.

1. Définition du conteneur DIV.

   Ajoutez un élément DIV vide à la page sur laquelle vous souhaitez que la visionneuse apparaisse. L’identifiant de l’élément DIV doit être défini, car cet identifiant est ensuite transmis à l’API de visionneuse.

   L’espace réservé DIV est un élément positionné, ce qui signifie que la propriété CSS `position` est définie sur `relative` ou `absolute`.

   Il incombe à la page web de spécifier le `z-index` approprié pour l’élément DIV d’espace réservé. Cela permet de s’assurer que la partie déroulante de la visionneuse s’affiche au-dessus des autres éléments de la page web.

   Exemple d’élément DIV d’espace réservé défini :

   ```html {.line-numbers}
   <div id="s7viewer" style="position:relative;z-index:1"></div> 
   ```

1. Définition de la taille de la visionneuse.

   Cette visionneuse affiche des miniatures lorsque vous travaillez avec des visionneuses multi-éléments. Sur les ordinateurs de bureau, des miniatures sont placées sous la vue principale. Dans le même temps, la visionneuse permet l’échange de la ressource principale pendant l’exécution à l’aide d’API `setAsset()` . En tant que développeur, vous contrôlez la façon dont la visionneuse gère la zone des vignettes dans la zone inférieure lorsque la nouvelle ressource ne comporte qu’un seul élément. Il est possible de garder la taille de la visionneuse extérieure intacte et de laisser la vue principale augmenter sa hauteur et occuper la zone des vignettes. Vous pouvez également conserver la taille de la vue principale statique et réduire la zone extérieure de la visionneuse, en laissant le contenu de la page Web se déplacer vers le haut, puis utiliser l’espace de page libre laissé par les vignettes.

   Pour conserver les limites extérieures de la visionneuse, définissez la taille de `.s7flyoutviewer` la classe CSS de niveau supérieur en unités absolues. Le dimensionnement dans CSS peut être placé directement sur la page HTML ou dans un fichier CSS de visionneuse personnalisé, attribué ultérieurement à un enregistrement de paramètre prédéfini de visionneuse dans Dynamic Media Classic, ou transmis explicitement à l’aide de la commande de style.

   Voir [Personnalisation de la visionneuse](../../c-html5-s7-aem-asset-viewers/c-html5-flyout-viewer-20-about/c-html5-flyout-viewer-20-customizingviewer/c-html5-flyout-viewer-20-customizingviewer.md#concept-82f8c71adbe54680a0c2f83f81e5f451) de fenêtre déroulante pour plus d’informations sur le style de la visionneuse avec CSS.

   Voici un exemple de définition de la taille statique de la visionneuse externe dans une page HTML :

   ```html {.line-numbers}
   #s7viewer.s7flyoutviewer { 
    width: 640px; 
    height: 480px; 
   }
   ```

   Vous pouvez voir le comportement avec une zone de visionneuse extérieure fixe sur l’exemple de page suivant. Notez que lorsque vous basculez entre des visionneuses, la taille extérieure de la visionneuse ne change pas :

   [https://experienceleague.adobe.com/tools/dynamic-media-demo/viewers-ref/flyout/FlyoutViewer-fixed-outer-area.html](https://experienceleague.adobe.com/tools/dynamic-media-demo/viewers-ref/flyout/FlyoutViewer-fixed-outer-area.html)

   Pour rendre les dimensions de la vue principale statiques, définissez la taille de la visionneuse en unités absolues pour le composant SDK interne `Container` à l’aide `.s7flyoutviewer .s7container` du sélecteur CSS. En outre, vous devez remplacer la taille fixe définie pour la `.s7flyoutviewer` classe CSS de niveau supérieur dans la feuille CSS par défaut de la visionneuse en la définissant sur `auto`.

   Voici un exemple de définition de la taille de la visionneuse pour le composant SDK interne `Container` afin que la zone d’affichage principale ne modifie pas sa taille lors du changement de ressource :

   ```html {.line-numbers}
   #s7viewer.s7flyoutviewer { 
    width: auto; 
    height: auto; 
   }  
   #s7viewer.s7flyoutviewer .s7container { 
    width: 640px; 
    height: 480px; 
   }
   ```

   L’exemple de page suivant illustre le comportement des visionneuses avec une taille d’affichage principale fixe. Notez que lorsque vous passez d’un ensemble à l’autre, la vue principale reste statique et le contenu de la page web se déplace verticalement :

   [https://experienceleague.adobe.com/tools/dynamic-media-demo/viewers-ref/flyout/FlyoutViewer-fixed-main-view.html](https://experienceleague.adobe.com/tools/dynamic-media-demo/viewers-ref/flyout/FlyoutViewer-fixed-main-view.html)

   En outre, la visionneuse CSS par défaut fournit une taille fixe pour sa zone extérieure prête à l’emploi.

1. Création et initialisation de la visionneuse.

   Lorsque vous avez terminé les étapes ci-dessus, vous créez une instance de classe, transmettez toutes les informations de configuration à son constructeur et appelez `s7viewers.FlyoutViewer` la méthode sur une instance de `init()` visionneuse. Les informations de configuration sont transmises au constructeur sous la forme d’un objet JSON. Au minimum, cet objet doit avoir le `containerId` champ qui contient le nom de l’ID de conteneur de la visionneuse et de l’objet JSON imbriqué `params` avec les paramètres de configuration pris en charge par la visionneuse. Dans ce cas, l’objet `params` doit avoir au moins l’URL Image Serving transmise en tant que propriété et la ressource initiale en tant que `serverUrl` `asset` paramètre. L’API d’initialisation basée sur JSON vous permet de créer et de démarrer la visionneuse avec une seule ligne de code.

   Il est important d’ajouter le conteneur de visionneuse au DOM afin que le code de visionneuse puisse trouver l’élément conteneur par son ID. Certains navigateurs retardent la création de DOM jusqu’à la fin de la page Web. Pour une compatibilité maximale, appelez la `init()` méthode juste avant la balise de fermeture `BODY` , ou sur l’événement body `onload()` .

   Dans le même temps, l’élément de conteneur ne doit pas nécessairement encore faire partie de la mise en page web. Par exemple, elle peut être masquée à l’aide `display:none` style qui lui est affecté. Dans ce cas, la visionneuse retarde son processus d’initialisation jusqu’au moment où la page web ramène l’élément de conteneur dans la mise en page. Lorsque cette action se produit, le chargement de la visionneuse reprend automatiquement.

   Voici un exemple de création d’une instance de visionneuse, transmettant les options de configuration minimales nécessaires au constructeur et appelant la méthode `init()`. L’exemple suppose que `flyoutViewer` est l’instance de visionneuse, `s7viewer` est le nom de l’espace réservé `DIV`, `http://s7d1.scene7.com/is/image/` est l’URL du service d’images et `Scene7SharedAssets/ImageSet-Views-Sample` est la ressource :

   ```html {.line-numbers}
   <script type="text/javascript"> 
   var flyoutViewer = new s7viewers.FlyoutViewer({ 
    "containerId":"s7viewer", 
   "params":{ 
    "asset":"Scene7SharedAssets/ImageSet-Views-Sample", 
    "serverurl":"http://s7d1.scene7.com/is/image/" 
   } 
   }).init(); 
   </script>
   ```

   Le code suivant est un exemple complet de page web triviale qui intègre la visionneuse Fenêtre déroulante à taille fixe :

   ```html {.line-numbers}
   <!DOCTYPE html> 
   <html> 
   <head> 
   <script type="text/javascript" src="http://s7d1.scene7.com/s7viewers/html5/js/FlyoutViewer.js"></script> 
   <style type="text/css"> 
   #s7viewer.s7flyoutviewer { 
    width: 640px; 
    height: 480px; 
   } 
   </style> 
   </head> 
   <body> 
   <div id="s7viewer" style="position:relative;z-index:1;"></div> 
   <script type="text/javascript"> 
   var flyoutViewer = new s7viewers.FlyoutViewer({ 
    "containerId":"s7viewer", 
   "params":{ 
    "asset":"Scene7SharedAssets/ImageSet-Views-Sample", 
    "serverurl":"http://s7d1.scene7.com/is/image/" 
   } 
   }).init(); 
   </script> 
   </body> 
   </html>
   ```

## Incorporation de conception réactive avec hauteur illimitée {#section-056cb574713c4d07be6d07cf3c598839}

Avec l’intégration de conception réactive, la page Web a normalement une sorte de mise en page flexible en place qui dicte la taille d’exécution du conteneur `DIV`de la visionneuse. Pour l’exemple suivant, supposons que la page Web autorise le conteneur `DIV` de la visionneuse à prendre 40 % de la taille de la fenêtre du navigateur Web, en laissant sa hauteur sans restriction. Le code d’HTML de la page web se présente comme suit :

```html {.line-numbers}
<!DOCTYPE html> 
<html> 
<head> 
<style type="text/css"> 
.holder { 
 width: 40%; 
} 
</style> 
</head> 
<body> 
<div class="holder"></div> 
</body> 
</html>
```

L’ajout de la visionneuse à une telle page est similaire aux étapes d’incorporation à taille fixe. La seule différence est que vous devez remplacer la taille fixe à partir du CSS de la visionneuse par défaut par la taille définie en unités relatives.

1. Ajout du fichier JavaScript de la visionneuse à votre page web.
1. La définition du `DIV` de conteneur.
1. Définition de la taille de la visionneuse.
1. Création et initialisation de la visionneuse.

Toutes les étapes ci-dessus sont identiques à celles de l’incorporation de taille fixe, à trois exceptions près :

* ajouter le conteneur `DIV` au « support » `DIV`existant ;
* ajout d’un `imagereload` paramètre avec des points d’arrêt explicites ;
* au lieu de définir une taille de visionneuse fixe à l’aide d’unités absolues, utilisez un CSS qui définit la largeur et la hauteur de la visionneuse sur 100 % comme dans ce qui suit :

```html {.line-numbers}
#s7viewer.s7flyoutviewer { 
 width: 100%; 
 height: 100%; 
}
```

Le code suivant en est un exemple complet. Notez la manière dont la taille de la visionneuse change lorsque le navigateur est redimensionné, ainsi que la manière dont les proportions de la visionneuse correspondent à la ressource.

```html {.line-numbers}
<!DOCTYPE html> 
<html> 
<head> 
<script type="text/javascript" src="http://s7d1.scene7.com/s7viewers/html5/js/FlyoutViewer.js"></script> 
<style type="text/css"> 
.holder { 
 width: 40%; 
} 
#s7viewer.s7flyoutviewer { 
 width: 100%; 
 height: 100%; 
} 
</style> 
</head> 
<body> 
<div class="holder"> 
<div id="s7viewer" style="position:relative;z-index:1"></div> 
</div> 
<script type="text/javascript"> 
var flyoutViewer = new s7viewers.FlyoutViewer({ 
 "containerId":"s7viewer", 
"params":{ 
 "asset":"Scene7SharedAssets/ImageSet-Views-Sample", 
 "serverurl":"http://s7d1.scene7.com/is/image/", 
 "imagereload":"1,breakpoint,200;400;800;1600" 
} 
}).init(); 
</script> 
</body> 
</html>
```

La page d’exemples suivante illustre d’autres utilisations réelles de l’incorporation Responsive Design avec une hauteur illimitée :

[Démonstrations en direct](https://landing.adobe.com/en/na/dynamic-media/ctir-2755/live-demos.html)

[Autre emplacement de démonstration](https://experienceleague.adobe.com/tools/dynamic-media-demo/vlist/vlist.html)

## Intégration de taille flexible avec largeur et hauteur définies {#section-0a329016f9414d199039776645c693de}

S’il existe une incorporation de taille flexible avec la largeur et la hauteur définies, le style de la page web est différent. Il fournit les deux tailles au DIV `"holder"` et le centre dans la fenêtre du navigateur. En outre, la page web définit la taille de l’élément `HTML` et `BODY` sur 100 %.

```html {.line-numbers}
<!DOCTYPE html> 
<html> 
<head> 
<style type="text/css"> 
html, body { 
 width: 100%; 
 height: 100%; 
} 
.holder { 
 position: absolute; 
 left: 20%; 
 top: 20%; 
 width: 60%; 
height: 60%; 
} 
</style> 
</head> 
<body> 
<div class="holder"></div> 
</body> 
</html>
```

Le reste des étapes d’incorporation est identique aux étapes utilisées pour l’incorporation de Responsive Design avec une hauteur illimitée. L’exemple qui en résulte est le suivant :

```html {.line-numbers}
<!DOCTYPE html> 
<html> 
<head> 
<script type="text/javascript" src="http://s7d1.scene7.com/s7viewers/html5/js/FlyoutViewer.js"></script> 
<style type="text/css"> 
html, body { 
 width: 100%; 
 height: 100%; 
} 
.holder { 
 position: absolute; 
 left: 20%; 
 top: 20%; 
 width: 60%; 
height: 60%; 
} 
#s7viewer.s7flyoutviewer { 
 width: 100%; 
 height: 100%; 
} 
</style> 
</head> 
<body> 
<div class="holder"> 
<div id="s7viewer" style="position:relative;z-index:1"></div> 
</div> 
<script type="text/javascript"> 
var flyoutViewer = new s7viewers.FlyoutViewer({ 
 "containerId":"s7viewer", 
"params":{ 
 "asset":"Scene7SharedAssets/ImageSet-Views-Sample", 
 "serverurl":"http://s7d1.scene7.com/is/image/", 
 "imagereload":"1,breakpoint,200;400;800;1600" 
} 
}).init(); 
</script> 
</body> 
</html>
```

## Incorporation à l’aide de l’API Setter {#section-af26f0cc2e5140e8a9bfd0c6a841a6d1}

Au lieu d’utiliser l’initialisation basée sur JSON, il est possible d’utiliser l’API basée sur setter et le constructeur sans args. L’utilisation de ce constructeur d’API ne prend aucun paramètre et les paramètres de configuration sont spécifiés à l’aide de `setContainerId()`, `setParam()`et `setAsset()` des méthodes d’API, avec des appels JavaScript distincts.

L’exemple suivant illustre l’utilisation de l’incorporation de taille fixe avec l’API basée sur setter :

```html {.line-numbers}
<!DOCTYPE html> 
<html> 
<head> 
<script type="text/javascript" src="http://s7d1.scene7.com/s7viewers/html5/js/FlyoutViewer.js"></script> 
<style type="text/css"> 
#s7viewer.s7flyoutviewer { 
 width: 640px; 
 height: 480px; 
} 
</style> 
</head><body> 
<div id="s7viewer" style="position:relative;z-index:1;"></div> 
<script type="text/javascript"> 
var flyoutViewer = new s7viewers.FlyoutViewer(); 
flyoutViewer.setContainerId("s7viewer"); 
flyoutViewer.setParam("serverurl", "http://s7d1.scene7.com/is/image/"); 
flyoutViewer.setAsset("Scene7SharedAssets/ImageSet-Views-Sample"); 
flyoutViewer.init(); 
</script> 
</body> 
</html>
```
