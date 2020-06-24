---
description: La visionneuse à 360° est une visionneuse d’images qui fournit une vue de l’image à 360 degrés, voire une vue multidimensionnelle, si une visionneuse à 360° appropriée est utilisée. Il comporte des outils de zoom et de rotation, une prise en charge en plein écran et un bouton de fermeture en option. Il est conçu pour fonctionner sur les ordinateurs de bureau et les périphériques mobiles.
keywords: responsive
seo-description: La visionneuse à 360° est une visionneuse d’images qui fournit une vue de l’image à 360 degrés, voire une vue multidimensionnelle, si une visionneuse à 360° appropriée est utilisée. Il comporte des outils de zoom et de rotation, une prise en charge en plein écran et un bouton de fermeture en option. Il est conçu pour fonctionner sur les ordinateurs de bureau et les périphériques mobiles.
seo-title: Spin
solution: Experience Manager
title: Spin
topic: Dynamic media
uuid: 5d5cdf83-cfe8-48cd-af74-b270f7400b14
translation-type: tm+mt
source-git-commit: 6380d839a794cbf82854a2ecd28c18f16f06d4c7
workflow-type: tm+mt
source-wordcount: '2166'
ht-degree: 0%

---


# Spin{#spin}

La visionneuse à 360° est une visionneuse d’images qui fournit une vue de l’image à 360 degrés, voire une vue multidimensionnelle, si une visionneuse à 360° appropriée est utilisée. Il comporte des outils de zoom et de rotation, une prise en charge en plein écran et un bouton de fermeture en option. Il est conçu pour fonctionner sur les ordinateurs de bureau et les périphériques mobiles.

>[!NOTE]
>
>Cette visionneuse ne prend pas en charge les images qui utilisent la fonction IR (Image Rendering) ou UGC (User-Generated Content).

Type de visionneuse 503.

Voir Configuration [requise et configuration requise](../../c-system-requirements-and-prerequisites.md#concept-9282e5b777de42cdaf72ef7ebd646842).

## URL de démonstration {#section-e1c3106f5b3e445d9b95be337c2f94e2}

[https://s7d9.scene7.com/s7viewers/html5/SpinViewer.html?asset=Scene7SharedAssets/SpinSet_Sample&amp;stagesize=500,400](https://s7d9.scene7.com/s7viewers/html5/SpinViewer.html?asset=Scene7SharedAssets/SpinSet_Sample&amp;stagesize=500,400)

## Utilisation de la visionneuse à 360° {#section-e6c68406ecdc4de781df182bbd8088b4}

La visionneuse à 360° représente un fichier JavaScript principal et un ensemble de fichiers d’aide (un seul fichier JavaScript est inclus avec tous les composants du SDK de la visionneuse utilisés par cette visionneuse, ressources et CSS) téléchargés par la visionneuse au moment de l’exécution.

La visionneuse à 360° peut être utilisée à la fois en mode contextuel à l’aide d’une page HTML prête à l’emploi fournie avec des visionneuses IS ou en mode intégré, où elle est intégrée dans la page Web de cible à l’aide d’une API documentée.

La configuration et l’habillage sont similaires à ceux des autres visionneuses. Tous les habillages peuvent être réalisés via une page CSS personnalisée.

Voir Référence de [commande commune à toutes les visionneuses - Attributs](../../r-html5-viewer-20-cmdref-configattrib/r-html5-viewer-20-cmdref-configattrib.md#concept-850e0f2c49b949deb7cfbfd330d329bd) de configuration et référence de [commande commune à toutes les visionneuses - URL](../../c-html5-viewer-20-cmdref-url/c-html5-viewer-20-cmdref-url.md#concept-9b337f349b7b406b8c33c7ee96b3e226)

## Interaction avec la visionneuse à 360° {#section-642e66ca38cd4032992840ec6c0b0cd2}

Spin Viewer prend en charge les mouvements tactiles suivants, courants dans d’autres applications mobiles. Lorsque le lecteur ne peut pas traiter le mouvement de glissement d’un utilisateur, il transfère le événement vers le navigateur Web pour effectuer un défilement de page natif. Cela permet à l’utilisateur de parcourir la page même si le lecteur occupe la majeure partie de l’écran du périphérique.

<table id="table_ED747CC7178448919C34A4FCD18922D0"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>Mouvement </p> </th> 
   <th colname="col2" class="entry"> <p>Description </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>Doublon </p> </td> 
   <td colname="col2"> <p> Applique un zoom à un niveau jusqu’à ce que le zoom maximal soit atteint. Le mouvement de pression du doublon suivant réinitialise l’affichage initial de la visionneuse. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Pincer </p> </td> 
   <td colname="col2"> <p>Effectue un zoom avant ou arrière sur l’image. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Glissement ou clic horizontal </p> </td> 
   <td colname="col2"> <p> Si l’image est à l’état de réinitialisation, elle s’étend sur la visionneuse horizontalement. </p> <p> Si l’image est agrandie, elle déplace l’image horizontalement. Si l’image est déplacée vers le bord de la vue et qu’un glissement est toujours effectué dans cette direction, le mouvement effectue un défilement de page natif. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Glissement ou clic vertical </p> </td> 
   <td colname="col2"> <p> Si l’image est à l’état reset, elle modifie l’angle de vue vertical en cas d’utilisation d’une visionneuse à 360° multidimensionnelle. Dans une visionneuse à 360° unidimensionnelle ou lorsqu’une visionneuse à 360° multidimensionnelle se trouve sur le dernier ou le premier axe, de sorte que le glissement vertical n’entraîne pas de changement de l’angle de vue vertical, le mouvement effectue un défilement de page natif. </p> <p> Si l’image est zoomée, elle bouge l’image verticalement. Si l’image est déplacée vers le bord de la vue et qu’un glissement est toujours effectué dans cette direction, le mouvement effectue un défilement de page natif. </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>Le lecteur prend également en charge les entrées tactiles et de souris sur les périphériques Windows dotés d’un écran tactile et d’une souris. Toutefois, cette prise en charge est limitée aux navigateurs Web Chrome, Internet Explorer 11 et Edge uniquement.

Cette visionneuse est entièrement accessible au clavier.

(voir la section Accessibilité et navigation [du](../../c-keyboard-accessibility.md#topic-f5650e9493404e55a3627c8d1366b861)clavier).

## Incorporation de la visionneuse à 360° {#section-6bb5d3c502544ad18a58eafe12a13435}

Différentes pages Web ont des besoins différents en ce qui concerne le comportement des visiteurs. Il arrive qu’une page Web fournisse un lien qui, lorsqu’un utilisateur clique dessus, ouvre le lecteur dans une fenêtre de navigateur distincte. Dans d’autres cas, il est nécessaire d’incorporer le droit du lecteur dans la page d’hébergement. Dans ce dernier cas, la page Web peut avoir une mise en page statique, ou utiliser une conception adaptée qui s’affiche différemment sur différents périphériques ou pour différentes tailles de fenêtre de navigateur. Pour répondre à ces besoins, le lecteur prend en charge trois modes de fonctionnement principaux : fenêtre contextuelle, incorporation de tailles fixes et incorporation de conceptions réactives.

**A propos du mode contextuel**

En mode contextuel, le lecteur s’ouvre dans une fenêtre ou un onglet distinct du navigateur Web. Elle prend toute la zone de la fenêtre du navigateur et s’ajuste au cas où le navigateur serait redimensionné ou où l’orientation d’un périphérique mobile serait modifiée.

Le mode contextuel est le plus courant pour les périphériques mobiles. La page Web charge la visionneuse à l’aide d’un appel `window.open()` JavaScript, d’un élément `A` HTML correctement configuré ou de toute autre méthode appropriée.

Il est recommandé d’utiliser une page HTML prête à l’emploi pour le mode d’opération contextuel. Dans ce cas, il est appelé [!DNL SpinViewer.html] et se trouve dans le [!DNL html5/] sous-dossier du déploiement des visionneuses IS standard :

[!DNL <s7viewers_root>/html5/SpinViewer.html]

Vous pouvez réaliser la personnalisation visuelle en appliquant une page CSS personnalisée.

Voici un exemple de code HTML qui ouvre la visionneuse dans une nouvelle fenêtre :

```
<a 
href="http://s7d1.scene7.com/s7viewers/html5/SpinViewer.html?asset=Scene7SharedAssets/SpinSet_Sample&stagesize=500,400" 
target="_blank">Open popup viewer</a>
```

**A propos du mode d&#39;incorporation de taille fixe et du mode d&#39;incorporation de conception réactif**

En mode incorporé, le lecteur est ajouté à la page Web existante, qui peut déjà contenir du contenu client qui n’est pas lié au lecteur. En règle générale, le lecteur occupe uniquement une partie de l’espace d’une page Web.

Les principales utilisations sont les pages Web orientées vers les ordinateurs de bureau ou les tablettes, ainsi que les pages de conception réactives qui ajustent automatiquement la mise en page en fonction du type de périphérique.

L’incorporation de taille fixe est utilisée lorsque la visionneuse ne change pas de taille après le chargement initial. Il s’agit du meilleur choix pour les pages Web présentant une disposition statique.

L’incorporation de la conception réactive suppose que la visionneuse doit peut-être être redimensionnée au moment de l’exécution en raison du changement de taille de son conteneur `DIV`. Le cas d’utilisation le plus courant consiste à ajouter une visionneuse à une page Web qui utilise une disposition de page souple.

En mode d’incorporation de conceptions réactives, le lecteur se comporte différemment selon la manière dont la page Web dimensionne son conteneur `DIV`. Si la page Web définit uniquement la largeur du conteneur `DIV`et que sa hauteur n’est pas restreinte, le lecteur sélectionne automatiquement sa hauteur en fonction des proportions du fichier utilisé. Cette fonctionnalité permet de s’assurer que la ressource s’intègre parfaitement à la vue sans remplissage sur les côtés. Ce cas d’utilisation est le plus courant pour les pages Web qui utilisent des structures de mise en page réactives telles que Bootstrap, Foundation, etc.

Sinon, si la page Web définit à la fois la largeur et la hauteur du conteneur du lecteur de contenu `DIV`, celui-ci remplit cette zone et suit la taille indiquée par la mise en page Web. Un bon exemple consiste à incorporer la visionneuse dans une incrustation modale, où l’incrustation est dimensionnée en fonction de la taille de la fenêtre du navigateur Web.

**Incorporation de taille fixe**

Pour ajouter la visionneuse à 360° à une page Web, procédez comme suit :

1. Ajouter le fichier JavaScript de la visionneuse sur votre page Web.
1. Définition du conteneur `DIV`.
1. Définition de la taille de la visionneuse.
1. Création et initialisation de la visionneuse.

1. Ajouter le fichier JavaScript de la visionneuse sur votre page Web.

   Pour créer une visionneuse, vous devez ajouter une balise de script dans l’en-tête HTML. Avant de pouvoir utiliser l’API du lecteur de contenu, veillez à inclure `SpinViewer.js`. `SpinViewer.js` se trouve sous le [!DNL html5/js/] sous-dossier de votre déploiement des visionneuses IS standard :

   `<s7viewers_root>/html5/js/SpinViewer.js`

   Vous pouvez utiliser un chemin relatif si la visionneuse est déployée sur l’un des serveurs Adobe Scene7 et qu’elle est diffusée à partir du même domaine. Sinon, vous spécifiez un chemin d’accès complet à l’un des serveurs Adobe Scene7 sur lesquels les visionneuses IS sont installées.

   Le chemin relatif ressemble à ce qui suit :

   ```
    <script language="javascript" type="text/javascript" src="/s7viewers/html5/js/SpinViewer.js"></script>
   ```

   >[!NOTE]
   >
   >Vous ne devez référencer que le fichier JavaScript du lecteur principal `include` sur votre page. Vous ne devez pas référencer de fichiers JavaScript supplémentaires dans le code de la page Web qui pourraient être téléchargés selon la logique du lecteur au moment de l’exécution. En particulier, ne référencez pas directement la `Utils.js` bibliothèque de SDK HTML5 chargée par la visionneuse à partir du chemin de `/s7viewers` contexte (appelé SDK consolidé `include`). La raison en est que l’emplacement des bibliothèques du lecteur d’exécution `Utils.js` ou similaires est entièrement géré par la logique du lecteur et que l’emplacement change entre les versions du lecteur. Adobe ne conserve pas les anciennes versions du lecteur secondaire `includes` sur le serveur.
   >
   >
   >Par conséquent, si vous placez une référence directe à tout code JavaScript secondaire `include` utilisé par la visionneuse sur la page, la fonctionnalité de visionneuse sera rompue à l’avenir lors du déploiement d’une nouvelle version de produit.

1. Définition de la balise DIV de conteneur.

   Ajoutez un élément DIV vide sur la page où doit apparaître le lecteur de contenu. L’identifiant de l’élément DIV doit être défini, car il est transmis ultérieurement à l’API du lecteur de contenu.

   L’espace réservé DIV est un élément positionné, ce qui signifie que la propriété `position` CSS est définie sur `relative` ou `absolute`.

   Voici un exemple d’élément DIV d’espace réservé défini :

   ```
   <div id="s7viewer" style="position:relative"></div>
   ```

1. Définition de la taille de la visionneuse

   Vous pouvez définir la taille statique de la visionneuse en la déclarant pour la classe CSS de `.s7spinviewer` niveau supérieur en unités absolues ou en utilisant `stagesize` des modificateurs.

   Vous pouvez placer le dimensionnement en CSS directement sur la page HTML ou dans un fichier CSS de visionneuse personnalisée, qui est ensuite affecté à un enregistrement de paramètre prédéfini de visionneuse dans Scene7 Publishing System ou transmis explicitement à l’aide d’une commande de style.

   See [Customizing Spin Viewer](../../c-html5-s7-aem-asset-viewers/c-html5-spin-viewer-about/c-html5-spin-viewer-customizingviewer/c-html5-spin-viewer-customizingviewer.md#concept-464f3bfa55764bc09c92d8c7480b0b55) for more information about styling the viewer with CSS.

   Voici un exemple de définition de la taille d’une visionneuse statique dans une page HTML :

   ```
   #s7viewer.s7spinviewer { 
    width: 640px; 
    height: 480px; 
   }
   ```

   Vous pouvez définir le `stagesize` modificateur soit dans l’enregistrement de paramètre prédéfini de la visionneuse dans Scene7 Publishing System, soit le transmettre explicitement avec le code d’initialisation de la visionneuse avec `params` la collection, soit sous la forme d’un appel d’API, comme décrit dans la section de référence des commandes, comme suit :

   ```
    spinViewer.setParam("stagesize", 
   "640,480");
   ```

   Une approche CSS est recommandée et est utilisée dans cet exemple.

1. Création et initialisation de la visionneuse.

   Une fois les étapes ci-dessus terminées, vous créez une instance de `s7viewers.SpinViewer` classe, vous transmettez toutes les informations de configuration à son constructeur et vous appelez `init()` la méthode sur une instance de visionneuse. Les informations de configuration sont transmises au constructeur sous la forme d’un objet JSON. Au minimum, cet objet comporte `containerId` un champ qui contient le nom de l’ID de conteneur de la visionneuse et l’objet `params` JSON imbriqué avec les paramètres de configuration pris en charge par la visionneuse. In this case of `params` object, it must have at least the Image Serving URL passed as `serverUrl` property and initial asset as `asset` parameter. L’API d’initialisation basée sur JSON vous permet de créer et de début le lecteur avec une seule ligne de code.

   Il est important que le conteneur de la visionneuse soit ajouté au modèle DOM afin que le code de la visionneuse puisse trouver l’élément de conteneur en fonction de son identifiant. Certains navigateurs retardent la création du modèle DOM jusqu’à la fin de la page Web. Pour une compatibilité maximale, appelez la `init()` méthode juste avant la balise `BODY` de fermeture, ou sur le `onload()` événement de contenu.

   Dans le même temps, l’élément conteneur ne doit pas nécessairement faire partie de la mise en page de la page Web pour le moment. Par exemple, il peut être masqué à l’aide du `display:none` style qui lui est affecté. Dans ce cas, le lecteur retarde son processus d’initialisation jusqu’au moment où la page Web ramène l’élément de conteneur à la mise en page. Lorsque cette action se produit, le chargement de la visionneuse reprend automatiquement.

   Voici un exemple de création d’une instance de visionneuse, en transmettant les options de configuration minimales nécessaires au constructeur et en appelant la `init()` méthode. L’exemple suppose `spinViewer` qu’il s’agit de l’instance de visionneuse, `s7viewer` du nom de l’espace réservé `DIV`, [!DNL http://s7d1.scene7.com/is/image/] de l’URL de diffusion d’images et [!DNL Scene7SharedAssets/SpinSet_Sample] du fichier.

   ```
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

   The following code is a complete example of a trivial web page that embeds the Spin Viewer with a fixed size:

   ```
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

**Incorporation de conception réactive avec une hauteur libre**

Avec l’incorporation de conceptions réactives, la page Web dispose normalement d’une sorte de disposition souple qui détermine la taille d’exécution du conteneur du lecteur `DIV`. Pour les besoins de cet exemple, supposons que la page Web permette au conteneur du lecteur `DIV` de prendre 40 % de la taille de la fenêtre du navigateur Web, en laissant sa hauteur libre. Le code HTML de la page Web qui en résulte ressemble à ce qui suit :

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

Adding the viewer to such a page is similar to fixed size embedding, with the only difference being that you do not need to explicitly define viewer size.

1. Ajouter le fichier JavaScript de la visionneuse sur votre page Web.
1. Définition de la balise DIV de conteneur.
1. Création et initialisation de la visionneuse.

Toutes les étapes ci-dessus sont identiques à celles de l’incorporation de tailles fixes. Add the container `DIV` to the existing &quot; holder&quot; `DIV`. Le code suivant est un exemple complet. You can see how the viewer size changes when the browser is resized, and how the viewer aspect ratio matches the asset.

```
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

La page d’exemples suivante illustre davantage de cas d’utilisation réelle d’incorporation de conceptions réactives avec une hauteur libre :

[Démonstrations en direct](https://landing.adobe.com/en/na/dynamic-media/ctir-2755/live-demos.html)

<!-- KEEP (https://marketing.adobe.com/resources/help/en_US/s7/vlist/vlist.html) -->

**Taille flexible incorporée avec définition de la largeur et de la hauteur**

Dans le cas d’une incorporation de taille flexible avec des valeurs de largeur et de hauteur définies, le style de la page Web est différent. Autrement dit, il fournit les deux tailles au &quot;détenteur&quot; `DIV` et le centre dans la fenêtre du navigateur. Also, the web page sets the size of the `HTML` and `BODY` element to 100%:

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

Les étapes d’incorporation restantes sont identiques à celles d’incorporation de conception adaptée avec une hauteur libre. L’exemple qui en résulte est le suivant :

```
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

**Incorporation à l’aide de l’API basée sur Setter**

Instead of using JSON-based initialization it is possible to use setter-based API and no-args constructor. With that API constructor does not take any parameters and configuration parameters is specified using `setContainerId()`, `setParam()`, and `setAsset()` API methods with separate JavaScript calls.

L’exemple suivant montre l’incorporation de tailles fixes avec l’API basée sur setter :

```
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

