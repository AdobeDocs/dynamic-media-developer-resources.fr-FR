---
title: Video360
description: La visionneuse de vidéos HTML5360 est un lecteur vidéo 360 degrés qui lit des vidéos 360 en flux continu et progressives codées au format H.264, diffusées depuis Dynamic Media Classic ou Adobe Experience Manager, Dynamic Media.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,360 VR Video
role: Developer,User
exl-id: 74dca3f6-ce89-4c5b-8459-c2c4ca8ed27c
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '2568'
ht-degree: 0%

---

# Video360{#video}

La visionneuse de vidéos HTML5360 est un lecteur vidéo 360 degrés qui lit des vidéos 360 en flux continu et progressives codées au format H.264, diffusées depuis Dynamic Media Classic ou Adobe Experience Manager, Dynamic Media.

Les vidéos 360 degrés, également appelées vidéos immersives ou vidéos sphériques, sont des enregistrements vidéo où une vue dans chaque direction est enregistrée en même temps, filmée à l’aide d’une caméra omnidirectionnelle ou d’une collection de caméras. Les visionneuses de vidéos uniques et adaptatives sont prises en charge. La visionneuse prend également en charge l’utilisation de flux vidéo progressive et HLS hébergés sur un emplacement externe.

Le rapport d’aspect recommandé pour la vidéo 360 est de 2:1. Le son spatial n’est pas pris en charge. La visionneuse est conçue pour fonctionner uniquement avec la vidéo 360 ; une tentative de lecture d’une vidéo non 360 entraîne une lecture vidéo déformée.

La visionneuse est conçue pour fonctionner à la fois sur les navigateurs web mobiles et de bureau qui prennent en charge la vidéo HTML5. La visionneuse prend en charge les outils de partage sur les réseaux sociaux facultatifs.

La visionneuse de vidéos 360 utilise la lecture vidéo en flux continu HTML5 au format HLS dans sa configuration par défaut chaque fois que le système sous-jacent la prend en charge. Sur les systèmes qui ne prennent pas en charge la diffusion HTML5, la visionneuse revient à la diffusion vidéo progressive par HTML5.

Le type de visionneuse est 517.

## URL de démonstration {#section-c0ad383db6a444979dc7eeb1ec4cf54d}

[https://s7d9.scene7.com/s7viewers/html5/Video360Viewer.html?asset=Viewers/space_station_360-AVS](https://s7d9.scene7.com/s7viewers/html5/Video360Viewer.html?asset=Viewers/space_station_360-AVS)

## Configuration système requise {#section-b7270cc4290043399681dc504f043609}

Voir [Configuration requise](../../c-system-requirements-and-prerequisites.md#concept-9282e5b777de42cdaf72ef7ebd646842).

## Utilisation de la visionneuse Video360 {#section-e6c68406ecdc4de781df182bbd8088b4}

La visionneuse de vidéos 360 HTML5 représente un fichier JavaScript principal et un ensemble de fichiers d’assistance (un seul script JavaScript inclus avec tous les composants du SDK de la visionneuse HTML5 utilisés par cette visionneuse, les ressources et le CSS) téléchargés par la visionneuse au moment de l’exécution.

La visionneuse de vidéos 360 HTML5 peut être utilisée à la fois en mode contextuel à l’aide d’une page de HTML prête pour la production fournie avec les visionneuses IS ou en mode intégré, où elle est intégrée à la page web cible à l’aide d’une API documentée.

La configuration et l’habillage sont similaires à ceux des autres visionneuses décrites dans ce guide. L’ensemble de l’habillage est réalisé au moyen de feuilles de style en cascade (CSS) personnalisées.

Voir [Référence de commande commune à toutes les visionneuses - Attributs de configuration](../../r-html5-viewer-20-cmdref-configattrib/r-html5-viewer-20-cmdref-configattrib.md#concept-850e0f2c49b949deb7cfbfd330d329bd) et [Référence de commande commune à toutes les visionneuses - URL](../../c-html5-aem-asset-viewers/c-html5-aem-video360/c-html5-aem-video360-cmdref-url/c-html5-aem-video360-cmdref-url.md#concept-9b337f349b7b406b8c33c7ee96b3e226)

Le contenu vidéo 360 nécessite des paramètres de codage plus élevés que la vidéo standard non 360. En d’autres termes, pour obtenir la même qualité perceptible, le contenu 360 doit présenter une résolution plus élevée que la vidéo non-360. Il est recommandé de tenir compte des paramètres prédéfinis de vidéo adaptative suivants pour la vidéo 360 :

* 720p, 2 500 Kbit/s
* 1 080 p, 5 000 Kbit/s
* 1440p, 6 600 Kbit/s

Notez toutefois que la diffusion de vidéos codées avec des paramètres de haute qualité nécessite une connexion à haut débit sur l’appareil d’un utilisateur final.

## Interaction avec la visionneuse Video360 {#section-642e66ca38cd4032992840ec6c0b0cd2}

La visionneuse vidéo HTML5360 fournit un ensemble de commandes standard de l’interface utilisateur pour la lecture vidéo, telles que le bouton de lecture/pause, la bulle temporelle vidéo de la barre de défilement, l’indicateur de temps de lecture/total, le contrôle du volume et le bouton plein écran. Tous ces contrôles sont regroupés dans une barre de contrôle au bas de l’interface utilisateur de la visionneuse.

Sur les périphériques tactiles, la commande de volume est masquée dans l’interface utilisateur, car il est uniquement possible de contrôler le volume à l’aide des boutons matériels de l’appareil.

Lorsque la visionneuse fonctionne en mode pop-up, un bouton plein écran n’est pas disponible dans l’interface utilisateur.

Le spectateur prend également en charge divers outils de partage sur les médias sociaux. Ils sont disponibles sous la forme d’un bouton unique dans l’interface utilisateur qui se développe dans une barre d’outils de partage lorsque l’utilisateur clique ou appuie dessus. La barre d’outils de partage contient une icône pour chaque type de canal de partage pris en charge, comme Facebook, le Twitter, le partage de courrier électronique, le partage de code incorporé et le partage de lien. Lorsque des outils de partage de courrier électronique, d’intégration de partage ou de lien sont activés, la visionneuse affiche une boîte de dialogue modale avec un formulaire de saisie de données correspondant. Lorsque Facebook ou Twitter est appelé, la visionneuse redirige l’utilisateur vers une boîte de dialogue de partage standard à partir d’un service de médias sociaux. En outre, lorsqu’un outil de partage est activé, la lecture vidéo est automatiquement suspendue. Les outils de partage ne sont pas disponibles en mode plein écran en raison des restrictions de sécurité du navigateur web.

La visionneuse prend en charge la lecture vidéo 360 sur les éléments suivants :

* casques VR (comme Oculus Go et Oculus Rift)
* Montage VR HMD (affichage monté sur la tête) (comme Google Cardboard)
* Périphériques non compatibles avec la réalité virtuelle (navigateurs de bureau, tablettes et téléphones mobiles non connectés à des supports VR HMD, par exemple)

Aucune configuration supplémentaire n’est nécessaire pour afficher le contenu vidéo 360 sur le casque VR. La visionneuse détecte automatiquement la présence d’un casque VR et affiche le bouton &quot;VR&quot; en plus du contenu vidéo. L’activation de ce bouton &quot;VR&quot; bascule le rendu vidéo en mode VR. La visionneuse prend uniquement en charge le rendu VR dans les navigateurs prenant en charge WebVR.

Pour utiliser le HMD VR, la fonction `Video360Player.vrrender` modifier doit être défini sur `1` dans la configuration de la visionneuse, qui force le rendu stéréoscopique.

Sur les casques de réalité virtuelle et les montures HMD VR, le changement de point de vue survient en réponse au mouvement du casque, et aucune autre commande de lecture n’est fournie en mode VR.

Lorsque vous visionnez une vidéo 360 sur des périphériques qui ne sont pas compatibles avec la réalité virtuelle, l’utilisateur final peut utiliser la souris, le toucher ou le clavier pour contrôler la lecture vidéo et le point de vue.

La visionneuse prend en charge les entrées tactiles et de souris sur les appareils Windows dotés d’un écran tactile et d’une souris. Toutefois, cette prise en charge est limitée aux navigateurs web Chrome, Internet Explorer 11 et Edge uniquement.

La visionneuse est entièrement accessible au clavier. Voir [Accessibilité du clavier et navigation](../../c-keyboard-accessibility.md#topic-f5650e9493404e55a3627c8d1366b861).

## Incorporation de la visionneuse Video360 {#section-6bb5d3c502544ad18a58eafe12a13435}

Le comportement de la visionneuse varie en fonction des pages web. Il arrive qu’une page web fournisse un lien qui, lorsqu’il est sélectionné, ouvre la visionneuse dans une fenêtre de navigateur distincte. Dans d’autres cas, il est nécessaire d’incorporer directement la visionneuse sur la page d’hébergement. Dans ce cas, la page web peut avoir une mise en page statique ou utiliser une conception réactive qui s’affiche différemment sur différents appareils ou pour différentes tailles de fenêtre de navigateur. Pour répondre à ces besoins, la visionneuse prend en charge trois modes de fonctionnement principaux : fenêtre contextuelle, incorporation des tailles fixes et incorporation des conceptions réactives.

L’incorporation de plusieurs vidéos sur la même page est prise en charge sur les tablettes et les appareils mobiles. En règle générale, une seule vidéo peut être lue à la fois. Lorsqu’un utilisateur commence la lecture d’une vidéo, puis tente de la lire, la première vidéo est automatiquement suspendue. La vidéo qui a été mise en pause automatique mémorise son temps de lecture actuel, de sorte que l’utilisateur puisse toujours y revenir et reprendre la lecture. La seule exception à cette règle est le navigateur Chrome sur les appareils Android™ 4.x, qui peuvent lire des vidéos en parallèle.

**A propos du mode pop-up**

En mode contextuel, la visionneuse s’ouvre dans une fenêtre ou un onglet de navigateur Web distinct. Il prend toute la zone de la fenêtre du navigateur et s’ajuste au cas où le navigateur serait redimensionné ou où l’orientation du périphérique serait modifiée.

Ce mode est le plus courant pour les appareils mobiles. La page web charge la visionneuse à l’aide de `window.open()` Appel JavaScript, correctement configuré `A` élément de HTML ou toute autre méthode appropriée.

Il est recommandé d’utiliser une page de HTML d’usine pour le mode de fonctionnement de la fenêtre contextuelle. Elle s’appelle [!DNL Video360Viewer.html] et se trouve sous le noeud [!DNL html5/] sous-dossier de votre déploiement IS-Viewers standard :

[!DNL <s7viewers_root>/html5/Video360Viewer.html]

Vous pouvez effectuer une personnalisation visuelle en appliquant une page CSS personnalisée.

Voici un exemple de code de HTML qui ouvre la visionneuse dans une nouvelle fenêtre :

```html {.line-numbers}
<a href="https://s7d9.scene7.com/s7viewers/html5/Video360Viewer.html?asset=Viewers/space_station_360-AVS" target="_blank">Open popup viewer</a>
```

**À propos du mode d’incorporation à taille fixe et du mode d’incorporation de responsive design**

En mode incorporé, la visionneuse est ajoutée à la page web existante, qui peut déjà comporter du contenu client non lié à la visionneuse. Normalement, la visionneuse occupe uniquement une partie de l’espace d’une page web.

Les principaux cas d’utilisation sont les pages web orientées vers les ordinateurs de bureau ou les tablettes, ainsi que les pages réactives qui ajustent automatiquement la mise en page en fonction du type d’appareil.

L’incorporation des tailles fixes est utilisée lorsque la visionneuse ne modifie pas sa taille après le chargement initial. Cette méthode est la meilleure solution pour les pages web avec une disposition statique.

L’incorporation de conceptions réactives suppose que la visionneuse doit être redimensionnée au moment de l’exécution en réponse au changement de taille de son conteneur. `DIV`. Le cas d’utilisation le plus courant consiste à ajouter une visionneuse à une page web qui utilise une mise en page flexible.

En mode d’incorporation de responsive design, la visionneuse se comporte différemment selon la manière dont la page web dimensionne son conteneur. `DIV`. Si la page web définit uniquement la largeur du conteneur `DIV`, sans restriction de hauteur, la visionneuse choisit automatiquement sa hauteur en fonction des proportions de la ressource utilisée. Cette fonctionnalité permet de s’assurer que la ressource s’intègre parfaitement dans la vue sans marge intérieure sur les côtés. Ce cas d’utilisation est le plus courant pour les pages web utilisant des structures de mise en page de conception web réactive comme Bootstrap et Foundation.

Sinon, si la page web définit la largeur et la hauteur du conteneur de la visionneuse. `DIV`, la visionneuse remplit uniquement cette zone et suit la taille fournie par la mise en page web. Un bon exemple consiste à incorporer la visionneuse dans une superposition modale, où la superposition est dimensionnée en fonction de la taille de la fenêtre du navigateur web.

**Incorporation de taille fixe**

Pour ajouter la visionneuse à une page web, procédez comme suit :

1. Ajout du fichier JavaScript de la visionneuse à votre page web.
1. Définir le conteneur `DIV`.
1. Définition de la taille de la visionneuse.
1. Création et initialisation de la visionneuse.

1. Ajout du fichier JavaScript de la visionneuse à votre page web.

   Pour créer une visionneuse, vous devez ajouter une balise de script dans l’en-tête du HTML. Avant d’utiliser l’API de visionneuse, veillez à inclure [!DNL Video360Viewer.js]. La variable [!DNL Video360Viewer.js] se trouve sous le fichier [!DNL html5/js/] sous-dossier de votre déploiement IS-Viewers standard :

[!DNL <s7viewers_root>/etc/dam/viewers/s7viewers/html5/js/Video360Viewer.js]

Vous pouvez utiliser un chemin relatif si la visionneuse est déployée sur l’un des serveurs Adobe Dynamic Media Classic et qu’elle est diffusée à partir du même domaine. Dans le cas contraire, vous spécifiez un chemin d’accès complet à l’un des serveurs Adobe Dynamic Media Classic sur lesquels les visionneuses IS sont installées.

Le chemin relatif ressemble à ce qui suit :

```html {.line-numbers}
<script language="javascript" type="text/javascript" src="/etc/dam/viewers/s7viewers/html5/js/InteractiveVideoViewer.js"></script>
```

>[!NOTE]
>
>Ne référencez que le code JavaScript de la visionneuse principale `include` sur votre page. Ne référencez pas de fichiers JavaScript supplémentaires dans le code de page web qui pourraient être téléchargés par la logique de la visionneuse au moment de l’exécution. En particulier, ne référencez pas directement le SDK HTML5 `Utils.js` bibliothèque chargée par la visionneuse depuis `/s7viewers` chemin d’accès au contexte (appelé SDK consolidé) `include`). La raison en est que l’emplacement de `Utils.js` ou des bibliothèques de visionneuses d’exécution similaires sont entièrement gérées par la logique de la visionneuse et l’emplacement change entre les versions de la visionneuse. Adobe ne conserve pas les anciennes versions de la visionneuse secondaire `includes` sur le serveur.
>
>
>Par conséquent, l’insertion d’une référence directe à tout JavaScript secondaire `include` utilisé par la visionneuse sur la page rompt la fonctionnalité de visionneuse à l’avenir lorsqu’une nouvelle version de produit est déployée.

1. Définir le conteneur `DIV`.

   Ajouter un champ vide `DIV` sur la page dans laquelle vous souhaitez que la visionneuse s’affiche. La variable `DIV` L’ID de l’élément doit être défini, car cet ID est transmis ultérieurement à l’API de visionneuse. La taille du DIV est spécifiée via CSS.

   Espace réservé `DIV` est un élément positionné, ce qui signifie que la variable `position` La propriété CSS est définie sur `relative` ou `absolute`.

   Pour que la fonction plein écran fonctionne correctement dans Internet Explorer, assurez-vous qu’aucun autre élément du DOM n’a un ordre d’empilement supérieur à celui de votre espace réservé. `DIV`.

   Voici un exemple d’espace réservé défini `DIV` element:

   ```html {.line-numbers}
   <div id="s7viewer" style="position:relative;width:640px;height:360px;"></div>
   ```

1. Définition de la taille de la visionneuse

   Vous pouvez définir la taille statique de la visionneuse en la déclarant pour `.s7video360viewer` classe CSS de niveau supérieur en unités absolues ou en utilisant `stagesize` modifier.

   Vous pouvez placer le dimensionnement dans CSS directement sur la page de HTML ou dans un fichier CSS de visionneuse personnalisé, qui est ultérieurement affecté à un enregistrement de paramètre prédéfini de visionneuse dans Adobe Experience Manager Assets - On-demand, ou transféré explicitement à l’aide de `style` .

   Voir [Personnalisation de la visionneuse Video360](../../c-html5-aem-asset-viewers/c-html5-aem-video360/c-html5-aem-video360-customizingviewer/c-html5-aem-video360-customizingviewer.md#concept-73a8546acdb444a387c49969ceca57d0) pour plus d’informations sur le style de la visionneuse avec CSS.

   Voici un exemple de définition d’une taille de visionneuse statique dans la page de HTML :

   ```html {.line-numbers}
   #s7viewer.s7video360viewer { 
    width: 640px; 
    height: 640px; 
   }
   ```

   Vous pouvez définir la variable `stagesize` modification dans l’enregistrement de paramètre prédéfini de visionneuse dans AEM Assets - on-demand. Vous pouvez également le transmettre explicitement avec le code d’initialisation de la visionneuse avec `params` ou sous la forme d’un appel API, comme décrit dans la section Référence de commande, comme suit :

   ```html {.line-numbers}
   video360viewer.setParam("stagesize", "640,640");
   ```

   Une approche basée sur CSS est recommandée et est utilisée dans cet exemple.

1. Création et initialisation de la visionneuse.

   Une fois les étapes ci-dessus terminées, vous créez une instance de `s7viewers.Video360Viewer` , transmettez toutes les informations de configuration à son constructeur, et appelez `init()` sur une instance de visionneuse. Les informations de configuration sont transmises au constructeur sous la forme d’un objet JSON. Au minimum, cet objet doit avoir la valeur `containerId` champ contenant le nom de l’identifiant de conteneur de la visionneuse et imbriqué `params` Objet JSON avec des paramètres de configuration pris en charge par la visionneuse.

   Dans ce cas, la variable `params` doit comporter au moins l’URL du serveur d’images transmise comme `serverUrl` et la ressource initiale en tant que `asset` . L’API d’initialisation basée sur JSON vous permet de créer et de démarrer la visionneuse avec une seule ligne de code, l’URL du serveur vidéo transmise comme `videoserverurl` propriété, ressource initiale en tant que `asset` et données interactives sous la forme `interactivedata` . L’API d’initialisation basée sur JSON vous permet de créer et de démarrer la visionneuse avec une seule ligne de code.

   Il est important que le conteneur de la visionneuse soit ajouté au modèle DOM afin que le code de la visionneuse puisse trouver l’élément de conteneur en fonction de son identifiant. Certains navigateurs retardent la création du DOM jusqu’à la fin de la page web. Pour une compatibilité maximale, appelez la méthode `init()` juste avant la fermeture `BODY` ou sur le corps `onload()` .

   Dans le même temps, l’élément de conteneur ne doit pas nécessairement faire partie de la mise en page web pour l’instant. Par exemple, il peut être masqué à l’aide de `display:none` style qui lui est affecté. Dans ce cas, la visionneuse retarde son processus d’initialisation jusqu’au moment où la page web ramène l’élément de conteneur à la mise en page. Lorsque cela se produit, le chargement de la visionneuse reprend automatiquement.

   Voici un exemple de création d’une instance de visionneuse, de transmission des options de configuration minimales nécessaires au constructeur et d’appel de la fonction `init()` . L’exemple suppose les éléments suivants :

   * L’instance de visionneuse est `video360Viewer`.
   * Nom de l’espace réservé `DIV` is `s7viewer`.
   * L’URL du serveur d’images est `https://s7d9.scene7.com/is/image`.
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

   Le code suivant est un exemple complet d’une page web triviale qui incorpore la visionneuse Video360 avec une taille fixe :

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

**Intégration de conception réactive avec une hauteur libre**

Avec l’incorporation de responsive design, la page web dispose normalement d’une sorte de disposition flexible qui détermine la taille d’exécution du conteneur de la visionneuse. `DIV`. Dans l’exemple suivant, supposons que la page web autorise le conteneur de la visionneuse. `DIV` pour prendre 40 % de la taille de la fenêtre du navigateur web, en ne limitant pas sa hauteur. Le code de HTML de la page web se présente comme suit :

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

L’ajout de la visionneuse à une telle page est similaire aux étapes d’incorporation à taille fixe. La seule différence est que vous n’avez pas besoin de définir explicitement la taille de la visionneuse.

1. Ajout du fichier JavaScript de la visionneuse à votre page web.
1. Définition du conteneur DIV.
1. Création et initialisation de la visionneuse.

Toutes les étapes ci-dessus sont identiques à l’incorporation de tailles fixes. Ajoutez le conteneur DIV au `"holder"` DIV. Le code suivant est un exemple complet. Notez comment la taille de la visionneuse change lorsque le navigateur est redimensionné et comment le rapport d’aspect de la visionneuse correspond à la ressource.

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

**Incorporation réactive avec largeur et hauteur définies**

Si une incorporation réactive est définie avec la largeur et la hauteur, le style de la page web est différent. Elle fournit les deux tailles au `"holder"` DIV et centrez-le dans la fenêtre du navigateur. En outre, la page web définit la taille de la variable `HTML` et `BODY` à 100 %.

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

Les autres étapes d’incorporation sont identiques aux étapes utilisées pour l’incorporation réactive avec une hauteur illimitée. L’exemple qui en résulte est le suivant :

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

**Incorporation à l’aide d’une API basée sur Setter**

Au lieu d’utiliser l’initialisation basée sur JSON, il est possible d’utiliser une API basée sur un setter et un constructeur sans args. L’utilisation de ce constructeur d’API ne prend aucun paramètre et les paramètres de configuration sont spécifiés à l’aide de `setContainerId()`, `setParam()`, et `setAsset()` Méthodes d’API avec des appels JavaScript distincts.

L’exemple suivant illustre l’utilisation de l’incorporation de tailles fixes avec l’API basée sur setter :

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
