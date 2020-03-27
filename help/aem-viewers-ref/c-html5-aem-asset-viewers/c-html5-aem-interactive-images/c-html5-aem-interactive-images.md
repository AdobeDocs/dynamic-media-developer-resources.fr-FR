---
description: Interactive Image Viewer est une visionneuse qui affiche une image unique non zoomable avec des zones réactives cliquables. Le but de ce lecteur est de mettre en oeuvre une expérience de "bannière modifiable". En d’autres termes, l’utilisateur peut sélectionner une zone réactive sur l’image de la bannière et être redirigé vers une  rapide ou une page des détails du produit sur votre site Web. Il est conçu pour fonctionner sur les ordinateurs de bureau et les périphériques mobiles.
seo-description: Interactive Image Viewer est une visionneuse qui affiche une image unique non zoomable avec des zones réactives cliquables. Le but de ce lecteur est de mettre en oeuvre une expérience de "bannière modifiable". En d’autres termes, l’utilisateur peut sélectionner une zone réactive sur l’image de la bannière et être redirigé vers une  rapide ou une page des détails du produit sur votre site Web. Il est conçu pour fonctionner sur les ordinateurs de bureau et les périphériques mobiles.
seo-title: Image interactive
solution: Experience Manager
title: Image interactive
topic: Dynamic media
uuid: 18b7a0c3-c047-4ce1-8920-1d8ebc1ab60e
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# Image interactive{#interactive-image}

Interactive Image Viewer est une visionneuse qui affiche une image unique non zoomable avec des zones réactives cliquables. Le but de ce lecteur est de mettre en oeuvre une expérience de &quot;bannière modifiable&quot;. En d’autres termes, l’utilisateur peut sélectionner une zone réactive sur l’image de la bannière et être redirigé vers une  rapide ou une page des détails du produit sur votre site Web. Il est conçu pour fonctionner sur les ordinateurs de bureau et les périphériques mobiles.

>[!NOTE]
>
>Les images qui utilisent la fonction IR (Image Rendering) ou UGC (User-Generated Content) ne sont pas prises en charge par cette visionneuse.

Le type de lecteur est 508.

## URL de démonstration {#section-c0ad383db6a444979dc7eeb1ec4cf54d}

[https://marketing.adobe.com/resources/help/en_US/dm/shoppable-banner/samples/InteractiveImage.html](https://marketing.adobe.com/resources/help/en_US/dm/shoppable-banner/samples/InteractiveImage.html)

## Configuration système requise {#section-b7270cc4290043399681dc504f043609}

Voir [Configuration requise](../../c-system-requirements-and-prerequisites.md#concept-9282e5b777de42cdaf72ef7ebd646842).

## Utilisation de la visionneuse d’images interactive {#section-e6c68406ecdc4de781df182bbd8088b4}

Interactive Image Viewer représente un fichier JavaScript principal et un ensemble de fichiers d’aide (un seul fichier JavaScript inclut tous les composants du SDK de la visionneuse utilisés par cette visionneuse, ressources et CSS) téléchargés par la visionneuse au moment de l’exécution.

La visionneuse d’images interactive ne peut être utilisée qu’en mode intégré, où elle est intégrée dans la page Web  du à l’aide de l’API documentée.

La configuration et l’habillage sont similaires à ceux des autres visionneuses décrites dans cette aide. L’habillage est effectué au moyen d’une page CSS personnalisée.

Voir Référence [de commande commune à toutes les visionneuses - Attributs](../../r-html5-viewer-20-cmdref-configattrib/r-html5-viewer-20-cmdref-configattrib.md#concept-850e0f2c49b949deb7cfbfd330d329bd) de configuration et référence de [commande commune à toutes les visionneuses - URL](../../c-html5-viewer-20-cmdref-url/c-html5-viewer-20-cmdref-url.md#concept-9b337f349b7b406b8c33c7ee96b3e226)

## Interaction avec Interactive Image Viewer {#section-642e66ca38cd4032992840ec6c0b0cd2}

L’interaction prise en charge par la visionneuse d’images vidéo est une zone réactive  un  sur les ordinateurs de bureau. Ce  se produit  sur les périphériques tactiles et de clic avec une seule pression.

Le lecteur est entièrement accessible au clavier.

Voir Accessibilité [du clavier et navigation](../../c-keyboard-accessibility.md#topic-f5650e9493404e55a3627c8d1366b861).

## Incorporation de la visionneuse d’images interactive {#section-6bb5d3c502544ad18a58eafe12a13435}

Interactive Image Viewer est conçu pour être incorporé à la page d’hébergement. Une telle page Web peut avoir une disposition statique ou être &quot;adaptée&quot; et s’afficher différemment sur différents périphériques ou selon la taille des fenêtres du navigateur.

Pour répondre à ces besoins, le lecteur prend en charge deux modes de fonctionnement principaux : incorporation de taille fixe et incorporation réactive.

**A propos du mode d’incorporation de taille fixe et du mode d’incorporation de conception réactif**

En mode intégré, le lecteur est ajouté à la page Web existante. Il se peut que cette page Web comporte déjà du contenu client qui n’est pas lié au lecteur. En règle générale, le lecteur n’occupe qu’une partie de l’espace d’une page Web.

Les principaux cas d’utilisation sont les pages Web orientées vers les ordinateurs de bureau ou les tablettes et les pages adaptées qui ajustent automatiquement la disposition en fonction du type de périphérique.

L’incorporation de taille fixe est utilisée lorsque la visionneuse ne modifie pas sa taille après le chargement initial. Il s’agit du meilleur choix pour les pages Web avec une disposition statique.

L’incorporation de la conception réactive suppose que le lecteur doit peut-être être redimensionné au moment de l’exécution en réponse au changement de taille de sa  de `DIV`. Le cas d’utilisation le plus courant consiste à ajouter une visionneuse à une page Web qui utilise une disposition de page souple.

En mode d’incorporation de conception réactif, le lecteur se comporte différemment selon la manière dont la page Web redimensionne son  `DIV`. Si la page Web définit uniquement la largeur du  du `DIV`et que sa hauteur reste illimitée, le lecteur choisit automatiquement sa hauteur en fonction des proportions du fichier utilisé. Cette fonctionnalité permet de s’assurer que la ressource s’intègre parfaitement dans le  du sans remplissage sur les côtés. Ce cas d’utilisation est le plus courant pour les pages Web qui utilisent des structures de mise en page Web adaptées, telles que Bootstrap, Foundation, etc.

Sinon, si la page Web définit à la fois la largeur et la hauteur du  du lecteur de contenu `DIV`, celui-ci remplit exactement cette zone. Il suit également la taille fournie par la mise en page Web. Un bon exemple est l’incorporation de la visionneuse dans une incrustation modale, où l’incrustation est dimensionnée en fonction de la taille de la fenêtre du navigateur Web.

**Incorporation de taille fixe**

Vous ajoutez le lecteur à une page Web en procédant comme suit :

1. Ajout du fichier JavaScript de la visionneuse à votre page Web.
1. Définition du  de `DIV`.
1. Définition de la taille de la visionneuse.
1. Création et initialisation de la visionneuse.

1. Ajout du fichier JavaScript de la visionneuse à votre page Web.

   Pour créer une visionneuse, vous devez ajouter une balise de script dans l’en-tête HTML. Avant d’utiliser l’API du lecteur de contenu, veillez à inclure [!DNL InterativeImage.js]. Le [!DNL InteractiveImage.js] fichier se trouve sous le [!DNL html5/js/] sous-dossier du déploiement des visionneuses IS standard :

[!DNL <s7viewers_root>/etc/dam/viewers/s7viewers/html5/js/InteractiveImage.js]

Vous pouvez utiliser un chemin relatif si le lecteur est déployé sur l’un des serveurs Adobe Dynamic Media Classic et qu’il est diffusé à partir du même domaine. Dans le cas contraire, vous spécifiez un chemin d’accès complet à l’un des serveurs Adobe Dynamic Media Classic sur lesquels les visionneuses IS sont installées.

Le chemin relatif ressemble à ce qui suit :

```
<script language="javascript" type="text/javascript" src="/etc/dam/viewers/s7viewers/html5/js/InteractiveImage.js"></script>
```

>[!NOTE]
>
>Vous ne devez référencer que le fichier JavaScript du lecteur principal `include` sur votre page. Vous ne devez pas référencer de fichiers JavaScript supplémentaires dans le code de la page Web qui pourraient être téléchargés par la logique du lecteur au moment de l’exécution. En particulier, ne référencez pas directement la `Utils.js` bibliothèque du SDK HTML5 chargée par le lecteur à partir du chemin `/s7viewers` contextuel (appelé SDK consolidé `include`). La raison en est que l’emplacement des bibliothèques de lecteurs de contenu d’exécution `Utils.js` ou similaires est entièrement géré par la logique du lecteur et que l’emplacement change entre les versions du lecteur. Adobe ne conserve pas les anciennes versions du lecteur secondaire `includes` sur le serveur.
>
>
>Par conséquent, le fait de placer une référence directe à tout code JavaScript secondaire `include` utilisé par le lecteur sur la page rompt la fonctionnalité du lecteur à l’avenir lorsqu’une nouvelle version de produit est déployée.

1. Définition du  de `DIV`.

   Ajouter un `DIV` élément vide sur la page où le lecteur doit apparaître. L’ID de l’ `DIV` élément doit être défini, car cet ID est transmis ultérieurement à l’API du lecteur de contenu. La taille du fichier DIV est spécifiée via CSS.

   L’espace réservé `DIV` est un élément positionné, ce qui signifie que la propriété `position` CSS est définie sur `relative` ou `absolute`.

   Voici un exemple d’élément d’espace réservé défini `DIV` :

   ```
   <div id="s7viewer" style="position:relative"></div>
   ```

1. Définition de la taille de la visionneuse

   Vous pouvez définir la taille statique de la visionneuse en la déclarant pour la classe CSS de `.s7interactiveimage` niveau supérieur en unités absolues ou en utilisant le modificateur `stagesize` .

   Vous pouvez placer le dimensionnement en CSS directement sur la page HTML ou dans un fichier CSS de lecteur personnalisé, qui est ensuite affecté à un enregistrement de paramètre prédéfini de visionneuse dans AEM Assets - à la demande ou transmis explicitement à l’aide de `style` la commande.

   Voir [Vidéo](../../c-html5-aem-asset-viewers/c-html5-aem-interactive-images/c-html5-aem-interactive-image-customizingviewer/c-html5-aem-interactive-image-customizingviewer.md#concept-73a8546acdb444a387c49969ceca57d0) pour plus d’informations sur le style de la visionneuse avec CSS.

   Voici un exemple de définition de la taille d’une visionneuse statique dans la page HTML :

   ```
   #s7viewer.s7interactiveimage { 
    width: 1174px; 
    height: 500px; 
   }
   ```

   Vous pouvez transmettre explicitement le `stagesize` modificateur avec le code d’initialisation de la visionneuse avec `params` collection ou en tant qu’appel API, comme décrit dans la section Référence de commande, comme suit :

   ```
   interactiveImage.setParam("stagesize", "1174,500");
   ```

   Une approche CSS est recommandée et utilisée dans cet exemple.

1. Création et initialisation de la visionneuse.

   Une fois les étapes ci-dessus terminées, vous créez une instance de `s7viewers.InteractiveImage` classe, vous transmettez toutes les informations de configuration à son constructeur, puis vous appelez `init()` la méthode sur une instance de visionneuse. Les informations de configuration sont transmises au constructeur sous forme d’objet JSON. Au minimum, cet objet doit avoir `containerId` un champ contenant le nom de l’ID de  de la visionneuse et l’objet `params` JSON imbriqué avec les paramètres de configuration pris en charge par la visionneuse. Dans ce cas, l’ `params` objet doit comporter au moins l’URL de diffusion d’images transmise en tant que `serverUrl` propriété et le fichier initial en tant que `asset` paramètre. L’API d’initialisation basée sur JSON vous permet de créer et de  le lecteur avec une seule ligne de code.

   Il est important que le de la visionneuse soit ajouté au modèle DOM afin que le code de la visionneuse puisse trouver l’élément  par son identifiant. Certains navigateurs retardent la création du modèle DOM jusqu’à la fin de la page Web. Pour une compatibilité maximale, appelez la `init()` méthode juste avant la `BODY` balise de fermeture ou sur le  du corps `onload()` .

   En même temps, l’élément  du ne doit pas nécessairement faire partie de la mise en page de la page Web pour le moment. Par exemple, il peut être masqué à l’aide du `display:none` style qui lui est affecté. Dans ce cas, le lecteur de contenu retarde son processus d’initialisation jusqu’au moment où la page Web ramène l’élément  du à la mise en page. Dans ce cas, le chargement du lecteur reprend automatiquement.

   Voici un exemple de création d’une instance de visionneuse, de transmission des options de configuration minimales nécessaires au constructeur et d’appel de la `init()` méthode. L’exemple suppose `interactiveImage` qu’il s’agit de l’instance de visionneuse ; `s7viewer` est le nom de l’espace réservé `DIV`; `http://aodmarketingna.assetsadobe.com/is/image` est l’URL de diffusion d’images et `/content/dam/mac/aodmarketingna/shoppable-banner/shoppable-banner.` est la ressource :

   ```
   <script type="text/javascript"> 
   var interactiveImage = new s7viewers.InteractiveImage ({ 
    "containerId":"s7viewer", 
   "params":{ 
    "asset":"/content/dam/mac/aodmarketingna/shoppable-banner/shoppable-banner.jpg", 
    "serverurl":"http://aodmarketingna.assetsadobe.com/is/image" 
   } 
   }).init(); 
   </script> 
   ```

   Le code suivant est un exemple complet d’une page Web triviale qui incorpore la visionneuse d’images vidéo à une taille fixe :

   ```
   <!DOCTYPE html> 
   <html> 
   <head> 
   <script type="text/javascript" src="http://aodmarketingna.assetsadobe.com/etc/dam/viewers/s7viewers/html5/js/InteractiveImage.js"></script> 
   <style type="text/css"> 
   #s7viewer.s7interactiveimage { 
    width: 1174px; 
    height: 500px; 
   } 
   </style> 
   </head> 
   <body> 
   <div id="s7viewer" style="position:relative"></div> 
   <script type="text/javascript"> 
   var interactiveImage = new s7viewers.InteractiveImage({ 
    "containerId":"s7viewer", 
   "params":{ 
    "asset":"/content/dam/mac/aodmarketingna/shoppable-banner/shoppable-banner.jpg", 
    "serverurl":"http://aodmarketingna.assetsadobe.com/is/image" 
   } 
   }).init(); 
   </script> 
   </body> 
   </html> 
   ```

**Incorporation de conception réactive avec une hauteur libre**

Avec l’incorporation de conceptions réactives, la page Web dispose normalement d’une sorte de disposition souple qui détermine la taille d’exécution du  du lecteur `DIV`. Dans l’exemple suivant, supposons que la page Web permette au du lecteur de  prendre 40 % de la taille de la fenêtre du navigateur Web. `DIV` Et sa hauteur reste illimitée. Le code HTML de la page Web se présente comme suit :

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
1. Définition du  de `DIV`.
1. Création et initialisation de la visionneuse.

Toutes les étapes ci-dessus sont identiques à celles de l’incorporation de taille fixe. Ajouter le  `DIV` au existant `"holder"` `DIV`. Le code suivant est un exemple complet. Notez la modification de la taille de la visionneuse lorsque le navigateur est redimensionné et la manière dont les proportions de la visionneuse correspondent à la ressource.

```
<!DOCTYPE html> 
<html> 
<head> 
<script type="text/javascript" src="http://aodmarketingna.assetsadobe.com/etc/dam/viewers/s7viewers/html5/js/InteractiveImage.js"></script> 
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
var interactiveImage = new s7viewers.InteractiveImage({ 
 "containerId":"s7viewer", 
"params":{ 
 "asset":"/content/dam/mac/aodmarketingna/shoppable-banner/shoppable-banner.jpg", 
 "serverurl":"http://aodmarketingna.assetsadobe.com/is/image" 
} 
}).init(); 
</script> 
</body> 
</html> 
```

La page d’exemples suivante illustre d’autres utilisations réelles de la conception adaptée incorporée à une hauteur illimitée :

[https://marketing.adobe.com/resources/help/en_US/dm/shoppable-banner/samples/InteractiveImage-responsive-unrestricted-height.html](https://marketing.adobe.com/resources/help/en_US/dm/shoppable-banner/samples/InteractiveImage-responsive-unrestricted-height.html)

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
<script type="text/javascript" src="http://aodmarketingna.assetsadobe.com/etc/dam/viewers/s7viewers/html5/js/InteractiveImage.js"></script> 
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
var interactiveImage = new s7viewers.InteractiveImage({ 
 "containerId":"s7viewer", 
"params":{ 
 "asset":"/content/dam/mac/aodmarketingna/shoppable-banner/shoppable-banner.jpg", 
 "serverurl":"http://aodmarketingna.assetsadobe.com/is/image" 
} 
}).init(); 
</script> 
</body> 
</html> 
```

**Incorporation à l’aide d’une API basée sur Setter**

Au lieu d’utiliser l’initialisation basée sur JSON, il est possible d’utiliser une API basée sur un setter et un constructeur sans args. L’utilisation de ce constructeur d’API ne prend aucun paramètre et les paramètres de configuration sont spécifiés à l’aide `setContainerId()`, `setParam()`et `setAsset()` des méthodes API avec des appels JavaScript distincts.

L’exemple suivant illustre l’utilisation de l’incorporation de tailles fixes avec l’API basée sur un setter :

```
<!DOCTYPE html> 
<html> 
<head> 
<script type="text/javascript" src="http://aodmarketingna.assetsadobe.com/etc/dam/viewers/s7viewers/html5/js/InteractiveImage.js"></script> 
<style type="text/css"> 
#s7viewer.s7interactiveimage { 
 width: 1174px; 
 height: 500px; 
} 
</style> 
</head> 
<body> 
<div id="s7viewer" style="position:relative"></div> 
<script type="text/javascript"> 
var interactiveImage = new s7viewers.InteractiveImage(); 
interactiveImage.setContainerId("s7viewer"); 
interactiveImage.setParam("serverurl", "http://aodmarketingna.assetsadobe.com/is/image"); 
interactiveImage.setAsset("/content/dam/mac/aodmarketingna/shoppable-banner/shoppable-banner.jpg"); 
interactiveImage.init(); 
</script> 
</body> 
</html> 
```

