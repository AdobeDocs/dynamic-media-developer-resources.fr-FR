---
description: Interactive Image Viewer est une visionneuse qui affiche une seule image non zoomable avec des zones réactives cliquables. L’objectif de ce lecteur est de mettre en oeuvre une expérience de "bannière modifiable". En d’autres termes, l’utilisateur peut sélectionner une zone réactive sur l’image de la bannière et être redirigé vers une Vue rapide ou une page des détails du produit sur votre site Web. Il est conçu pour fonctionner sur les ordinateurs de bureau et les périphériques mobiles.
solution: Experience Manager
title: Image interactive
feature: Dynamic Media Classic,Viewers,SDK/API,Interactive Images
role: Developer,Business Practitioner
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '1752'
ht-degree: 0%

---


# Image interactive{#interactive-image}

Interactive Image Viewer est une visionneuse qui affiche une seule image non zoomable avec des zones réactives cliquables. L’objectif de ce lecteur est de mettre en oeuvre une expérience de &quot;bannière modifiable&quot;. En d’autres termes, l’utilisateur peut sélectionner une zone réactive sur l’image de la bannière et être redirigé vers une Vue rapide ou une page des détails du produit sur votre site Web. Il est conçu pour fonctionner sur les ordinateurs de bureau et les périphériques mobiles.

>[!NOTE]
>
>Les images qui utilisent la fonction IR (Image Rendering) ou UGC (User-Generated Content) ne sont pas prises en charge par cette visionneuse.

Le type de lecteur est 508.

## URL de la démonstration {#section-c0ad383db6a444979dc7eeb1ec4cf54d}

[https://marketing.adobe.com/resources/help/en_US/dm/shoppable-banner/samples/InteractiveImage.html](https://marketing.adobe.com/resources/help/en_US/dm/shoppable-banner/samples/InteractiveImage.html)

## Configuration système requise {#section-b7270cc4290043399681dc504f043609}

Voir [Configuration système requise](../../c-system-requirements-and-prerequisites.md#concept-9282e5b777de42cdaf72ef7ebd646842).

## Utilisation de la visionneuse d’images interactive {#section-e6c68406ecdc4de781df182bbd8088b4}

Interactive Image Viewer représente un fichier JavaScript principal et un ensemble de fichiers d’aide (un seul fichier JavaScript comprenant tous les composants du SDK de la visionneuse utilisés par cette visionneuse, ressources et CSS) téléchargés par la visionneuse au moment de l’exécution.

La visionneuse d’images interactive ne peut être utilisée qu’en mode incorporé, où elle est intégrée dans la page Web de cible à l’aide de l’API documentée.

La configuration et l’habillage sont similaires à ceux des autres visionneuses décrits dans cette aide. L’habillage est effectué au moyen d’une page CSS personnalisée.

Voir [Référence de commande commune à toutes les visionneuses - Attributs de configuration](../../r-html5-viewer-20-cmdref-configattrib/r-html5-viewer-20-cmdref-configattrib.md#concept-850e0f2c49b949deb7cfbfd330d329bd) et [Référence de commande commune à toutes les visionneuses - URL](../../c-html5-viewer-20-cmdref-url/c-html5-viewer-20-cmdref-url.md#concept-9b337f349b7b406b8c33c7ee96b3e226)

## Interaction avec la visionneuse d’images interactive {#section-642e66ca38cd4032992840ec6c0b0cd2}

L’interaction prise en charge par la visionneuse d’images vidéo est une activation de zone réactive sur les ordinateurs de bureau. Cette activation survient sur les périphériques tactiles et de clic à l’aide d’une seule pression.

Le lecteur est entièrement accessible au clavier.

Voir [Accessibilité du clavier et navigation](../../c-keyboard-accessibility.md#topic-f5650e9493404e55a3627c8d1366b861).

## Incorporation de la visionneuse d’images interactive {#section-6bb5d3c502544ad18a58eafe12a13435}

Interactive Image Viewer est conçu pour être incorporé à la page d’hébergement. Une telle page Web peut avoir une mise en page statique, ou elle peut être &quot;adaptée&quot; et s’afficher différemment sur différents périphériques ou pour différentes tailles de fenêtre de navigateur.

Pour répondre à ces besoins, le lecteur prend en charge deux modes de fonctionnement Principaux : incorporation de taille fixe et incorporation réactive.

**A propos du mode d&#39;incorporation de taille fixe et du mode d&#39;incorporation de conception réactif**

En mode incorporé, le lecteur est ajouté à la page Web existante. Il se peut que cette page Web comporte déjà du contenu client qui n’est pas lié au lecteur. En règle générale, le lecteur occupe uniquement une partie de l’espace d’une page Web.

Les cas d&#39;utilisation Principaux sont les pages Web orientées vers les ordinateurs de bureau ou les tablettes et les pages adaptées qui ajustent automatiquement la mise en page en fonction du type de périphérique.

L’incorporation de taille fixe est utilisée lorsque la visionneuse ne change pas de taille après le chargement initial. Il s’agit du meilleur choix pour les pages Web présentant une disposition statique.

L’incorporation de la conception réactive suppose que la visionneuse doit peut-être être redimensionnée au moment de l’exécution en réponse au changement de taille de son conteneur `DIV`. Le cas d’utilisation le plus courant consiste à ajouter une visionneuse à une page Web qui utilise une disposition de page souple.

En mode d’incorporation de conceptions réactives, le lecteur se comporte différemment selon la manière dont la page Web dimensionne son conteneur `DIV`. Si la page Web ne définit que la largeur du conteneur `DIV`, en ne limitant pas sa hauteur, le lecteur sélectionne automatiquement sa hauteur en fonction des proportions du fichier utilisé. Cette fonctionnalité permet de s’assurer que la ressource s’intègre parfaitement à la vue sans remplissage sur les côtés. Ce cas d’utilisation est le plus courant pour les pages Web utilisant des structures de mise en page de conception Web réactives telles que Bootstrap, Foundation, etc.

Sinon, si la page Web définit à la fois la largeur et la hauteur du conteneur `DIV` du lecteur, celui-ci remplit uniquement cette zone. Il respecte également la taille de la mise en page Web. Un bon exemple est l’incorporation de la visionneuse dans une incrustation modale, où l’incrustation est dimensionnée en fonction de la taille de la fenêtre du navigateur Web.

**Incorporation de taille fixe**

Pour ajouter la visionneuse à une page Web, procédez comme suit :

1. Ajouter le fichier JavaScript de la visionneuse sur votre page Web.
1. Définition du conteneur `DIV`.
1. Définition de la taille de la visionneuse.
1. Création et initialisation de la visionneuse.

1. Ajouter le fichier JavaScript de la visionneuse sur votre page Web.

   Pour créer une visionneuse, vous devez ajouter une balise de script dans l’en-tête HTML. Avant de pouvoir utiliser l’API du lecteur de contenu, veillez à inclure [!DNL InterativeImage.js]. Le fichier [!DNL InteractiveImage.js] se trouve sous le sous-dossier [!DNL html5/js/] de votre déploiement des visionneuses IS standard :

[!DNL <s7viewers_root>/etc/dam/viewers/s7viewers/html5/js/InteractiveImage.js]

Vous pouvez utiliser un chemin relatif si la visionneuse est déployée sur l’un des serveurs Dynamic Media Classic de l’Adobe et qu’elle est diffusée à partir du même domaine. Sinon, vous spécifiez un chemin d’accès complet à l’un des serveurs Dynamic Media Classic Adobe sur lesquels les visionneuses IS sont installées.

Le chemin relatif ressemble à ce qui suit :

```
<script language="javascript" type="text/javascript" src="/etc/dam/viewers/s7viewers/html5/js/InteractiveImage.js"></script>
```

>[!NOTE]
>
>Vous ne devez référencer que le fichier JavaScript du lecteur principal `include` sur votre page. Vous ne devez pas référencer de fichiers JavaScript supplémentaires dans le code de la page Web qui pourraient être téléchargés selon la logique du lecteur au moment de l’exécution. En particulier, ne référencez pas directement la bibliothèque HTML5 SDK `Utils.js` chargée par la visionneuse à partir du chemin de contexte `/s7viewers` (appelé SDK consolidé `include`). La raison en est que l’emplacement des bibliothèques de lecteurs de contenu d’exécution `Utils.js` ou similaires est entièrement géré par la logique du lecteur et que l’emplacement change entre les versions du lecteur. Adobe ne conserve pas les anciennes versions du lecteur secondaire `includes` sur le serveur.
>
>
>Par conséquent, le fait de placer une référence directe à tout script JavaScript secondaire `include` utilisé par le lecteur sur la page rompt la fonctionnalité du lecteur à l’avenir lorsqu’une nouvelle version du produit est déployée.

1. Définition du conteneur `DIV`.

   Ajoutez un élément `DIV` vide sur la page dans laquelle vous souhaitez que le lecteur s’affiche. L&#39;identifiant de l&#39;élément `DIV` doit être défini, car il est transmis ultérieurement à l&#39;API du lecteur de contenu. La taille du DIV est spécifiée par le biais de CSS.

   L’espace réservé `DIV` est un élément positionné, ce qui signifie que la propriété CSS `position` est définie sur `relative` ou `absolute`.

   Voici un exemple d’élément d’espace réservé défini `DIV` :

   ```
   <div id="s7viewer" style="position:relative"></div>
   ```

1. Définition de la taille de la visionneuse

   Vous pouvez définir la taille statique de la visionneuse en la déclarant pour la classe CSS de niveau supérieur `.s7interactiveimage` en unités absolues ou en utilisant le modificateur `stagesize`.

   Vous pouvez placer le dimensionnement en CSS directement sur la page HTML ou dans un fichier CSS de visionneuse personnalisée, qui est ensuite affecté à un enregistrement de paramètre prédéfini de visionneuse en AEM Assets - à la demande ou transmis explicitement à l’aide de la commande `style`.

   Voir [Vidéo](../../c-html5-aem-asset-viewers/c-html5-aem-interactive-images/c-html5-aem-interactive-image-customizingviewer/c-html5-aem-interactive-image-customizingviewer.md#concept-73a8546acdb444a387c49969ceca57d0) pour plus d’informations sur le style de la visionneuse avec CSS.

   Voici un exemple de définition de la taille d’une visionneuse statique dans la page HTML :

   ```
   #s7viewer.s7interactiveimage { 
    width: 1174px; 
    height: 500px; 
   }
   ```

   Vous pouvez transmettre explicitement le modificateur `stagesize` avec le code d’initialisation de la visionneuse avec la collection `params` ou en tant qu’appel d’API comme décrit dans la section Référence de commandes, comme suit :

   ```
   interactiveImage.setParam("stagesize", "1174,500");
   ```

   Une approche CSS est recommandée et est utilisée dans cet exemple.

1. Création et initialisation de la visionneuse.

   Une fois les étapes ci-dessus terminées, vous créez une instance de classe `s7viewers.InteractiveImage`, transmettez toutes les informations de configuration à son constructeur et appelez la méthode `init()` sur une instance de lecteur. Les informations de configuration sont transmises au constructeur sous la forme d’un objet JSON. Au minimum, cet objet doit comporter un champ `containerId` contenant le nom de l’ID de conteneur de la visionneuse et un objet JSON imbriqué `params` avec les paramètres de configuration pris en charge par la visionneuse. Dans ce cas, l’objet `params` doit avoir au moins la propriété Image Serving URL transmise en tant que propriété `serverUrl` et la ressource initiale en tant que paramètre `asset`. L’API d’initialisation basée sur JSON vous permet de créer et de début le lecteur avec une seule ligne de code.

   Il est important que le conteneur de la visionneuse soit ajouté au modèle DOM afin que le code de la visionneuse puisse trouver l’élément de conteneur en fonction de son identifiant. Certains navigateurs retardent la création du modèle DOM jusqu’à la fin de la page Web. Pour une compatibilité maximale, appelez la méthode `init()` juste avant la balise de fermeture `BODY` ou sur le événement body `onload()`.

   Dans le même temps, l’élément conteneur ne doit pas nécessairement faire partie de la mise en page de la page Web pour le moment. Par exemple, il peut être masqué à l’aide du style `display:none` qui lui est affecté. Dans ce cas, le lecteur retarde son processus d’initialisation jusqu’au moment où la page Web ramène l’élément de conteneur à la mise en page. Dans ce cas, le chargement du lecteur reprend automatiquement.

   Voici un exemple de création d’une instance de visionneuse, de transmission des options de configuration minimales nécessaires au constructeur et d’appel de la méthode `init()`. L’exemple suppose que `interactiveImage` correspond à l’instance de visionneuse ; `s7viewer` est le nom de l&#39;espace réservé `DIV`; `http://aodmarketingna.assetsadobe.com/is/image` correspond à l’URL de diffusion d’images et `/content/dam/mac/aodmarketingna/shoppable-banner/shoppable-banner.` à la ressource :

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

   Le code suivant est un exemple complet d’une page Web triviale qui incorpore la visionneuse d’images vidéo d’une taille fixe :

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

Avec l’incorporation de conceptions réactives, la page Web dispose normalement d’une sorte de disposition souple qui détermine la taille d’exécution du conteneur `DIV` du lecteur. Pour l’exemple suivant, supposons que la page Web permette au conteneur `DIV` du lecteur de prendre 40 % de la taille de la fenêtre du navigateur Web. Et sa hauteur est laissée sans restriction. Le code HTML de la page Web se présenterait comme suit :

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
1. Définition du conteneur `DIV`.
1. Création et initialisation de la visionneuse.

Toutes les étapes ci-dessus sont identiques à celles de l’incorporation de taille fixe. Ajoutez le conteneur `DIV` au `"holder"` `DIV` existant. Le code suivant est un exemple complet. Notez comment la taille de la visionneuse change lorsque le navigateur est redimensionné et comment les proportions de la visionneuse correspondent à la ressource.

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

La page d’exemples suivante illustre d’autres utilisations réelles de l’incorporation de conceptions réactives avec une hauteur libre :

[https://marketing.adobe.com/resources/help/en_US/dm/shoppable-banner/samples/InteractiveImage-responsive-unrestricted-height.html](https://marketing.adobe.com/resources/help/en_US/dm/shoppable-banner/samples/InteractiveImage-responsive-unrestricted-height.html)

**Incorporation de taille flexible avec définition de largeur et de hauteur**

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

Le reste des étapes d&#39;incorporation est identique aux étapes utilisées pour l&#39;incorporation réactive avec une hauteur libre. L’exemple qui en résulte est le suivant :

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

Au lieu d’utiliser l’initialisation basée sur JSON, il est possible d’utiliser une API basée sur un setter et un constructeur sans args. L&#39;utilisation de ce constructeur d&#39;API ne prend aucun paramètre et les paramètres de configuration sont spécifiés à l&#39;aide des méthodes d&#39;API `setContainerId()`, `setParam()` et `setAsset()` avec des appels JavaScript distincts.

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

