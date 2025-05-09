---
title: Visionneuse panoramique
description: La visionneuse panoramique HTML5 est une visionneuse d’images qui affiche une image panoramique. L’objectif de cette visionneuse est d’afficher un panorama sphérique, également appelé image équirectangulaire. Il prend en charge le panoramique et le panoramique automatiques par mouvement gyroscopique. Il est conçu pour fonctionner sur les ordinateurs de bureau et les appareils mobiles. Le mode d’affichage de la réalité virtuelle est disponible sur les appareils mobiles pris en charge.
keywords: responsive
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Panoramic
role: Developer,User
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '1924'
ht-degree: 0%

---

# Panoramique{#panoramic}

La visionneuse panoramique HTML5 est une visionneuse d’images qui affiche une image panoramique. L’objectif de cette visionneuse est d’afficher un panorama sphérique, également appelé image équirectangulaire. Il prend en charge le panoramique et le panoramique automatiques par mouvement gyroscopique. Il est conçu pour fonctionner sur les ordinateurs de bureau et les appareils mobiles. Le mode d’affichage de la réalité virtuelle est disponible sur les appareils mobiles pris en charge.

Voir [ Configuration requise et conditions préalables](../../c-system-requirements-and-prerequisites.md#concept-9282e5b777de42cdaf72ef7ebd646842).


Type de visionneuse 514.

## URL de démonstration {#section-e1c3106f5b3e445d9b95be337c2f94e2}

[http://s7d1.scene7.com/s7viewers/html5/PanoramicViewer.html?asset=Scene7SharedAssets/PanoramicImage-Sample](http://s7d1.scene7.com/s7viewers/html5/PanoramicViewer.html?asset=Scene7SharedAssets/PanoramicImage-Sample)

## Utilisation de la visionneuse panoramique {#section-f21ac23d3f6449ad9765588d69584772}

La visionneuse panoramique HTML5 représente un fichier JavaScript principal et un ensemble de fichiers d’assistance téléchargés par la visionneuse au moment de l’exécution. L’ensemble de fichiers d’assistance est une seule inclusion JavaScript avec tous les composants SDK de visionneuse HTML5 utilisés par cette visionneuse, ressources et CSS particulière.
La visionneuse panoramique HTML5 peut être utilisée en mode contextuel à l’aide de la page d’HTML prête pour la production fournie avec les visionneuses IS ou en mode intégré, où elle est intégrée à la page web cible à l’aide d’une API documentée.
La configuration et l’habillage sont similaires à ceux des autres visionneuses HTML5. L’habillage peut être effectué au moyen d’une feuille CSS personnalisée.

Voir [Référence de commande commune à toutes les visionneuses - Attributs de configuration](../../r-html5-viewer-20-cmdref-configattrib/r-html5-viewer-20-cmdref-configattrib.md#concept-850e0f2c49b949deb7cfbfd330d329bd) et [Référence de commande commune à toutes les visionneuses - URL](../../c-html5-viewer-20-cmdref-url/c-html5-viewer-20-cmdref-url.md#concept-9b337f349b7b406b8c33c7ee96b3e226)

## Interaction avec la visionneuse panoramique HTML5 {#section-ab66eb6955aa4a8aa6d14a3b3acfed3f}

La visionneuse panoramique HTML5 prend en charge le panoramique automatique et la navigation par glisser ou mouvement gyroscopique.

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
   <td colname="col2"> <p>Effectuez un panoramique automatique et effectuez un glisser-déposer pour naviguer. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Appareil tactile </p> </td> 
   <td colname="col2"> <p>Effectuez un panoramique automatique et effectuez un glisser-déposer pour naviguer par défaut. Navigation par mouvement gyroscopique en mode de rendu VR (vrrender=true).
 </p> </td> 
  </tr> 
 </tbody> 
</table>

La visionneuse prend en charge les entrées tactiles et de souris sur les appareils Windows dotés d’un écran tactile et d’une souris. Toutefois, cette prise en charge est limitée aux navigateurs Web Chrome, Internet Explorer 11 et Edge uniquement.
La visionneuse panoramique peut afficher des images panoramiques en mode réalité virtuelle (VR) en spécifiant le modificateur de rendu. Lorsque le rendu est activé, une image panoramique s’affiche dans des écrans fractionnés. Un cas d’utilisation courant serait de diffuser l’image dans un téléphone portable monté dans un casque de réalité virtuelle, fournissant des images distinctes pour chaque oeil. La visionneuse répond au mouvement gyroscopique de la tête et navigue à travers l’image.

## Intégration de la visionneuse panoramique HTML5 {#section-6bb5d3c502544ad18a58eafe12a13435}

Le comportement de la visionneuse varie en fonction des pages web. Il arrive qu’une page web fournisse un lien. La sélection de ce lien ouvre la visionneuse dans une fenêtre de navigateur distincte. Dans d’autres cas, il peut être nécessaire d’incorporer la visionneuse dans la page d’hébergement. Dans ce cas, la page web peut avoir une mise en page statique ou être &quot;réactive&quot; et s’afficher différemment sur différents appareils ou pour différentes tailles de fenêtre de navigateur. Pour répondre à ces besoins, la visionneuse prend en charge trois modes de fonctionnement principaux : fenêtre contextuelle, incorporation des tailles fixes et incorporation réactive.

**À propos du mode pop-up**

En mode contextuel, la visionneuse s’ouvre dans une fenêtre ou un onglet de navigateur Web distinct. Elle prend toute la zone de la fenêtre du navigateur et s’ajuste au cas où le navigateur serait redimensionné ou l’orientation du périphérique modifiée.

Ce mode est le plus courant pour les appareils mobiles. La page web charge la visionneuse à l’aide de l’appel JavaScript `window.open()`, d’un élément d’HTML correctement configuré ou de toute autre méthode appropriée.

Il est recommandé d’utiliser une page d’HTML d’usine pour le mode de fonctionnement de la fenêtre contextuelle. Il s’appelle [!DNL PanoramicViewer.html] et se trouve sous le sous-dossier [!DNL html5/] de votre déploiement IS-Viewers standard :

[!DNL <s7viewers_root>/html5/PanoramicViewer.html]

La personnalisation visuelle peut être réalisée en appliquant une page CSS personnalisée.

Voici un exemple de code d’HTML qui ouvre la visionneuse dans la nouvelle fenêtre :

```html {.line-numbers}
<a href="http://s7d1.scene7.com/s7viewers/html5/PanoramicViewer.html?asset=Scene7SharedAssets/PanoramicImage-Sample" target="_blank">Open popup viewer</a>
```

**À propos du mode d’incorporation à taille fixe et du mode d’incorporation réactif**

En mode incorporé, la visionneuse est ajoutée à la page web existante, qui peut déjà comporter du contenu client qui n’est pas lié à la visionneuse. Normalement, la visionneuse occupe uniquement une partie de l’espace des pages web.

Les principaux cas d’utilisation sont les pages web orientées vers les ordinateurs de bureau ou les tablettes, ainsi que les pages web réactives qui ajustent automatiquement la mise en page en fonction du type de périphérique.

L’incorporation des tailles fixes est utilisée lorsque la visionneuse ne modifie pas sa taille après le chargement initial. Cette méthode est la meilleure solution pour les pages web avec une mise en page statique.

L’incorporation réactive suppose que la visionneuse doit être redimensionnée au moment de l’exécution en réponse au changement de taille de son conteneur DIV. Le cas d’utilisation le plus courant consiste à ajouter une visionneuse à une page web qui utilise une mise en page flexible.

En mode réactif, la visionneuse se comporte différemment selon la manière dont la page web dimensionne son conteneur DIV. Si la page web définit uniquement la largeur du conteneur DIV, sans restriction de hauteur, la visionneuse choisit automatiquement sa hauteur en fonction des proportions de la ressource utilisée. Cette méthode permet de s’assurer que la ressource s’intègre parfaitement dans la vue sans marge intérieure sur les côtés. Ce cas d’utilisation est le plus courant pour les pages web qui utilisent des structures de mise en page réactive telles que Bootstrap, Foundation, etc.

Dans le cas contraire, si la page web définit la largeur et la hauteur du conteneur DIV de la visionneuse, celle-ci remplit cette zone et suit la taille fournie par la mise en page de la page web. Un bon exemple consiste à incorporer la visionneuse dans une superposition modale, où la superposition est dimensionnée en fonction de la taille de la fenêtre du navigateur web.

**Intégration de taille fixe**

Pour ajouter la visionneuse à une page web, procédez comme suit :

1. Ajout du fichier JavaScript de la visionneuse à votre page web.
1. Définition du conteneur `DIV`.
1. Définition de la taille de la visionneuse.
1. Création et initialisation de la visionneuse.

1. Ajout du fichier JavaScript de la visionneuse à votre page web.

   Pour créer une visionneuse, vous devez ajouter une balise de script dans l’en-tête de l’HTML. Avant de pouvoir utiliser l’API de visionneuse, veillez à inclure [!DNL PanoramicViewer.js]. Le fichier [!DNL PanoramicViewer.js] se trouve sous le sous-dossier [!DNL html5/js/] de votre déploiement IS-Viewers standard :

[!DNL <s7viewers_root>/html5/js/PanoramicViewer.js]

Vous pouvez utiliser un chemin relatif si la visionneuse est déployée sur l’un des serveurs Adobe Dynamic Media Classic et qu’elle est diffusée à partir du même domaine. Dans le cas contraire, vous spécifiez un chemin d’accès complet à l’un des serveurs Adobe Dynamic Media Classic sur lesquels les visionneuses IS sont installées.

Le chemin relatif ressemble à ce qui suit :

```html {.line-numbers}
<script language="javascript" type="text/javascript" src="/s7viewers/html5/js/PanoramicViewer.js"></script>
```

>[!NOTE]
>
>Ne référencez que le fichier JavaScript `include` de la visionneuse principale sur votre page. Ne référencez aucun fichier JavaScript supplémentaire dans le code de page web qui peut être téléchargé par la logique de la visionneuse au moment de l’exécution. En particulier, ne référencez pas directement la bibliothèque `Utils.js` du SDK HTML5 chargée par la visionneuse à partir du chemin de contexte `/s7viewers` (appelé SDK consolidé `include`). La raison en est que l’emplacement de `Utils.js` ou de bibliothèques de visionneuses d’exécution similaires est entièrement géré par la logique de la visionneuse et que l’emplacement change entre les versions de la visionneuse. Adobe ne conserve pas les anciennes versions de la visionneuse secondaire `includes` sur le serveur.
>
>
>Par conséquent, le fait de placer une référence directe à tout JavaScript secondaire `include` utilisé par la visionneuse sur la page rompt la fonctionnalité de visionneuse à l’avenir lorsqu’une nouvelle version de produit est déployée.

1. Définition du conteneur DIV.

   Ajoutez un élément DIV vide à la page sur laquelle vous souhaitez que la visionneuse apparaisse. L’ID de l’élément DIV doit être défini, car cet ID est transmis ultérieurement à l’API de visionneuse. La taille du DIV est spécifiée via CSS.

   L’espace réservé DIV est un élément positionné, ce qui signifie que la propriété CSS `position` est définie sur `relative` ou `absolute`.


   Voici un exemple d’élément DIV d’espace réservé défini :

   ```html {.line-numbers}
   <div id="s7viewer" style="position:relative"></div> 
   ```

1. Définition de la taille de la visionneuse

   Vous pouvez définir la taille statique de la visionneuse en la déclarant pour la classe CSS de niveau supérieur `.s7panoramicviewer` en unités absolues ou en utilisant le modificateur `stagesize`.

   Le dimensionnement en CSS peut être placé directement sur la page d’HTML ou dans un fichier CSS de visionneuse personnalisé, qui est ultérieurement affecté à un enregistrement de paramètre prédéfini de visionneuse dans AOD ou transmis explicitement à l’aide de la commande de style. Pour plus d’informations sur le style de la visionneuse avec CSS, voir Personnalisation de la visionneuse . Vous trouverez ci-dessous un exemple de définition de la taille de la visionneuse statique dans la page d’HTML :

   ```html {.line-numbers}
   #s7viewer.s7panoramicviewer {
     width: 1024px;
     height: 512px;
   }
   ```

   Le modificateur `stagesize` peut être transmis explicitement avec le code d’initialisation de la visionneuse avec la collection params ou en tant qu’appel API, comme décrit dans la section Référence de commande, comme suit :

   ```html {.line-numbers}
   panoramicViewer.setParam("stagesize", "512,256");
   ```

   L’approche basée sur CSS est recommandée et est utilisée dans cet exemple.

1. Création et initialisation de la visionneuse.

   Une fois que vous avez suivi les étapes ci-dessus, vous créez une instance de la classe `s7viewers.PanoramicViewer`, transmettez toutes les informations de configuration à son constructeur et appelez la méthode `init(` sur une instance de visionneuse. Les informations de configuration sont transmises au constructeur sous la forme d’un objet JSON. Au minimum, cet objet doit comporter un champ containerId qui contient le nom de l’ID de conteneur de la visionneuse et l’objet JSON params imbriqué avec les paramètres de configuration pris en charge par la visionneuse. Dans ce cas, l’objet params doit avoir au moins l’URL de diffusion d’images transmise comme propriété `serverUrl` et la ressource initiale comme paramètre de ressource. L’API d’initialisation basée sur JSON vous permet de créer et de démarrer la visionneuse avec une seule ligne de code.

   Il est important que le conteneur de la visionneuse soit ajouté au modèle DOM afin que le code de la visionneuse puisse trouver l’élément de conteneur en fonction de son identifiant. Certains navigateurs retardent la création du DOM jusqu’à la fin de la page web. Pour bénéficier d’une compatibilité maximale, appelez la méthode `init()` juste avant la balise de fermeture `BODY` ou sur l’événement body `onload()` .

   Dans le même temps, l’élément de conteneur ne doit pas nécessairement faire partie de la mise en page web pour l’instant. Par exemple, il peut être masqué à l’aide du style `display:none` qui lui est affecté. Dans ce cas, la visionneuse retarde son processus d’initialisation jusqu’au moment où la page web ramène l’élément de conteneur à la mise en page. Lorsque cette action se produit, le chargement de la visionneuse reprend automatiquement.

   Voici un exemple de création d’une instance de visionneuse, de transmission des options de configuration minimales nécessaires au constructeur et d’appel de la méthode `init()`. Cet exemple suppose que `panoramicViewer` est l’instance de visionneuse, `s7viewer` est le nom de l’espace réservé `DIV`, [!DNL http://s7d1.scene7.com/is/image/] est l’URL de diffusion d’images et [!DNL Scene7SharedAssets/PanoramicImage-Sample] est la ressource.

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

   Le code suivant est un exemple complet d’une page web triviale qui incorpore la visionneuse panoramique à une taille fixe :

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

**Intégration de conception réactive avec une hauteur libre**

Avec l’incorporation réactive, la page web dispose normalement d’une sorte de disposition flexible qui détermine la taille d’exécution du conteneur DIV de la visionneuse. Pour les besoins de cet exemple, supposons que la page web autorise le conteneur DIV du visiteur à prendre 80 % de la taille de la fenêtre du navigateur web, en ne restreignant pas sa hauteur. Le code d’HTML de la page web peut se présenter comme suit :

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

L’ajout de la visionneuse à cette page est similaire à l’incorporation de taille fixe, à la seule différence que vous n’avez pas besoin de définir explicitement la taille de la visionneuse :

1. Ajout du fichier JavaScript de la visionneuse à votre page web.
1. Définition du conteneur DIV.
1. Création et initialisation de la visionneuse.

Toutes les étapes ci-dessus sont identiques à l’incorporation de tailles fixes. Les balises DIV du conteneur doivent être ajoutées au DIV &quot;détenteur&quot; existant. Le code suivant est un exemple complet. Vous pouvez voir comment la taille de la visionneuse change lorsque le navigateur est redimensionné et comment le rapport d’aspect de la visionneuse correspond à la ressource.

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

La page d’exemples suivante illustre une utilisation plus concrète de l’incorporation de conceptions réactives avec une hauteur illimitée :

[Démonstrations en direct](https://landing.adobe.com/en/na/dynamic-media/ctir-2755/live-demos.html)

[Autre emplacement de démonstration](https://experienceleague.adobe.com/tools/dynamic-media-demo/vlist/vlist.html?lang=fr)

**Intégration de conception réactive avec largeur et hauteur définies**

Si une conception réactive est incorporée avec une largeur et une hauteur définies, le style de la page web est différent. Il fournit les deux tailles au &quot; détenteur &quot; `DIV` et le centre dans la fenêtre du navigateur. En outre, la page web définit la taille de l’élément `HTML` et `BODY` sur 100 % :

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

Les autres étapes d’incorporation sont identiques à l’incorporation réactive avec une hauteur libre. L’exemple qui en résulte est :

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

**Incorporation à l’aide d’une API basée sur setter**

Au lieu d’utiliser l’initialisation basée sur JSON, il est possible d’utiliser une API basée sur un setter et un constructeur sans args. Avec cette API, le constructeur ne prend aucun paramètre et les paramètres de configuration sont spécifiés à l’aide des méthodes d’API `setContainerId()`, `setParam()` et `setAsset()` avec des appels JavaScript distincts.

L’exemple suivant illustre l’incorporation de tailles fixes avec l’API basée sur setter :

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
