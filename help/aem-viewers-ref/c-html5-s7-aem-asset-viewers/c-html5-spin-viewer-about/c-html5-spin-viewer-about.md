---
title: Spin
description: La visionneuse à 360° est une visionneuse d’images qui fournit une vue à 360 degrés de l’image ou même une vue multidimensionnelle si la visionneuse à 360° appropriée est utilisée. Il dispose d’outils de zoom et de rotation, d’une prise en charge du plein écran et d’un bouton de fermeture en option. Il est conçu pour fonctionner sur les ordinateurs de bureau et les appareils mobiles.
keywords: sensible
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Spin Sets
role: Developer,User
exl-id: 4c802d42-ea5b-4f28-b6ef-2689aa16839d
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '2095'
ht-degree: 0%

---

# Spin{#spin}

La visionneuse à 360° est une visionneuse d’images qui fournit une vue à 360 degrés de l’image ou même une vue multidimensionnelle si la visionneuse à 360° appropriée est utilisée. Il dispose d’outils de zoom et de rotation, d’une prise en charge du plein écran et d’un bouton de fermeture en option. Il est conçu pour fonctionner sur les ordinateurs de bureau et les appareils mobiles.

>[!NOTE]
>
>Les images qui utilisent IR (Image Rendering) ou UGC (User-Generated Content) ne sont pas prises en charge par cette visionneuse.

Type de visionneuse 503.

Voir [Configuration requise et conditions préalables](../../c-system-requirements-and-prerequisites.md#concept-9282e5b777de42cdaf72ef7ebd646842).

## URL de démonstration {#section-e1c3106f5b3e445d9b95be337c2f94e2}

[https://s7d9.scene7.com/s7viewers/html5/SpinViewer.html?asset=Scene7SharedAssets/SpinSet_Sample&amp;stagesize=500,400](https://s7d9.scene7.com/s7viewers/html5/SpinViewer.html?asset=Scene7SharedAssets/SpinSet_Sample&stagesize=500,400)

## Utilisation de la visionneuse à 360° {#section-e6c68406ecdc4de781df182bbd8088b4}

Spin Viewer représente un fichier JavaScript principal et un ensemble de fichiers d’assistance (un seul JavaScript inclure avec tous les composants SDK de la visionneuse utilisés par cette visionneuse particulière, ressources, CSS) téléchargés par la visionneuse au moment de l’exécution.

Spin Viewer peut être utilisé à la fois en mode pop-up à l’aide d’une page HTML prête pour la production fournie avec IS-Viewers ou en mode intégré, où il est intégré dans la page Web cible à l’aide d’une API documentée.

La configuration et l’habillage sont similaires à ceux des autres visionneuses. Tous les skinning peuvent être obtenus par le biais d’une feuille de style CSS personnalisée.

Voir [Référence de commande commune à tous les visualiseurs - Attributs](../../r-html5-viewer-20-cmdref-configattrib/r-html5-viewer-20-cmdref-configattrib.md#concept-850e0f2c49b949deb7cfbfd330d329bd) de configuration et [Référence de commande communs à tous les visualiseurs - URL](../../c-html5-viewer-20-cmdref-url/c-html5-viewer-20-cmdref-url.md#concept-9b337f349b7b406b8c33c7ee96b3e226)

## Interaction avec la visionneuse à 360° {#section-642e66ca38cd4032992840ec6c0b0cd2}

Spin Viewer prend en charge les gestes tactiles suivants qui sont courants dans d’autres applications mobiles. Lorsque le spectateur ne peut pas traiter le mouvement de glissement d’un utilisateur, il transfère l’événement au navigateur Web pour effectuer un défilement de page natif. Cette fonctionnalité permet à l’utilisateur de naviguer dans la page même si la visionneuse occupe la majeure partie de la zone de l’écran de l’appareil.

<table id="table_ED747CC7178448919C34A4FCD18922D0"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>Mouvement </p> </th> 
   <th colname="col2" class="entry"> <p>Description </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>Double appui </p> </td> 
   <td colname="col2"> <p> Applique un zoom sur un niveau jusqu’à ce que le facteur d’agrandissement maximal soit atteint. Le mouvement de double appui suivant réinitialise la visionneuse à son état d’affichage initial. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Pincer </p> </td> 
   <td colname="col2"> <p>Effectue un zoom avant ou arrière sur l’image. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Glissement horizontal </p> </td> 
   <td colname="col2"> <p> Si l’image est dans un état de réinitialisation, elle tourne horizontalement dans la visionneuse. </p> <p> Si l’image fait l’objet d’un zoom avant, elle se déplace horizontalement. Si l’image est déplacée vers le bord d’affichage et qu’un glissement est toujours effectué dans cette direction, le mouvement effectue un défilement natif de la page. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Balayage vertical ou battement </p> </td> 
   <td colname="col2"> <p> Si l’image est dans un état de réinitialisation, cela change l’angle de vue vertical en cas d’utilisation d’une visionneuse à 360° multidimensionnelle. Dans une visionneuse à 360° unidimensionnelle, le mouvement effectue un défilement de page natif. Ou, lorsqu’une visionneuse à 360° multidimensionnelle se trouve sur le dernier ou le premier axe de sorte que le balayage vertical n’entraîne pas de changement d’angle de vue vertical, le mouvement effectue également un défilement natif de la page. </p> <p> Si l’image fait l’objet d’un zoom avant, elle se déplace verticalement. Si l’image est déplacée vers le bord de la vue et qu’un balayage est toujours effectué dans cette direction, le geste effectue un défilement de page natif. </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>La visionneuse prend également en charge l’entrée tactile et l’entrée souris sur les appareils Windows dotés d’un écran tactile et d’une souris. Cette prise en charge est toutefois limitée aux navigateurs Web Chrome, Internet Explorer 11 et Edge uniquement.

Cette visionneuse est entièrement accessible à partir du clavier.

Voir [Accessibilité clavier et navigation](../../c-keyboard-accessibility.md#topic-f5650e9493404e55a3627c8d1366b861).

## Intégration de la visionneuse à 360° {#section-6bb5d3c502544ad18a58eafe12a13435}

Les différentes pages web ont des besoins différents en termes de comportement des observateurs. Parfois, une page Web fournit un lien qui, lorsqu’il est sélectionné, ouvre la visionneuse dans une fenêtre de navigateur distincte. Dans d’autres cas, il est nécessaire d’intégrer la visionneuse directement sur la page d’hébergement. Dans ce dernier cas, la page Web peut avoir une mise en page statique ou utiliser un design réactif qui s’affiche différemment sur différents appareils ou pour différentes tailles de fenêtre de navigateur. Pour répondre à ces besoins, la visionneuse prend en charge trois modes de fonctionnement principaux : pop-up, incorporation de taille fixe et incorporation de conception réactive.

**A propos du mode pop-up**

En mode pop-up, la visionneuse est ouverte dans une fenêtre ou un onglet de navigateur Web distinct. Il prend toute la zone de la fenêtre du navigateur et s’ajuste en cas de redimensionnement du navigateur ou de changement d’orientation d’un appareil mobile.

Le mode pop-up est le plus courant pour les appareils mobiles. La page Web charge la visionneuse à l’aide `window.open()` d’JavaScript appel, d’un élément HTML correctement configuré `A` ou de toute autre méthode appropriée.

Il est recommandé d’utiliser une page HTML prête à l’emploi pour le mode de fonctionnement des fenêtres pop-up. Dans ce cas, il s’appelle [!DNL SpinViewer.html] et se trouve dans le sous-dossier [!DNL html5/] de votre déploiement d’observateurs IS standard :

[!DNL <s7viewers_root>/html5/SpinViewer.html]

Vous pouvez effectuer une personnalisation visuelle en appliquant un CSS personnalisé.

Voici un exemple de code HTML qui permet d’ouvrir la visionneuse dans une nouvelle fenêtre :

```html {.line-numbers}
<a href="https://s7d1.scene7.com/s7viewers/html5/SpinViewer.html?asset=Scene7SharedAssets/SpinSet_Sample&stagesize=500,400" 
target="_blank">Open popup viewer</a>
```

**À propos du mode d’incorporation de taille fixe et du mode d’incorporation de conception réactive**

En mode intégré, la visionneuse est ajoutée à la page Web existante, qui peut déjà contenir du contenu client non lié à la visionneuse. Le spectateur n’occupe normalement qu’une partie de l’espace d’une page Web.

Les principaux cas d’utilisation sont les pages Web orientées vers les ordinateurs de bureau ou les tablettes, ainsi que les pages de conception réactive qui ajustent automatiquement la mise en page en fonction du type d’appareil.

L’incorporation de taille fixe est utilisée lorsque la visionneuse ne modifie pas sa taille après le chargement initial. Cette action constitue le meilleur choix pour les pages Web dotées d’une disposition statique.

L’incorporation de conception réactive suppose que la visionneuse doit se redimensionner au moment de l’exécution en réponse au changement de taille de son conteneur `DIV`. Le cas d’utilisation le plus courant est l’ajout d’une visionneuse à une page Web qui utilise une mise en page flexible.

En mode d’incorporation de conception réactive, la visionneuse se comporte différemment selon la façon dont la page Web dimensionne son conteneur `DIV`. Si la page Web définit uniquement la largeur du conteneur `DIV`, en laissant sa hauteur illimitée, le visualisateur choisit automatiquement sa hauteur en fonction du format de la ressource utilisée. Cette fonctionnalité garantit que l’actif s’intègre parfaitement dans la vue sans aucun rembourrage sur les côtés. Ce cas d’utilisation est le plus courant pour les pages Web utilisant des structures de mise en page de conception réactive telles que Bootstrap ou Foundation.

Sinon, si la page Web définit à la fois la largeur et la hauteur du conteneur `DIV`de la visionneuse, celle-ci remplit uniquement cette zone et suit la taille fournie par la mise en page Web. Un bon exemple peut être l’incorporation de la visionneuse dans une superposition modale, où la superposition est dimensionnée en fonction de la taille de la fenêtre du navigateur Web.

**Incorporation de taille fixe**

Pour ajouter la visionneuse à 360° à une page Web, procédez comme suit :

1. Ajout du fichier JavaScript de visionneuse à votre page Web.
1. Définition du conteneur `DIV`.
1. Définition de la taille de la visionneuse.
1. Création et initialisation de la visionneuse.

1. Ajout du fichier JavaScript de visionneuse à votre page Web.

   Pour créer une visionneuse, vous devez ajouter une balise de script dans l’en-tête HTML. Avant d’utiliser l’API de visionneuse, veillez à inclure `SpinViewer.js`le fichier . `SpinViewer.js` se trouve dans le [!DNL html5/js/] sous-dossier de votre déploiement IS-Viewers standard :

   `<s7viewers_root>/html5/js/SpinViewer.js`

   Vous pouvez utiliser un chemin d’accès relatif si la visionneuse est déployée sur l’un des serveurs Dynamic Media Adobe et qu’elle est diffusée à partir du même domaine. Sinon, vous spécifiez un chemin d’accès complet à l’un des serveurs Adobe Dynamic Media sur lesquels les IS-Viewers sont installés.

   Le chemin d’accès relatif ressemble à ce qui suit :

   ```html {.line-numbers}
    <script language="javascript" type="text/javascript" src="/s7viewers/html5/js/SpinViewer.js"></script>
   ```

   >[!NOTE]
   >
   >Référencez uniquement le fichier JavaScript `include` de visionneuse principal sur votre page. Ne référencez pas de fichiers JavaScript supplémentaires dans le code de la page Web qui pourraient être téléchargés par la logique du visualiseur au moment de l’exécution. En particulier, ne référencez pas directement la bibliothèque SDK `Utils.js` HTML5 chargée par la visionneuse à partir du chemin d’accès `/s7viewers` au contexte (SDK `include`consolidé). La raison en est que l’emplacement des bibliothèques d’exécution ou des bibliothèques de `Utils.js` visionneuse similaires est entièrement géré par la logique de la visionneuse et que l’emplacement change entre les versions de la visionneuse. Adobe ne conserve pas les anciennes versions de la visionneuse `includes` secondaire sur le serveur.
   >
   >
   >Par conséquent, le fait de placer une référence directe à une JavaScript `include` secondaire utilisée par l’utilisateur sur la page interrompt la fonctionnalité de la visionneuse à l’avenir lorsqu’une nouvelle version du produit est déployée.

1. Définition du conteneur DIV.

   Ajoutez un élément DIV vide à la page dans laquelle vous souhaitez que la visionneuse apparaisse. L’ID de l’élément DIV doit être défini, car cet identifiant est transmis ultérieurement à l’API de visionneuse.

   L’espace réservé DIV est un élément positionné, ce qui signifie que la `position` propriété CSS est définie sur `relative` ou `absolute`.

   Voici un exemple d’élément DIV d’espace réservé défini :

   ```html {.line-numbers}
   <div id="s7viewer" style="position:relative"></div>
   ```

1. Définition de la taille de la visionneuse

   Vous pouvez définir la taille statique de la visionneuse en la déclarant pour `.s7spinviewer` la classe CSS de niveau supérieur en unités absolues ou en utilisant le `stagesize` modificateur.

   Vous pouvez placer le dimensionnement dans CSS directement sur la page HTML ou dans un fichier CSS de visionneuse personnalisé. Il est ensuite attribué à un enregistrement de paramètre prédéfini de visionneuse dans Dynamic Media Classic, ou transmis explicitement à l’aide d’une commande de style.

   Voir [Personnalisation de la visionneuse](../../c-html5-s7-aem-asset-viewers/c-html5-spin-viewer-about/c-html5-spin-viewer-customizingviewer/c-html5-spin-viewer-customizingviewer.md#concept-464f3bfa55764bc09c92d8c7480b0b55) à 360° pour plus d’informations sur le style de la visionneuse avec CSS.

   Voici un exemple de définition d’une taille de visionneuse statique sur une page HTML :

   ```html {.line-numbers}
   #s7viewer.s7spinviewer { 
    width: 640px; 
    height: 480px; 
   }
   ```

   Vous pouvez définir le modificateur dans l’enregistrement `stagesize` des paramètres prédéfinis de la visionneuse dans Dynamic Media Classic. Vous pouvez également le transmettre explicitement avec le code d’initialisation de la visionneuse avec `params` collection, ou sous la forme d’un appel d’API comme décrit dans la section Référence des commandes, comme suit :

   ```html {.line-numbers}
    spinViewer.setParam("stagesize", 
   "640,480");
   ```

   Une approche basée sur le code CSS est recommandée et est utilisée dans cet exemple.

1. Création et initialisation de la visionneuse.

   Une fois les étapes ci-dessus terminées, vous créez une instance de `s7viewers.SpinViewer` classe, transmettez toutes les informations de configuration à son constructeur et appelez `init()` méthode sur une instance de visionneuse. Les informations de configuration sont transmises au constructeur en tant qu’objet JSON. Au minimum, cet objet comporte `containerId` champ qui contient le nom de l’ID de conteneur de visionneuse et de l’objet JSON `params` imbriqué avec les paramètres de configuration pris en charge par la visionneuse. Dans ce cas d’objet `params`, au moins l’URL du service d’images doit être transmise en tant que propriété `serverUrl` et la ressource initiale doit être transmise en tant que paramètre `asset`. L’API d’initialisation basée sur JSON vous permet de créer et de démarrer la visionneuse avec une seule ligne de code.

   Il est important d’ajouter le conteneur de visionneuse au DOM afin que le code de visionneuse puisse trouver l’élément conteneur par son identifiant. Certains navigateurs retardent la création de DOM jusqu’à la fin de la page Web. Pour une compatibilité maximale, appelez la `init()` méthode juste avant la balise de fermeture `BODY` , ou sur l’événement body `onload()` .

   Dans le même temps, l’élément conteneur ne doit pas nécessairement faire partie de la mise en page Web pour le moment. Par exemple, il peut être masqué à l’aide du `display:none` style qui lui est attribué. Dans ce cas, la visionneuse retarde son processus d’initialisation jusqu’au moment où la page Web ramène l’élément conteneur à la mise en page. Lorsque cette action se produit, le chargement de la visionneuse reprend automatiquement.

   Voici un exemple de création d’une instance de visionneuse, en transmettant les options de configuration minimales nécessaires au constructeur et en appelant la `init()` méthode. L’exemple suppose qu’il `spinViewer` s’agit de l’instance de visionneuse, du nom de l’espace réservé, `s7viewer` de l’URL `DIV`[!DNL http://s7d1.scene7.com/is/image/] du serveur d’images et [!DNL Scene7SharedAssets/SpinSet_Sample] de l’actif.

   ```html {.line-numbers}
   <script type="text/javascript"> 
   var spinViewer = new s7viewers.SpinViewer({ 
    "containerId":"s7viewer", 
   "params":{ 
    "asset":"Scene7SharedAssets/SpinSet_Sample", 
    "serverurl":"http://s7d1.scene7.com/is/image/" 
   } 
   }).init(); 
   </script>
   ```

   Le code suivant est un exemple complet de page Web triviale qui intègre la visionneuse à 360° avec une taille fixe :

   ```html {.line-numbers}
   <!DOCTYPE html> 
   <html> 
   <head> 
   <script type="text/javascript" src="http://s7d1.scene7.com/s7viewers/html5/js/SpinViewer.js"></script> 
   <style type="text/css"> 
   #s7viewer.s7spinviewer { 
    width: 640px; 
    height: 480px; 
   } 
   </style> 
   </head> 
   <body> 
   <div id="s7viewer" style="position:relative"></div> 
   <script type="text/javascript"> 
   var spinViewer = new s7viewers.SpinViewer({ 
    "containerId":"s7viewer", 
   "params":{ 
    "asset":"Scene7SharedAssets/SpinSet_Sample", 
    "serverurl":"http://s7d1.scene7.com/is/image/" 
   } 
   }).init(); 
   </script> 
   </body> 
   </html>
   ```

**Intégration de conception réactive avec une hauteur illimitée**

Avec l’intégration de conception réactive, la page Web a normalement une sorte de mise en page flexible en place qui dicte la taille d’exécution du conteneur `DIV`de la visionneuse. Pour les besoins de cet exemple, supposons que la page Web autorise le conteneur `DIV` du spectateur à prendre 40 % de la taille de la fenêtre du navigateur Web, en laissant sa hauteur sans restriction. Le code HTML résultant de la page Web ressemble à ce qui suit :

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

L’ajout de la visionneuse à une telle page est similaire à l’incorporation de taille fixe, à la seule différence que vous n’avez pas besoin de définir explicitement la taille de la visionneuse.

1. Ajout du fichier JavaScript de visionneuse à votre page Web.
1. Définition du conteneur DIV.
1. Création et initialisation de la visionneuse.

Toutes les étapes ci-dessus sont identiques à celles de l’incorporation à taille fixe. Ajoutez l’`DIV` de conteneur au `DIV` « holder » existant. Le code suivant en est un exemple complet. Vous pouvez voir comment la taille de la visionneuse change lorsque le navigateur est redimensionné et comment les proportions de la visionneuse correspondent à la ressource.

```html {.line-numbers}
<!DOCTYPE html> 
<html> 
<head> 
<script type="text/javascript" src="http://s7d1.scene7.com/s7viewers/html5/js/SpinViewer.js"></script> 
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
var spinViewer = new s7viewers.SpinViewer({ 
 "containerId":"s7viewer", 
"params":{ 
 "asset":"Scene7SharedAssets/SpinSet_Sample", 
 "serverurl":"http://s7d1.scene7.com/is/image/" 
} 
}).init(); 
</script> 
</body> 
</html>
```

La page d’exemples suivante illustre d’autres cas d’utilisation réels d’incorporation de conception réactive avec une hauteur non limitée :

[Démonstrations en direct](https://landing.adobe.com/en/na/dynamic-media/ctir-2755/live-demos.html)

[Autre emplacement de démonstration](https://experienceleague.adobe.com/tools/dynamic-media-demo/vlist/vlist.html)

**Intégration de taille flexible avec largeur et hauteur définies**

S’il existe un incorporation de taille flexible avec la largeur et la hauteur définies, le style de la page Web est différent. C’est-à-dire qu’il fournit les deux tailles au « titulaire » `DIV` et le centre dans la fenêtre du navigateur. En outre, la page web définit la taille de l’élément `HTML` ET `BODY` sur 100 % :

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

Les étapes d’incorporation restantes sont identiques à l’incorporation de conception réactive avec une hauteur illimitée. L’exemple qui en résulte est le suivant :

```html {.line-numbers}
<!DOCTYPE html> 
<html> 
<head> 
<script type="text/javascript" src="http://s7d1.scene7.com/s7viewers/html5/js/SpinViewer.js"></script> 
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
var spinViewer = new s7viewers.SpinViewer({ 
 "containerId":"s7viewer", 
"params":{ 
 "asset":"Scene7SharedAssets/SpinSet_Sample", 
 "serverurl":"http://s7d1.scene7.com/is/image/" 
} 
}).init(); 
</script> 
</body> 
</html>
```

**Incorporation à l’aide de l’API Setter**

Au lieu d’utiliser l’initialisation basée sur JSON, il est possible d’utiliser une API basée sur setter et un constructeur no-args. Avec cette API, le constructeur ne prend aucun paramètre et les paramètres de configuration sont spécifiés à l’aide de `setContainerId()`, `setParam()`et `setAsset()` des méthodes API avec des appels JavaScript distincts.

L’exemple suivant illustre l’incorporation de taille fixe avec l’API basée sur setter :

```html {.line-numbers}
<!DOCTYPE html> 
<html> 
<head> 
<script type="text/javascript" src="http://s7d1.scene7.com/s7viewers/html5/js/SpinViewer.js"></script> 
<style type="text/css"> 
#s7viewer.s7spinviewer { 
 width: 640px; 
 height: 480px; 
} 
</style> 
</head> 
<body> 
<div id="s7viewer" style="position:relative"></div> 
<script type="text/javascript"> 
var spinViewer = new s7viewers.SpinViewer(); 
spinViewer.setContainerId("s7viewer"); 
spinViewer.setParam("serverurl", "http://s7d1.scene7.com/is/image/"); 
spinViewer.setAsset("Scene7SharedAssets/SpinSet_Sample"); 
spinViewer.init(); 
</script> 
</body> 
</html>
```
