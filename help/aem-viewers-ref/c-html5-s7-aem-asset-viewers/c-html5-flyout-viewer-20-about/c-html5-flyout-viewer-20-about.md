---
description: La visionneuse Fenêtre déroulante est une visionneuse d’images. Il affiche une image statique avec la version agrandie affichée dans la vue de fenêtre déroulante qu’un utilisateur active. Cette visionneuse fonctionne avec les visionneuses d’images et la navigation s’effectue à l’aide de nuances. Il est conçu pour fonctionner sur les ordinateurs de bureau et les périphériques mobiles.
keywords: réactif
solution: Experience Manager
title: Fenêtre déroulante
feature: Dynamic Media Classic,Viewers,SDK/API,Flyout
role: Developer,Business Practitioner
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '2095'
ht-degree: 0%

---


# Fenêtre déroulante{#flyout}

La visionneuse Fenêtre déroulante est une visionneuse d’images. Il affiche une image statique avec la version agrandie affichée dans la vue de fenêtre déroulante qu’un utilisateur active. Cette visionneuse fonctionne avec les visionneuses d’images et la navigation s’effectue à l’aide de nuances. Il est conçu pour fonctionner sur les ordinateurs de bureau et les périphériques mobiles.

>[!NOTE]
>
>Cette visionneuse ne prend pas en charge les images qui utilisent la fonction IR (Image Rendering) ou UGC (User-Generated Content).

Le type de lecteur est 504.

Voir [Configuration système requise et configuration requise](../../c-system-requirements-and-prerequisites.md#concept-9282e5b777de42cdaf72ef7ebd646842).

## URL de la démonstration {#section-e1c3106f5b3e445d9b95be337c2f94e2}

[https://s7d9.scene7.com/s7viewers/html5/FlyoutViewer.html?asset=Scene7SharedAssets/ImageSet-Views-Sample](https://s7d9.scene7.com/s7viewers/html5/FlyoutViewer.html?asset=Scene7SharedAssets/ImageSet-Views-Sample)

## Utilisation de la visionneuse Fenêtre déroulante {#section-f21ac23d3f6449ad9765588d69584772}

Flyout Viewer représente un fichier JavaScript principal et un ensemble de fichiers d’aide (un seul fichier JavaScript inclut tous les composants du SDK de la visionneuse utilisés par cette visionneuse, ressources, CSS) téléchargés par la visionneuse au moment de l’exécution.

La visionneuse Fenêtre déroulante n’est destinée qu’à une utilisation incorporée, ce qui signifie qu’elle est intégrée à la page Web à l’aide d’une API documentée. Aucune page Web prête pour la production n’est disponible pour la visionneuse Fenêtre déroulante.

La configuration et l’habillage sont similaires à ceux des autres visionneuses. Vous pouvez utiliser une page CSS personnalisée pour appliquer l’habillage.

Voir [Référence de commande commune à toutes les visionneuses - Attributs de configuration](../../r-html5-viewer-20-cmdref-configattrib/r-html5-viewer-20-cmdref-configattrib.md#concept-850e0f2c49b949deb7cfbfd330d329bd) et [Référence de commande commune à toutes les visionneuses - URL](../../c-html5-viewer-20-cmdref-url/c-html5-viewer-20-cmdref-url.md#concept-9b337f349b7b406b8c33c7ee96b3e226)

## Interaction avec la visionneuse Fenêtre déroulante {#section-ab66eb6955aa4a8aa6d14a3b3acfed3f}

Flyout Viewer prend en charge les mouvements tactiles simples et multipoints courants dans d’autres applications mobiles.

<table id="table_ED747CC7178448919C34A4FCD18922D0"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>Mouvement </p> </th> 
   <th colname="col2" class="entry"> <p>Description </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>Touche unique </p> </td> 
   <td colname="col2"> <p> Active la vue de la fenêtre déroulante ou les modifications entre le niveau de zoom Principal et le niveau de zoom secondaire. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Glissement ou clic horizontal </p> </td> 
   <td colname="col2"> <p> Fait défiler la liste des nuances dans la barre d’échantillons. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Glissement vertical </p> </td> 
   <td colname="col2"> <p>Si le mouvement est effectué dans la zone des échantillons, il effectue un défilement de page natif. </p> </td> 
  </tr> 
 </tbody> 
</table>

Le lecteur prend également en charge les entrées tactiles et de souris sur les périphériques Windows dotés d’un écran tactile et d’une souris. Toutefois, cette prise en charge est limitée aux navigateurs Web Chrome, Internet Explorer 11 et Edge uniquement.

Cette visionneuse est entièrement accessible au clavier.

Voir [Accessibilité du clavier et navigation](../../c-keyboard-accessibility.md#topic-f5650e9493404e55a3627c8d1366b861).

## Incorporation de la visionneuse déroulante {#section-6bb5d3c502544ad18a58eafe12a13435}

Différentes pages Web ont des besoins différents en ce qui concerne le comportement des visiteurs. La page Web peut avoir une mise en page statique ou utiliser une conception adaptée qui s’affiche différemment sur différents périphériques ou pour différentes tailles de fenêtre de navigateur. Pour répondre à ces besoins, le lecteur prend en charge deux modes de fonctionnement Principaux : incorporation de taille fixe et incorporation de conception adaptée.

Le mode d’incorporation de taille fixe est utilisé lorsque la visionneuse ne change pas de taille après son chargement initial. Ce choix est préférable pour les pages Web dont la mise en page est statique.

Le mode d’incorporation de la conception réactive suppose que la visionneuse doit peut-être être redimensionnée au moment de l’exécution en réponse au changement de taille de son conteneur `DIV`. Le cas d’utilisation le plus courant consiste à ajouter une visionneuse à une page Web qui utilise une disposition de page souple.

Lors de l’utilisation du mode d’incorporation de la conception adaptée avec la visionneuse Fenêtre déroulante, veillez à spécifier des points d’arrêt explicites pour l’image de la vue principale à l’aide du paramètre `imagereload`. Idéalement, faites correspondre vos points d’arrêt avec les points d’arrêt de la largeur de la visionneuse, comme l’indique le CSS de la page Web.

En mode d’incorporation de conceptions réactives, le lecteur se comporte différemment selon la manière dont une page Web dimensionne son conteneur `DIV`. Si la page Web définit uniquement la largeur du conteneur `DIV`, en ne limitant pas sa hauteur, le lecteur sélectionne automatiquement sa hauteur en fonction des proportions du fichier utilisé. Cela signifie que l&#39;actif s&#39;intègre parfaitement dans la vue sans remplissage sur les côtés. Ce cas d’utilisation particulier est le plus courant pour les pages Web qui utilisent des structures de mise en page réactives telles que Bootstrap, Foundation, etc.

Dans le cas contraire, si la page Web définit à la fois la largeur et la hauteur du conteneur du lecteur `DIV`, celui-ci ne remplit que cette zone et suit la taille indiquée par la mise en page Web. L’incorporation de la visionneuse dans une incrustation modale constitue un bon exemple de cas d’utilisation : elle est dimensionnée en fonction de la taille de la fenêtre du navigateur Web.

**Incorporation de taille fixe**

Pour ajouter la visionneuse à une page Web, procédez comme suit :

1. Ajouter le fichier JavaScript de la visionneuse sur votre page Web.
1. Définition du conteneur `DIV`.
1. Définition de la taille de la visionneuse.
1. Création et initialisation de la visionneuse.

1. Ajouter le fichier JavaScript de la visionneuse sur votre page Web.

   Pour créer une visionneuse, vous devez ajouter une balise de script dans l’en-tête HTML. Avant de pouvoir utiliser l’API du lecteur de contenu, veillez à inclure `FlyoutViewer.js`. `FlyoutViewer.js` se trouve dans le  [!DNL html5/js/] sous-dossier suivant de votre déploiement des visionneuses IS standard :

[!DNL <s7viewers_root>/html5/js/FlyoutViewer.js]

Vous pouvez utiliser un chemin relatif si le lecteur est déployé sur l’un des serveurs Dynamic Media d’Adobe et qu’il est diffusé à partir du même domaine. Sinon, vous spécifiez un chemin d’accès complet à l’un des serveurs Dynamic Media d’Adobe sur lesquels les visionneuses IS sont installées.

Un chemin relatif ressemble à ce qui suit :

```
<script language="javascript" type="text/javascript" src="/s7viewers/html5/js/FlyoutViewer.js"></script>
```

>[!NOTE]
>
>Vous ne devez référencer que le fichier JavaScript du lecteur principal `include` sur votre page. Vous ne devez pas référencer de fichiers JavaScript supplémentaires dans le code de la page Web qui pourraient être téléchargés selon la logique du lecteur au moment de l’exécution. En particulier, ne référencez pas directement la bibliothèque HTML5 SDK `Utils.js` chargée par la visionneuse à partir du chemin de contexte `/s7viewers` (appelé SDK consolidé `include`). La raison en est que l’emplacement des bibliothèques de lecteurs de contenu d’exécution `Utils.js` ou similaires est entièrement géré par la logique du lecteur et que l’emplacement change entre les versions du lecteur. Adobe ne conserve pas les anciennes versions du lecteur secondaire `includes` sur le serveur.
>
>
>Par conséquent, le fait de placer une référence directe à tout script JavaScript secondaire `include` utilisé par le lecteur sur la page rompt la fonctionnalité du lecteur à l’avenir lorsqu’une nouvelle version du produit est déployée.

1. Définition de la balise DIV de conteneur.

   Ajoutez un élément DIV vide sur la page où doit apparaître le lecteur de contenu. L’identifiant de l’élément DIV doit être défini, car il est transmis ultérieurement à l’API du lecteur de contenu.

   L’espace réservé DIV est un élément positionné, ce qui signifie que la propriété CSS `position` est définie sur `relative` ou `absolute`.

   Il appartient à la page Web de spécifier le `z-index` approprié pour l’élément DIV d’espace réservé. Ainsi, la partie Fenêtre déroulante du lecteur s’affiche au-dessus des autres éléments de la page Web.

   Voici un exemple d’élément DIV d’espace réservé défini :

   ```
   <div id="s7viewer" style="position:relative;z-index:1"></div> 
   ```

1. Définition de la taille de la visionneuse.

   Cette visionneuse affiche des miniatures lorsque vous travaillez avec des jeux d’éléments multiples. Sur les systèmes de bureau, les miniatures sont placées sous la vue principale. En même temps, le lecteur permet la permutation de la ressource principale lors de l’exécution à l’aide de l’API `setAsset()`. En tant que développeur, vous contrôlez la manière dont le lecteur gère la zone des miniatures dans la partie inférieure lorsque la nouvelle ressource ne comporte qu’un seul élément. Il est possible de garder intacte la taille de la visionneuse extérieure et de laisser la vue principale augmenter sa hauteur et occuper la zone des vignettes. Vous pouvez également maintenir la taille de la vue principale statique et réduire la zone extérieure du lecteur de contenu, ce qui permet au contenu de la page Web de se déplacer vers le haut, puis d’utiliser l’espace de la page libre qui reste des miniatures.

   Pour que les limites extérieures de la visionneuse restent intactes, définissez la taille de la classe CSS de niveau supérieur `.s7flyoutviewer` en unités absolues. Le dimensionnement en CSS peut être placé directement sur la page HTML ou dans un fichier CSS de visionneuse personnalisée, qui est ultérieurement affecté à un enregistrement de paramètre prédéfini de visionneuse dans Dynamic Media Classic, ou transmis explicitement à l’aide de la commande de style.

   Voir [Personnalisation de la visionneuse Fenêtre déroulante](../../c-html5-s7-aem-asset-viewers/c-html5-flyout-viewer-20-about/c-html5-flyout-viewer-20-customizingviewer/c-html5-flyout-viewer-20-customizingviewer.md#concept-82f8c71adbe54680a0c2f83f81e5f451) pour plus d’informations sur le style de la visionneuse avec CSS.

   Voici un exemple de définition de la taille de la visionneuse externe statique dans une page HTML :

   ```
   #s7viewer.s7flyoutviewer { 
    width: 640px; 
    height: 480px; 
   }
   ```

   Vous pouvez voir le comportement avec une zone de visionneuse externe fixe sur l’exemple de page suivant. Notez que lorsque vous passez d’un jeu à l’autre, la taille de la visionneuse externe ne change pas :

   [https://marketing.adobe.com/resources/help/en_US/s7/viewers_ref/samples/FlyoutViewer-fixed-outer-area.html](https://marketing.adobe.com/resources/help/en_US/s7/viewers_ref/samples/FlyoutViewer-fixed-outer-area.html)

   Pour rendre statiques les dimensions de la vue principale, définissez la taille de la visionneuse en unités absolues pour le composant SDK interne `Container` à l’aide du sélecteur CSS `.s7flyoutviewer .s7container`. En outre, vous devez remplacer la taille fixe définie pour la classe CSS de niveau supérieur `.s7flyoutviewer` dans le fichier CSS de visionneuse par défaut en la définissant sur `auto`.

   Voici un exemple de définition de la taille de la visionneuse pour le composant SDK interne `Container` de sorte que la zone de vue principale ne change pas sa taille lors du changement de fichier :

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

   L’exemple de page suivant montre le comportement de la visionneuse avec une taille de vue principale fixe. Notez que lorsque vous passez d’un jeu à l’autre, la vue principale reste statique et le contenu de la page Web se déplace verticalement :

   [https://marketing.adobe.com/resources/help/en_US/s7/viewers_ref/samples/FlyoutViewer-fixed-main-view.html](https://marketing.adobe.com/resources/help/en_US/s7/viewers_ref/samples/FlyoutViewer-fixed-main-view.html)

   Notez également que le fichier CSS de la visionneuse par défaut fournit une taille fixe pour sa zone externe prête à l’emploi.

1. Création et initialisation de la visionneuse.

   Une fois les étapes ci-dessus terminées, vous créez une instance de classe `s7viewers.FlyoutViewer`, vous transmettez toutes les informations de configuration à son constructeur et vous appelez la méthode `init()` sur une instance de lecteur. Les informations de configuration sont transmises au constructeur sous la forme d’un objet JSON. Au minimum, cet objet doit avoir le champ `containerId` qui contient le nom de l’ID de conteneur de la visionneuse et l’objet JSON imbriqué `params` avec les paramètres de configuration pris en charge par la visionneuse. Dans ce cas, l’objet `params` doit avoir au moins la propriété Image Serving URL transmise en tant que propriété `serverUrl` et la ressource initiale en tant que paramètre `asset`. L’API d’initialisation basée sur JSON vous permet de créer et de début le lecteur avec une seule ligne de code.

   Il est important que le conteneur de la visionneuse soit ajouté au modèle DOM afin que le code de la visionneuse puisse trouver l’élément de conteneur en fonction de son identifiant. Certains navigateurs retardent la création du modèle DOM jusqu’à la fin de la page Web. Pour une compatibilité maximale, appelez la méthode `init()` juste avant la balise de fermeture `BODY` ou sur le événement body `onload()`.

   Dans le même temps, l’élément conteneur ne doit pas nécessairement faire partie de la mise en page de la page Web pour le moment. Par exemple, il peut être masqué à l’aide du style `display:none` qui lui est affecté. Dans ce cas, le lecteur retarde son processus d’initialisation jusqu’au moment où la page Web ramène l’élément de conteneur à la mise en page. Dans ce cas, le chargement du lecteur reprend automatiquement.

   Voici un exemple de création d’une instance de visionneuse, de transmission des options de configuration minimales nécessaires au constructeur et d’appel de la méthode `init()`. L’exemple suppose que `flyoutViewer` correspond à l’instance de visionneuse ; `s7viewer` est le nom de l&#39;espace réservé `DIV`; `http://s7d1.scene7.com/is/image/` correspond à l’URL de diffusion d’images ; et `Scene7SharedAssets/ImageSet-Views-Sample` est l’actif :

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

   Le code suivant est un exemple complet d’une page Web triviale qui incorpore la visionneuse Fenêtre déroulante avec une taille fixe :

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

## Incorporation de conception réactive avec une hauteur sans restriction {#section-056cb574713c4d07be6d07cf3c598839}

Avec l’incorporation de conceptions réactives, la page Web dispose normalement d’une sorte de disposition souple qui détermine la taille d’exécution du conteneur `DIV` du lecteur. Pour l’exemple suivant, supposons que la page Web permette au conteneur `DIV` du lecteur de prendre 40 % de la taille de la fenêtre du navigateur Web, en laissant sa hauteur libre. Le code HTML de la page Web se présenterait comme suit :

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

Ajouter le lecteur à une telle page est similaire à la procédure d’incorporation de taille fixe. La seule différence réside dans le fait que vous devez remplacer la taille fixe du CSS de la visionneuse par défaut par la taille définie en unités relatives.

1. Ajouter le fichier JavaScript de la visionneuse sur votre page Web.
1. Définition du conteneur `DIV`.
1. Définition de la taille de la visionneuse.
1. Création et initialisation de la visionneuse.

Toutes les étapes ci-dessus sont identiques à celles de la taille fixe incorporée avec les trois exceptions suivantes :

* ajouter le conteneur `DIV` au &quot;titulaire&quot; `DIV` existant ;
* ajout du paramètre `imagereload` avec des points d&#39;arrêt explicites ;
* au lieu de définir une taille de visionneuse fixe à l’aide d’unités absolues, utilisez un fichier CSS qui définit la largeur et la hauteur de la visionneuse à 100 %, comme dans l’exemple suivant :

```
#s7viewer.s7flyoutviewer { 
 width: 100%; 
 height: 100%; 
}
```

Le code suivant est un exemple complet. Notez comment la taille de la visionneuse change lorsque le navigateur est redimensionné et comment les proportions de la visionneuse correspondent à la ressource.

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

La page d’exemples suivante illustre d’autres utilisations réelles de l’incorporation de conceptions réactives avec une hauteur libre :

[Démonstrations en direct](https://landing.adobe.com/en/na/dynamic-media/ctir-2755/live-demos.html)

<!-- KEEP (https://marketing.adobe.com/resources/help/en_US/s7/vlist/vlist.html) -->

## Taille flexible incorporée avec largeur et hauteur définies {#section-0a329016f9414d199039776645c693de}

Dans le cas d’une incorporation de taille flexible avec des valeurs de largeur et de hauteur définies, le style de la page Web est différent. Il fournit les deux tailles à la balise `"holder"` DIV et le centre dans la fenêtre du navigateur. En outre, la page Web définit la taille des éléments `HTML` et `BODY` sur 100 %.

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

Le reste des étapes d&#39;incorporation est identique aux étapes utilisées pour l&#39;incorporation de conceptions réactives avec une hauteur libre. L’exemple qui en résulte est le suivant :

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

## Incorporation à l’aide de l’API basée sur Setter {#section-af26f0cc2e5140e8a9bfd0c6a841a6d1}

Au lieu d’utiliser l’initialisation basée sur JSON, il est possible d’utiliser une API basée sur un setter et un constructeur sans args. L&#39;utilisation de ce constructeur d&#39;API ne prend aucun paramètre et les paramètres de configuration sont spécifiés à l&#39;aide des méthodes d&#39;API `setContainerId()`, `setParam()` et `setAsset()`, avec des appels JavaScript distincts.

L’exemple suivant illustre l’utilisation de l’incorporation de tailles fixes avec l’API basée sur un setter :

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

