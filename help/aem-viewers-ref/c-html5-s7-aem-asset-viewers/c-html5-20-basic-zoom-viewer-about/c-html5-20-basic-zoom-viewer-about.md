---
description: La visionneuse de zoom de base est une visionneuse d’images qui affiche une image pouvant faire l’objet d’un zoom unique. Il comporte des outils de zoom, une prise en charge du mode plein écran et un bouton de fermeture en option. Cette visionneuse est la plus légère. Il est conçu pour fonctionner sur les ordinateurs de bureau et les périphériques mobiles.
keywords: responsive
seo-description: La visionneuse de zoom de base est une visionneuse d’images qui affiche une image pouvant faire l’objet d’un zoom unique. Il comporte des outils de zoom, une prise en charge du mode plein écran et un bouton de fermeture en option. Cette visionneuse est la plus légère. Il est conçu pour fonctionner sur les ordinateurs de bureau et les périphériques mobiles.
seo-title: Zoom de base
solution: Experience Manager
title: Zoom de base
topic: Dynamic media
uuid: 5466d647-af70-4503-9898-bb712ba6a007
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# Zoom de base{#basic-zoom}

La visionneuse de zoom de base est une visionneuse d’images qui affiche une image pouvant faire l’objet d’un zoom unique. Il comporte des outils de zoom, une prise en charge du mode plein écran et un bouton de fermeture en option. Cette visionneuse est la plus légère. Il est conçu pour fonctionner sur les ordinateurs de bureau et les périphériques mobiles.

>[!NOTE]
>
>Les images qui utilisent la fonction IR (Image Rendering) ou UGC (User Generated Content) ne sont pas prises en charge par cette visionneuse.

Type de lecteur 501.

Voir Configuration [système requise et configuration requise](../../c-system-requirements-and-prerequisites.md#concept-9282e5b777de42cdaf72ef7ebd646842).

## URL de démonstration {#section-e1c3106f5b3e445d9b95be337c2f94e2}

[https://s7d9.scene7.com/s7viewers/html5/BasicZoomViewer.html?asset=Scene7SharedAssets/Backpack_B](https://s7d9.scene7.com/s7viewers/html5/BasicZoomViewer.html?asset=Scene7SharedAssets/Backpack_B)

## Utilisation de la visionneuse de zoom de base {#section-e6c68406ecdc4de781df182bbd8088b4}

La visionneuse de zoom de base représente un fichier JavaScript principal et un ensemble de fichiers d’aide (un seul code JavaScript inclut tous les composants SDK de la visionneuse utilisés par cette visionneuse, ressources, CSS) que les visionneuses téléchargent au moment de l’exécution.

Vous pouvez utiliser la visionneuse de zoom de base en mode contextuel à l’aide d’une page HTML prête à l’emploi fournie avec des visionneuses IS ou en mode intégré, où elle est intégrée dans une page Web de  à l’aide d’une API documentée.

La configuration et l’habillage sont similaires à ceux des autres visionneuses. L’habillage est effectué au moyen d’une page CSS personnalisée.

Voir Référence [de commande commune à toutes les visionneuses - Attributs](../../r-html5-viewer-20-cmdref-configattrib/r-html5-viewer-20-cmdref-configattrib.md#concept-850e0f2c49b949deb7cfbfd330d329bd) de configuration et référence de [commande commune à toutes les visionneuses - URL](../../c-html5-viewer-20-cmdref-url/c-html5-viewer-20-cmdref-url.md#concept-9b337f349b7b406b8c33c7ee96b3e226)

## Interaction avec la visionneuse de zoom de base {#section-642e66ca38cd4032992840ec6c0b0cd2}

La visionneuse de zoom de base prend en charge les mouvements tactiles suivants, qui sont courants dans d’autres applications mobiles.

Lorsque le lecteur ne peut pas traiter le mouvement de glissement d’un utilisateur, il transfère le  au navigateur Web pour effectuer un défilement de page natif. Ce type de fonctionnalité permet à l’utilisateur de parcourir la page même si le lecteur occupe la majeure partie de l’écran du périphérique.

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
   <td colname="col2"> <p>Masque ou affiche les éléments de l’interface utilisateur. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Touche  </p> </td> 
   <td colname="col2"> <p> Applique un zoom à un niveau jusqu’à ce que le facteur de zoom maximal soit atteint. Le mouvement de  du clic suivant réinitialise la visionneuse à l’état d’affichage initial. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Pincer </p> </td> 
   <td colname="col2"> <p>Applique un zoom avant ou arrière. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Balayer </p> </td> 
   <td colname="col2"> <p> Si l’image est à l’état reset, le mouvement effectue un défilement de page natif. </p> <p> Lorsque l’image est agrandie, elle déplace l’image. Si l’image est déplacée vers le bord  du et qu’un glissement est effectué dans cette direction, le mouvement effectue un défilement de page natif. </p> </td> 
  </tr> 
 </tbody> 
</table>

Le lecteur prend également en charge la saisie tactile et la saisie de la souris sur les périphériques Windows dotés d’un écran tactile et d’une souris. Cette prise en charge est toutefois limitée aux navigateurs Web Chrome, Internet Explorer 11 et Edge.

Cette visionneuse est entièrement accessible au clavier.

Voir Accessibilité [du clavier et navigation](../../c-keyboard-accessibility.md#topic-f5650e9493404e55a3627c8d1366b861).

## Incorporation de la visionneuse de zoom de base {#section-6bb5d3c502544ad18a58eafe12a13435}

Le comportement des visiteurs varie selon les pages Web. Il arrive qu’une page Web fournisse un lien qui, lorsqu’un utilisateur clique dessus, ouvre le lecteur dans une fenêtre de navigateur distincte. Dans d’autres cas, il est nécessaire d’incorporer le lecteur de contenu directement dans la page d’hébergement. Dans ce dernier cas, la page Web peut avoir une mise en page statique, ou utiliser une conception adaptée qui s’affiche différemment sur différents périphériques ou pour différentes tailles de fenêtre de navigateur. Pour répondre à ces besoins, le lecteur prend en charge trois modes de fonctionnement principaux : fenêtre contextuelle, incorporation de taille fixe et incorporation de conception adaptée.

**A propos du mode contextuel**

En mode contextuel, le lecteur s’ouvre dans une fenêtre ou un onglet distinct du navigateur Web. Il prend toute la zone de la fenêtre du navigateur et s’ajuste au cas où le navigateur serait redimensionné ou où l’orientation du périphérique serait modifiée.

Le mode contextuel est le plus courant pour les périphériques mobiles. La page Web charge le lecteur à l’aide de l’appel JavaScript, d’un élément `window.open()` `A` HTML correctement configuré ou de toute autre méthode appropriée.

Il est recommandé d’utiliser une page HTML prête à l’emploi pour le mode d’opération contextuel. Dans ce cas, il est appelé [!DNL BasicZoomViewer.html] et se trouve dans le [!DNL html5/] sous-dossier du déploiement des visionneuses IS standard :

[!DNL <s7viewers_root>/html5/BasicZoomViewer.html]

Vous pouvez réaliser la personnalisation visuelle en appliquant une page CSS personnalisée.

Voici un exemple de code HTML qui ouvre la visionneuse dans une nouvelle fenêtre :

```
<a href="http://s7d1.scene7.com/s7viewers/html5/BasicZoomViewer.html?asset=Scene7SharedAssets/Backpack_B" target="_blank">Open popup viewer</a>
```

**A propos du mode d’incorporation de taille fixe et du mode d’incorporation de conception réactif**

En mode intégré, le lecteur est ajouté à la page Web existante, qui peut déjà comporter du contenu client qui n’est pas lié au lecteur. En règle générale, le lecteur n’occupe qu’une partie de l’espace d’une page Web.

Les principales utilisations sont les pages Web orientées vers les ordinateurs de bureau ou les tablettes, ainsi que les pages adaptées qui ajustent automatiquement la disposition en fonction du type de périphérique.

L’incorporation de taille fixe est utilisée lorsque la visionneuse ne modifie pas sa taille après le chargement initial. Il s’agit du meilleur choix pour les pages Web avec une disposition statique.

L’incorporation de la conception réactive suppose que le lecteur doit peut-être être redimensionné au moment de l’exécution en réponse au changement de taille de sa  de `DIV`. Le cas d’utilisation le plus courant consiste à ajouter une visionneuse à une page Web qui utilise une disposition de page souple.

En mode d’incorporation de conception réactif, le lecteur se comporte différemment selon la manière dont la page Web redimensionne son  `DIV`. Si la page Web définit uniquement la largeur du  du `DIV`et que sa hauteur reste illimitée, le lecteur choisit automatiquement sa hauteur en fonction des proportions du fichier utilisé. Cette fonctionnalité permet de s’assurer que la ressource s’intègre parfaitement dans le  du sans remplissage sur les côtés. Ce cas d’utilisation est le plus courant pour les pages Web qui utilisent des structures de mise en page Web adaptées, telles que Bootstrap, Foundation, etc.

Sinon, si la page Web définit à la fois la largeur et la hauteur du  du lecteur `DIV`, celui-ci remplit cette zone et suit la taille fournie par la mise en page Web. Un bon exemple est l’incorporation de la visionneuse dans une incrustation modale, où l’incrustation est dimensionnée en fonction de la taille de la fenêtre du navigateur Web.

**Incorporation de taille fixe**

Vous ajoutez le lecteur à une page Web en procédant comme suit :

1. Ajout du fichier JavaScript de la visionneuse à votre page Web.
1. Définition de la  DIV du.
1. Définition de la taille de la visionneuse.
1. Création et initialisation de la visionneuse.

1. Ajout du fichier JavaScript de la visionneuse à votre page Web.

   Pour créer une visionneuse, vous devez ajouter une balise de script dans l’en-tête HTML. Avant d’utiliser l’API du lecteur de contenu, veillez à inclure [!DNL BasicZoomViewer.js]. Le [!DNL BasicZoomViewer.js] fichier se trouve sous le [!DNL html5/js/] sous-dossier du déploiement des visionneuses IS standard :

[!DNL <s7viewers_root>/html5/js/BasicZoomViewer.js]

Vous pouvez utiliser un chemin relatif si le lecteur est déployé sur l’un des serveurs Adobe Dynamic Media Classic et qu’il est diffusé à partir du même domaine. Dans le cas contraire, vous spécifiez un chemin d’accès complet à l’un des serveurs Adobe Dynamic Media Classic sur lesquels les visionneuses IS sont installées.

Le chemin relatif ressemble à ce qui suit :

```
<script language="javascript" type="text/javascript" src="/s7viewers/html5/js/BasicZoomViewer.js"></script>
```

>[!NOTE]
>
>Vous ne devez référencer que le fichier JavaScript du lecteur principal `include` sur votre page. Vous ne devez pas référencer de fichiers JavaScript supplémentaires dans le code de la page Web qui pourraient être téléchargés par la logique du lecteur au moment de l’exécution. En particulier, ne référencez pas directement la `Utils.js` bibliothèque du SDK HTML5 chargée par le lecteur à partir du chemin `/s7viewers` contextuel (appelé SDK consolidé `include`). La raison en est que l’emplacement des bibliothèques de lecteurs de contenu d’exécution `Utils.js` ou similaires est entièrement géré par la logique du lecteur et que l’emplacement change entre les versions du lecteur. Adobe ne conserve pas les anciennes versions du lecteur secondaire `includes` sur le serveur.
>
>
>Par conséquent, le fait de placer une référence directe à tout code JavaScript secondaire `include` utilisé par le lecteur sur la page rompt la fonctionnalité du lecteur à l’avenir lorsqu’une nouvelle version de produit est déployée.

1. Définition de la  DIV du.

   Ajouter un élément DIV vide sur la page où le lecteur doit apparaître. L’ID de l’élément DIV doit être défini, car cet ID est transmis ultérieurement à l’API du lecteur de contenu. La taille du fichier DIV est spécifiée via CSS.

   L’espace réservé DIV est un élément positionné, ce qui signifie que la propriété `position` CSS est définie sur `relative` ou `absolute`.

   Voici un exemple d’élément DIV d’espace réservé défini :

   ```
   <div id="s7viewer" style="position:relative"></div>
   ```

1. Définition de la taille de la visionneuse

   Vous pouvez définir la taille statique de la visionneuse en la déclarant pour la classe CSS de `.s7basiczoomviewer` niveau supérieur en unités absolues ou en utilisant le modificateur `stagesize` .

   Vous pouvez placer le dimensionnement en CSS directement sur la page HTML ou dans un fichier CSS de visionneuse personnalisé, qui est ensuite affecté à un enregistrement de paramètre prédéfini de visionneuse dans SPS, ou transmis explicitement à l’aide d’une commande de style.

   Voir [Personnalisation de la visionneuse](../../c-html5-s7-aem-asset-viewers/c-html5-20-basic-zoom-viewer-about/c-html5-20-basic-zoom-viewer-customizingviewer/c-html5-20-basic-zoom-viewer-customizingviewer.md#concept-73a8546acdb444a387c49969ceca57d0) de zoom de base pour plus d’informations sur le style de la visionneuse avec CSS.

   Voici un exemple de définition de la taille d’une visionneuse statique dans une page HTML :

   ```
   #s7viewer.s7basiczoomviewer { 
    width: 640px; 
    height: 480px; 
   }
   ```

   Vous pouvez définir le `stagesize` modificateur soit dans l’enregistrement de paramètre prédéfini de la visionneuse dans SPS, soit le transmettre explicitement avec le code d’initialisation de la visionneuse avec `params` la collection, soit sous la forme d’un appel API, comme décrit dans la section Référence de commande, comme suit :

   ```
   basicZoomViewer.setParam("stagesize", "640,480");
   ```

   Une approche CSS est recommandée et utilisée dans cet exemple.

1. Création et initialisation de la visionneuse.

   Une fois les étapes ci-dessus terminées, vous créez une instance de `s7viewers.BasicZoomViewer` classe, vous transmettez toutes les informations de configuration à son constructeur, puis vous appelez `init()` la méthode sur une instance de visionneuse. Les informations de configuration sont transmises au constructeur sous forme d’objet JSON. Au minimum, cet objet doit comporter un champ containerId contenant le nom de la visionneuse `container ID` et l’objet `params` JSON imbriqué avec les paramètres de configuration pris en charge par la visionneuse. Dans ce cas, l’ `params` objet doit comporter au moins l’URL de diffusion d’images transmise en tant que `serverUrl` propriété et le fichier initial en tant que `asset` paramètre. L’API d’initialisation basée sur JSON vous permet de créer et de  le lecteur avec une seule ligne de code.

   Il est important que le de la visionneuse soit ajouté au modèle DOM afin que le code de la visionneuse puisse trouver l’élément  par son identifiant. Certains navigateurs retardent la création du modèle DOM jusqu’à la fin de la page Web. Pour une compatibilité maximale, appelez la `init()` méthode juste avant la `BODY` balise de fermeture ou sur le  du corps `onload()` .

   En même temps, l’élément  du ne doit pas nécessairement faire partie de la mise en page de la page Web pour le moment. Par exemple, il peut être masqué à l’aide du `display:none` style qui lui est affecté. Dans ce cas, le lecteur de contenu retarde son processus d’initialisation jusqu’au moment où la page Web ramène l’élément  du à la mise en page. Dans ce cas, le chargement du lecteur reprend automatiquement.

   Voici un exemple de création d’une instance de visionneuse, de transmission des options de configuration minimales nécessaires au constructeur et d’appel de la `init()` méthode. L’exemple suppose `basicZoomViewer` qu’il s’agit de l’instance de visionneuse ; `s7viewer` est le nom de l’espace réservé `DIV`; `http://s7d1.scene7.com/is/image/` est l’URL de diffusion d’images et `Scene7SharedAssets/Backpack_B` est la ressource :

   ```
   <script type="text/javascript"> 
   var basicZoomViewer = new s7viewers.BasicZoomViewer({ 
    "containerId":"s7viewer", 
   "params":{ 
    "asset":"Scene7SharedAssets/Backpack_B", 
    "serverurl":"http://s7d1.scene7.com/is/image/" 
   } 
   }).init(); 
   </script>
   ```

   Le code suivant est un exemple complet d’une page Web triviale qui incorpore la visionneuse de zoom de base à une taille fixe :

   ```
   <!DOCTYPE html> 
   <html> 
   <head> 
   <script type="text/javascript" src="http://s7d1.scene7.com/s7viewers/html5/js/BasicZoomViewer.js"></script> 
   <style type="text/css"> 
   #s7viewer.s7basiczoomviewer { 
    width: 640px; 
    height: 480px; 
   } 
   </style> 
   </head> 
   <body> 
   <div id="s7viewer" style="position:relative"></div> 
   <script type="text/javascript"> 
   var basicZoomViewer = new s7viewers.BasicZoomViewer({ 
    "containerId":"s7viewer", 
    "params":{ 
     "asset":"Scene7SharedAssets/Backpack_B", 
     "serverurl":"http://s7d1.scene7.com/is/image/" 
   } 
   }).init(); 
   </script> 
   </body> 
   </html>
   ```

**Incorporation de conception réactive avec une hauteur libre**

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

L’ajout de la visionneuse à une telle page est similaire à la procédure d’incorporation de taille fixe. La seule différence est que vous n’avez pas besoin de définir explicitement la taille de la visionneuse.

1. Ajout du fichier JavaScript de la visionneuse à votre page Web.
1. Définition de la  DIV du.
1. Création et initialisation de la visionneuse.

Toutes les étapes ci-dessus sont identiques à celles de l’incorporation de taille fixe. Ajouter la  DIV à la `"holder"` DIV existante. Le code suivant est un exemple complet. Notez la modification de la taille de la visionneuse lorsque le navigateur est redimensionné et la manière dont les proportions de la visionneuse correspondent à la ressource.

```
<!DOCTYPE html> 
<html> 
<head> 
<script type="text/javascript" src="http://s7d1.scene7.com/s7viewers/html5/js/BasicZoomViewer.js"></script> 
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
var basicZoomViewer = new s7viewers.BasicZoomViewer({ 
 "containerId":"s7viewer", 
 "params":{ 
  "asset":"Scene7SharedAssets/Backpack_B", 
  "serverurl":"http://s7d1.scene7.com/is/image/" 
} 
}).init(); 
</script> 
</body> 
</html>
```

La page d’exemples suivante illustre d’autres utilisations réelles de la conception adaptée incorporée à une hauteur illimitée :

[https://marketing.adobe.com/resources/help/en_US/s7/vlist/vlist.html](https://marketing.adobe.com/resources/help/en_US/s7/vlist/vlist.html)

**Incorporation de taille flexible avec définition de la largeur et de la hauteur**

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

Le reste des étapes d&#39;incorporation est identique à celles utilisées pour l&#39;incorporation réactive avec une hauteur libre. L’exemple qui en résulte est le suivant :

```
<!DOCTYPE html> 
<html> 
<head> 
<script type="text/javascript" src="http://s7d1.scene7.com/s7viewers/html5/js/BasicZoomViewer.js"></script> 
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
var basicZoomViewer = new s7viewers.BasicZoomViewer({ 
 "containerId":"s7viewer", 
 "params":{ 
  "asset":"Scene7SharedAssets/Backpack_B", 
  "serverurl":"http://s7d1.scene7.com/is/image/" 
} 
}).init(); 
</script> 
</body> 
</html>
```

**Incorporation à l’aide d’une API basée sur Setter**

Au lieu d’utiliser l’initialisation basée sur JSON, il est possible d’utiliser une API basée sur un setter et un constructeur sans args. L’utilisation de ce constructeur d’API ne prend aucun paramètre et les paramètres de configuration sont spécifiés à l’aide `setContainerId()`, `setParam()`et `setAsset()` des méthodes API avec des appels JavaScript distincts.

L’exemple suivant illustre l’utilisation de l’incorporation de tailles fixes avec l’API basée sur setter :

```
<!DOCTYPE html> 
<html> 
<head> 
<script type="text/javascript" src="http://s7d1.scene7.com/s7viewers/html5/js/BasicZoomViewer.js"></script> 
<style type="text/css"> 
#s7viewer.s7basiczoomviewer { 
 width: 640px; 
 height: 480px; 
} 
</style> 
</head> 
<body> 
<div id="s7viewer" style="position:relative"></div> 
<script type="text/javascript"> 
var basicZoomViewer = new s7viewers.BasicZoomViewer(); 
basicZoomViewer.setContainerId("s7viewer"); 
basicZoomViewer.setParam("serverurl", "http://s7d1.scene7.com/is/image/"); 
basicZoomViewer.setAsset("Scene7SharedAssets/Backpack_B"); 
basicZoomViewer.init(); 
</script> 
</body> 
</html>
```

