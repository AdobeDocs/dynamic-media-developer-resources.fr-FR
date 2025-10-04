---
title: Video360
description: La visionneuse HTML5 Video360 est un lecteur vidéo à 360 degrés qui lit de la vidéo en flux continu et en vidéo progressive 360 codée au format H.264, diffusée à partir de Dynamic Media Classic ou de Adobe Experience Manager, Dynamic Media.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,360 VR Video
role: Developer,User
exl-id: 74dca3f6-ce89-4c5b-8459-c2c4ca8ed27c
source-git-commit: ce1ac4938c7baf482c6c55a9ad13379153a3ec5b
workflow-type: tm+mt
source-wordcount: '2561'
ht-degree: 0%

---

# Video360{#video}

La visionneuse HTML5 Video360 est un lecteur vidéo à 360 degrés qui lit de la vidéo en flux continu et en vidéo progressive 360 codée au format H.264, diffusée à partir de Dynamic Media Classic ou de Adobe Experience Manager, Dynamic Media.

Les vidéos à 360 degrés, également appelées vidéos immersives ou vidéos sphériques, sont des enregistrements vidéo où une vue dans toutes les directions est enregistrée en même temps, filmée à l’aide d’une caméra omnidirectionnelle ou d’une collection de caméras. Les visionneuses de vidéos adaptatives et uniques sont prises en charge. La visionneuse prend également en charge l’utilisation de vidéos progressives et de flux HLS hébergés sur un emplacement externe.

Le rapport d’aspect recommandé pour la vidéo 360 est de 2 :1. Le son spatial n’est pas pris en charge. La visionneuse est conçue pour fonctionner uniquement avec une vidéo 360. Toute tentative de lecture d’une vidéo autre que la vidéo 360 entraîne une distorsion de la lecture vidéo.

La visionneuse est conçue pour fonctionner sur les navigateurs web de bureau et mobiles qui prennent en charge la vidéo HTML5. La visionneuse prend en charge les outils facultatifs de partage sur les réseaux sociaux.

La visionneuse Video360 utilise la lecture vidéo en flux continu d’HTML5 au format HLS dans sa configuration par défaut chaque fois que le système sous-jacent le prend en charge. Sur les systèmes qui ne prennent pas en charge la diffusion en continu d’HTML5, la visionneuse revient à la diffusion vidéo progressive d’HTML5.

Le type de visionneuse est 517.

## URL de démonstration {#section-c0ad383db6a444979dc7eeb1ec4cf54d}

[https://s7d9.scene7.com/s7viewers/html5/Video360Viewer.html?asset=Viewers/space_station_360-AVS](https://s7d9.scene7.com/s7viewers/html5/Video360Viewer.html?asset=Viewers/space_station_360-AVS)


## Configuration système requise {#section-b7270cc4290043399681dc504f043609}

Voir [Configuration requise](../../c-system-requirements-and-prerequisites.md#concept-9282e5b777de42cdaf72ef7ebd646842).

## Utilisation de la visionneuse Video360 {#section-e6c68406ecdc4de781df182bbd8088b4}

La visionneuse HTML5 Video360 représente un fichier JavaScript principal et un ensemble de fichiers d’assistance (une seule JavaScript à inclure avec tous les composants HTML5 Viewer SDK utilisés par cette visionneuse, les ressources, CSS) téléchargés par la visionneuse au moment de l’exécution.

La visionneuse HTML5 Video360 peut être utilisée en mode pop-up à l’aide d’une page HTML prête pour l’exploitation fournie avec des visionneuses IS, ou en mode intégré, où elle est intégrée à la page web cible à l’aide d’une API documentée.

La configuration et l’habillage sont similaires à ceux des autres visionneuses décrites dans ce guide. Toute application de la peau est réalisée au moyen de feuilles de style en cascade (CSS) personnalisées.

Voir [&#x200B; Référence des commandes commune à toutes les visionneuses - Attributs de configuration &#x200B;](../../r-html5-viewer-20-cmdref-configattrib/r-html5-viewer-20-cmdref-configattrib.md#concept-850e0f2c49b949deb7cfbfd330d329bd) et [&#x200B; Référence des commandes commune à toutes les visionneuses - URL](../../c-html5-aem-asset-viewers/c-html5-aem-video360/c-html5-aem-video360-cmdref-url/c-html5-aem-video360-cmdref-url.md#concept-9b337f349b7b406b8c33c7ee96b3e226)

Le contenu vidéo 360 nécessite des paramètres de codage plus élevés que la vidéo standard non 360. En d’autres termes, le contenu 360 doit être de résolution supérieure à la vidéo 360 pour obtenir la même qualité perceptible. Il est recommandé de prendre en compte les paramètres prédéfinis de vidéo adaptative suivants pour la vidéo 360 :

* 720p, 2 500 kbit/s
* 1 080 p, 5 000 kbit/s
* 1440p, 6 600 kbit/s

Notez toutefois que la diffusion de vidéos codées avec des paramètres de qualité élevée nécessite une connexion à bande passante élevée sur l’appareil de l’utilisateur final.

## Interaction avec la visionneuse Video360 {#section-642e66ca38cd4032992840ec6c0b0cd2}

La visionneuse HTML5 Video360 fournit un ensemble de commandes d’interface utilisateur standard pour la lecture vidéo, telles que le bouton de lecture/pause, la bulle de temps vidéo du nettoyeur vidéo, l’indicateur de temps de lecture/temps total, le contrôle du volume et le bouton plein écran. Toutes ces commandes sont regroupées dans la barre de commandes au bas de l’interface utilisateur de la visionneuse.

Sur les appareils tactiles, le contrôle du volume est masqué dans l’interface utilisateur, car il n’est possible de contrôler le volume qu’à l’aide des boutons matériels de l’appareil.

Lorsque la visionneuse fonctionne en mode pop-up, un bouton plein écran n’est pas disponible dans l’interface utilisateur.

La visionneuse prend également en charge divers outils de partage sur les médias sociaux. Ils sont disponibles sous la forme d’un seul bouton dans l’interface utilisateur, qui se développe en barre d’outils de partage lorsque l’utilisateur clique ou appuie dessus. La barre d’outils de partage contient une icône pour chaque type de canal de partage pris en charge, tel que Facebook, Twitter, le partage d’e-mail, le partage de code intégré et le partage de lien. Lorsque les outils de partage d’e-mail, de partage intégré ou de partage de lien sont activés, la visionneuse affiche une boîte de dialogue modale avec un formulaire de saisie de données correspondant. Lorsque Facebook ou Twitter sont appelés, l’utilisateur est redirigé vers une boîte de dialogue de partage standard à partir d’un service de médias sociaux. En outre, lorsqu’un outil de partage est activé, la lecture vidéo est automatiquement suspendue. Les outils de partage ne sont pas disponibles en mode plein écran en raison de restrictions de sécurité du navigateur web.

La visionneuse prend en charge la lecture vidéo 360 sur les éléments suivants :

* Casques VR (comme Oculus Go et Oculus Rift)
* VR HMD (affichage monté sur la tête) se monte (comme la carte Google)
* Appareils non-VR (comme les navigateurs de bureau, les tablettes et les téléphones mobiles non connectés aux montures HMD VR)

Aucune configuration supplémentaire n’est nécessaire pour afficher du contenu vidéo 360 sur le casque VR. La visionneuse détecte automatiquement la présence d’un casque VR et affiche le bouton « VR » en plus du contenu vidéo. L’activation de ce bouton « VR » fait passer le rendu vidéo en mode VR. La visionneuse ne prend en charge le rendu VR que dans les navigateurs prenant en charge WebVR.

Pour utiliser les montages HMD VR, le modificateur `Video360Player.vrrender` doit être défini sur `1` dans la configuration de la visionneuse, ce qui force le rendu stéréoscopique.

Sur les casques VR et les supports HMD VR, le changement de point de vue se produit en réponse au mouvement du casque, aucune autre commande de lecture n&#39;est fournie en mode VR.

Lorsque vous regardez une vidéo 360 sur des appareils non compatibles avec la réalité virtuelle, l’utilisateur final peut utiliser la souris, le toucher ou le clavier pour contrôler la lecture vidéo et le point de vue.

La visionneuse prend en charge l’entrée tactile et l’entrée souris sur les appareils Windows à écran tactile et souris. Toutefois, cette prise en charge se limite aux navigateurs web Chrome, Internet Explorer 11 et Edge uniquement.

La visionneuse est entièrement accessible à l’aide du clavier. Voir [Accessibilité clavier et navigation](../../c-keyboard-accessibility.md#topic-f5650e9493404e55a3627c8d1366b861).

## Incorporation de la visionneuse Video360 {#section-6bb5d3c502544ad18a58eafe12a13435}

Les différentes pages web ont des besoins différents en termes de comportement des observateurs. Parfois, une page web fournit un lien qui, lorsqu’il est sélectionné, ouvre la visionneuse dans une fenêtre de navigateur distincte. Dans d’autres cas, il est nécessaire d’incorporer directement la visionneuse dans la page d’hébergement. Dans ce dernier cas, la page web peut avoir une mise en page statique ou utiliser une conception réactive qui s’affiche différemment sur différents appareils ou pour différentes tailles de fenêtre du navigateur. Pour répondre à ces besoins, la visionneuse prend en charge trois modes de fonctionnement principaux : fenêtre contextuelle, incorporation de taille fixe et incorporation de conception réactive.

L’incorporation de plusieurs vidéos sur la même page est prise en charge sur les tablettes et les appareils mobiles. En règle générale, une seule vidéo peut être lue à la fois. Lorsqu’un utilisateur ou une utilisatrice commence la lecture d’une vidéo, puis tente de lire une autre vidéo, la première vidéo est automatiquement mise en pause. La vidéo qui a été mise en pause automatique se souvient de son heure de lecture actuelle, de sorte que l’utilisateur peut toujours y revenir et reprendre la lecture. La seule exception à cette règle se trouve dans le navigateur Chrome sur les appareils Android™ 4.x, qui peuvent lire des vidéos en parallèle.

**À propos du mode pop-up**

En mode pop-up, la visionneuse s’ouvre dans une fenêtre ou un onglet distinct du navigateur web. Il occupe toute la zone de la fenêtre du navigateur et s’ajuste au cas où le navigateur serait redimensionné ou l’orientation de l’appareil modifiée.

Ce mode est le plus courant pour les appareils mobiles. La page web charge la visionneuse à l’aide de `window.open()`’appel JavaScript, correctement configuré `A` l’élément HTML ou de toute autre méthode appropriée.

Il est recommandé d’utiliser une page HTML prête à l’emploi pour le mode de fonctionnement des fenêtres pop-up. Il s’appelle [!DNL Video360Viewer.html] et se trouve sous le sous-dossier [!DNL html5/] de votre déploiement d’observateurs IS standard :

[!DNL <s7viewers_root>/html5/Video360Viewer.html]

Vous pouvez effectuer une personnalisation visuelle en appliquant un CSS personnalisé.

Voici un exemple de code HTML qui permet d’ouvrir la visionneuse dans une nouvelle fenêtre :

```html {.line-numbers}
<a href="https://s7d9.scene7.com/s7viewers/html5/Video360Viewer.html?asset=Viewers/space_station_360-AVS" target="_blank">Open popup viewer</a>
```


**À propos du mode d’incorporation de taille fixe et du mode d’incorporation de conception réactive**

En mode incorporé, la visionneuse est ajoutée à la page web existante, qui peut déjà comporter du contenu client non lié à la visionneuse. L’observateur n’occupe normalement qu’une partie de l’espace d’une page web.

Les principaux cas d’utilisation sont des pages web orientées pour les ordinateurs de bureau ou les tablettes, ainsi que des pages conçues en responsive design qui ajustent automatiquement la disposition en fonction du type d’appareil.

L’incorporation de taille fixe est utilisée lorsque la visionneuse ne modifie pas sa taille après le chargement initial. Cette méthode est recommandée pour les pages web avec une disposition statique.

L’incorporation de conception réactive suppose que la visionneuse doit être redimensionnée au moment de l’exécution en réponse au changement de taille de son `DIV` de conteneur. Le cas d’utilisation le plus courant consiste à ajouter une visionneuse à une page web qui utilise une disposition de page flexible.

En mode d’incorporation de responsive design, la visionneuse se comporte différemment selon la manière dont la page web dimensionne son `DIV` de conteneur. Si la page web définit uniquement la largeur du `DIV` de conteneur, sans restriction de hauteur, la visionneuse choisit automatiquement sa hauteur en fonction des proportions de la ressource utilisée. Cette fonctionnalité garantit que la ressource s’adapte parfaitement à la vue sans marge intérieure sur les côtés. Ce cas d’utilisation est le plus courant pour les pages web utilisant des structures de disposition de conception web réactive telles que Bootstrap et Foundation.

Dans le cas contraire, si la page web définit à la fois la largeur et la hauteur du `DIV` de conteneur de la visionneuse, celle-ci remplit exactement cette zone et suit la taille fournie par la disposition de la page web. Un bon exemple consiste à incorporer la visionneuse dans une superposition modale, où la superposition est dimensionnée en fonction de la taille de la fenêtre du navigateur web.

**Incorporation de taille fixe**

Ajoutez la visionneuse à une page web en procédant comme suit :

1. Ajout du fichier JavaScript de la visionneuse à votre page web.
1. La définition du `DIV` de conteneur.
1. Définition de la taille de la visionneuse.
1. Création et initialisation de la visionneuse.

1. Ajout du fichier JavaScript de la visionneuse à votre page web.

   La création d’une visionneuse nécessite l’ajout d’une balise de script dans l’en-tête HTML. Avant de pouvoir utiliser l’API de visionneuse, veillez à inclure [!DNL Video360Viewer.js]. Le fichier [!DNL Video360Viewer.js] se trouve sous le sous-dossier [!DNL html5/js/] de votre déploiement d’observateurs IS standard :

[!DNL <s7viewers_root>/etc/dam/viewers/s7viewers/html5/js/Video360Viewer.js]

Vous pouvez utiliser un chemin relatif si la visionneuse est déployée sur l’un des serveurs d’Adobe Dynamic Media Classic et qu’elle est diffusée à partir du même domaine. Sinon, vous spécifiez un chemin d’accès complet à l’un des serveurs Adobe Dynamic Media Classic sur lesquels les visionneuses IS sont installées.

Le chemin d’accès relatif ressemble à ce qui suit :

```html {.line-numbers}
<script language="javascript" type="text/javascript" src="/etc/dam/viewers/s7viewers/html5/js/InteractiveVideoViewer.js"></script>
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

   Pour que la fonctionnalité plein écran fonctionne correctement dans Internet Explorer, assurez-vous qu’aucun autre élément du DOM n’a un ordre d’empilement supérieur à celui de votre espace réservé `DIV`.

   Voici un exemple d’élément `DIV` d’espace réservé défini :

   ```html {.line-numbers}
   <div id="s7viewer" style="position:relative;width:640px;height:360px;"></div>
   ```

1. Définition de la taille de la visionneuse

   Vous pouvez définir la taille statique de la visionneuse en la déclarant pour `.s7video360viewer` classe CSS de niveau supérieur dans des unités absolues ou à l’aide du modificateur `stagesize`.

   Vous pouvez définir le dimensionnement dans CSS directement sur la page HTML ou dans un fichier CSS de visionneuse personnalisé, qui est ensuite affecté à un enregistrement de paramètre prédéfini de visionneuse dans Adobe Experience Manager Assets - À la demande, ou transmis explicitement à l’aide de la commande `style`.

   Consultez [Personnalisation de la visionneuse Video360](../../c-html5-aem-asset-viewers/c-html5-aem-video360/c-html5-aem-video360-customizingviewer/c-html5-aem-video360-customizingviewer.md#concept-73a8546acdb444a387c49969ceca57d0) pour plus d’informations sur la mise en forme de la visionneuse avec CSS.

   Voici un exemple de définition d’une taille de visionneuse statique dans la page HTML :

   ```html {.line-numbers}
   #s7viewer.s7video360viewer { 
    width: 640px; 
    height: 640px; 
   }
   ```

   Vous pouvez définir le modificateur `stagesize` dans l’enregistrement du paramètre prédéfini de la visionneuse dans AEM Assets - à la demande. Vous pouvez également le transmettre explicitement avec le code d’initialisation de la visionneuse avec `params` collection ou sous la forme d’un appel API, comme décrit dans la section Référence des commandes , comme suit :

   ```html {.line-numbers}
   video360viewer.setParam("stagesize", "640,640");
   ```

   Une approche basée sur CSS est recommandée et est utilisée dans cet exemple.

1. Création et initialisation de la visionneuse.

   Une fois les étapes ci-dessus terminées, vous créez une instance de `s7viewers.Video360Viewer` classe, transmettez toutes les informations de configuration à son constructeur, puis appelez `init()` méthode sur une instance de visionneuse. Les informations de configuration sont transmises au constructeur en tant qu’objet JSON. Au minimum, cet objet doit comporter `containerId` champ qui contient le nom de l’ID de conteneur de visionneuse et de l’objet JSON `params` imbriqué avec les paramètres de configuration pris en charge par la visionneuse.

   Dans ce cas, l’objet `params` doit comporter au moins l’URL du service d’images transmise en tant que propriété `serverUrl`, et la ressource initiale en tant que paramètre `asset`. L’API d’initialisation basée sur JSON vous permet de créer et de démarrer la visionneuse avec une seule ligne de code, l’URL du serveur vidéo transmise en tant que propriété `videoserverurl`, la ressource initiale en tant que paramètre `asset` et les données interactives en tant que propriété `interactivedata`. L’API d’initialisation basée sur JSON vous permet de créer et de démarrer la visionneuse avec une seule ligne de code.

   Il est important d’ajouter le conteneur de visionneuse au DOM afin que le code de la visionneuse puisse trouver l’élément de conteneur à l’aide de son identifiant. Certains navigateurs retardent la création du DOM jusqu’à la fin de la page web. Pour une compatibilité maximale, appelez la méthode `init()` juste avant la balise `BODY` de fermeture ou sur l’événement body `onload()`.

   Dans le même temps, l’élément de conteneur ne doit pas nécessairement encore faire partie de la mise en page web. Par exemple, elle peut être masquée à l’aide `display:none` style qui lui est affecté. Dans ce cas, la visionneuse retarde son processus d’initialisation jusqu’au moment où la page web ramène l’élément de conteneur dans la mise en page. Lorsque cela se produit, le chargement de la visionneuse reprend automatiquement.


   Voici un exemple de création d’une instance de visionneuse, transmettant les options de configuration minimales nécessaires au constructeur et appelant la méthode `init()`. L’exemple suppose ce qui suit :

   * L’instance de la visionneuse est `video360Viewer`.
   * Le nom de l’espace réservé `DIV` est `s7viewer`.
   * L’URL du service d’images est `https://s7d9.scene7.com/is/image`.
   * L’URL du serveur vidéo est `https://s7d9.scene7.com/is/content`.
   * La ressource est `Viewers/space_station_360-AVS`.


   ```html {.line-numbers}
   <script type="text/javascript"> 
   var video360Viewer = new s7viewers.Video360Viewer({ 
    "containerId":"s7viewer", 
   "params":{ 
    "asset":"Viewers/space_station_360-AVS", 
    "serverurl":"https://s7d9.scene7.com/is/image/", 
    "videoserverurl":"https://s7d9.scene7.com/is/content/" 
   } 
   }).init(); 
   </script>
   ```


   Le code suivant est un exemple complet de page web triviale qui intègre la visionneuse Video360 avec une taille fixe :


   ```html {.line-numbers}
   <!DOCTYPE html> 
   <html> 
   <head> 
   <script type="text/javascript" src="https://s7d9.scene7.com/s7viewers/html5/js/Video360Viewer.js"></script> 
   <style type="text/css"> 
   #s7viewer.s7video360viewer { 
    width: 640px; 
    height: 480px; 
   } 
   </style> 
   </head> 
   <body> 
   <div id="s7viewer" style="position:relative;width:640px;height:360px;"></div> 
   <script type="text/javascript"> 
   var video360Viewer = new s7viewers.Video360Viewer({ 
    "containerId":"s7viewer", 
   "params":{ 
    "asset":"Viewers/space_station_360-AVS", 
    "serverurl":"https://s7d9.scene7.com/is/image/", 
    "videoserverurl":"https://s7d9.scene7.com/is/content/" 
   } 
   }).init(); 
   </script> 
   </body> 
   </html>
   ```


**Incorporation de conception réactive avec hauteur illimitée**

Avec l’incorporation de responsive design, la page web dispose normalement d’un type de disposition flexible qui détermine la taille d’exécution du `DIV` de conteneur de la visionneuse. Dans l’exemple suivant, supposons que la page web permette au `DIV` de conteneur de la visionneuse de prendre 40 % de la taille de la fenêtre du navigateur web, sans restriction de hauteur. Le code d’HTML de la page web se présente comme suit :

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
1. Définition du DIV du conteneur.
1. Création et initialisation de la visionneuse.

Toutes les étapes ci-dessus sont identiques à l’incorporation de taille fixe. Ajoutez le conteneur DIV au DIV `"holder"` existant.

Le code suivant en est un exemple complet. Notez comment la taille de la visionneuse change lorsque le navigateur est redimensionné et comment les proportions de la visionneuse correspondent à la ressource.

```html {.line-numbers}
<!DOCTYPE html> 
<html> 
<head> 
<script type="text/javascript" src="https://s7d9.scene7.com/s7viewers/html5/js/Video360Viewer.js"></script> 
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
var video360Viewer = new s7viewers.Video360Viewer({ 
 "containerId":"s7viewer", 
"params":{ 
 "asset":"Viewers/space_station_360-AVS", 
 "serverurl":"https://s7d9.scene7.com/is/image/", 
 "videoserverurl":"https://s7d9.scene7.com/is/content/" 
} 
}).init(); 
</script> 
</body> 
</html>
```


**Incorporation réactive avec définition de la largeur et de la hauteur**

S’il existe une incorporation réactive avec la largeur et la hauteur définies, le style de la page web est différent. Il fournit les deux tailles au DIV `"holder"` et le centre dans la fenêtre du navigateur. En outre, la page web définit la taille de l’élément `HTML` et `BODY` sur 100 %.


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


Le reste des étapes d&#39;incorporation est identique aux étapes utilisées pour une incorporation réactive avec une hauteur illimitée.

L’exemple qui en résulte est le suivant :

```html {.line-numbers}
<!DOCTYPE html> 
<html> 
<head> 
<script type="text/javascript" src="https://s7d9.scene7.com/s7viewers/html5/js/Video360Viewer.js"></script> 
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
var video360Viewer = new s7viewers.Video360Viewer({ 
 "containerId":"s7viewer", 
"params":{ 
 "asset":"Viewers/space_station_360-AVS", 
 "serverurl":"https://s7d9.scene7.com/is/image/", 
 "videoserverurl":"https://s7d9.scene7.com/is/content/" 
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
<script type="text/javascript" src="https://s7d9.scene7.com/s7viewers/html5/js/Video360Viewer.js"></script> 
<style type="text/css"> 
#s7viewer.s7video360viewer { 
 width: 640px; 
 height: 480px; 
} 
</style> 
</head> 
<body> 
<div id="s7viewer" style="position:relative;width:640px;height:360px;"></div> 
<script type="text/javascript"> 
var video360Viewer = new s7viewers.Video360Viewer(); 
video360Viewer.setContainerId("s7viewer"); 
video360Viewer.setParam("serverurl", "https://s7d9.scene7.com/is/image/"); 
video360Viewer.setParam("videoserverurl", "https://s7d9.scene7.com/is/content/"); 
video360Viewer.setAsset("Viewers/space_station_360-AVS"); 
video360Viewer.init(); 
</script> 
</body> 
</html>
```


