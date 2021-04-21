---
description: La visionneuse de zoom est une visionneuse d’images qui affiche une image agrandie. Cette visionneuse fonctionne avec les visionneuses d’images et la navigation s’effectue à l’aide de nuances. Il comprend des outils de zoom, une prise en charge en plein écran, des échantillons et un bouton de fermeture en option. Il est conçu pour fonctionner sur les ordinateurs de bureau et les périphériques mobiles.
keywords: réactif
solution: Experience Manager
title: Zoom
feature: Dynamic Media Classic,Viewers,SDK/API,Zoom
role: Developer,Business Practitioner
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '2423'
ht-degree: 0%

---


# Zoom{#zoom}

La visionneuse de zoom est une visionneuse d’images qui affiche une image agrandie. Cette visionneuse fonctionne avec les visionneuses d’images et la navigation s’effectue à l’aide de nuances. Il comprend des outils de zoom, une prise en charge en plein écran, des échantillons et un bouton de fermeture en option. Il est conçu pour fonctionner sur les ordinateurs de bureau et les périphériques mobiles.

>[!NOTE]
>
>Cette visionneuse ne prend pas en charge les images qui utilisent la fonction IR (Image Rendering) ou UGC (User-Generated Content).

Type de visionneuse 502.

Voir [Configuration système requise et configuration requise](../../c-system-requirements-and-prerequisites.md#concept-9282e5b777de42cdaf72ef7ebd646842).

## URL de la démonstration {#section-e1c3106f5b3e445d9b95be337c2f94e2}

[https://s7d9.scene7.com/s7viewers/html5/ZoomViewer.html?asset=Scene7SharedAssets/ImageSet-Views-Sample](https://s7d9.scene7.com/s7viewers/html5/ZoomViewer.html?asset=Scene7SharedAssets/ImageSet-Views-Sample)

## Utilisation de la visionneuse de zoom {#section-e6c68406ecdc4de781df182bbd8088b4}

La visionneuse de zoom représente un fichier JavaScript principal et un ensemble de fichiers d’aide (un seul fichier JavaScript est inclus avec tous les composants du SDK de la visionneuse utilisés par cette visionneuse, ressources et CSS) téléchargés par la visionneuse au moment de l’exécution.

Vous pouvez utiliser la visionneuse de zoom en mode contextuel à l’aide d’une page HTML prête à l’emploi fournie avec les visionneuses IS ou en mode intégré, où elle est intégrée dans la page Web de cible à l’aide d’une API documentée.

La configuration et l’habillage sont similaires à ceux des autres visionneuses. L’habillage est effectué au moyen d’une page CSS personnalisée.

Voir [Référence de commande commune à toutes les visionneuses - Attributs de configuration](../../r-html5-viewer-20-cmdref-configattrib/r-html5-viewer-20-cmdref-configattrib.md#concept-850e0f2c49b949deb7cfbfd330d329bd) et [Référence de commande commune à toutes les visionneuses - URL](../../c-html5-viewer-20-cmdref-url/c-html5-viewer-20-cmdref-url.md#concept-9b337f349b7b406b8c33c7ee96b3e226)

## Interaction avec la visionneuse de zoom {#section-642e66ca38cd4032992840ec6c0b0cd2}

La visionneuse de zoom prend en charge les mouvements tactiles suivants, courants dans d’autres applications mobiles. Lorsque le lecteur ne peut pas traiter le mouvement de glissement de l’utilisateur, il transfère le événement vers le navigateur Web pour effectuer un défilement de page natif. Ce type de fonctionnalité permet à l’utilisateur de parcourir la page même si le lecteur occupe la majeure partie de l’écran du périphérique.

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
   <td colname="col2"> <p> Sélectionne une nouvelle miniature dans les échantillons. Dans la vue principale, il masque ou révèle les éléments de l’interface utilisateur. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Doublon </p> </td> 
   <td colname="col2"> <p> Applique un zoom à un niveau jusqu’à ce que le zoom maximal soit atteint. Le mouvement de pression du doublon suivant réinitialise l’affichage initial de la visionneuse. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Pincer </p> </td> 
   <td colname="col2"> <p>Applique un zoom avant ou arrière. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Glissement ou clic horizontal </p> </td> 
   <td colname="col2"> <p> Fait défiler la liste des nuances dans la barre d’échantillons. </p> <p> Si l’image est à l’état reset et que le paramètre de transition de cadre <span class="codeph"> </span> est défini sur slide, le fichier est modifié avec l’animation de la diapositive. Pour les autres modes de transition de cadre <span class="codeph"> </span>, le mouvement effectue le défilement de page natif. </p> <p> Si l’image est agrandie, elle déplace l’image horizontalement. Si l’image est déplacée vers le bord de la vue et qu’un glissement est effectué dans la même direction, le mouvement effectue le défilement natif de la page. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Glissement vertical </p> </td> 
   <td colname="col2"> <p> Si l’image est à l’état reset, le mouvement effectue le défilement natif de la page. </p> <p> Lorsque l’image est agrandie, elle bouge l’image verticalement. Si l’image est déplacée vers le bord de la vue et qu’un glissement est effectué dans la même direction, le mouvement effectue un défilement de page natif. </p> <p> Si le mouvement est effectué dans la zone des échantillons, il effectue un défilement de page natif. </p> </td> 
  </tr> 
 </tbody> 
</table>

Le lecteur prend en charge les entrées tactiles et de souris sur les périphériques Windows avec un écran tactile et une souris. Toutefois, cette prise en charge est limitée aux navigateurs Web Chrome, Internet Explorer 11 et Edge uniquement.

Cette visionneuse est entièrement accessible au clavier.

Voir [Accessibilité du clavier et navigation](../../c-keyboard-accessibility.md#topic-f5650e9493404e55a3627c8d1366b861).

## Incorporation de la visionneuse de zoom {#section-6bb5d3c502544ad18a58eafe12a13435}

Différentes pages Web ont des besoins différents en ce qui concerne le comportement des visiteurs. Il arrive qu’une page Web fournisse un lien qui, lorsqu’un utilisateur clique dessus, ouvre le lecteur dans une fenêtre de navigateur distincte. Dans d’autres cas, il est nécessaire d’incorporer directement la visionneuse dans la page d’hébergement. Dans ce dernier cas, la page Web peut avoir une mise en page statique ou utiliser une conception adaptée qui s’affiche différemment sur différents périphériques ou pour différentes tailles de fenêtre de navigateur. Pour répondre à ces besoins, le lecteur prend en charge trois modes de fonctionnement Principaux : fenêtre contextuelle, incorporation de tailles fixes et incorporation de conceptions réactives.

**A propos du mode contextuel**

En mode contextuel, le lecteur s’ouvre dans une fenêtre ou un onglet distinct du navigateur Web. Elle prend toute la zone de la fenêtre du navigateur et s’ajuste au cas où le navigateur serait redimensionné ou où l’orientation du périphérique serait modifiée.

Ce mode est le plus courant pour les périphériques mobiles. La page Web charge la visionneuse à l’aide de l’appel JavaScript `window.open()`, d’un élément HTML `A` correctement configuré ou de toute autre méthode appropriée.

Il est recommandé d’utiliser une page HTML prête à l’emploi pour le mode d’opération contextuel. La page HTML prête à l’emploi est appelée `ZoomViewer.html` et se trouve sous le sous-dossier `html5/` de votre déploiement des visionneuses IS standard, comme dans l’exemple suivant :

`<s7viewers_root>/html5/ZoomViewer.html`

Appliquez une page CSS personnalisée pour obtenir une apparence personnalisée pour la page.

Voici un exemple de code HTML qui ouvre la visionneuse dans la nouvelle fenêtre :

```
 <a 
href="http://s7d1.scene7.com/s7viewers/html5/ZoomViewer.html?asset=Scene7SharedAssets/ImageSet-Views-Sample" 
target="_blank">Open popup viewer</a>
```

**A propos du mode d&#39;incorporation de taille fixe et du mode d&#39;incorporation de conception réactif**

En mode incorporé, le lecteur est ajouté à la page Web existante, qui peut déjà contenir du contenu client qui n’est pas lié au lecteur. En règle générale, le lecteur n’occupe qu’une partie de l’espace de la page Web.

Les cas d&#39;utilisation Principaux sont les pages Web orientées vers les ordinateurs de bureau ou les tablettes, ainsi que les pages adaptées qui ajustent automatiquement la mise en page, en fonction du type de périphérique.

L’incorporation de taille fixe est utilisée lorsque la visionneuse ne change pas de taille après le chargement initial. Cette option est le meilleur choix pour les pages Web avec une disposition statique.

Le mode d’incorporation de la conception réactive suppose que le redimensionnement de la visionneuse est nécessaire pendant l’exécution en raison du changement de taille de son conteneur `DIV`. Le cas d’utilisation le plus courant consiste à ajouter une visionneuse à une page Web qui utilise une disposition souple.

En mode d’incorporation de conceptions réactives, le lecteur se comporte différemment selon la manière dont la page Web dimensionne son conteneur `DIV`. Si la page Web ne définit que la largeur du conteneur `DIV`, en ne limitant pas sa hauteur, le lecteur sélectionne automatiquement sa hauteur en fonction des proportions du fichier utilisé. Cette logique permet de s&#39;assurer que la ressource s&#39;intègre parfaitement à la vue sans remplissage sur les côtés. Ce cas d’utilisation est le plus courant pour les pages Web qui utilisent des structures de mise en page réactives telles que Bootstrap, Foundation, etc.

Si la page Web définit à la fois la largeur et la hauteur du conteneur `DIV` du lecteur, celui-ci remplit cette zone et suit la taille fournie par la page Web. Par exemple, l’incorporation de la visionneuse dans une incrustation modale, où l’incrustation est dimensionnée en fonction de la taille de la fenêtre du navigateur Web.

## Incorporation de taille fixe {#section-44f365e6c0dd40709467a459afa82a7f}

Pour ajouter la visionneuse à une page Web, procédez comme suit :

1. Ajouter le fichier JavaScript de la visionneuse sur votre page Web.
1. Définition de la balise DIV de conteneur.
1. Définition de la taille de la visionneuse.
1. Création et initialisation de la visionneuse.

1. Ajouter le fichier JavaScript de la visionneuse sur votre page Web.

   Pour créer une visionneuse, vous devez ajouter une balise de script dans l’en-tête HTML. Avant de pouvoir utiliser l’API du lecteur de contenu, veillez à inclure [!DNL ZoomViewer.js]. Le fichier [!DNL ZoomViewer.js] se trouve sous le sous-dossier [!DNL html5/js/] de votre déploiement des visionneuses IS standard :

[!DNL <s7viewers_root>/html5/js/ZoomViewer.js]

Vous pouvez utiliser un chemin relatif si la visionneuse est déployée sur l’un des serveurs Dynamic Media Classic de l’Adobe et qu’elle est diffusée à partir du même domaine. Sinon, vous spécifiez un chemin d’accès complet à l’un des serveurs Dynamic Media Classic Adobe sur lesquels les visionneuses IS sont installées.

Le chemin relatif ressemble à ce qui suit :

```
<script language="javascript" type="text/javascript" src="/s7viewers/html5/js/ZoomViewer.js"></script>
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

   Voici un exemple d’élément DIV d’espace réservé défini :

   ```
   <div id="s7viewer" style="position:relative"></div>
   ```

1. Définition de la taille de la visionneuse.

   Cette visionneuse affiche des miniatures lorsque vous travaillez avec des jeux d’éléments multiples. Sur les systèmes de bureau, les miniatures sont placées sous la vue principale. En même temps, le lecteur permet la permutation de la ressource principale au moment de l’exécution à l’aide de l’API `setAsset()`. En tant que développeur, vous avez le contrôle sur la manière dont le lecteur gère la zone des vignettes en bas lorsque la nouvelle ressource ne comporte qu’un seul élément. Il est possible de garder intacte la taille de la visionneuse extérieure et de laisser la vue principale augmenter sa hauteur et occuper la zone des vignettes. Vous pouvez également maintenir la taille de la vue principale statique et réduire la zone extérieure du lecteur de contenu, en laissant le contenu de la page Web augmenter et en utilisant les restes d’espace de l’écran libre depuis les miniatures.

   Pour que les limites extérieures de la visionneuse restent intactes, définissez la taille de la classe CSS de niveau supérieur `.s7zoomviewer` en unités absolues. Le dimensionnement en CSS peut être placé directement sur la page HTML ou dans un fichier CSS de visionneuse personnalisée, qui est ultérieurement affecté à un enregistrement de paramètre prédéfini de visionneuse dans Dynamic Media Classic ou transmis explicitement à l’aide d’une commande de style.

   Voir [Personnalisation de la visionneuse de zoom](../../c-html5-s7-aem-asset-viewers/c-html5-20-zoom-viewer-about/c-html5-20-zoom-viewer-customizingviewer/c-html5-20-zoom-viewer-customizingviewer.md#concept-73a8546acdb444a387c49969ceca57d0) pour plus d’informations sur le style de la visionneuse avec CSS.

   Voici un exemple de définition d’une taille de visionneuse externe statique dans une page HTML :

   ```
   #s7viewer.s7zoomviewer { 
    width: 640px; 
    height: 480px; 
   }
   ```

   L’exemple suivant illustre le comportement d’une visionneuse externe fixe. Notez que lorsque vous passez d’un jeu à l’autre, la taille de la visionneuse externe ne change pas :

   [https://marketing.adobe.com/resources/help/en_US/s7/viewers_ref/samples/ZoomViewer-fixed-outer-area.html](https://marketing.adobe.com/resources/help/en_US/s7/viewers_ref/samples/ZoomViewer-fixed-outer-area.html)

   Pour rendre statiques les dimensions de la vue principale, définissez la taille de la visionneuse en unités absolues pour le composant SDK interne `Container` à l’aide du sélecteur CSS `.s7zoomviewer` `.s7container` ou du modificateur `stagesize`.

   Voici un exemple de définition de la taille de la visionneuse pour le composant SDK interne `Container` de sorte que la zone de vue principale ne change pas sa taille lors du changement de fichier :

   ```
   #s7viewer.s7zoomviewer .s7container { 
    width: 640px; 
    height: 480px; 
   }
   ```

   La page de démonstration suivante présente le comportement de la visionneuse avec une taille de vue principale fixe. Notez que lorsque vous passez d’un jeu à l’autre, la vue principale reste statique et le contenu de la page Web se déplace verticalement.

   [https://marketing.adobe.com/resources/help/en_US/s7/viewers_ref/samples/ZoomViewer-fixed-main-view.html](https://marketing.adobe.com/resources/help/en_US/s7/viewers_ref/samples/ZoomViewer-fixed-main-view.html)

   Vous pouvez définir le modificateur `stagesize` dans l’enregistrement de paramètre prédéfini de la visionneuse dans Dynamic Media Classic ou le transmettre explicitement avec le code d’initialisation de la visionneuse avec la collection `params` ou en tant qu’appel d’API comme décrit dans la section Référence de commandes de cette aide, comme dans l’exemple suivant :

   ```
    zoomViewer.setParam("stagesize", 
   "640,480");
   ```

   Une approche CSS est recommandée et est utilisée dans cet exemple.

1. Création et initialisation de la visionneuse.

   Une fois les étapes ci-dessus terminées, vous créez une instance de classe `s7viewers.ZoomViewer`, vous transmettez toutes les informations de configuration à son constructeur et vous appelez la méthode `init()` sur une instance de lecteur.

   Les informations de configuration sont transmises au constructeur sous la forme d’un objet JSON. Au minimum, cet objet doit comporter un champ `containerId` contenant le nom de l’identifiant de conteneur de la visionneuse et l’objet JSON `params` imbriqué avec les paramètres de configuration pris en charge par la visionneuse. Dans ce cas, l’objet `params` doit comporter au moins la propriété `serverUrl` de l’URL de diffusion d’images et le paramètre `asset` de l’actif initial. L’API d’initialisation basée sur JSON vous permet de créer et de début le lecteur avec une seule ligne de code.

   Il est important que le conteneur de la visionneuse soit ajouté au modèle DOM afin que le code de la visionneuse puisse trouver l’élément de conteneur en fonction de son identifiant. Certains navigateurs retardent la création du modèle DOM jusqu’à la fin de la page Web. Pour une compatibilité maximale, appelez la méthode `init()` juste avant la balise de fermeture `BODY` ou sur le événement body `onload()`.

   Dans le même temps, l’élément conteneur ne doit pas nécessairement faire partie de la mise en page de la page Web pour le moment. Par exemple, il peut être masqué à l’aide du style `display:none` qui lui est affecté. Dans ce cas, le lecteur retarde son processus d’initialisation jusqu’au moment où la page Web ramène l’élément de conteneur à la mise en page. Dans ce cas, le chargement du lecteur reprend automatiquement.

   Voici un exemple de création d’une instance de visionneuse, de transmission des options de configuration minimales nécessaires au constructeur et d’appel de la méthode `init()`. Cet exemple suppose que `zoomViewer` correspond à l’instance de visionneuse, `s7viewer` au nom de l’espace réservé DIV, `http://s7d1.scene7.com/is/image/` à l’URL de diffusion d’images et `Scene7SharedAssets/ImageSet-Views-Sample` à l’actif.

   ```
   <script type="text/javascript"> 
   var zoomViewer = new s7viewers.ZoomViewer({ 
    "containerId":"s7viewer", 
   "params":{ 
    "asset":"Scene7SharedAssets/ImageSet-Views-Sample", 
    "serverurl":"http://s7d1.scene7.com/is/image/" 
   } 
   }).init(); 
   </script>
   ```

   Le code suivant est un exemple complet d’une page Web triviale qui incorpore la visionneuse de vidéos à une taille fixe :

   ```
   <!DOCTYPE html> 
   <html> 
   <head> 
   <script type="text/javascript" src="http://s7d1.scene7.com/s7viewers/html5/js/ZoomViewer.js"></script> 
   <style type="text/css"> 
   #s7viewer.s7zoomviewer { 
    width: 640px; 
    height: 480px; 
   } 
   </style> 
   </head> 
   <body> 
   <div id="s7viewer" style="position:relative"></div> 
   <script type="text/javascript"> 
   var zoomViewer = new s7viewers.ZoomViewer({ 
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

## Incorporation de conception réactive avec une hauteur sans restriction {#section-b9ca11a7e7aa4f74ab43244cbca37ae0}

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

Ajouter le lecteur à une telle page est similaire à la procédure d’incorporation de taille fixe. La seule différence est que vous n’avez pas besoin de définir explicitement la taille de la visionneuse.

1. Ajouter le fichier JavaScript de la visionneuse sur votre page Web.
1. Définition de la balise DIV de conteneur.
1. Création et initialisation de la visionneuse.

Toutes les étapes ci-dessus sont identiques à celles de l’incorporation de taille fixe. Ajoutez le conteneur DIV sur le `"holder"` DIV existant. Le code suivant est un exemple complet. Notez comment la taille de la visionneuse change lorsque le navigateur est redimensionné et comment les proportions de la visionneuse correspondent à la ressource.

```
<!DOCTYPE html> 
<html> 
<head> 
<script type="text/javascript" src="http://s7d1.scene7.com/s7viewers/html5/js/ZoomViewer.js"></script> 
<style type="text/css"> 
.holder { 
 width: 40%; 
} 
</style> 
</head> 
<body> 
<div class="holder"> 
<div id="s7viewer" style="position:relative"></div> 
</div> 
<script type="text/javascript"> 
var zoomViewer = new s7viewers.ZoomViewer({ 
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

La page d’exemples suivante illustre d’autres utilisations réelles de l’incorporation de conceptions réactives avec une hauteur libre :

[Démonstrations en direct](https://landing.adobe.com/en/na/dynamic-media/ctir-2755/live-demos.html)

## Incorporation de taille flexible avec largeur et hauteur définies {#section-3674e6c032594441a6576b7fb1de6e64}

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
<script type="text/javascript" src="http://s7d1.scene7.com/s7viewers/html5/js/ZoomViewer.js"></script> 
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
<div class="holder"> 
<div id="s7viewer" style="position:relative"></div> 
</div> 
<script type="text/javascript"> 
var zoomViewer = new s7viewers.ZoomViewer({ 
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

## Incorporation à l’aide de l’API basée sur un setter {#section-44e014925f24418b900696003855c0a9}

Au lieu d’utiliser l’initialisation basée sur JSON, il est possible d’utiliser une API basée sur un setter et un constructeur sans args. L&#39;utilisation de ce constructeur d&#39;API ne prend aucun paramètre et les paramètres de configuration sont spécifiés à l&#39;aide des méthodes d&#39;API `setContainerId()`, `setParam()` et `setAsset()` avec des appels JavaScript distincts.

L’exemple suivant illustre l’utilisation de l’incorporation de tailles fixes avec l’API basée sur un setter :

```
<!DOCTYPE html> 
<html> 
<head> 
<script type="text/javascript" src="http://s7d1.scene7.com/s7viewers/html5/js/ZoomViewer.js"></script> 
<style type="text/css"> 
#s7viewer.s7zoomviewer { 
 width: 640px; 
 height: 480px; 
} 
</style> 
</head> 
<body> 
<div id="s7viewer" style="position:relative"></div> 
<script type="text/javascript"> 
var zoomViewer = new s7viewers.ZoomViewer(); 
zoomViewer.setContainerId("s7viewer"); 
zoomViewer.setParam("serverurl", "http://s7d1.scene7.com/is/image/"); 
zoomViewer.setAsset("Scene7SharedAssets/ImageSet-Views-Sample"); 
zoomViewer.init(); 
</script> 
</body> 
</html> 
```

