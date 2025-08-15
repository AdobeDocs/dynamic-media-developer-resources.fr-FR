---
title: Zoom
description: La visionneuse Zoom est une visionneuse d’images qui affiche une image zoomable. Cette visionneuse fonctionne avec les visionneuses d’images et la navigation s’effectue à l’aide d’échantillons. Il dispose d’outils de zoom, d’une prise en charge du plein écran, d’échantillons et d’un bouton de fermeture facultatif. Il est conçu pour fonctionner sur les ordinateurs de bureau et les appareils mobiles.
keywords: réactif
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Zoom
role: Developer,User
exl-id: 81a74026-fb15-4f57-a4c7-1ab005950245
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '2343'
ht-degree: 0%

---

# Zoom{#zoom}

La visionneuse Zoom est une visionneuse d’images qui affiche une image zoomable. Cette visionneuse fonctionne avec les visionneuses d’images et la navigation s’effectue à l’aide d’échantillons. Il dispose d’outils de zoom, d’une prise en charge du plein écran, d’échantillons et d’un bouton de fermeture facultatif. Il est conçu pour fonctionner sur les ordinateurs de bureau et les appareils mobiles.

>[!NOTE]
>
>Les images qui utilisent le rendu d’image (IR) ou le contenu créé par l’utilisateur (UGC) ne sont pas pris en charge par cette visionneuse.

Type de visionneuse 502.

Voir [Configuration requise et conditions préalables](../../c-system-requirements-and-prerequisites.md#concept-9282e5b777de42cdaf72ef7ebd646842).

## URL de démonstration {#section-e1c3106f5b3e445d9b95be337c2f94e2}

[https://s7d9.scene7.com/s7viewers/html5/ZoomViewer.html?asset=Scene7SharedAssets/ImageSet-Views-Sample](https://s7d9.scene7.com/s7viewers/html5/ZoomViewer.html?asset=Scene7SharedAssets/ImageSet-Views-Sample)

## Utilisation de la visionneuse Zoom {#section-e6c68406ecdc4de781df182bbd8088b4}

La visionneuse Zoom représente un fichier JavaScript principal et un ensemble de fichiers d’assistance (un seul JavaScript inclus avec tous les composants SDK de la visionneuse utilisés par cette visionneuse particulière, les ressources, le code CSS) téléchargés par la visionneuse au moment de l’exécution.

Vous pouvez utiliser la visionneuse Zoom en mode pop-up à l’aide d’une page HTML prête pour l’exploitation fournie avec des visionneuses IS, ou en mode intégré, où elle est intégrée à la page web cible à l’aide d’une API documentée.

La configuration et l’habillage sont similaires à ceux des autres visionneuses. Toute application de la peau est réalisée au moyen d’un CSS personnalisé.

Voir [ Référence des commandes commune à toutes les visionneuses - Attributs de configuration ](../../r-html5-viewer-20-cmdref-configattrib/r-html5-viewer-20-cmdref-configattrib.md#concept-850e0f2c49b949deb7cfbfd330d329bd) et [ Référence des commandes commune à toutes les visionneuses - URL](../../c-html5-viewer-20-cmdref-url/c-html5-viewer-20-cmdref-url.md#concept-9b337f349b7b406b8c33c7ee96b3e226)

## Interaction avec la visionneuse Zoom {#section-642e66ca38cd4032992840ec6c0b0cd2}

La visionneuse Zoom prend en charge les gestes tactiles suivants, courants dans d’autres applications mobiles. Lorsque la visionneuse ne peut pas traiter le mouvement de balayage de l’utilisateur, elle transfère l’événement au navigateur web pour effectuer un défilement natif de la page. Ce type de fonctionnalité permet à l’utilisateur de parcourir la page même si la visionneuse occupe la majeure partie de la zone de l’écran de l’appareil.

<table id="table_ED747CC7178448919C34A4FCD18922D0"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>Mouvement </p> </th> 
   <th colname="col2" class="entry"> <p>Description </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>Clic unique </p> </td> 
   <td colname="col2"> <p> Sélectionne la nouvelle miniature dans les échantillons. Dans la vue principale, il masque ou affiche les éléments de l’interface utilisateur. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Appuyer deux fois </p> </td> 
   <td colname="col2"> <p> Effectue un zoom d’un niveau jusqu’à ce que le zoom maximal soit atteint. Le mouvement de double appui suivant réinitialise la visionneuse à l’état d’affichage initial. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Pincer </p> </td> 
   <td colname="col2"> <p>Effectue un zoom avant ou arrière. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Balayage horizontal ou clic </p> </td> 
   <td colname="col2"> <p> Fait défiler la liste des échantillons dans la barre d’échantillons. </p> <p> Si l’image est à l’état réinitialisé et que le paramètre de <span class="codeph"> de transition d’image </span> est défini sur diapositive, la ressource est modifiée lors de l’animation de la diapositive. Pour d’autres modes de <span class="codeph"> de transition de structure </span>, le mouvement effectue un défilement natif de la page. </p> <p> Si l’image fait l’objet d’un zoom avant, elle se déplace horizontalement. Si l’image est déplacée vers le bord de la vue et qu’un balayage est effectué dans la même direction, le mouvement effectue un défilement natif de la page. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Balayage vertical </p> </td> 
   <td colname="col2"> <p> Si l’image est à l’état réinitialisé, le mouvement effectue un défilement natif de la page. </p> <p> Lorsque l’image fait l’objet d’un zoom avant, elle se déplace verticalement. Si l’image est déplacée vers le bord de la vue et qu’un balayage est effectué dans la même direction, le mouvement effectue un défilement natif de la page. </p> <p> Si le mouvement est effectué dans la zone d’échantillons, il effectue un défilement natif de la page. </p> </td> 
  </tr> 
 </tbody> 
</table>

La visionneuse prend en charge l’entrée tactile et l’entrée souris sur les appareils Windows dotés d’un écran tactile et d’une souris. Cette prise en charge se limite toutefois aux navigateurs web Chrome, Internet Explorer 11 et Edge uniquement.

Cette visionneuse est entièrement accessible à partir du clavier.

Voir [Accessibilité clavier et navigation](../../c-keyboard-accessibility.md#topic-f5650e9493404e55a3627c8d1366b861).

## Incorporation de la visionneuse Zoom {#section-6bb5d3c502544ad18a58eafe12a13435}

Les différentes pages web ont des besoins différents en termes de comportement des observateurs. Parfois, une page web fournit un lien qui, lorsqu’il est sélectionné, ouvre la visionneuse dans une fenêtre de navigateur distincte. Dans d’autres cas, il est nécessaire d’incorporer directement la visionneuse dans la page d’hébergement. Dans ce dernier cas, la page web peut avoir une disposition statique ou utiliser un responsive design qui s’affiche différemment selon les appareils ou les tailles de fenêtre du navigateur. Pour répondre à ces besoins, la visionneuse prend en charge trois modes de fonctionnement principaux : pop-up, incorporation de taille fixe et incorporation de conception réactive.

**À propos du mode pop-up**

En mode pop-up, la visionneuse s’ouvre dans une fenêtre ou un onglet distinct du navigateur web. Il utilise toute la zone de la fenêtre du navigateur et s’ajuste au cas où le navigateur serait redimensionné ou si l’orientation de l’appareil était modifiée.

Ce mode est le plus courant pour les appareils mobiles. La page web charge la visionneuse à l’aide de `window.open()`’appel JavaScript, correctement configuré `A` l’élément HTML ou de toute autre méthode appropriée.

Il est recommandé d’utiliser une page HTML prête à l’emploi pour le mode de fonctionnement des fenêtres pop-up. La page HTML prête à l’emploi est appelée `ZoomViewer.html` et se trouve sous le sous-dossier `html5/` de votre déploiement d’observateurs IS standard, comme dans l’exemple suivant :

`<s7viewers_root>/html5/ZoomViewer.html`

Appliquez le CSS personnalisé pour personnaliser l’apparence de la page.

Voici un exemple de code HTML qui permet d’ouvrir la visionneuse dans la nouvelle fenêtre :

```html {.line-numbers}
 <a href="http://s7d1.scene7.com/s7viewers/html5/ZoomViewer.html?asset=Scene7SharedAssets/ImageSet-Views-Sample" 
target="_blank">Open popup viewer</a>
```

**À propos du mode d’incorporation de taille fixe et du mode d’incorporation de conception réactive**

En mode incorporé, la visionneuse est ajoutée à la page web existante, qui peut déjà comporter du contenu client non lié à la visionneuse. L’observateur n’occupe normalement qu’une partie de l’espace de la page web.

Les principaux cas d’utilisation sont des pages web orientées pour les ordinateurs de bureau ou les tablettes, ainsi que des pages conçues en responsive design qui ajustent automatiquement la disposition en fonction du type d’appareil.

L’incorporation de taille fixe est utilisée lorsque la visionneuse ne modifie pas sa taille après le chargement initial. Cette option est le meilleur choix pour les pages web avec une disposition statique.

Le mode d’incorporation de conception réactive suppose que le redimensionnement de la visionneuse est nécessaire lors de l’exécution en raison du changement de taille de son `DIV` de conteneur. Le cas d’utilisation le plus courant consiste à ajouter une visionneuse à une page web qui utilise une disposition flexible.

En mode d’incorporation de responsive design, la visionneuse se comporte différemment selon la manière dont la page web dimensionne son `DIV` de conteneur. Si la page web définit uniquement la largeur du `DIV` de conteneur, sans restriction de hauteur, la visionneuse choisit automatiquement sa hauteur en fonction des proportions de la ressource utilisée. Cette logique garantit que la ressource s’adapte parfaitement à la vue sans marge intérieure sur les côtés. Ce cas d’utilisation est le plus courant pour les pages web qui utilisent des structures de disposition réactives telles que Bootstrap et Foundation.

Si la page web définit à la fois la largeur et la hauteur du `DIV` de conteneur de la visionneuse, celle-ci remplit cette zone et suit la taille fournie par la page web. Par exemple, lors de l’incorporation de la visionneuse dans une superposition modale, où la superposition est dimensionnée en fonction de la taille de la fenêtre du navigateur web.

## Incorporation à taille fixe {#section-44f365e6c0dd40709467a459afa82a7f}

Ajoutez la visionneuse à une page web en procédant comme suit :

1. Ajout du fichier JavaScript de la visionneuse à votre page web.
1. Définition du DIV du conteneur.
1. Définition de la taille de la visionneuse.
1. Création et initialisation de la visionneuse.

1. Ajout du fichier JavaScript de la visionneuse à votre page web.

   La création d’une visionneuse nécessite l’ajout d’une balise de script dans l’en-tête HTML. Avant de pouvoir utiliser l’API de visionneuse, veillez à inclure [!DNL ZoomViewer.js]. Le fichier [!DNL ZoomViewer.js] se trouve sous le sous-dossier [!DNL html5/js/] de votre déploiement d’observateurs IS standard :

[!DNL <s7viewers_root>/html5/js/ZoomViewer.js]

Vous pouvez utiliser un chemin relatif si la visionneuse est déployée sur l’un des serveurs d’Adobe Dynamic Media Classic et qu’elle est diffusée à partir du même domaine. Sinon, vous spécifiez un chemin d’accès complet à l’un des serveurs Adobe Dynamic Media Classic sur lesquels les visionneuses IS sont installées.

Le chemin d’accès relatif ressemble à ce qui suit :

```html {.line-numbers}
<script language="javascript" type="text/javascript" src="/s7viewers/html5/js/ZoomViewer.js"></script>
```

>[!NOTE]
>
>Référencez uniquement le fichier de `include` JavaScript de la visionneuse principale sur votre page. Ne référencez aucun fichier JavaScript supplémentaire dans le code de page web qui pourrait être téléchargé par la logique de la visionneuse au moment de l’exécution. En particulier, ne référencez pas directement la bibliothèque de `Utils.js` SDK HTML5 chargée par la visionneuse à partir `/s7viewers` chemin de contexte (appelé `include` consolidée de SDK). En effet, l’emplacement des bibliothèques de visionneuse d’exécution `Utils.js` ou similaires est entièrement géré par la logique de la visionneuse et l’emplacement change entre les versions de la visionneuse. Adobe ne conserve pas les anciennes versions des `includes` secondaires de la visionneuse sur le serveur.
>
>
>Par conséquent, le fait de placer une référence directe à toute `include` JavaScript secondaire utilisée par la visionneuse sur la page interrompt la fonctionnalité de la visionneuse à l’avenir lorsqu’une nouvelle version du produit est déployée.

1. Définition du DIV du conteneur.

   Ajoutez un élément DIV vide à la page sur laquelle vous souhaitez que la visionneuse apparaisse. L’identifiant de l’élément DIV doit être défini, car cet identifiant est transmis ultérieurement à l’API de visionneuse.

   L’espace réservé DIV est un élément positionné, ce qui signifie que la propriété CSS `position` est définie sur `relative` ou `absolute`.

   Exemple d’élément DIV d’espace réservé défini :

   ```html {.line-numbers}
   <div id="s7viewer" style="position:relative"></div>
   ```

1. Définition de la taille de la visionneuse.

   Cette visionneuse affiche des miniatures lorsque vous travaillez avec des ensembles d’éléments multiples. Sur les systèmes de bureau, les miniatures sont placées sous la vue principale. Dans le même temps, la visionneuse permet de permuter la ressource principale au moment de l’exécution à l’aide de l’API `setAsset()`. En tant que développeur ou développeuse, vous avez un contrôle sur la manière dont la visionneuse gère la zone des miniatures en bas lorsque la nouvelle ressource ne comporte qu’un seul élément. Il est possible de conserver la taille de la visionneuse extérieure intacte et de laisser la vue principale augmenter sa hauteur et occuper la zone des miniatures. Vous pouvez également conserver la taille de l’affichage principal statique et réduire la zone extérieure de la visionneuse, ce qui permet au contenu de la page web de se déplacer vers le haut, et utiliser l’espace réservé à l’écran libre qui reste des miniatures.

   Pour conserver les limites de la visionneuse externe intactes, définissez la taille de la classe CSS de niveau supérieur `.s7zoomviewer` en unités absolues. Le dimensionnement dans CSS peut être placé directement sur la page HTML. Il peut également être placé dans un fichier CSS de visionneuse personnalisé, qui est ensuite attribué à un enregistrement de paramètre prédéfini de visionneuse dans Dynamic Media Classic ou transmis explicitement à l’aide d’une commande de style.

   Consultez [Personnalisation de la visionneuse Zoom](../../c-html5-s7-aem-asset-viewers/c-html5-20-zoom-viewer-about/c-html5-20-zoom-viewer-customizingviewer/c-html5-20-zoom-viewer-customizingviewer.md#concept-73a8546acdb444a387c49969ceca57d0) pour plus d’informations sur la mise en forme de la visionneuse avec CSS.

   Voici un exemple de définition d’une taille de visionneuse externe statique dans une page HTML :

   ```html {.line-numbers}
   #s7viewer.s7zoomviewer { 
    width: 640px; 
    height: 480px; 
   }
   ```

   Vous pouvez voir le comportement avec une visionneuse externe fixe dans l’exemple suivant. Notez que lorsque vous passez d’une visionneuse à l’autre, la taille de la visionneuse externe ne change pas :

   [https://experienceleague.adobe.com/tools/dynamic-media-demo/viewers-ref/zoom/ZoomViewer-fixed-outer-area.html?lang=fr](https://experienceleague.adobe.com/tools/dynamic-media-demo/viewers-ref/zoom/ZoomViewer-fixed-outer-area.html?lang=fr)

   Pour rendre les dimensions de la vue principale statiques, définissez la taille de la visionneuse en unités absolues pour le composant SDK `Container` interne à l’aide du sélecteur CSS `.s7zoomviewer` `.s7container` ou à l’aide du modificateur `stagesize`.

   Voici un exemple de définition de la taille de la visionneuse pour le composant SDK `Container` interne afin que la zone d’affichage principale ne modifie pas sa taille lors du changement de ressource :

   ```html {.line-numbers}
   #s7viewer.s7zoomviewer .s7container { 
    width: 640px; 
    height: 480px; 
   }
   ```

   La page de démonstration suivante montre le comportement de la visionneuse avec une taille d’affichage principale fixe. Notez que lorsque vous basculez entre les visionneuses, la vue principale reste statique et le contenu de la page web se déplace verticalement.

   [https://experienceleague.adobe.com/tools/dynamic-media-demo/viewers-ref/zoom/ZoomViewer-fixed-main-view.html?lang=fr](https://experienceleague.adobe.com/tools/dynamic-media-demo/viewers-ref/zoom/ZoomViewer-fixed-main-view.html?lang=fr)

   Vous pouvez définir le modificateur `stagesize` dans l’enregistrement du paramètre prédéfini de visionneuse dans Dynamic Media Classic. Vous pouvez également le transmettre explicitement avec le code d’initialisation de la visionneuse avec la collection `params` ou sous la forme d’un appel API, comme décrit dans la section Référence des commandes de cette aide, comme dans ce qui suit :

   ```html {.line-numbers}
    zoomViewer.setParam("stagesize", 
   "640,480");
   ```

   Une approche basée sur CSS est recommandée et est utilisée dans cet exemple.

1. Création et initialisation de la visionneuse.

   Une fois les étapes ci-dessus terminées, vous créez une instance de `s7viewers.ZoomViewer` classe, transmettez toutes les informations de configuration à son constructeur et appelez `init()` méthode sur une instance de visionneuse.

   Les informations de configuration sont transmises au constructeur en tant qu’objet JSON. Au minimum, cet objet doit comporter `containerId` champ qui contient le nom de l’ID de conteneur de visionneuse et de l’objet JSON `params` imbriqué avec les paramètres de configuration pris en charge par la visionneuse. Dans ce cas, l’objet `params` doit comporter au moins l’URL du service d’images transmise en tant que propriété `serverUrl` et la ressource initiale en tant que paramètre `asset`. L’API d’initialisation basée sur JSON vous permet de créer et de démarrer la visionneuse avec une seule ligne de code.

   Il est important d’ajouter le conteneur de visionneuse au DOM afin que le code de la visionneuse puisse trouver l’élément de conteneur à l’aide de son identifiant. Certains navigateurs retardent la création du DOM jusqu’à la fin de la page web. Pour une compatibilité maximale, appelez la méthode `init()` juste avant la balise `BODY` de fermeture ou sur l’événement body `onload()`.

   Dans le même temps, l’élément de conteneur ne doit pas nécessairement encore faire partie de la mise en page web. Par exemple, elle peut être masquée à l’aide `display:none` style qui lui est affecté. Dans ce cas, la visionneuse retarde son processus d’initialisation jusqu’au moment où la page web ramène l’élément de conteneur dans la mise en page. Lorsque cette action se produit, le chargement de la visionneuse reprend automatiquement.

   Voici un exemple de création d’une instance de visionneuse, de transmission des options de configuration minimales nécessaires au constructeur et d’appel de la méthode `init()`. Cet exemple suppose que `zoomViewer` est l’instance de visionneuse, `s7viewer` est le nom de l’espace réservé DIV, `http://s7d1.scene7.com/is/image/` est l’URL du service d’images et `Scene7SharedAssets/ImageSet-Views-Sample` est la ressource.

   ```html {.line-numbers}
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

   Le code suivant est un exemple complet de page web triviale qui incorpore la visionneuse de vidéos avec une taille fixe :

   ```html {.line-numbers}
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

## Incorporation de conception réactive avec hauteur illimitée {#section-b9ca11a7e7aa4f74ab43244cbca37ae0}

Avec l’incorporation de responsive design, la page web dispose normalement d’un type de disposition flexible qui détermine la taille d’exécution du `DIV` de conteneur de la visionneuse. Dans l’exemple suivant, supposons que la page web permette au `DIV` de conteneur de la visionneuse de prendre 40 % de la taille de la fenêtre du navigateur web, sans restriction de hauteur. Le code d’HTML de la page web se présente comme suit :

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

L’ajout de la visionneuse à une telle page est similaire aux étapes d’incorporation à taille fixe. La seule différence réside dans le fait que vous n’avez pas besoin de définir explicitement la taille de la visionneuse.

1. Ajout du fichier JavaScript de la visionneuse à votre page web.
1. Définition du DIV du conteneur.
1. Création et initialisation de la visionneuse.

Toutes les étapes ci-dessus sont identiques à l’incorporation de taille fixe. Ajoutez le conteneur DIV au DIV `"holder"` existant. Le code suivant en est un exemple complet. Notez comment la taille de la visionneuse change lorsque le navigateur est redimensionné et comment les proportions de la visionneuse correspondent à la ressource.

```html {.line-numbers}
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

La page d’exemples suivante illustre d’autres utilisations réelles de l’incorporation Responsive Design avec une hauteur illimitée :

[Démonstrations en direct](https://landing.adobe.com/en/na/dynamic-media/ctir-2755/live-demos.html)

## Incorporation de taille flexible avec largeur et hauteur définies {#section-3674e6c032594441a6576b7fb1de6e64}

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

## Incorporation à l’aide de l’API setter {#section-44e014925f24418b900696003855c0a9}

Au lieu d’utiliser l’initialisation basée sur JSON, il est possible d’utiliser l’API basée sur setter et le constructeur sans args. L’utilisation de ce constructeur d’API ne prend aucun paramètre et les paramètres de configuration sont spécifiés à l’aide des méthodes d’API `setContainerId()`, `setParam()` et `setAsset()` avec des appels JavaScript distincts.

L’exemple suivant illustre l’utilisation de l’incorporation de taille fixe avec l’API setter :

```html {.line-numbers}
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
