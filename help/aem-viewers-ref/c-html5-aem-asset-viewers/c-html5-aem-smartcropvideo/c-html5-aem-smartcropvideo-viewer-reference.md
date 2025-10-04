---
title: Visionneuse de vidéos de recadrage intelligent
description: La visionneuse de vidéos avec recadrage intelligent lit la vidéo en flux continu et progressive codée au format H.264 avec prise en charge du recadrage intelligent. Elle est diffusée à partir de Dynamic Media Classic ou Adobe Experience Manager avec Dynamic Media.
keywords: réactif
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Smart Crop,Video
role: Developer,User
exl-id: 937be8a2-307e-47bb-9fc8-d354f780a214
source-git-commit: ce1ac4938c7baf482c6c55a9ad13379153a3ec5b
workflow-type: tm+mt
source-wordcount: '2364'
ht-degree: 0%

---

# Recadrage intelligent de vidéo{#smart-crop-video}

La visionneuse de vidéos avec recadrage intelligent lit la vidéo en flux continu et progressive codée au format H.264 avec prise en charge du recadrage intelligent. Elle est diffusée à partir de Dynamic Media Classic ou d’Experience Manager avec Dynamic Media.

Voir [Configuration requise et conditions préalables](../../c-system-requirements-and-prerequisites.md#concept-9282e5b777de42cdaf72ef7ebd646842).

Les visionneuses de vidéos adaptatives et uniques sont prises en charge. En outre, la visionneuse prend en charge l’utilisation de vidéos progressives et de flux HLS hébergés à des emplacements externes. Il est conçu pour fonctionner sur les navigateurs web de bureau et mobiles qui prennent en charge la vidéo HTML5. Cette visionneuse prend également en charge les sous-titres facultatifs qui s’affichent en haut du contenu vidéo, de la navigation dans les chapitres vidéo et des outils de partage sur les médias sociaux.

La visionneuse de vidéos avec recadrage intelligent utilise la lecture vidéo en flux continu HTML5 au format HLS dans sa configuration par défaut chaque fois que le système sous-jacent la prend en charge. Sur les systèmes qui ne prennent pas en charge la diffusion en continu d’HTML5, la visionneuse revient à la diffusion vidéo progressive d’HTML5.

Type de visionneuse 518.


## URL de démonstration {#section-e1c3106f5b3e445d9b95be337c2f94e2}

[https://s7d9.scene7.com/s7viewers/html5/SmartCropVideoViewer.html?asset=html5automation/frisbee-AVS](https://s7d9.scene7.com/s7viewers/html5/SmartCropVideoViewer.html?asset=html5automation/frisbee-AVS)


## Utilisation de la visionneuse de vidéos avec recadrage intelligent {#section-f21ac23d3f6449ad9765588d69584772}

La visionneuse de vidéos avec recadrage intelligent représente un fichier JavaScript principal et un ensemble de fichiers d’assistance (un seul JavaScript inclus avec tous les composants SDK de la visionneuse utilisés par cette visionneuse spécifique, les ressources et les fichiers CSS téléchargés par la visionneuse au moment de l’exécution).

Vous pouvez utiliser la visionneuse de vidéos avec recadrage intelligent en mode pop-up à l’aide de la page HTML prête pour l’exploitation fournie avec les visionneuses IS. Vous pouvez également utiliser la visionneuse en mode incorporé, où elle est intégrée à une page web cible à l’aide de l’API documentée.

La tâche de configuration et d’application de la peau à la visionneuse est similaire aux autres visionneuses. Toute application de la peau est réalisée au moyen d’un CSS personnalisé.

Voir [&#x200B; Référence des commandes commune à toutes les visionneuses - Attributs de configuration &#x200B;](../../r-html5-viewer-20-cmdref-configattrib/r-html5-viewer-20-cmdref-configattrib.md#concept-850e0f2c49b949deb7cfbfd330d329bd) et [&#x200B; Référence des commandes commune à toutes les visionneuses - URL](../../c-html5-viewer-20-cmdref-url/c-html5-viewer-20-cmdref-url.md#concept-9b337f349b7b406b8c33c7ee96b3e226)

## Interaction avec la visionneuse de vidéos avec recadrage intelligent {#section-ab66eb6955aa4a8aa6d14a3b3acfed3f}

La visionneuse de vidéos avec recadrage intelligent fournit un ensemble de commandes d’interface utilisateur standard pour la lecture vidéo, telles que :

* Bouton Lecture/Pause.
* Bulle de temps vidéo du nettoyeur vidéo.
* Indicateur de temps de lecture/temps total.
* Contrôle du volume.
* bouton plein écran.
* Bouton bascule des sous-titres.

Toutes ces commandes sont regroupées dans une barre de commandes située dans la partie inférieure de l’interface utilisateur de la visionneuse.

Sur les appareils tactiles, le contrôle du volume est masqué dans l’interface utilisateur, car il n’est possible de le contrôler qu’à l’aide des boutons matériels.

Lorsque la visionneuse fonctionne en mode pop-up, le bouton Plein écran n’est pas disponible dans l’interface utilisateur.

Il est possible de parcourir rapidement le contenu d’une vidéo lorsque le chapitre vidéo est activé. Les chapitres vidéo s’affichent en tant que marqueurs dans la piste de nettoyage vidéo et indiquent le titre du chapitre et la description associée lors d’un survol de la souris ou en appuyant une seule fois sur les systèmes tactiles. Les utilisateurs peuvent rechercher un chapitre particulier en sélectionnant un marqueur de chapitre ou en sélectionnant la bulle de description du chapitre.

La visionneuse prend en charge l’entrée tactile et l’entrée souris sur les appareils Windows dotés d’un écran tactile et d’une souris. Cette prise en charge se limite toutefois aux navigateurs web Chrome, Internet Explorer 11 et Edge uniquement.

Cette visionneuse est entièrement accessible à partir du clavier.

Voir [Accessibilité clavier et navigation](../../c-keyboard-accessibility.md#topic-f5650e9493404e55a3627c8d1366b861).

## Outils de partage sur les médias sociaux avec la visionneuse de vidéos avec recadrage intelligent {#section-907d316fe1da4b87abb9775f02464704}

La visionneuse de vidéos avec recadrage intelligent prend en charge les outils de partage sur les médias sociaux. Ils sont disponibles sous la forme d’un seul bouton dans l’interface utilisateur, qui se développe en barre d’outils de partage lorsque l’utilisateur clique ou appuie dessus.

La barre d’outils de partage contient une icône pour chaque type de canal de partage pris en charge, tel que Facebook, Twitter, le partage d’e-mail, le partage de code intégré et le partage de lien. Lorsque les outils de partage d’e-mail, de partage intégré ou de partage de lien sont activés, la visionneuse affiche une boîte de dialogue modale avec un formulaire de saisie de données correspondant. Lorsque Facebook ou Twitter sont appelés, l’utilisateur est redirigé vers une boîte de dialogue de partage standard à partir d’un service de médias sociaux. En outre, lorsqu’un outil de partage est activé, la lecture vidéo est automatiquement suspendue.

Les outils de partage ne sont pas disponibles en mode plein écran en raison de restrictions de sécurité du navigateur web.

## Incorporation de la visionneuse de vidéos de recadrage intelligent {#section-6bb5d3c502544ad18a58eafe12a13435}

Les différentes pages web ont des besoins différents en termes de comportement des observateurs. Parfois, une page web fournit un lien qui, lorsqu’il est sélectionné, ouvre la visionneuse dans une fenêtre de navigateur distincte. Dans d’autres cas, il est nécessaire d’incorporer directement la visionneuse dans la page d’hébergement. Dans ce dernier cas, la page web peut avoir une mise en page statique ou utiliser une conception réactive qui s’affiche différemment sur différents appareils ou pour différentes tailles de fenêtre du navigateur. Pour répondre à ces besoins, la visionneuse prend en charge trois modes de fonctionnement principaux : fenêtre contextuelle, incorporation de taille fixe et incorporation de conception réactive.

L’incorporation de plusieurs vidéos sur la même page est prise en charge sur les tablettes et les appareils mobiles. En règle générale, une seule vidéo peut être lue à la fois. Lorsqu’un utilisateur ou une utilisatrice commence la lecture d’une vidéo, puis tente de lire une autre vidéo, la première vidéo est automatiquement mise en pause. La vidéo qui a été mise en pause automatique se souvient de son heure de lecture actuelle, de sorte que l’utilisateur peut toujours y revenir et reprendre la lecture. La seule exception à cette règle se trouve dans le navigateur Chrome sur les appareils Android™ 4.x, qui peuvent lire des vidéos en parallèle.

**À propos du mode pop-up**

En mode pop-up, la visionneuse s’ouvre dans une fenêtre ou un onglet distinct du navigateur web. Il occupe toute la zone de la fenêtre du navigateur et s’ajuste au cas où le navigateur serait redimensionné ou l’orientation de l’appareil modifiée.

Ce mode est le plus courant pour les appareils mobiles. La page web charge la visionneuse à l’aide de `window.open()`’appel JavaScript, correctement configuré `A` l’élément HTML ou de toute autre méthode appropriée.

Il est recommandé d’utiliser une page HTML prête à l’emploi pour le mode de fonctionnement des fenêtres pop-up. Il s’appelle [!DNL SmartCropVideoViewer.html] et se trouve sous le sous-dossier [!DNL html5/] de votre déploiement d’observateurs IS standard :

[!DNL <s7viewers_root>/html5/SmartCropVideoViewer.html]

Vous pouvez effectuer une personnalisation visuelle en appliquant un CSS personnalisé.

Voici un exemple de code HTML qui permet d’ouvrir la visionneuse dans une nouvelle fenêtre :

```html {.line-numbers}
<a href="http://s7d1.scene7.com/s7viewers/html5/SmartCropVideoViewer.html?asset=html5automation/frisbee-AVS" target="_blank">Open popup viewer</a>
```

**À propos du mode d’incorporation de taille fixe et du mode d’incorporation réactif**

En mode incorporé, la visionneuse est ajoutée à la page web existante, qui peut déjà comporter du contenu client non lié à la visionneuse. L’observateur n’occupe normalement qu’une partie de l’espace de la page web.

Les principaux cas d’utilisation sont des pages web orientées pour les ordinateurs de bureau ou les tablettes, ainsi que des pages en responsive design qui ajustent automatiquement la disposition en fonction du type d’appareil.

L’incorporation de taille fixe est utilisée lorsque la visionneuse ne modifie pas sa taille après le chargement initial. Ce choix est idéal pour les pages web avec une disposition de page statique.

L’incorporation de conception réactive suppose que la visionneuse doit être redimensionnée au moment de l’exécution en réponse au changement de taille de son `DIV` de conteneur. Le cas d’utilisation le plus courant consiste à ajouter la visionneuse à une page web qui utilise une disposition de page flexible.

En mode d’incorporation de responsive design, la visionneuse se comporte différemment selon la manière dont la page web dimensionne son `DIV` de conteneur. Si la page web définit uniquement la largeur du `DIV` de conteneur, sans restriction de hauteur, la visionneuse choisit automatiquement sa hauteur en fonction des proportions de la ressource utilisée. Cette méthode garantit que la ressource s’adapte parfaitement à la vue sans marge intérieure sur les côtés. Ce cas d’utilisation est le plus courant pour les pages web qui utilisent un framework de disposition en responsive design comme Bootstrap ou Foundation.

Dans le cas contraire, si la page web définit à la fois la largeur et la hauteur du `DIV` de conteneur de la visionneuse, celle-ci remplit exactement cette zone et respecte la taille fournie par la disposition de la page web. Un bon exemple consiste à incorporer la visionneuse dans un recouvrement modal, le recouvrement étant dimensionné en fonction de la taille de la fenêtre du navigateur web.

**Incorporation de taille fixe**

Ajoutez la visionneuse à une page web en procédant comme suit :

1. Ajout du fichier JavaScript de la visionneuse à votre page web.
1. La définition du `DIV` de conteneur.
1. Définition de la taille de la visionneuse.
1. Création et initialisation de la visionneuse.

1. Ajout du fichier JavaScript de la visionneuse à votre page web.

   La création d’une visionneuse nécessite l’ajout d’une balise de script dans l’en-tête HTML. Avant de pouvoir utiliser l’API de visionneuse, veillez à inclure [!DNL SmartCropVideoViewer.js]. Le fichier [!DNL SmartCropVideoViewer.js] se trouve sous le sous-dossier [!DNL html5/js/] de votre déploiement d’observateurs IS standard :

[!DNL <s7viewers_root>/html5/js/SmartCropVideoViewer.js]

Vous pouvez utiliser un chemin relatif si la visionneuse est déployée sur l’un des serveurs d’Adobe Dynamic Media Classic et qu’elle est diffusée à partir du même domaine. Sinon, vous spécifiez un chemin d’accès complet à l’un des serveurs Adobe Dynamic Media Classic sur lesquels les visionneuses IS sont installées.

Le chemin relatif ressemble à ce qui suit :

```html {.line-numbers}
<script language="javascript" type="text/javascript" src="/s7viewers/html5/js/SmartCropVideoViewer.js"></script>
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

   Assurez-vous que la fonction Plein écran fonctionne correctement dans Internet Explorer. Vérifiez qu’aucun autre élément du DOM n’a un ordre d’empilement supérieur à celui de votre DIV d’espace réservé.

   Exemple d’élément DIV d’espace réservé défini :

   ```html {.line-numbers}
   <div id="s7viewer" style="position:relative;width:640px;height:360px;"></div> 
   ```

1. Définition de la taille de la visionneuse

   Vous pouvez définir la taille statique de la visionneuse en la déclarant pour `.s7videoviewer` classe CSS de niveau supérieur dans des unités absolues ou à l’aide du `stagesize` de modificateur.

   Vous pouvez définir le dimensionnement dans CSS directement sur la page HTML ou dans un fichier CSS de visionneuse personnalisé. Il est ensuite affecté à un enregistrement de paramètre prédéfini de visionneuse dans Dynamic Media Classic ou transmis explicitement à l’aide d’une commande de style.

   Consultez [Personnalisation de la visionneuse de vidéos avec recadrage intelligent](../../c-html5-s7-aem-asset-viewers/c-html5-video-reference/c-html5-video-viewer-20-customizingviewer/c-html5-video-viewer-20-customizingviewer.md#concept-072a52b10b5f4c0789393dc6e2134c0e) pour plus d’informations sur la mise en forme de la visionneuse à l’aide de CSS.

   Voici un exemple de définition de la taille d’une visionneuse statique dans une page HTML :

   ```html {.line-numbers}
   #s7viewer.s7videoviewer { 
    width: 640px; 
    height: 480px; 
   }
   ```

   Vous pouvez définir `stagesize` modificateur dans l’enregistrement du paramètre prédéfini de la visionneuse dans Dynamic Media Classic ou le transmettre explicitement avec le code d’initialisation de la visionneuse avec la collection de `params`. Ou, comme un appel API, comme décrit dans la section Référence des commandes , comme dans ce qui suit :

   ```html {.line-numbers}
   smartCropVideoViewer.setParam("stagesize", "640,480");
   ```

   Une approche basée sur CSS est recommandée et est utilisée dans cet exemple.

1. Création et initialisation de la visionneuse.

   Une fois les étapes ci-dessus terminées, vous créez une instance de `s7viewers.SmartCropVideoViewer` classe, transmettez toutes les informations de configuration à son constructeur, puis appelez `init()` méthode sur une instance de visionneuse. Les informations de configuration sont transmises au constructeur en tant qu’objet JSON. Au minimum, cet objet doit comporter `containerId` champ qui contient le nom de l’ID de conteneur de visionneuse et de l’objet JSON `params` imbriqué avec les paramètres de configuration pris en charge par la visionneuse. Dans ce cas, `params`’objet doit avoir au moins l’URL du service d’images transmise en tant que propriété `serverUrl`, l’URL du serveur vidéo transmise en tant que propriété `videoserverurl` et la ressource initiale en tant que paramètre `asset`. L’API d’initialisation basée sur JSON vous permet de créer et de démarrer la visionneuse avec une seule ligne de code.

   Il est important d’ajouter le conteneur de visionneuse au DOM afin que le code de la visionneuse puisse trouver l’élément de conteneur à l’aide de son identifiant. Certains navigateurs retardent la création du DOM jusqu’à la fin de la page web. Pour une compatibilité maximale, appelez la méthode `init()` juste avant la balise `BODY` de fermeture ou sur l’événement body `onload()`.

   Dans le même temps, l’élément de conteneur ne doit pas nécessairement encore faire partie de la mise en page web. Par exemple, elle peut être masquée à l’aide `display:none` style qui lui est affecté. Dans ce cas, la visionneuse retarde son processus d’initialisation jusqu’au moment où la page web ramène l’élément de conteneur dans la mise en page. Lorsque cette action se produit, le chargement de la visionneuse reprend automatiquement.

   Voici un exemple de création d’une instance de visionneuse, de transmission des options de configuration minimales nécessaires au constructeur et d’appel de la méthode `init()`. Cet exemple suppose que `smartCropVideoViewer` est l’instance de visionneuse, `s7viewer` est le nom de l’espace réservé `DIV`, [!DNL http://s7d1.scene7.com/is/image/] est l’URL du service d’images, [!DNL http://s7d1.scene7.com/is/content/] est l’URL du serveur vidéo et [!DNL html5automation/frisbee-AVS] est la ressource.

   ```html {.line-numbers}
   <script type="text/javascript"> 
   var smartCropVideoViewer = new s7viewers.SmartCropVideoViewer({ 
    "containerId":"s7viewer", 
   "params":{ 
    "asset":"html5automation/frisbee-AVS", 
    "serverurl":"http://s7d1.scene7.com/is/image/", 
    "videoserverurl":"http://s7d1.scene7.com/is/content/" 
   } 
   }).init(); 
   </script> 
   ```

   Le code suivant est un exemple complet de page web triviale qui intègre la visionneuse de vidéos avec recadrage intelligent avec une taille fixe :

   ```html {.line-numbers}
   <!DOCTYPE html> 
   <html> 
   <head> 
   <script type="text/javascript" src="http://s7d1.scene7.com/s7viewers/html5/js/SmartCropVideoViewer.js"></script> 
   <style type="text/css"> 
   #s7viewer.s7videoviewer { 
    width: 640px; 
    height: 480px; 
   } 
   </style> 
   </head> 
   <body> 
   <div id="s7viewer" style="position:relative;width:640px;height:360px;"></div> 
   <script type="text/javascript"> 
   var smartCropVideoViewer = new s7viewers.SmartCropVideoViewer({ 
    "containerId":"s7viewer", 
   "params":{ 
    "asset":"html5automation/frisbee-AVS", 
    "serverurl":"http://s7d1.scene7.com/is/image/", 
    "videoserverurl":"http://s7d1.scene7.com/is/content/" 
   } 
   }).init(); 
   </script> 
   </body> 
   </html> 
   ```

**Incorporation de conception réactive avec hauteur illimitée**

Avec l’incorporation de responsive design, la page web dispose normalement d’un certain type de disposition flexible en place qui détermine la taille d’exécution du `DIV` de conteneur de la visionneuse. Pour les besoins de cet exemple, supposons que la page web permette au `DIV` de conteneur de la visionneuse de prendre 40 % de la taille de la fenêtre du navigateur web, sans restriction de hauteur. Le code d’HTML de la page web se présente comme suit :

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

L’ajout de la visionneuse à une telle page est similaire à l’incorporation de taille fixe. La seule différence réside dans le fait que vous n’avez pas besoin de définir explicitement la taille de la visionneuse.

1. Ajout du fichier JavaScript de la visionneuse à votre page web.
1. Définition du DIV du conteneur.
1. Création et initialisation de la visionneuse.

Toutes les étapes ci-dessus sont identiques à l’incorporation de taille fixe. Ajoutez des `DIV` de conteneur au `DIV` « holder » existant. Le code suivant en est un exemple complet. Vous pouvez voir comment la taille de la visionneuse change lorsque le navigateur est redimensionné et comment les proportions de la visionneuse correspondent à la ressource.

```html {.line-numbers}
<!DOCTYPE html> 
<html> 
<head> 
<script type="text/javascript" src="http://s7d1.scene7.com/s7viewers/html5/js/SmartCropVideoViewer.js"></script> 
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
var smartCropVideoViewer = new s7viewers.SmartCropVideoViewer({ 
 "containerId":"s7viewer", 
"params":{ 
 "asset":"html5automation/frisbee-AVS", 
 "serverurl":"http://s7d1.scene7.com/is/image/", 
 "videoserverurl":"http://s7d1.scene7.com/is/content/" 
} 
}).init(); 
</script> 
</body> 
</html> 
```

La page d’exemples suivante illustre une utilisation plus concrète de l’incorporation Responsive Design avec une hauteur illimitée :

[Démonstrations en direct](https://landing.adobe.com/en/na/dynamic-media/ctir-2755/live-demos.html)

<!--

[Alternate demo location](https://experienceleague.adobe.com/tools/dynamic-media-demo/vlist/vlist.html?lang=fr)

-->

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

Les étapes d’incorporation restantes sont identiques à l’incorporation de conception réactive avec une hauteur illimitée. L’exemple qui en résulte est le suivant :

```html {.line-numbers}
<!DOCTYPE html> 
<html> 
<head> 
<script type="text/javascript" src="http://s7d1.scene7.com/s7viewers/html5/js/SmartCropVideoViewer.js"></script> 
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
var smartCropVideoViewer = new s7viewers.SmartCropVideoViewer({ 
 "containerId":"s7viewer", 
"params":{ 
 "asset":"html5automation/frisbee-AVS", 
 "serverurl":"http://s7d1.scene7.com/is/image/", 
 "videoserverurl":"http://s7d1.scene7.com/is/content/" 
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
<script type="text/javascript" src="http://s7d1.scene7.com/s7viewers/html5/js/SmartCropVideoViewer.js"></script> 
<style type="text/css"> 
#s7viewer.s7videoviewer { 
 width: 640px; 
 height: 480px; 
} 
</style> 
</head> 
<body> 
<div id="s7viewer" style="position:relative;width:640px;height:360px;"></div> 
<script type="text/javascript"> 
var smartCropVideoViewer = new s7viewers.SmartCropVideoViewer(); 
smartCropVideoViewer.setContainerId("s7viewer"); 
smartCropVideoViewer.setParam("serverurl", "http://s7d1.scene7.com/is/image/"); 
smartCropVideoViewer.setParam("videoserverurl", "http://s7d1.scene7.com/is/content/"); 
smartCropVideoViewer.setAsset("html5automation/frisbee-AVS"); 
smartCropVideoViewer.init(); 
</script> 
</body> 
</html> 
```
