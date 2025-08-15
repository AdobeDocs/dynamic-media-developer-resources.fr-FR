---
title: Carrousel
description: La visionneuse Carrousel affiche un carrousel d’images de bannières non zoomables, comportant des zones réactives cliquables. Cette visionneuse peut vous aider à implémenter une expérience de « carrousel d’achat » dans laquelle les utilisateurs peuvent sélectionner une zone réactive ou une zone sur l’image de bannière. Il peut être redirigé vers une page d’aperçu rapide ou de détails du produit sur le site web du client. Il est conçu pour fonctionner sur les ordinateurs de bureau et les appareils mobiles.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Carousel Banners
role: Developer,User
exl-id: d506dc6e-8929-4f7f-a205-1683e77681f1
source-git-commit: b89ca96947f751b750623e1f18d2a5d86f0cd759
workflow-type: tm+mt
source-wordcount: '1867'
ht-degree: 0%

---

# Carrousel{#carousel}

La visionneuse Carrousel affiche un carrousel d’images de bannières non zoomables, comportant des zones réactives cliquables. Cette visionneuse peut vous aider à implémenter une expérience de « carrousel d’achat » dans laquelle les utilisateurs peuvent sélectionner une zone réactive ou une zone sur l’image de bannière. Il peut être redirigé vers une page d’aperçu rapide ou de détails du produit sur le site web du client. Il est conçu pour fonctionner sur les ordinateurs de bureau et les appareils mobiles.

>[!NOTE]
>
>Les images qui utilisent le rendu d’image ou le contenu créé par l’utilisateur ne sont pas pris en charge par cette visionneuse.

Type de visionneuse : 511.

## URL de démonstration {#section-c0ad383db6a444979dc7eeb1ec4cf54d}

[https://experienceleague.adobe.com/tools/dynamic-media-demo/viewers-ref/carousel/CarouselViewerDemo.html](https://experienceleague.adobe.com/tools/dynamic-media-demo/viewers-ref/carousel/CarouselViewerDemo.html)

## Configuration système requise {#section-b7270cc4290043399681dc504f043609}

Voir [Configuration requise](../../c-system-requirements-and-prerequisites.md#concept-9282e5b777de42cdaf72ef7ebd646842).

## Utilisation de la visionneuse de carrousel {#section-e6c68406ecdc4de781df182bbd8088b4}

La visionneuse de carrousel représente un fichier JavaScript principal et un ensemble de fichiers d’assistance (une seule JavaScript inclure avec tous les composants SDK de la visionneuse utilisés par cette visionneuse particulière, ressources, CSS) téléchargés par la visionneuse au moment de l’exécution.

Carousel Viewer peut être utilisé à la fois en mode pop-up à l’aide d’une page HTML prête pour la production fournie avec IS Viewers, ou en mode incorporé où il est intégré dans la page Web cible à l’aide d’une API documentée.

La configuration et l’habillage sont similaires à ceux des autres visionneuses décrites dans cette aide. Tout l’habillage est réalisé par le biais d’une feuille de style CSS personnalisée.

Voir [Référence de commande commune à tous les visualiseurs - Attributs](../../r-html5-viewer-20-cmdref-configattrib/r-html5-viewer-20-cmdref-configattrib.md#concept-850e0f2c49b949deb7cfbfd330d329bd) de configuration et [Référence de commande communs à tous les visualiseurs - URL](../../c-html5-viewer-20-cmdref-url/c-html5-viewer-20-cmdref-url.md#concept-9b337f349b7b406b8c33c7ee96b3e226)

## Interaction avec la visionneuse de carrousel {#section-642e66ca38cd4032992840ec6c0b0cd2}

La navigation dans l’ensemble de carrousel se fait à l’aide d’un balayage horizontal sur la vue principale ou avec deux boutons fléchés disponibles sur l’appareil de bureau. Les points indicateurs définissent la position actuelle dans l’ensemble.

La visionneuse peut afficher des zones réactives ou des régions au-dessus de l’image de bannière pour indiquer la zone interactive du produit.

Le fait de cliquer ou d’appuyer sur une zone réactive ou une région déclenche une action qui lui est associée pendant le temps de création. L’action peut être redirigée vers une autre page du site Web ou elle peut renvoyer des informations produit à la logique de la page Web, ce qui peut déclencher un aperçu rapide avec le contenu produit associé.

La visionneuse est entièrement accessible à l’aide du clavier.

Voir [Accessibilité clavier et navigation](../../c-keyboard-accessibility.md#topic-f5650e9493404e55a3627c8d1366b861).

## Incorporation de la visionneuse de carrousel {#section-6bb5d3c502544ad18a58eafe12a13435}

**A propos du mode pop-up**

En mode pop-up, la visionneuse est ouverte dans une fenêtre ou un onglet de navigateur Web distinct. Il prend toute la zone de la fenêtre du navigateur et s’ajuste en cas de redimensionnement du navigateur ou de changement d’orientation d’un appareil mobile.

Le mode pop-up est le plus courant pour les appareils mobiles. La page Web charge la visionneuse à l’aide `window.open()` d’JavaScript appel, d’un élément HTML correctement configuré `A` ou de toute autre méthode appropriée.

Il est recommandé d’utiliser une page HTML prête à l’emploi pour le mode de fonctionnement contextuel. Dans ce cas, il est appelé `CarouselViewer.html` et se trouve dans le `html5/` sous-dossier de votre déploiement IS-Viewers standard :

`<s7viewers_root>/html5/CarouselViewer.html`

Vous pouvez obtenir une personnalisation visuelle en appliquant une feuille de style CSS personnalisée.

Voici un exemple de code HTML qui ouvre la visionneuse dans une nouvelle fenêtre :

```html {.line-numbers}
<a href="https://demos-pub.assetsadobe.com/etc/dam/viewers/s7viewers/html5/CarouselViewer.html?asset=/content/dam/dm-public-facing-live-demo-page/04_shoppable_carousel/05_shoppable_banner&serverurl=https://adobedemo62-h.assetsadobe.com/is/image" target="_blank">Open popup viewer</a>
```

**A propos du mode d’incorporation de taille fixe et du mode d’incorporation de conception réactive**

En mode intégré, la visionneuse est ajoutée à la page Web existante. Cette page Web peut déjà contenir du contenu client non lié à la visionneuse. Le spectateur n’occupe normalement qu’une partie de l’espace d’une page Web.

Les principaux cas d’utilisation sont les pages Web orientées vers les ordinateurs de bureau ou les tablettes, et les pages réactives qui ajustent automatiquement la mise en page en fonction du type d’appareil.

L’incorporation de taille fixe est utilisée lorsque la visionneuse ne modifie pas sa taille après le chargement initial. Cette méthode est le meilleur choix pour les pages Web qui ont une disposition statique.

L’incorporation de conception réactive suppose que la visionneuse doit se redimensionner au moment de l’exécution en réponse au changement de taille de son conteneur `DIV`. Le cas d’utilisation le plus courant est l’ajout d’une visionneuse à une page Web qui utilise une mise en page flexible.

En mode d’incorporation de responsive design, la visionneuse se comporte différemment selon la manière dont la page web dimensionne son `DIV` de conteneur. Si la page web définit uniquement la largeur du `DIV` de conteneur, sans restriction de hauteur, la visionneuse choisit automatiquement sa hauteur en fonction des proportions de la ressource utilisée. Cette fonctionnalité garantit que la ressource s’adapte parfaitement à la vue sans marge intérieure sur les côtés. Ce cas d’utilisation est le plus courant pour les pages web utilisant des structures de disposition de conception web réactive telles que Bootstrap et Foundation.

Dans le cas contraire, si la page web définit à la fois la largeur et la hauteur du `DIV` de conteneur de la visionneuse, celle-ci remplit exactement cette zone. Elle respecte également la taille fournie par la mise en page web. Un bon exemple consiste à incorporer la visionneuse dans une superposition modale, où la superposition est dimensionnée en fonction de la taille de la fenêtre du navigateur web.

**Incorporation de taille fixe**

Pour ajouter la visionneuse à une page Web, procédez comme suit :

1. Ajout du fichier JavaScript de visionneuse à votre page Web.
1. Définition du conteneur `DIV`.
1. Définition de la taille de la visionneuse.
1. Création et initialisation de la visionneuse.

1. Ajout du fichier JavaScript de visionneuse à votre page Web.

   Pour créer une visionneuse, vous devez ajouter une balise de script dans l’en-tête HTML. Avant de pouvoir utiliser l’API de visionneuse, veillez à inclure [!DNL CarouselViewer.js]le fichier . Le [!DNL CarouselViewer.js] fichier se trouve dans le [!DNL html5/js/] sous-dossier de votre déploiement IS-Viewers standard :

[!DNL <s7viewers_root>/etc/dam/viewers/s7viewers/html5/js/CarouselViewer.js]

Vous pouvez utiliser un chemin d’accès relatif si la visionneuse est déployée sur l’un des serveurs Adobe Dynamic Media Classic et qu’elle est diffusée à partir du même domaine. Sinon, vous spécifiez un chemin d’accès complet à l’un des serveurs Adobe Dynamic Media Classic sur lesquels les IS-Viewers sont installés.

Le chemin d’accès relatif ressemble à ce qui suit :

```html {.line-numbers}
<script language="javascript" type="text/javascript" src="/etc/dam/viewers/s7viewers/html5/js/CarouselViewer.js"></script>
```

>[!NOTE]
>
>Référencez uniquement le fichier JavaScript `include` de visionneuse principal sur votre page. Ne référencez aucun fichier JavaScript supplémentaire dans le code de page web qui pourrait être téléchargé par la logique de la visionneuse au moment de l’exécution. En particulier, ne référencez pas directement la bibliothèque de `Utils.js` SDK HTML5 chargée par la visionneuse à partir `/s7viewers` chemin de contexte (appelé `include` consolidée de SDK). En effet, l’emplacement des bibliothèques de visionneuse d’exécution `Utils.js` ou similaires est entièrement géré par la logique de la visionneuse et l’emplacement change entre les versions de la visionneuse. Adobe ne conserve pas les anciennes versions des `includes` secondaires de la visionneuse sur le serveur.
>
>
>Par conséquent, le fait de placer une référence directe à toute `include` JavaScript secondaire utilisée par la visionneuse sur la page interrompt la fonctionnalité de la visionneuse à l’avenir lorsqu’une nouvelle version du produit est déployée.

1. La définition du `DIV` de conteneur.

   Ajoutez un élément vide `DIV` à la page dans laquelle vous souhaitez que la visionneuse apparaisse. L’ID `DIV` doit être défini pour l’élément, car cet identifiant est transmis ultérieurement à l’API de visionneuse. La taille de la DIV est spécifiée via CSS.

   L’espace réservé `DIV` est un élément positionné, ce qui signifie que la `position` propriété CSS est définie sur `relative` ou `absolute`.

   Voici un exemple d’élément `DIV` d’espace réservé défini :

   ```CSS {.line-numbers}
   <div id="s7viewer" style="position:relative"></div>
   ```

1. Définition de la taille de la visionneuse

   Vous pouvez définir la taille statique de la visionneuse en la déclarant pour `.s7carouselviewer` classe CSS de niveau supérieur dans des unités absolues ou à l’aide du modificateur `stagesize`.

   Vous pouvez définir le dimensionnement dans CSS directement sur la page HTML. Vous pouvez également placer le dimensionnement dans un fichier CSS de visionneuse personnalisé, qui est ensuite affecté à un enregistrement de paramètre prédéfini de visionneuse dans AEM Assets - À la demande, ou transmis explicitement à l’aide de la `style` commande.

   Voir [Personnalisation de la visionneuse](../../c-html5-aem-asset-viewers/c-html5-aem-carousel/c-html5-aem-carousel-customizingviewer/c-html5-aem-carousel-customizingviewer.md#concept-73a8546acdb444a387c49969ceca57d0) de carrousel pour plus d’informations sur le style de la visionneuse avec CSS.

   Voici un exemple de définition d’une taille de visionneuse statique dans la page HTML :

   ```CSS {.line-numbers}
   #s7viewer.s7carouselviewer { 
    width: 1174px; 
    height: 500px; 
   }
   ```

   Vous pouvez transmettre explicitement le `stagesize` modificateur avec le code d’initialisation de la visionneuse avec `params` collection ou sous forme d’appel d’API comme décrit dans la section Référence des commandes, comme suit :

   ```CSS {.line-numbers}
   carouselViewer.setParam("stagesize", "1174,500");
   ```

   Une approche basée sur le code CSS est recommandée et est utilisée dans cet exemple.

1. Création et initialisation de la visionneuse.

   Lorsque vous avez terminé les étapes ci-dessus, vous créez une instance de classe, transmettez toutes les informations de configuration à son constructeur et appelez `s7viewers.CarouselViewer` la méthode sur une instance de `init()` visionneuse. Les informations de configuration sont transmises au constructeur sous la forme d’un objet JSON. Au minimum, cet objet doit avoir `containerId` un champ qui contient le nom de l’ID de conteneur de la visionneuse et l’objet JSON imbriqué `params` avec les paramètres de configuration pris en charge par la visionneuse. Dans ce cas, l’objet `params` doit avoir au moins l’URL Image Serving transmise en tant que propriété et la ressource initiale en tant que `serverUrl` `asset` paramètre. L’API d’initialisation basée sur JSON vous permet de créer et de démarrer la visionneuse avec une seule ligne de code.

   Il est important d’ajouter le conteneur de visionneuse au DOM afin que le code de visionneuse puisse trouver l’élément conteneur par son identifiant. Certains navigateurs retardent la création de DOM jusqu’à la fin de la page Web. Pour une compatibilité maximale, appelez la `init()` méthode juste avant la balise de fermeture `BODY` , ou sur l’événement body `onload()` .

   Dans le même temps, l’élément conteneur ne doit pas nécessairement faire partie de la mise en page Web pour le moment. Par exemple, il peut être masqué à l’aide `display:none` du style qui lui est attribué. Dans ce cas, la visionneuse retarde son processus d’initialisation jusqu’au moment où la page Web ramène l’élément conteneur à la mise en page. Lorsque cette fonctionnalité se produit, le chargement de la visionneuse reprend automatiquement.

   Voici un exemple de création d’une instance de visionneuse, en transmettant les options de configuration minimales nécessaires au constructeur et en appelant la `init()` méthode. L’exemple suppose `carouselViewer` est l’instance de visionneuse ; `s7viewer` est le nom de l’espace `DIV`réservé ; `https://adobedemo62-h.assetsadobe.com/is/image` est l’URL du serveur d’images et `/content/dam/dm-public-facing-live-demo-page/04_shoppable_carousel/05_shoppable_banner` est l’actif :

   ```javascript {.line-numbers}
   <script type="text/javascript"> 
   var carouselViewer = new s7viewers.CarouselViewer ({ 
    "containerId":"s7viewer", 
   "params":{ 
    "asset":"/content/dam/dm-public-facing-live-demo-page/04_shoppable_carousel/05_shoppable_banner", 
    "serverurl":"https://adobedemo62-h.assetsadobe.com/is/image" 
   } 
   }).init(); 
   </script>
   ```

   Le code suivant est un exemple complet de page Web triviale qui intègre la visionneuse de carrousel avec une taille fixe :

   ```html {.line-numbers}
   <!DOCTYPE html> 
   <html> 
   <head> 
   <script type="text/javascript" src="https://demos-pub.assetsadobe.com/etc/dam/viewers/s7viewers/html5/js/CarouselViewer.js"></script> 
   <style type="text/css"> 
   #s7viewer.s7carouselviewer { 
    width: 1174px; 
    height: 500px; 
   } 
   </style> 
   </head> 
   <body> 
   <div id="s7viewer" style="position:relative"></div> 
   <script type="text/javascript"> 
   var carouselViewer = new s7viewers.CarouselViewer({ 
    "containerId":"s7viewer", 
   "params":{ 
    "asset":"/content/dam/dm-public-facing-live-demo-page/04_shoppable_carousel/05_shoppable_banner", 
    "serverurl":"https://adobedemo62-h.assetsadobe.com/is/image" 
   } 
   }).init(); 
   </script> 
   </body> 
   </html>
   ```

**Intégration de conception réactive avec une hauteur illimitée**

Avec l’intégration de conception réactive, la page Web a normalement une sorte de mise en page flexible en place qui dicte la taille d’exécution du conteneur `DIV`de la visionneuse. Pour l’exemple suivant, supposons que la page Web autorise le conteneur `DIV` de la visionneuse à utiliser 40 % de la taille de la fenêtre du navigateur Web. Et, sa hauteur est laissée sans restriction. Le code HTML de la page Web doit ressembler à ce qui suit :

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

L’ajout de la visionneuse à une telle page est similaire aux étapes d’incorporation de taille fixe. La seule différence réside dans le fait que vous n’avez pas besoin de définir explicitement la taille de la visionneuse.

1. Ajout du fichier JavaScript de visionneuse à votre page Web.
1. Définition du conteneur `DIV`.
1. Création et initialisation de la visionneuse.

Toutes les étapes ci-dessus sont identiques à celles de l’incorporation de taille fixe. Ajoutez le conteneur `DIV` au conteneur existant `"holder"` `DIV`. Le code suivant est un exemple complet. Notez comment la taille de la visionneuse change lorsque le navigateur est redimensionné et comment le rapport d’aspect de la visionneuse correspond à la ressource.

```html {.line-numbers}
<!DOCTYPE html> 
<html> 
<head> 
<script type="text/javascript" src="https://demos-pub.assetsadobe.com/etc/dam/viewers/s7viewers/html5/js/CarouselViewer.js"></script> 
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
var carouselViewer = new s7viewers.CarouselViewer({ 
 "containerId":"s7viewer", 
"params":{ 
 "asset":"/content/dam/dm-public-facing-live-demo-page/04_shoppable_carousel/05_shoppable_banner", 
 "serverurl":"https://adobedemo62-h.assetsadobe.com/is/image" 
} 
}).init(); 
</script> 
</body> 
</html>
```

La page d’exemples suivante illustre d’autres utilisations réelles de l’incorporation de conception réactive avec une hauteur illimitée :

[https://experienceleague.adobe.com/tools/dynamic-media-demo/viewers-ref/carousel/CarouselViewer-responsive-unrestricted-height.html](https://experienceleague.adobe.com/tools/dynamic-media-demo/viewers-ref/carousel/CarouselViewer-responsive-unrestricted-height.html)

**Taille flexible Incorporation avec largeur et hauteur définies**

Dans un incorporation de taille flexible avec la largeur et la hauteur définies, le style de page Web est différent. Il fournit les deux tailles au `"holder"` DIV et le centre dans la fenêtre du navigateur. En outre, la page Web définit la taille de l’élément `HTML` et `BODY` sur 100 %.

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

Le reste des étapes d’incorporation sont identiques aux étapes utilisées pour l’incorporation réactive avec une hauteur illimitée. L’exemple résultant est le suivant :

```html {.line-numbers}
<!DOCTYPE html> 
<html> 
<head> 
<script type="text/javascript" src="https://demos-pub.assetsadobe.com/etc/dam/viewers/s7viewers/html5/js/CarouselViewer.js"></script> 
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
var carouselViewer = new s7viewers.CarouselViewer({ 
 "containerId":"s7viewer", 
"params":{ 
 "asset":"/content/dam/dm-public-facing-live-demo-page/04_shoppable_carousel/05_shoppable_banner", 
 "serverurl":"https://adobedemo62-h.assetsadobe.com/is/image" 
} 
}).init(); 
</script> 
</body> 
</html>
```

**Incorporation à l’aide de l’API basée sur Setter**

Au lieu d’utiliser l’initialisation basée sur JSON, il est possible d’utiliser l’API basée sur setter et le constructeur no-args. L’utilisation de ce constructeur d’API ne prend aucun paramètre et les paramètres de configuration sont spécifiés à l’aide de `setContainerId()`, `setParam()`et `setAsset()` des méthodes API avec des appels JavaScript distincts.

L’exemple suivant illustre l’utilisation de l’incorporation de taille fixe avec l’API basée sur setter :

```html {.line-numbers}
<!DOCTYPE html> 
<html> 
<head> 
<script type="text/javascript" src="https://demos-pub.assetsadobe.com/etc/dam/viewers/s7viewers/html5/js/CarouselViewer.js"></script> 
<style type="text/css"> 
#s7viewer.s7carouselviewer { 
 width: 1174px; 
 height: 500px; 
} 
</style> 
</head> 
<body> 
<div id="s7viewer" style="position:relative"></div> 
<script type="text/javascript"> 
var carouselViewer = new s7viewers.CarouselViewer(); 
carouselViewer.setContainerId("s7viewer"); 
carouselViewer.setParam("serverurl", "https://adobedemo62-h.assetsadobe.com/is/image"); 
carouselViewer.setAsset("/content/dam/dm-public-facing-live-demo-page/04_shoppable_carousel/05_shoppable_banner"); 
carouselViewer.init(); 
</script> 
</body> 
</html>
```
