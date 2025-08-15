---
title: Visionneuse panoramique
description: La visionneuse panoramique HTML5 est une visionneuse d’images qui affiche une image panoramique. Cette visionneuse a pour but d’afficher un panorama sphérique, également appelé image équirectangulaire. Il prend en charge le panoramique automatique et le panoramique par mouvement gyroscopique. Il est conçu pour fonctionner sur les ordinateurs de bureau et les appareils mobiles. Le mode d’affichage de la réalité virtuelle est disponible sur les appareils mobiles compatibles.
keywords: réactif
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Panoramic
role: Developer,User
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '1924'
ht-degree: 0%

---

# Panoramique{#panoramic}

La visionneuse panoramique HTML5 est une visionneuse d’images qui affiche une image panoramique. Cette visionneuse a pour but d’afficher un panorama sphérique, également appelé image équirectangulaire. Il prend en charge le panoramique automatique et le panoramique par mouvement gyroscopique. Il est conçu pour fonctionner sur les ordinateurs de bureau et les appareils mobiles. Le mode d’affichage de la réalité virtuelle est disponible sur les appareils mobiles compatibles.

Voir [Configuration requise et conditions préalables](../../c-system-requirements-and-prerequisites.md#concept-9282e5b777de42cdaf72ef7ebd646842).


Type de visionneuse 514.

## URL de démonstration {#section-e1c3106f5b3e445d9b95be337c2f94e2}

[http://s7d1.scene7.com/s7viewers/html5/PanoramicViewer.html?asset=Scene7SharedAssets/PanoramicImage-Sample](http://s7d1.scene7.com/s7viewers/html5/PanoramicViewer.html?asset=Scene7SharedAssets/PanoramicImage-Sample)

## Utilisation de la visionneuse panoramique {#section-f21ac23d3f6449ad9765588d69584772}

La visionneuse panoramique HTML5 représente un fichier JavaScript principal et un ensemble de fichiers d’assistance téléchargés par la visionneuse au moment de l’exécution. L’ensemble de fichiers d’assistance est un JavaScript unique inclus avec tous les composants SDK de la visionneuse HTML5 utilisés par cette visionneuse particulière, Assets, CSS.
La visionneuse panoramique HTML5 peut être utilisée en mode pop-up à l’aide d’une page HTML prête pour l’exploitation fournie avec les visionneuses IS, ou en mode intégré, où elle est intégrée à la page web cible à l’aide d’une API documentée.
La configuration et l’habillage sont similaires à ceux des autres visionneuses HTML5. Toute application de la peau peut être réalisée au moyen d’un CSS personnalisé.

Voir [ Référence des commandes commune à toutes les visionneuses - Attributs de configuration ](../../r-html5-viewer-20-cmdref-configattrib/r-html5-viewer-20-cmdref-configattrib.md#concept-850e0f2c49b949deb7cfbfd330d329bd) et [ Référence des commandes commune à toutes les visionneuses - URL](../../c-html5-viewer-20-cmdref-url/c-html5-viewer-20-cmdref-url.md#concept-9b337f349b7b406b8c33c7ee96b3e226)

## Interaction avec la visionneuse panoramique HTML5 {#section-ab66eb6955aa4a8aa6d14a3b3acfed3f}

La visionneuse panoramique HTML5 prend en charge le panoramique automatique et la navigation par glisser-déplacer ou mouvement gyroscopique.

<table id="table_panoramic"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>Navigation </p> </th> 
   <th colname="col2" class="entry"> <p>Description </p> </th> 
  </tr>
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>Bureau </p> </td> 
   <td colname="col2"> <p>Panoramique automatique et glisser pour naviguer. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Appareil tactile </p> </td> 
   <td colname="col2"> <p>Déplacez et faites glisser automatiquement pour naviguer par défaut. Naviguez par mouvement gyroscopique en mode de rendu VR (vrrender=true).
 </p> </td> 
  </tr> 
 </tbody> 
</table>

La visionneuse prend en charge l’entrée tactile et l’entrée souris sur les appareils Windows à écran tactile et souris. Toutefois, cette prise en charge se limite aux navigateurs web Chrome, Internet Explorer 11 et Edge uniquement.
La visionneuse panoramique peut effectuer le rendu d’images panoramiques en mode Réalité virtuelle (VR) en spécifiant le modificateur vrrender. Lorsque le rendu est activé, une image panoramique s’affiche dans les écrans partagés. Un cas d’utilisation courant serait de diffuser l’image sur un téléphone mobile monté dans un casque de réalité virtuelle, fournissant des images distinctes pour chaque œil. Le spectateur réagit au mouvement gyroscopique de la tête et navigue dans l&#39;image.

## Incorporation de la visionneuse panoramique HTML5 {#section-6bb5d3c502544ad18a58eafe12a13435}

Les différentes pages web ont des besoins différents en termes de comportement des observateurs. Parfois, une page web fournit un lien. La sélection de ce lien ouvre la visionneuse dans une fenêtre de navigateur distincte. Dans d’autres cas, il peut être nécessaire d’incorporer la visionneuse dans la page d’hébergement. Dans ce dernier cas, la page web peut avoir une disposition statique, ou être « réactive » et s’afficher différemment sur différents appareils ou pour différentes tailles de fenêtre du navigateur. Pour répondre à ces besoins, la visionneuse prend en charge trois modes de fonctionnement principaux : fenêtre contextuelle, incorporation de taille fixe et incorporation réactive.

**À propos du mode pop-up**

En mode pop-up, la visionneuse s’ouvre dans une fenêtre ou un onglet distinct du navigateur web. Il prend toute la zone de la fenêtre du navigateur et s’ajuste au cas où le navigateur est redimensionné ou que l’orientation de l’appareil est modifiée.

Ce mode est le plus courant pour les appareils mobiles. La page web charge la visionneuse à l’aide de `window.open()`’appel JavaScript, d’un élément HTML correctement configuré ou de toute autre manière appropriée.

Il est recommandé d’utiliser une page HTML prête à l’emploi pour le mode de fonctionnement des fenêtres pop-up. Il s’appelle [!DNL PanoramicViewer.html] et se trouve sous le sous-dossier [!DNL html5/] de votre déploiement d’observateurs IS standard :

[!DNL <s7viewers_root>/html5/PanoramicViewer.html]

La personnalisation visuelle peut être réalisée en appliquant un CSS personnalisé.

Voici un exemple de code HTML qui permet d&#39;ouvrir la visionneuse dans la nouvelle fenêtre :

```html {.line-numbers}
<a href="http://s7d1.scene7.com/s7viewers/html5/PanoramicViewer.html?asset=Scene7SharedAssets/PanoramicImage-Sample" target="_blank">Open popup viewer</a>
```

**À propos du mode d’incorporation de taille fixe et du mode d’incorporation réactif**

En mode incorporé, la visionneuse est ajoutée à la page web existante, qui peut déjà comporter du contenu client non lié à la visionneuse. Normalement, la visionneuse n’occupe qu’une partie de l’espace réservé à la page web.

Les principaux cas d’utilisation sont des pages web orientées pour les ordinateurs de bureau ou les tablettes, ainsi que des pages web réactives qui ajustent automatiquement la disposition en fonction du type d’appareil.

L’incorporation de taille fixe est utilisée lorsque la visionneuse ne modifie pas sa taille après le chargement initial. Cette méthode est recommandée pour les pages web avec une disposition statique.

L’incorporation réactive suppose que la visionneuse doit être redimensionnée au moment de l’exécution en réponse au changement de taille de son DIV de conteneur. Le cas d’utilisation le plus courant consiste à ajouter une visionneuse à une page web qui utilise une disposition flexible.

En mode réactif, la visionneuse se comporte différemment selon la manière dont la page web dimensionne son DIV de conteneur. Si la page web définit uniquement la largeur du DIV du conteneur, sans restriction de hauteur, la visionneuse choisit automatiquement sa hauteur en fonction des proportions de la ressource utilisée. Cette méthode garantit que la ressource s’adapte parfaitement à la vue sans marge intérieure sur les côtés. Ce cas d’utilisation est le plus courant pour les pages web utilisant des structures de disposition réactives telles que Bootstrap, Foundation, etc.

Dans le cas contraire, si la page web définit à la fois la largeur et la hauteur du DIV du conteneur de la visionneuse, celle-ci remplit cette zone et respecte la taille fournie par la disposition de la page web. Un bon exemple consiste à incorporer la visionneuse dans une superposition modale, où la superposition est dimensionnée en fonction de la taille de la fenêtre du navigateur web.

**Incorporation de taille fixe**

Ajoutez la visionneuse à une page web en procédant comme suit :

1. Ajout du fichier JavaScript de la visionneuse à votre page web.
1. La définition du `DIV` de conteneur.
1. Définition de la taille de la visionneuse.
1. Création et initialisation de la visionneuse.

1. Ajout du fichier JavaScript de la visionneuse à votre page web.

   La création d’une visionneuse nécessite l’ajout d’une balise de script dans l’en-tête HTML. Avant de pouvoir utiliser l’API de visionneuse, veillez à inclure [!DNL PanoramicViewer.js]. Le fichier [!DNL PanoramicViewer.js] se trouve sous le sous-dossier [!DNL html5/js/] de votre déploiement d’observateurs IS standard :

[!DNL <s7viewers_root>/html5/js/PanoramicViewer.js]

Vous pouvez utiliser un chemin relatif si la visionneuse est déployée sur l’un des serveurs d’Adobe Dynamic Media Classic et qu’elle est diffusée à partir du même domaine. Sinon, vous spécifiez un chemin d’accès complet à l’un des serveurs Adobe Dynamic Media Classic sur lesquels les visionneuses IS sont installées.

Le chemin relatif ressemble à ce qui suit :

```html {.line-numbers}
<script language="javascript" type="text/javascript" src="/s7viewers/html5/js/PanoramicViewer.js"></script>
```

>[!NOTE]
>
>Référencez uniquement le fichier de `include` JavaScript de la visionneuse principale sur votre page. Ne référencez aucun fichier JavaScript supplémentaire dans le code de page web qui pourrait être téléchargé par la logique de la visionneuse au moment de l’exécution. En particulier, ne référencez pas directement la bibliothèque de `Utils.js` SDK HTML5 chargée par la visionneuse à partir `/s7viewers` chemin de contexte (appelé `include` consolidée de SDK). En effet, l’emplacement des bibliothèques de visionneuse d’exécution `Utils.js` ou similaires est entièrement géré par la logique de la visionneuse et l’emplacement change entre les versions de la visionneuse. Adobe ne conserve pas les anciennes versions des `includes` secondaires de la visionneuse sur le serveur.
>
>
>Par conséquent, le fait de placer une référence directe à toute `include` JavaScript secondaire utilisée par la visionneuse sur la page interrompt la fonctionnalité de la visionneuse à l’avenir lorsqu’une nouvelle version du produit est déployée.

1. Définition du DIV du conteneur.

   Ajoutez un élément DIV vide à la page sur laquelle vous souhaitez que la visionneuse apparaisse. L’identifiant de l’élément DIV doit être défini, car cet identifiant est transmis ultérieurement à l’API de visionneuse. La taille du DIV est spécifiée via CSS.

   L’espace réservé DIV est un élément positionné, ce qui signifie que la propriété CSS `position` est définie sur `relative` ou `absolute`.


   Exemple d’élément DIV d’espace réservé défini :

   ```html {.line-numbers}
   <div id="s7viewer" style="position:relative"></div> 
   ```

1. Définition de la taille de la visionneuse

   Vous pouvez définir la taille statique de la visionneuse en la déclarant pour `.s7panoramicviewer` classe CSS de niveau supérieur dans des unités absolues ou à l’aide du `stagesize` de modificateur.

   Le dimensionnement dans CSS peut être placé directement sur la page HTML ou dans le fichier CSS de la visionneuse personnalisée, qui est ensuite affecté à un enregistrement de paramètre prédéfini de visionneuse dans AOD ou transmis explicitement à l’aide de la commande de style. Pour plus d’informations sur la mise en forme de la visionneuse avec CSS, consultez Personnalisation de la visionneuse . Vous trouverez ci-dessous un exemple de définition de la taille de la visionneuse statique dans la page HTML :

   ```html {.line-numbers}
   #s7viewer.s7panoramicviewer {
     width: 1024px;
     height: 512px;
   }
   ```

   `stagesize` modificateur peut être transmis explicitement avec le code d’initialisation de la visionneuse avec la collection params ou en tant qu’appel API, comme décrit dans la section Référence des commandes , comme suit :

   ```html {.line-numbers}
   panoramicViewer.setParam("stagesize", "512,256");
   ```

   Une approche basée sur CSS est recommandée et est utilisée dans cet exemple.

1. Création et initialisation de la visionneuse.

   Une fois les étapes ci-dessus terminées, vous créez une instance de `s7viewers.PanoramicViewer` classe, transmettez toutes les informations de configuration à son constructeur et appelez la méthode `init(`) sur une instance de visionneuse. Les informations de configuration sont transmises au constructeur en tant qu’objet JSON. Au minimum, cet objet doit comporter le champ containerId qui contient le nom de l’ID de conteneur de la visionneuse et des paramètres imbriqués de l’objet JSON avec les paramètres de configuration pris en charge par la visionneuse. Dans ce cas, l’objet params doit avoir au moins une URL de diffusion d’images transmise en tant que propriété `serverUrl` et la ressource initiale en tant que paramètre de ressource. L’API d’initialisation basée sur JSON vous permet de créer et de démarrer la visionneuse avec une seule ligne de code.

   Il est important d’ajouter le conteneur de visionneuse au DOM afin que le code de la visionneuse puisse trouver l’élément de conteneur à l’aide de son identifiant. Certains navigateurs retardent la création du DOM jusqu’à la fin de la page web. Pour une compatibilité maximale, appelez la méthode `init()` juste avant la balise `BODY` de fermeture ou sur l’événement body `onload()`.

   Dans le même temps, l’élément de conteneur ne doit pas nécessairement encore faire partie de la mise en page web. Par exemple, elle peut être masquée à l’aide `display:none` style qui lui est affecté. Dans ce cas, la visionneuse retarde son processus d’initialisation jusqu’au moment où la page web ramène l’élément de conteneur dans la mise en page. Lorsque cette action se produit, le chargement de la visionneuse reprend automatiquement.

   Voici un exemple de création d’une instance de visionneuse, de transmission des options de configuration minimales nécessaires au constructeur et d’appel de la méthode `init()`. Cet exemple suppose que `panoramicViewer` est l’instance de visionneuse, `s7viewer` est le nom de l’espace réservé `DIV`, [!DNL http://s7d1.scene7.com/is/image/] est l’URL du service d’images et [!DNL Scene7SharedAssets/PanoramicImage-Sample] est la ressource.

   ```html {.line-numbers}
   <script type="text/javascript"> 
   var panoramicViewer = new s7viewers.PanoramicViewer({ 
    "containerId":"s7viewer", 
   "params":{ 
     "asset":"Scene7SharedAssets/PanoramicImage-Sample",
     "serverurl":"http://s7d1.scene7.com/is/image/"
   } 
   }).init(); 
   </script> 
   ```

   Le code suivant est un exemple complet de page web triviale qui incorpore la visionneuse panoramique avec une taille fixe :

   ```html {.line-numbers}
   <!DOCTYPE html> 
   <html> 
    <head>
    <script type="text/javascript" src="http://s7d1.scene7.com/s7viewers/html5/js/PanoramicViewer.js"></script>
    <style type="text/css">
    #s7viewer.s7panoramicviewer {
        width: 1024px;
        height: 512px;
    }
    </style>
    </head>
    <body>
    <div id="s7viewer" style="position:relative"></div>
    <script type="text/javascript">
    var panoramicViewer = new s7viewers.PanoramicViewer({
        "containerId":"s7viewer",
    "params":{
        "asset":"Scene7SharedAssets/PanoramicImage-Sample",
        "serverurl":"http://s7d1.scene7.com/is/image/"
    }
    }).init();
    </script>
    </body>
    </html>
   ```

**Incorporation de conception réactive avec hauteur illimitée**

Avec l’incorporation réactive, la page web dispose normalement d’une disposition flexible qui détermine la taille d’exécution du DIV du conteneur de la visionneuse. Pour les besoins de cet exemple, supposons que la page web autorise le DIV du conteneur de la visionneuse à prendre 80 % de la taille de la fenêtre du navigateur web, sans restriction de hauteur. Le code d’HTML de la page web pourrait se présenter comme suit :

```html {.line-numbers}
<!DOCTYPE html> 
<html> 
<head> 
<style type="text/css"> 
.holder {
	width: 80%;
}
</style>
</head>
<body>
<div class="holder"></div>
</body>
</html> 
```

L’ajout de la visionneuse à une telle page est similaire à l’incorporation de taille fixe, à la seule différence que vous n’avez pas besoin de définir explicitement la taille de la visionneuse :

1. Ajout du fichier JavaScript de la visionneuse à votre page web.
1. Définition du DIV du conteneur.
1. Création et initialisation de la visionneuse.

Toutes les étapes ci-dessus sont identiques à l’incorporation de taille fixe. Le DIV de conteneur doit être ajouté au DIV « de support » existant. Le code suivant est un exemple complet. Vous pouvez voir comment la taille de la visionneuse change lorsque le navigateur est redimensionné et comment les proportions de la visionneuse correspondent à la ressource.

```html {.line-numbers}
<!DOCTYPE html>
<html>
<head>
<script type="text/javascript" src="http://s7d1.scene7.com/s7viewers/html5/js/PanoramicViewer.js"></script>
<style type="text/css">
.holder {
	width: 80%;
}
</style>
</head>
<body>
<div class="holder">
<div id="s7viewer" style="position:relative"></div>
</div>
<script type="text/javascript">
var panoramicViewer = new s7viewers.PanoramicViewer({
	"containerId":"s7viewer",
"params":{
	"asset":"Scene7SharedAssets/PanoramicImage-Sample",
	"serverurl":"http://s7d1.scene7.com/is/image/"
}
}).init();
</script>
</body>
</html>
```

La page d’exemples suivante illustre une utilisation plus concrète de l’incorporation Responsive Design avec une hauteur illimitée :

[Démonstrations en direct](https://landing.adobe.com/en/na/dynamic-media/ctir-2755/live-demos.html)

[Autre emplacement de démonstration](https://experienceleague.adobe.com/tools/dynamic-media-demo/vlist/vlist.html?lang=fr)

**Incorporation de conception réactive avec définition de la largeur et de la hauteur**

S’il existe une incorporation Responsive Design avec la largeur et la hauteur définies, le style de la page web est différent ; les deux tailles sont fournies au `DIV` « holder » et centrées dans la fenêtre du navigateur. En outre, la page web définit la taille de l’élément `HTML` et `BODY` sur 100 % :

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

Le reste des étapes d’incorporation est identique à l’incorporation réactive avec une hauteur illimitée. L’exemple qui en résulte est

```html {.line-numbers}
<!DOCTYPE html>
<html>
<head>
<script type="text/javascript" src="http://s7d1.scene7.com/s7viewers/html5/js/PanoramicViewer.js"></script>
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
var panoramicViewer = new s7viewers.PanoramicViewer({
	"containerId":"s7viewer",
"params":{
	"asset":"Scene7SharedAssets/PanoramicImage-Sample",
	"serverurl":"http://s7d1.scene7.com/is/image/"
}
}).init();
</script>
</body>
</html>
```

**Incorporation à l’aide de l’API Setter**

Au lieu d’utiliser l’initialisation basée sur JSON, il est possible d’utiliser l’API basée sur setter et le constructeur sans args. Avec cette API, le constructeur ne prend aucun paramètre et les paramètres de configuration sont spécifiés à l’aide des méthodes d’API `setContainerId()`, `setParam()` et `setAsset()` avec des appels JavaScript distincts.

L’exemple suivant illustre l’incorporation à taille fixe avec l’API basée sur setter :

```html {.line-numbers}
<!DOCTYPE html>
<html>
<head>
<script language="text/javascript" src="http://s7d1.scene7.com/s7viewers/html5/js/PanoramicViewer.js"></script>
<style type="text/css">
#s7viewer.s7panoramicviewer {
	width: 1024;
	height: 512;
}
</style>
</head>
<body>
<div id="s7viewer" style="position:relative"></div>
<script type="text/javascript">
var panoramicViewer = new s7viewers.PanoramicViewer();
panoramicViewer.setContainerId("s7viewer");
panoramicViewer.setParam("serverurl", "http://s7d1.scene7.com/is/image/");
panoramicViewer.setAsset("Scene7SharedAssets/PanoramicImage-Sample");
panoramicViewer.init();
</script>
</body>
</html>
```
