---
description: La visionneuse Fenêtre déroulante est une visionneuse d’images. Il affiche une image statique avec la version agrandie affichée dans le de fenêtre déroulante  qu’un utilisateur active. Cette visionneuse fonctionne avec des visionneuses d’images et la navigation s’effectue à l’aide de nuances. Il est conçu pour fonctionner sur les ordinateurs de bureau et les périphériques mobiles.
keywords: responsive
seo-description: La visionneuse Fenêtre déroulante est une visionneuse d’images. Il affiche une image statique avec la version agrandie affichée dans le de fenêtre déroulante  qu’un utilisateur active. Cette visionneuse fonctionne avec des visionneuses d’images et la navigation s’effectue à l’aide de nuances. Il est conçu pour fonctionner sur les ordinateurs de bureau et les périphériques mobiles.
seo-title: Fenêtre déroulante
solution: Experience Manager
title: Fenêtre déroulante
topic: Dynamic media
uuid: 588e1baa-4165-4aec-8fbe-1a916c0f409f
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# Fenêtre déroulante{#flyout}

La visionneuse Fenêtre déroulante est une visionneuse d’images. Il affiche une image statique avec la version agrandie affichée dans le de fenêtre déroulante  qu’un utilisateur active. Cette visionneuse fonctionne avec des visionneuses d’images et la navigation s’effectue à l’aide de nuances. Il est conçu pour fonctionner sur les ordinateurs de bureau et les périphériques mobiles.

>[!NOTE]
>
>Les images qui utilisent la fonction IR (Image Rendering) ou UGC (User-Generated Content) ne sont pas prises en charge par cette visionneuse.

Le type de lecteur est 504.

Voir Configuration [système requise et configuration requise](../../c-system-requirements-and-prerequisites.md#concept-9282e5b777de42cdaf72ef7ebd646842).

## URL de démonstration {#section-e1c3106f5b3e445d9b95be337c2f94e2}

[https://s7d9.scene7.com/s7viewers/html5/FlyoutViewer.html?asset=Scene7SharedAssets/ImageSet-Views-Sample](https://s7d9.scene7.com/s7viewers/html5/FlyoutViewer.html?asset=Scene7SharedAssets/ImageSet-Views-Sample)

## Utilisation de la visionneuse Fenêtre déroulante {#section-f21ac23d3f6449ad9765588d69584772}

La visionneuse Fenêtre déroulante représente un fichier JavaScript principal et un ensemble de fichiers d’aide (un seul fichier JavaScript inclut tous les composants du SDK de la visionneuse utilisés par cette visionneuse, ressources, CSS) téléchargés par la visionneuse au moment de l’exécution.

La visionneuse Fenêtre déroulante est uniquement destinée à une utilisation incorporée, ce qui signifie qu’elle est intégrée dans la page Web à l’aide d’une API documentée. Aucune page Web prête pour la production n’est disponible pour la visionneuse Fenêtre déroulante.

La configuration et l’habillage sont similaires à ceux des autres visionneuses. Vous pouvez utiliser une page CSS personnalisée pour appliquer l’habillage.

Voir Référence [de commande commune à toutes les visionneuses - Attributs](../../r-html5-viewer-20-cmdref-configattrib/r-html5-viewer-20-cmdref-configattrib.md#concept-850e0f2c49b949deb7cfbfd330d329bd) de configuration et référence de [commande commune à toutes les visionneuses - URL](../../c-html5-viewer-20-cmdref-url/c-html5-viewer-20-cmdref-url.md#concept-9b337f349b7b406b8c33c7ee96b3e226)

## Interaction avec la visionneuse déroulante {#section-ab66eb6955aa4a8aa6d14a3b3acfed3f}

Le lecteur de fenêtre déroulante prend en charge les mouvements tactiles simples et multipoints courants dans d’autres applications mobiles.

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
   <td colname="col2"> <p> Active le  de la fenêtre déroulante ou modifie le niveau de zoom principal et secondaire. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Glissement ou clic horizontal </p> </td> 
   <td colname="col2"> <p> Fait défiler le  des échantillons dans la barre d’échantillons. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Glissement vertical </p> </td> 
   <td colname="col2"> <p>Si le mouvement est effectué dans la zone des échantillons, il effectue un défilement de page natif. </p> </td> 
  </tr> 
 </tbody> 
</table>

Le lecteur prend également en charge la saisie tactile et la saisie de la souris sur les périphériques Windows dotés d’un écran tactile et d’une souris. Cette prise en charge est toutefois limitée aux navigateurs Web Chrome, Internet Explorer 11 et Edge.

Cette visionneuse est entièrement accessible au clavier.

Voir Accessibilité [du clavier et navigation](../../c-keyboard-accessibility.md#topic-f5650e9493404e55a3627c8d1366b861).

## Incorporation de la visionneuse déroulante {#section-6bb5d3c502544ad18a58eafe12a13435}

Le comportement des visiteurs varie selon les pages Web. La page Web peut avoir une mise en page statique ou utiliser une conception adaptée qui s’affiche différemment sur différents périphériques ou pour différentes tailles de fenêtre de navigateur. Pour répondre à ces besoins, le lecteur prend en charge deux modes de fonctionnement principaux : incorporation de taille fixe et incorporation de conception adaptée.

Le mode d’incorporation de taille fixe est utilisé lorsque la visionneuse ne modifie pas sa taille après son chargement initial. Ce choix est préférable pour les pages Web qui ont une mise en page statique.

Le mode d’incorporation de conception réactive suppose que le lecteur doit peut-être redimensionner au cours de l’exécution en réponse au changement de taille de sa  de `DIV`. Le cas d’utilisation le plus courant consiste à ajouter une visionneuse à une page Web qui utilise une disposition de page souple.

Lors de l’utilisation du mode d’incorporation de conception réactive avec la visionneuse Fenêtre déroulante, veillez à spécifier des points d’arrêt explicites pour l’image  principale à l’aide du `imagereload` paramètre. Dans l’idéal, faites correspondre vos points d’arrêt aux points d’arrêt de la largeur de la visionneuse, comme le dicte le CSS de la page Web.

En mode d’incorporation de conception réactive, le lecteur se comporte différemment selon la manière dont une page Web redimensionne son  `DIV`. Si la page Web définit uniquement la largeur de la  du `DIV`, en laissant sa hauteur libre, le lecteur choisit automatiquement sa hauteur en fonction des proportions de la ressource utilisée. Cela signifie que le fichier s’intègre parfaitement dans le  sans remplissage sur les côtés. Ce cas d’utilisation particulier est le plus courant pour les pages Web qui utilisent des structures de mise en page réactives telles que Bootstrap, Foundation, etc.

Dans le cas contraire, si la page Web définit à la fois la largeur et la hauteur du  du lecteur de contenu `DIV`, celui-ci remplit uniquement cette zone et suit la taille fournie par la mise en page de la page Web. Un bon exemple d’utilisation est l’incorporation de la visionneuse dans une incrustation modale, où l’incrustation est dimensionnée en fonction de la taille de la fenêtre du navigateur Web.

**Incorporation de taille fixe**

Vous ajoutez le lecteur à une page Web en procédant comme suit :

1. Ajout du fichier JavaScript de la visionneuse à votre page Web.
1. Définition du  de `DIV`.
1. Définition de la taille de la visionneuse.
1. Création et initialisation de la visionneuse.

1. Ajout du fichier JavaScript de la visionneuse à votre page Web.

   Pour créer une visionneuse, vous devez ajouter une balise de script dans l’en-tête HTML. Avant d’utiliser l’API du lecteur de contenu, veillez à inclure `FlyoutViewer.js`. `FlyoutViewer.js` se trouve dans le [!DNL html5/js/] sous-dossier suivant de votre déploiement des visionneuses IS standard :

[!DNL <s7viewers_root>/html5/js/FlyoutViewer.js]

Vous pouvez utiliser un chemin relatif si la visionneuse est déployée sur l’un des serveurs Adobe Scene7 et qu’elle est diffusée à partir du même domaine. Dans le cas contraire, vous spécifiez un chemin d’accès complet à l’un des serveurs Adobe Scene7 sur lesquels les visionneuses IS sont installées.

Un chemin relatif se présente comme suit :

```
<script language="javascript" type="text/javascript" src="/s7viewers/html5/js/FlyoutViewer.js"></script>
```

>[!NOTE]
>
>Vous ne devez référencer que le fichier JavaScript du lecteur principal `include` sur votre page. Vous ne devez pas référencer de fichiers JavaScript supplémentaires dans le code de la page Web qui pourraient être téléchargés par la logique du lecteur au moment de l’exécution. En particulier, ne référencez pas directement la `Utils.js` bibliothèque du SDK HTML5 chargée par le lecteur à partir du chemin `/s7viewers` contextuel (appelé SDK consolidé `include`). La raison en est que l’emplacement des bibliothèques de lecteurs de contenu d’exécution `Utils.js` ou similaires est entièrement géré par la logique du lecteur et que l’emplacement change entre les versions du lecteur. Adobe ne conserve pas les anciennes versions du lecteur secondaire `includes` sur le serveur.
>
>
>Par conséquent, le fait de placer une référence directe à tout code JavaScript secondaire `include` utilisé par le lecteur sur la page rompt la fonctionnalité du lecteur à l’avenir lorsqu’une nouvelle version de produit est déployée.

1. Définition de la  DIV du.

   Ajouter un élément DIV vide sur la page où le lecteur doit apparaître. L’ID de l’élément DIV doit être défini, car cet ID est transmis ultérieurement à l’API du lecteur de contenu.

   L’espace réservé DIV est un élément positionné, ce qui signifie que la propriété `position` CSS est définie sur `relative` ou `absolute`.

   Il est de la responsabilité de la page Web de spécifier la valeur appropriée `z-index` pour l’élément DIV d’espace réservé. Cela permet de s’assurer que la partie Fenêtre déroulante du lecteur s’affiche au-dessus des autres éléments de la page Web.

   Voici un exemple d’élément DIV d’espace réservé défini :

   ```
   <div id="s7viewer" style="position:relative;z-index:1"></div> 
   ```

1. Définition de la taille de la visionneuse.

   Cette visionneuse affiche des miniatures lorsque vous travaillez avec des jeux d’éléments multiples. Sur les systèmes de bureau, les miniatures sont placées sous le  principal du. En même temps, le lecteur permet la permutation de la ressource principale pendant l’exécution à l’aide de `setAsset()` l’API. En tant que développeur, vous contrôlez la manière dont le lecteur gère la zone des miniatures dans la zone inférieure lorsque le nouvel élément ne comporte qu’un seul élément. Il est possible de conserver la taille de la visionneuse extérieure et de laisser le principal augmenter sa hauteur et occuper la zone des vignettes. Vous pouvez également conserver la taille du principal statique et réduire la zone extérieure du lecteur de contenu, ce qui permet au contenu de la page Web de se déplacer vers le haut, puis d’utiliser l’espace de page libre laissé par les vignettes.

   Pour que les limites extérieures de la visionneuse restent intactes, définissez la taille de la classe CSS de `.s7flyoutviewer` niveau supérieur en unités absolues. Le dimensionnement en CSS peut être placé directement sur la page HTML ou dans un fichier CSS de visionneuse personnalisé, qui est ultérieurement affecté à un enregistrement de paramètre prédéfini de visionneuse dans Scene7 Publishing System, ou transmis explicitement à l’aide de la commande de style.

   Voir [Personnalisation de la visionneuse](../../c-html5-s7-aem-asset-viewers/c-html5-flyout-viewer-20-about/c-html5-flyout-viewer-20-customizingviewer/c-html5-flyout-viewer-20-customizingviewer.md#concept-82f8c71adbe54680a0c2f83f81e5f451) Fenêtre déroulante pour plus d’informations sur le style de la visionneuse avec CSS.

   Voici un exemple de définition de la taille statique de la visionneuse externe dans une page HTML :

   ```
   #s7viewer.s7flyoutviewer { 
    width: 640px; 
    height: 480px; 
   }
   ```

   Vous pouvez voir le comportement d’une zone extérieure de visionneuse fixe sur l’exemple de page suivant. Notez que lorsque vous passez d’un jeu à l’autre, la taille de la visionneuse extérieure ne change pas :

   [https://marketing.adobe.com/resources/help/en_US/s7/viewers_ref/samples/FlyoutViewer-fixed-outer-area.html](https://marketing.adobe.com/resources/help/en_US/s7/viewers_ref/samples/FlyoutViewer-fixed-outer-area.html)

   Pour rendre statiques les dimensions  principal du, définissez la taille de la visionneuse en unités absolues pour le composant `Container` SDK interne à l’aide du sélecteur `.s7flyoutviewer .s7container` CSS. En outre, vous devez remplacer la taille fixe définie pour la classe CSS de `.s7flyoutviewer` niveau supérieur dans le fichier CSS de visionneuse par défaut, en le définissant sur `auto`.

   Voici un exemple de définition de la taille de la visionneuse pour le composant `Container` SDK interne afin que la zone de  principale ne change pas sa taille lors du changement de fichier :

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

   L’exemple de page suivant illustre le comportement de la visionneuse avec une taille de  principale fixe. Notez que lorsque vous passez d’un jeu à l’autre, le  principal reste statique et le contenu de la page Web se déplace verticalement :

   [https://marketing.adobe.com/resources/help/en_US/s7/viewers_ref/samples/FlyoutViewer-fixed-main-view.html](https://marketing.adobe.com/resources/help/en_US/s7/viewers_ref/samples/FlyoutViewer-fixed-main-view.html)

   Notez également que le fichier CSS de la visionneuse par défaut fournit une taille fixe pour sa zone extérieure prête à l’emploi.

1. Création et initialisation de la visionneuse.

   Une fois les étapes ci-dessus terminées, vous créez une instance de `s7viewers.FlyoutViewer` classe, vous transmettez toutes les informations de configuration à son constructeur et vous appelez `init()` la méthode sur une instance de visionneuse. Les informations de configuration sont transmises au constructeur sous forme d’objet JSON. Au minimum, cet objet doit avoir le `containerId` champ qui contient le nom de l’ID de de la visionneuse et l’objet `params` JSON imbriqué avec les paramètres de configuration pris en charge par la visionneuse. Dans ce cas, l’ `params` objet doit comporter au moins l’URL de diffusion d’images transmise en tant que `serverUrl` propriété et le fichier initial en tant que `asset` paramètre. L’API d’initialisation basée sur JSON vous permet de créer et de  le lecteur avec une seule ligne de code.

   Il est important que le de la visionneuse soit ajouté au modèle DOM afin que le code de la visionneuse puisse trouver l’élément  par son identifiant. Certains navigateurs retardent la création du modèle DOM jusqu’à la fin de la page Web. Pour une compatibilité maximale, appelez la `init()` méthode juste avant la `BODY` balise de fermeture ou sur le  du corps `onload()` .

   En même temps, l’élément  du ne doit pas nécessairement faire partie de la mise en page de la page Web pour le moment. Par exemple, il peut être masqué à l’aide du `display:none` style qui lui est affecté. Dans ce cas, le lecteur de contenu retarde son processus d’initialisation jusqu’au moment où la page Web ramène l’élément  du à la mise en page. Dans ce cas, le chargement du lecteur reprend automatiquement.

   Voici un exemple de création d’une instance de visionneuse, de transmission des options de configuration minimales nécessaires au constructeur et d’appel de la `init()` méthode. L’exemple suppose `flyoutViewer` qu’il s’agit de l’instance de visionneuse ; `s7viewer` est le nom de l’espace réservé `DIV`; `http://s7d1.scene7.com/is/image/` est l’URL de diffusion d’images ; et `Scene7SharedAssets/ImageSet-Views-Sample` est l’actif :

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

## Incorporation de conception réactive avec une hauteur libre {#section-056cb574713c4d07be6d07cf3c598839}

Avec l’incorporation de conceptions réactives, la page Web dispose normalement d’une sorte de disposition souple qui détermine la taille d’exécution du  du lecteur `DIV`. Dans l’exemple suivant, supposons que la page Web permette au du lecteur de  prendre 40 % de la taille de la fenêtre du navigateur Web, en laissant sa hauteur libre. `DIV` Le code HTML de la page Web se présente comme suit :

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

L’ajout de la visionneuse à une telle page est similaire à la procédure d’incorporation de taille fixe. La seule différence est que vous devez remplacer le dimensionnement fixe du fichier CSS de la visionneuse par défaut par la taille définie en unités relatives.

1. Ajout du fichier JavaScript de la visionneuse à votre page Web.
1. Définition du  de `DIV`.
1. Définition de la taille de la visionneuse.
1. Création et initialisation de la visionneuse.

Toutes les étapes ci-dessus sont identiques à celles de la taille fixe incorporée avec les trois exceptions suivantes :

* ajouter le  `DIV` au &quot;titulaire&quot; existant `DIV`;
* ajout `imagereload` d’un paramètre avec des points d’arrêt explicites ;
* au lieu de définir une taille fixe de visionneuse à l’aide d’unités absolues, utilisez un fichier CSS qui définit la largeur et la hauteur de la visionneuse sur 100 %, comme dans l’exemple suivant :

```
#s7viewer.s7flyoutviewer { 
 width: 100%; 
 height: 100%; 
}
```

Le code suivant est un exemple complet. Notez la modification de la taille de la visionneuse lorsque le navigateur est redimensionné et la manière dont les proportions de la visionneuse correspondent à la ressource.

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

La page d’exemples suivante illustre d’autres utilisations réelles de la conception adaptée incorporée à une hauteur illimitée :

[https://marketing.adobe.com/resources/help/en_US/s7/vlist/vlist.html](https://marketing.adobe.com/resources/help/en_US/s7/vlist/vlist.html)

## Incorporation flexible de taille avec définition de la largeur et de la hauteur {#section-0a329016f9414d199039776645c693de}

Dans le cas d’une incorporation de taille flexible avec une largeur et une hauteur définies, le style de la page Web est différent. Il fournit les deux tailles à la `"holder"` balise DIV et le centre dans la fenêtre du navigateur. En outre, la page Web définit la taille de l’ `HTML` `BODY` élément et de l’élément sur 100 %.

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

Les autres étapes d’incorporation sont identiques aux étapes utilisées pour l’incorporation de conception réactive avec une hauteur libre. L’exemple qui en résulte est le suivant :

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

Au lieu d’utiliser l’initialisation basée sur JSON, il est possible d’utiliser une API basée sur un setter et un constructeur sans args. L’utilisation de ce constructeur d’API ne prend aucun paramètre et les paramètres de configuration sont spécifiés à l’aide des méthodes `setContainerId()`, `setParam()`et `setAsset()` API, avec des appels JavaScript distincts.

L’exemple suivant illustre l’utilisation de l’incorporation de tailles fixes avec l’API basée sur setter :

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

