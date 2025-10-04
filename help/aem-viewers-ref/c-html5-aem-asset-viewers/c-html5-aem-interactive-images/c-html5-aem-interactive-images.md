---
title: Image interactive
description: La visionneuse d’images interactives est une visionneuse qui affiche une image unique, non zoomable, avec des zones réactives cliquables. Cette visionneuse a pour objectif de mettre en œuvre une expérience de « bannière shoppable ». En d’autres termes, l’utilisateur peut sélectionner une zone réactive au-dessus de l’image de bannière et être redirigé vers une page d’aperçu rapide ou de détails de produit sur votre site web. Il est conçu pour fonctionner sur les ordinateurs de bureau et les appareils mobiles.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Interactive Images
role: Developer,User
exl-id: c7089ecd-6ff3-4fe9-9ee7-3b48c9201558
source-git-commit: ce1ac4938c7baf482c6c55a9ad13379153a3ec5b
workflow-type: tm+mt
source-wordcount: '1686'
ht-degree: 0%

---

# Image interactive{#interactive-image}

La visionneuse d’images interactives est une visionneuse qui affiche une image unique, non zoomable, avec des zones réactives cliquables. Cette visionneuse a pour objectif de mettre en œuvre une expérience de « bannière shoppable ». En d’autres termes, l’utilisateur peut sélectionner une zone réactive au-dessus de l’image de bannière et être redirigé vers une page d’aperçu rapide ou de détails de produit sur votre site web. Il est conçu pour fonctionner sur les ordinateurs de bureau et les appareils mobiles.

>[!NOTE]
>
>Les images qui utilisent le rendu d’image (IR) ou le contenu créé par l’utilisateur (UGC) ne sont pas pris en charge par cette visionneuse.

Le type de visionneuse est 508.

## URL de démonstration {#section-c0ad383db6a444979dc7eeb1ec4cf54d}

[https://landing.adobe.com/en/na/dynamic-media/ctir-2755/live-demos.html](https://landing.adobe.com/en/na/dynamic-media/ctir-2755/live-demos.html)

<!--

[https://experienceleague.adobe.com/tools/dynamic-media-demo/shoppable-banner/InteractiveImage.html](https://experienceleague.adobe.com/tools/dynamic-media-demo/shoppable-banner/InteractiveImage.html)

-->

## Configuration système requise {#section-b7270cc4290043399681dc504f043609}

Voir [Configuration requise](../../c-system-requirements-and-prerequisites.md#concept-9282e5b777de42cdaf72ef7ebd646842).

## Utilisation de la visionneuse d’images interactives {#section-e6c68406ecdc4de781df182bbd8088b4}

La visionneuse d’images interactives représente un fichier JavaScript principal et un ensemble de fichiers d’assistance (un seul JavaScript inclus avec tous les composants SDK de la visionneuse utilisés par cette visionneuse particulière, ressources, CSS) téléchargés par la visionneuse au moment de l’exécution.

La visionneuse d’images interactive ne peut être utilisée qu’en mode incorporé, où elle est intégrée à la page web cible à l’aide de l’API documentée.

La configuration et l’habillage sont similaires à ceux des autres visionneuses décrites dans cette aide. Toute application de la peau est réalisée au moyen d’un CSS personnalisé.

Voir [&#x200B; Référence des commandes commune à toutes les visionneuses - Attributs de configuration &#x200B;](../../r-html5-viewer-20-cmdref-configattrib/r-html5-viewer-20-cmdref-configattrib.md#concept-850e0f2c49b949deb7cfbfd330d329bd) et [&#x200B; Référence des commandes commune à toutes les visionneuses - URL](../../c-html5-viewer-20-cmdref-url/c-html5-viewer-20-cmdref-url.md#concept-9b337f349b7b406b8c33c7ee96b3e226)

## Interaction avec la visionneuse d’images interactives {#section-642e66ca38cd4032992840ec6c0b0cd2}

L’interaction prise en charge par la visionneuse d’images vidéo est l’activation des zones réactives sur les systèmes de bureau. Cette activation s’effectue en un seul clic et sur les appareils tactiles.

La visionneuse est entièrement accessible à l’aide du clavier.

Voir [Accessibilité clavier et navigation](../../c-keyboard-accessibility.md#topic-f5650e9493404e55a3627c8d1366b861).

## Incorporation de la visionneuse d’images interactives {#section-6bb5d3c502544ad18a58eafe12a13435}

La visionneuse d’images interactives est incorporée à la page d’hébergement. Une telle page web peut avoir une disposition statique, ou elle peut être « réactive » et s’afficher différemment sur différents appareils ou pour différentes tailles de fenêtre du navigateur.

Pour répondre à ces besoins, la visionneuse prend en charge deux modes de fonctionnement principaux : l’incorporation de taille fixe et l’incorporation réactive.

**À propos du mode d’incorporation de taille fixe et du mode d’incorporation de conception réactive**

En mode incorporé, la visionneuse est ajoutée à la page web existante. Il se peut que cette page web contienne déjà du contenu client sans rapport avec la visionneuse. L’observateur n’occupe normalement qu’une partie de l’espace d’une page web.

Les principaux cas d’utilisation sont des pages web orientées pour les ordinateurs de bureau ou les tablettes, et des pages en responsive design qui ajustent automatiquement la disposition en fonction du type d’appareil.

L’incorporation de taille fixe est utilisée lorsque la visionneuse ne modifie pas sa taille après le chargement initial. Cette méthode est recommandée pour les pages web avec une disposition statique.

L’incorporation de conception réactive suppose que la visionneuse doit être redimensionnée au moment de l’exécution en réponse au changement de taille de son `DIV` de conteneur. Le cas d’utilisation le plus courant consiste à ajouter une visionneuse à une page web qui utilise une disposition de page flexible.

En mode d’incorporation de responsive design, la visionneuse se comporte différemment selon la manière dont la page web dimensionne son `DIV` de conteneur. Si la page web définit uniquement la largeur du `DIV` de conteneur, sans restriction de hauteur, la visionneuse choisit automatiquement sa hauteur en fonction des proportions de la ressource utilisée. Cette fonctionnalité garantit que la ressource s’adapte parfaitement à la vue sans marge intérieure sur les côtés. Ce cas d’utilisation est le plus courant pour les pages web utilisant des structures de disposition de conception web réactive telles que Bootstrap et Foundation.

Dans le cas contraire, si la page web définit à la fois la largeur et la hauteur du `DIV` de conteneur de la visionneuse, celle-ci remplit exactement cette zone. Elle respecte également la taille fournie par la mise en page web. Un bon exemple consiste à incorporer la visionneuse dans une superposition modale, où la superposition est dimensionnée en fonction de la taille de la fenêtre du navigateur web.

**Incorporation de taille fixe**

Ajoutez la visionneuse à une page web en procédant comme suit :

1. Ajout du fichier JavaScript de la visionneuse à votre page web.
1. La définition du `DIV` de conteneur.
1. Définition de la taille de la visionneuse.
1. Création et initialisation de la visionneuse.

1. Ajout du fichier JavaScript de la visionneuse à votre page web.

   La création d’une visionneuse nécessite l’ajout d’une balise de script dans l’en-tête HTML. Avant de pouvoir utiliser l’API de visionneuse, veillez à inclure [!DNL InterativeImage.js]. Le fichier [!DNL InteractiveImage.js] se trouve sous le sous-dossier [!DNL html5/js/] de votre déploiement d’observateurs IS standard :

[!DNL <s7viewers_root>/etc/dam/viewers/s7viewers/html5/js/InteractiveImage.js]

Vous pouvez utiliser un chemin relatif si la visionneuse est déployée sur l’un des serveurs d’Adobe Dynamic Media Classic et qu’elle est diffusée à partir du même domaine. Sinon, vous spécifiez un chemin d’accès complet à l’un des serveurs Adobe Dynamic Media Classic sur lesquels les visionneuses IS sont installées.

Le chemin d’accès relatif ressemble à ce qui suit :

```html {.line-numbers}
<script language="javascript" type="text/javascript" src="/etc/dam/viewers/s7viewers/html5/js/InteractiveImage.js"></script>
```

>[!NOTE]
>
>Référencez uniquement le fichier de `include` JavaScript de la visionneuse principale sur votre page. Ne référencez aucun fichier JavaScript supplémentaire dans le code de page web qui pourrait être téléchargé par la logique de la visionneuse au moment de l’exécution. En particulier, ne référencez pas directement la bibliothèque de `Utils.js` SDK HTML5 chargée par la visionneuse à partir `/s7viewers` chemin de contexte (appelé `include` consolidée de SDK). En effet, l’emplacement des bibliothèques de visionneuse d’exécution `Utils.js` ou similaires est entièrement géré par la logique de la visionneuse et l’emplacement change entre les versions de la visionneuse. Adobe ne conserve pas les anciennes versions des `includes` secondaires de la visionneuse sur le serveur.
>
>
>Par conséquent, le fait de placer une référence directe à toute `include` JavaScript secondaire utilisée par la visionneuse sur la page interrompt la fonctionnalité de la visionneuse à l’avenir lorsqu’une nouvelle version du produit est déployée.

1. La définition du `DIV` de conteneur.

   Ajoutez un élément de `DIV` vide sur la page où vous souhaitez que la visionneuse apparaisse. L’ID de l’élément `DIV` doit être défini, car cet ID est transmis ultérieurement à l’API de visionneuse. La taille du DIV est spécifiée via CSS.

   L’espace réservé `DIV` est un élément positionné, ce qui signifie que la propriété CSS `position` est définie sur `relative` ou `absolute`.

   Voici un exemple d’élément `DIV` d’espace réservé défini :

   ```html {.line-numbers}
   <div id="s7viewer" style="position:relative"></div>
   ```

1. Définition de la taille de la visionneuse

   Vous pouvez définir la taille statique de la visionneuse en la déclarant pour `.s7interactiveimage` classe CSS de niveau supérieur dans des unités absolues ou à l’aide du modificateur `stagesize`.

   Vous pouvez définir le dimensionnement dans CSS directement sur la page HTML. Vous pouvez également définir le dimensionnement d’un fichier CSS de visionneuse personnalisé, qui est ensuite affecté à un enregistrement de paramètre prédéfini de visionneuse dans Adobe Experience Manager Assets - À la demande, ou transmis explicitement à l’aide de la commande `style`.

   Voir [Vidéo](../../c-html5-aem-asset-viewers/c-html5-aem-interactive-images/c-html5-aem-interactive-image-customizingviewer/c-html5-aem-interactive-image-customizingviewer.md#concept-73a8546acdb444a387c49969ceca57d0) pour plus d’informations sur la mise en forme de la visionneuse avec CSS.

   Voici un exemple de définition d’une taille de visionneuse statique dans la page HTML :

   ```html {.line-numbers}
   #s7viewer.s7interactiveimage { 
    width: 1174px; 
    height: 500px; 
   }
   ```

   Vous pouvez transmettre explicitement le modificateur `stagesize` avec le code d’initialisation de la visionneuse avec `params` collection ou sous la forme d’un appel API, comme décrit dans la section Référence des commandes , comme suit :

   ```html {.line-numbers}
   interactiveImage.setParam("stagesize", "1174,500");
   ```

   Une approche basée sur CSS est recommandée et est utilisée dans cet exemple.

1. Création et initialisation de la visionneuse.

   Une fois les étapes ci-dessus terminées, vous créez une instance de `s7viewers.InteractiveImage` classe, transmettez toutes les informations de configuration à son constructeur, puis appelez `init()` méthode sur une instance de visionneuse. Les informations de configuration sont transmises au constructeur en tant qu’objet JSON. Au minimum, cet objet doit comporter `containerId` champ qui contient le nom de l’ID de conteneur de visionneuse et de l’objet JSON `params` imbriqué avec les paramètres de configuration pris en charge par la visionneuse. Dans ce cas, l’objet `params` doit comporter au moins l’URL du service d’images transmise en tant que propriété `serverUrl`, et la ressource initiale en tant que paramètre `asset`. L’API d’initialisation basée sur JSON vous permet de créer et de démarrer la visionneuse avec une seule ligne de code.

   Il est important d’ajouter le conteneur de visionneuse au DOM afin que le code de la visionneuse puisse trouver l’élément de conteneur à l’aide de son identifiant. Certains navigateurs retardent la création du DOM jusqu’à la fin de la page web. Pour une compatibilité maximale, appelez la méthode `init()` juste avant la balise `BODY` de fermeture ou sur l’événement body `onload()`.

   Dans le même temps, l’élément de conteneur ne doit pas nécessairement encore faire partie de la mise en page web. Par exemple, elle peut être masquée à l’aide `display:none` style qui lui est affecté. Dans ce cas, la visionneuse retarde son processus d’initialisation jusqu’au moment où la page web ramène l’élément de conteneur dans la mise en page. Lorsque cet événement se produit, le chargement de la visionneuse reprend automatiquement.

   Voici un exemple de création d’une instance de visionneuse, transmettant les options de configuration minimales nécessaires au constructeur et appelant la méthode `init()`. L’exemple suppose que `interactiveImage` est l’instance de visionneuse, `s7viewer` est le nom de l’espace réservé `DIV`, `http://aodmarketingna.assetsadobe.com/is/image` est l’URL du service d’images et `/content/dam/mac/aodmarketingna/shoppable-banner/shoppable-banner.` est la ressource :

   ```html {.line-numbers}
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

   Le code suivant est un exemple complet de page web triviale qui incorpore la visionneuse d’images vidéo à taille fixe :

   ```html {.line-numbers}
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

**Incorporation de conception réactive avec hauteur illimitée**

Avec l’incorporation de responsive design, la page web dispose normalement d’un type de disposition flexible qui détermine la taille d’exécution du `DIV` de conteneur de la visionneuse. Pour l’exemple suivant, supposons que la page web permette au `DIV` du conteneur de la visionneuse de prendre 40 % de la taille de la fenêtre du navigateur web. Et sa hauteur n&#39;est pas limitée. Le code d’HTML de la page web se présente comme suit :

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
1. La définition du `DIV` de conteneur.
1. Création et initialisation de la visionneuse.

Toutes les étapes ci-dessus sont identiques à l’incorporation de taille fixe. Ajoutez le `DIV` de conteneur au `"holder"` de `DIV` existant. Le code suivant en est un exemple complet. Notez la manière dont la taille de la visionneuse change lorsque le navigateur est redimensionné, ainsi que la manière dont les proportions de la visionneuse correspondent à la ressource.

```html {.line-numbers}
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

<!-- The following examples page illustrates more real-life uses of responsive design embedding with unrestricted height: -->

<!--

[https://experienceleague.adobe.com/tools/dynamic-media-demo/shoppable-banner/InteractiveImage-responsive-unrestricted-height.html](https://experienceleague.adobe.com/tools/dynamic-media-demo/shoppable-banner/InteractiveImage-responsive-unrestricted-height.html)

-->

**Incorporation de taille flexible avec largeur et hauteur définies**

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

Le reste des étapes d&#39;incorporation est identique aux étapes utilisées pour une incorporation réactive avec une hauteur illimitée. L’exemple qui en résulte est le suivant :

```html {.line-numbers}
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

**Incorporation à l’aide de l’API Setter**

Au lieu d’utiliser l’initialisation basée sur JSON, il est possible d’utiliser l’API basée sur setter et le constructeur sans args. L’utilisation de ce constructeur d’API ne prend aucun paramètre et les paramètres de configuration sont spécifiés à l’aide des méthodes d’API `setContainerId()`, `setParam()` et `setAsset()` avec des appels JavaScript distincts.

L’exemple suivant illustre l’utilisation de l’incorporation de taille fixe avec l’API basée sur setter :

```html {.line-numbers}
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
