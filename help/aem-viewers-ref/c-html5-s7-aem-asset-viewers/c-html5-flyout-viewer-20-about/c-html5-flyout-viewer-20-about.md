---
description: Visionneuse déroulante est une visionneuse d’images. Il affiche une image statique avec la version agrandie affichée dans la vue déroulante qu’un utilisateur active. Cette visionneuse fonctionne avec des visionneuses d’images et la navigation est effectuée à l’aide d’échantillons. Il est conçu pour fonctionner sur les ordinateurs de bureau et les appareils mobiles.
keywords: responsive
solution: Experience Manager
title: Fenêtre déroulante
feature: Dynamic Media Classic,Visionneuses,SDK/API,Fenêtre déroulante
role: Developer,User
exl-id: 9b60330f-5348-431d-9682-cf97aace3679
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '2084'
ht-degree: 0%

---

# Fenêtre déroulante{#flyout}

Visionneuse déroulante est une visionneuse d’images. Il affiche une image statique avec la version agrandie affichée dans la vue déroulante qu’un utilisateur active. Cette visionneuse fonctionne avec des visionneuses d’images et la navigation est effectuée à l’aide d’échantillons. Il est conçu pour fonctionner sur les ordinateurs de bureau et les appareils mobiles.

>[!NOTE]
>
>Les images qui utilisent IR (Image Rendering) ou UGC (User-Generated Content) ne sont pas prises en charge par cette visionneuse.

Le type de visionneuse est 504.

Voir [Configuration requise et conditions préalables](../../c-system-requirements-and-prerequisites.md#concept-9282e5b777de42cdaf72ef7ebd646842).

## URL de démonstration {#section-e1c3106f5b3e445d9b95be337c2f94e2}

[https://s7d9.scene7.com/s7viewers/html5/FlyoutViewer.html?asset=Scene7SharedAssets/ImageSet-Views-Sample](https://s7d9.scene7.com/s7viewers/html5/FlyoutViewer.html?asset=Scene7SharedAssets/ImageSet-Views-Sample)

## Utilisation de la visionneuse déroulante {#section-f21ac23d3f6449ad9765588d69584772}

La visionneuse déroulante représente un fichier JavaScript principal et un ensemble de fichiers d’assistance (un seul fichier JavaScript inclus avec tous les composants du SDK de la visionneuse utilisés par cette visionneuse, ressources et CSS particulière) téléchargés par la visionneuse au moment de l’exécution.

La visionneuse Fenêtre déroulante est uniquement destinée à une utilisation incorporée, ce qui signifie qu’elle est intégrée à la page web à l’aide d’une API documentée. Aucune page web prête pour la production n’est disponible pour la visionneuse Fenêtre déroulante.

La configuration et l’habillage sont similaires à ceux des autres visionneuses. Vous pouvez utiliser une page CSS personnalisée pour appliquer l’habillage.

Voir [Référence de commande commune à toutes les visionneuses - Attributs de configuration](../../r-html5-viewer-20-cmdref-configattrib/r-html5-viewer-20-cmdref-configattrib.md#concept-850e0f2c49b949deb7cfbfd330d329bd) et [Référence de commande commune à toutes les visionneuses - URL](../../c-html5-viewer-20-cmdref-url/c-html5-viewer-20-cmdref-url.md#concept-9b337f349b7b406b8c33c7ee96b3e226)

## Interaction avec la visionneuse déroulante {#section-ab66eb6955aa4a8aa6d14a3b3acfed3f}

La visionneuse Fenêtre déroulante prend en charge les gestes tactiles simples et multipoints communs aux autres applications mobiles.

<table id="table_ED747CC7178448919C34A4FCD18922D0"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>Mouvement </p> </th> 
   <th colname="col2" class="entry"> <p>Description </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>Appuyer une seule fois </p> </td> 
   <td colname="col2"> <p> Active la vue déroulante ou modifie le niveau de zoom Principal et secondaire. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Glissement ou clic horizontal </p> </td> 
   <td colname="col2"> <p> Fait défiler la liste des échantillons dans la barre d’échantillons. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Glissement vertical </p> </td> 
   <td colname="col2"> <p>Si le mouvement est effectué dans la zone des échantillons, il effectue un défilement de page natif. </p> </td> 
  </tr> 
 </tbody> 
</table>

La visionneuse prend également en charge les entrées tactile et de souris sur les périphériques Windows dotés d’un écran tactile et d’une souris. Toutefois, cette prise en charge est limitée aux navigateurs Chrome, Internet Explorer 11 et Edge uniquement.

Cette visionneuse est entièrement accessible au clavier.

Voir [Accessibilité clavier et navigation](../../c-keyboard-accessibility.md#topic-f5650e9493404e55a3627c8d1366b861).

## Intégration de la visionneuse déroulante {#section-6bb5d3c502544ad18a58eafe12a13435}

Le comportement de la visionneuse varie en fonction des pages web. La page web peut avoir une mise en page statique ou utiliser une conception réactive qui s’affiche différemment sur différents appareils ou pour différentes tailles de fenêtre de navigateur. Pour répondre à ces besoins, la visionneuse prend en charge deux modes de fonctionnement Principaux : incorporation de tailles fixes et incorporation de conceptions réactives.

Le mode d’incorporation des tailles fixe est utilisé lorsque la visionneuse ne modifie pas sa taille après son chargement initial. Ce choix est préférable pour les pages web ayant une mise en page statique.

Le mode d’incorporation des conceptions réactives suppose que la visionneuse doit peut-être redimensionner au moment de l’exécution en réponse au changement de taille de son conteneur `DIV`. Le cas d’utilisation le plus courant consiste à ajouter une visionneuse à une page web qui utilise une mise en page flexible.

Lors de l’utilisation du mode d’incorporation de Responsive Design avec la visionneuse Fenêtre déroulante, veillez à spécifier des points d’arrêt explicites pour l’image de la vue principale à l’aide du paramètre `imagereload` . Idéalement, faites correspondre vos points d’arrêt avec les points d’arrêt de largeur de la visionneuse comme dicté par la page web CSS.

En mode d’incorporation en responsive design, la visionneuse se comporte différemment selon la façon dont une page web dimensionne son conteneur `DIV`. Si la page web définit uniquement la largeur du conteneur `DIV`, en ne limitant pas sa hauteur, la visionneuse choisit automatiquement sa hauteur en fonction des proportions de la ressource utilisée. Cela signifie que la ressource s’intègre parfaitement dans la vue sans marge intérieure sur les côtés. Ce cas d’utilisation particulier est le plus courant pour les pages web qui utilisent des structures de mise en page en responsive design comme Bootstrap, Foundation, etc.

Dans le cas contraire, si la page web définit à la fois la largeur et la hauteur du conteneur de la visionneuse `DIV`, la visionneuse ne remplit que cette zone et suit la taille fournie par la mise en page web. Un bon exemple de cas d’utilisation consiste à incorporer la visionneuse dans une superposition modale, où la superposition est dimensionnée en fonction de la taille de la fenêtre du navigateur web.

**Incorporation de taille fixe**

Pour ajouter la visionneuse à une page web, procédez comme suit :

1. Ajout du fichier JavaScript de la visionneuse à votre page web.
1. Définition du conteneur `DIV`.
1. Définition de la taille de la visionneuse.
1. Création et initialisation de la visionneuse.

1. Ajout du fichier JavaScript de la visionneuse à votre page web.

   Pour créer une visionneuse, vous devez ajouter une balise de script dans l’en-tête HTML. Avant d’utiliser l’API de visionneuse, veillez à inclure `FlyoutViewer.js`. `FlyoutViewer.js` se trouve dans le sous- [!DNL html5/js/] dossier suivant de votre déploiement IS-Viewers standard :

[!DNL <s7viewers_root>/html5/js/FlyoutViewer.js]

Vous pouvez utiliser un chemin relatif si la visionneuse est déployée sur l’un des serveurs Dynamic Media Adobe et qu’elle est diffusée à partir du même domaine. Dans le cas contraire, vous spécifiez un chemin d’accès complet à l’un des serveurs Dynamic Media Adobe sur lesquels les visionneuses IS sont installées.

Un chemin relatif ressemble à ce qui suit :

```
<script language="javascript" type="text/javascript" src="/s7viewers/html5/js/FlyoutViewer.js"></script>
```

>[!NOTE]
>
>Vous ne devez référencer que le fichier JavaScript de la visionneuse principale `include` sur votre page. Vous ne devez pas référencer de fichiers JavaScript supplémentaires dans le code de page web qui peuvent être téléchargés selon la logique de la visionneuse au moment de l’exécution. En particulier, ne référencez pas directement la bibliothèque `Utils.js` SDK HTML5 chargée par la visionneuse à partir du chemin de contexte `/s7viewers` (appelé SDK consolidé `include`). Cela est dû au fait que l’emplacement des bibliothèques de visionneuses `Utils.js` ou d’exécution similaires est entièrement géré par la logique de la visionneuse et que l’emplacement change entre les versions de la visionneuse. Adobe ne conserve pas les anciennes versions de la visionneuse secondaire `includes` sur le serveur.
>
>
>Par conséquent, l’insertion d’une référence directe à tout JavaScript secondaire `include` utilisé par la visionneuse sur la page rompt la fonctionnalité de visionneuse à l’avenir lorsqu’une nouvelle version de produit est déployée.

1. Définition du conteneur DIV.

   Ajoutez un élément DIV vide à la page sur laquelle vous souhaitez que la visionneuse apparaisse. L’ID de l’élément DIV doit être défini, car cet ID est ensuite transmis à l’API de visionneuse.

   L’espace réservé DIV est un élément positionné, ce qui signifie que la propriété CSS `position` est définie sur `relative` ou `absolute`.

   Il est de la responsabilité de la page web de spécifier la balise `z-index` appropriée pour l’élément DIV de l’espace réservé. Cela garantit que la partie fenêtre déroulante de la visionneuse s’affiche au-dessus des autres éléments de la page web.

   Voici un exemple d’élément DIV d’espace réservé défini :

   ```
   <div id="s7viewer" style="position:relative;z-index:1"></div> 
   ```

1. Définition de la taille de la visionneuse.

   Cette visionneuse affiche des miniatures lorsque vous utilisez des jeux de plusieurs éléments. Sur les systèmes de bureau, les miniatures sont placées sous la vue principale. En même temps, la visionneuse permet la permutation de la ressource principale lors de l’exécution à l’aide de l’API `setAsset()`. En tant que développeur, vous contrôlez la manière dont la visionneuse gère la zone des miniatures dans la zone inférieure lorsque la nouvelle ressource ne comporte qu’un seul élément. Il est possible de conserver la taille de la visionneuse externe intacte et de laisser la vue principale augmenter sa hauteur et occuper la zone des miniatures. Vous pouvez également conserver la taille d’affichage principale statique et réduire la zone de la visionneuse externe, ce qui permet au contenu de la page web de se déplacer vers le haut, puis utiliser l’espace libre de la page laissé par les miniatures.

   Pour conserver les limites de la visionneuse extérieure intactes, définissez la taille de la classe CSS de niveau supérieur `.s7flyoutviewer` en unités absolues. Le dimensionnement en CSS peut être directement placé sur la page HTML ou dans un fichier CSS de visionneuse personnalisé, qui est ultérieurement affecté à un enregistrement de paramètre prédéfini de visionneuse dans Dynamic Media Classic, ou transmis explicitement à l’aide de la commande de style.

   Voir [Personnalisation de la visionneuse déroulante](../../c-html5-s7-aem-asset-viewers/c-html5-flyout-viewer-20-about/c-html5-flyout-viewer-20-customizingviewer/c-html5-flyout-viewer-20-customizingviewer.md#concept-82f8c71adbe54680a0c2f83f81e5f451) pour plus d’informations sur le style de la visionneuse avec CSS.

   Voici un exemple de définition de la taille statique de la visionneuse externe dans une page HTML :

   ```
   #s7viewer.s7flyoutviewer { 
    width: 640px; 
    height: 480px; 
   }
   ```

   Vous pouvez voir le comportement avec une zone de visionneuse externe fixe sur l’exemple de page suivant. Notez que lorsque vous passez d’un ensemble à l’autre, la taille de la visionneuse externe ne change pas :

   [https://experienceleague.adobe.com/tools/dynamic-media-demo/viewers-ref/flyout/FlyoutViewer-fixed-outer-area.html](https://experienceleague.adobe.com/tools/dynamic-media-demo/viewers-ref/flyout/FlyoutViewer-fixed-outer-area.html)

   Pour rendre les dimensions d’affichage principales statiques, définissez la taille de la visionneuse en unités absolues pour le composant SDK interne `Container` à l’aide du sélecteur CSS `.s7flyoutviewer .s7container`. En outre, vous devez remplacer la taille fixe définie pour la classe CSS de niveau supérieur `.s7flyoutviewer` dans le CSS de la visionneuse par défaut, en la définissant sur `auto`.

   Voici un exemple de définition de la taille de la visionneuse pour le composant SDK interne `Container` afin que la zone d’affichage principale ne change pas sa taille lors du changement de ressource :

   ```
   #s7viewer.s7flyoutviewer { 
    width: auto; 
    height: auto; 
   }  
   #s7viewer.s7flyoutviewer .s7container { 
    width: 640px; 
    height: 480px; 
   }
   ```

   L’exemple de page suivant montre le comportement de la visionneuse avec une taille d’affichage principale fixe. Notez que lorsque vous basculez entre deux ensembles, la vue principale reste statique et le contenu de la page web se déplace verticalement :

   [https://experienceleague.adobe.com/tools/dynamic-media-demo/viewers-ref/flyout/FlyoutViewer-fixed-main-view.html](https://experienceleague.adobe.com/tools/dynamic-media-demo/viewers-ref/flyout/FlyoutViewer-fixed-main-view.html)

   Notez également que la feuille CSS de visionneuse par défaut fournit une taille fixe pour sa zone externe prête à l’emploi.

1. Création et initialisation de la visionneuse.

   Une fois les étapes ci-dessus terminées, vous créez une instance de la classe `s7viewers.FlyoutViewer`, transmettez toutes les informations de configuration à son constructeur et appelez la méthode `init()` sur une instance de visionneuse. Les informations de configuration sont transmises au constructeur sous la forme d’un objet JSON. Au minimum, cet objet doit comporter le champ `containerId` qui contient le nom de l’ID de conteneur de la visionneuse et l’objet JSON `params` imbriqué avec les paramètres de configuration pris en charge par la visionneuse. Dans ce cas, l’objet `params` doit avoir au moins la propriété URL de diffusion d’images transmise en tant que propriété `serverUrl` et la ressource initiale en tant que paramètre `asset`. L’API d’initialisation basée sur JSON vous permet de créer et de démarrer la visionneuse avec une seule ligne de code.

   Il est important que le conteneur de la visionneuse soit ajouté au modèle DOM afin que le code de la visionneuse puisse trouver l’élément de conteneur en fonction de son identifiant. Certains navigateurs retardent la création du DOM jusqu’à la fin de la page web. Pour bénéficier d’une compatibilité maximale, appelez la méthode `init()` juste avant la balise `BODY` de fermeture ou sur l’événement `onload()` body .

   Dans le même temps, l’élément de conteneur ne doit pas nécessairement faire partie de la mise en page de la page web pour l’instant. Par exemple, il peut être masqué à l’aide du style `display:none` qui lui est affecté. Dans ce cas, la visionneuse retarde son processus d’initialisation jusqu’au moment où la page web ramène l’élément de conteneur à la mise en page. Dans ce cas, le chargement de la visionneuse reprend automatiquement.

   Voici un exemple de création d’une instance de visionneuse, en transmettant les options de configuration minimales nécessaires au constructeur et en appelant la méthode `init()` . L’exemple suppose que `flyoutViewer` est l’instance de visionneuse ; `s7viewer` est le nom de l’espace réservé `DIV` ; `http://s7d1.scene7.com/is/image/` est l’URL du serveur d’images ; et `Scene7SharedAssets/ImageSet-Views-Sample` correspond à la ressource :

   ```
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

   Le code suivant est un exemple complet d’une page web triviale qui incorpore la visionneuse déroulante à taille fixe :

   ```
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

## Intégration de conception réactive avec une hauteur libre {#section-056cb574713c4d07be6d07cf3c598839}

Avec l’incorporation de responsive design, la page web dispose normalement d’une sorte de disposition flexible qui détermine la taille d’exécution du conteneur de la visionneuse `DIV`. Pour l’exemple suivant, supposons que la page web permette au conteneur de la visionneuse `DIV` de prendre 40 % de la taille de la fenêtre du navigateur web, en ne restreignant pas sa hauteur. Le code HTML de la page web se présente comme suit :

```
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

L’ajout de la visionneuse à une telle page est similaire aux étapes d’incorporation à taille fixe. La seule différence est que vous devez remplacer le dimensionnement fixe du CSS de la visionneuse par défaut par la taille définie en unités relatives.

1. Ajout du fichier JavaScript de la visionneuse à votre page web.
1. Définition du conteneur `DIV`.
1. Définition de la taille de la visionneuse.
1. Création et initialisation de la visionneuse.

Toutes les étapes ci-dessus sont identiques à celles de l’incorporation d’une taille fixe avec les trois exceptions suivantes :

* ajouter le conteneur `DIV` au &quot;détenteur&quot; existant `DIV` ;
* ajout du paramètre `imagereload` avec des points d’arrêt explicites ;
* au lieu de définir une taille de visionneuse fixe à l’aide d’unités absolues, utilisez une feuille CSS qui définit la largeur et la hauteur de la visionneuse à 100 %, comme dans l’exemple suivant :

```
#s7viewer.s7flyoutviewer { 
 width: 100%; 
 height: 100%; 
}
```

Le code suivant est un exemple complet. Notez comment la taille de la visionneuse change lorsque le navigateur est redimensionné et comment le rapport d’aspect de la visionneuse correspond à la ressource.

```
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

La page d’exemples suivante illustre d’autres utilisations réelles de l’incorporation en responsive design avec une hauteur illimitée :

[Démonstrations en direct](https://landing.adobe.com/en/na/dynamic-media/ctir-2755/live-demos.html)

[Autre emplacement de démonstration](https://experienceleague.adobe.com/tools/vlist/vlist.html)

## Intégration flexible de taille avec définition de largeur et de hauteur {#section-0a329016f9414d199039776645c693de}

Dans le cas d’une incorporation à taille flexible avec des valeurs de largeur et de hauteur définies, le style de la page web est différent. Il fournit les deux tailles à la balise `"holder"` DIV et le centre dans la fenêtre du navigateur. En outre, la page web définit la taille de l’élément `HTML` et `BODY` sur 100 %.

```
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

Les autres étapes d’incorporation sont identiques aux étapes utilisées pour l’incorporation en responsive design avec une hauteur illimitée. L’exemple qui en résulte est le suivant :

```
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

## Incorporation à l’aide d’une API basée sur Setter {#section-af26f0cc2e5140e8a9bfd0c6a841a6d1}

Au lieu d’utiliser l’initialisation basée sur JSON, il est possible d’utiliser une API basée sur un setter et un constructeur sans args. L’utilisation de ce constructeur d’API ne prend aucun paramètre et les paramètres de configuration sont spécifiés à l’aide des méthodes d’API `setContainerId()`, `setParam()` et `setAsset()`, avec des appels JavaScript distincts.

L’exemple suivant illustre l’utilisation de l’incorporation de tailles fixes avec une API basée sur setter :

```
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
