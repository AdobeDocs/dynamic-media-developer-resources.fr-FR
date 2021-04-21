---
description: La visionneuse de vidéos HTML5 Video360 est un lecteur vidéo de 360 degrés qui lit la diffusion en flux continu et la vidéo de 360 degrés progressive codée au format H.264, diffusée à partir de Dynamic Media Classic ou de AEM Dynamic Media.
solution: Experience Manager
title: Vidéo360
feature: Dynamic Media Classic,Viewers,SDK/API,360 VR Video
role: Developer,Business Practitioner
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '2593'
ht-degree: 0%

---


# Video360{#video}

La visionneuse de vidéos HTML5 Video360 est un lecteur vidéo de 360 degrés qui lit la diffusion en flux continu et la vidéo de 360 degrés progressive codée au format H.264, diffusée à partir de Dynmaic Media Classic ou d’AEM Dynamic Media.

Les vidéos à 360 degrés, également connues sous le nom de vidéos immersives ou sphériques, sont des enregistrements vidéo où une vue dans toutes les directions est enregistrée en même temps, filmée à l&#39;aide d&#39;une caméra omnidirectionnelle ou d&#39;une collection de caméras. Les visionneuses de vidéos uniques et adaptatives sont prises en charge. Le lecteur prend également en charge l’utilisation de flux vidéo et HLS progressifs hébergés sur un emplacement externe.

Le format recommandé pour la vidéo 360 est de 2:1. Le son spatial n’est pas pris en charge. La visionneuse est conçue pour fonctionner avec une vidéo 360 uniquement ; une tentative de lecture d’une vidéo non-360 entraîne une lecture vidéo déformée.

La visionneuse est conçue pour fonctionner sur les navigateurs Web mobiles et de bureau qui prennent en charge la vidéo HTML5. Le lecteur prend en charge les outils de partage sur les réseaux sociaux en option.

La visionneuse de vidéos 360 utilise la lecture vidéo en flux continu HTML5 au format HLS dans sa configuration par défaut chaque fois que le système sous-jacent la prend en charge. Sur les systèmes qui ne prennent pas en charge la diffusion en flux continu HTML5, la visionneuse revient à la diffusion vidéo progressive HTML5.

Le type de lecteur est 517.

## URL de démonstration {#section-c0ad383db6a444979dc7eeb1ec4cf54d}

[https://s7d9.scene7.com/s7viewers/html5/Video360Viewer.html?asset=Viewers/space_station_360-AVS](https://s7d9.scene7.com/s7viewers/html5/Video360Viewer.html?asset=Viewers/space_station_360-AVS)

## Configuration système requise {#section-b7270cc4290043399681dc504f043609}

Voir [Configuration système requise](../../c-system-requirements-and-prerequisites.md#concept-9282e5b777de42cdaf72ef7ebd646842).

## Utilisation de la visionneuse Video360 {#section-e6c68406ecdc4de781df182bbd8088b4}

La visionneuse de vidéos HTML5 360 représente un fichier JavaScript principal et un ensemble de fichiers d’aide (un seul code JavaScript inclut tous les composants du kit de développement de la visionneuse HTML5 utilisés par cette visionneuse, ressources et CSS) téléchargés par la visionneuse au moment de l’exécution.

La visionneuse de vidéos HTML5 360 peut être utilisée à la fois en mode contextuel à l’aide d’une page HTML prête à l’emploi fournie avec des visionneuses IS ou en mode intégré, où elle est intégrée dans la page Web de cible à l’aide d’une API documentée.

La configuration et l’habillage sont similaires à ceux des autres visionneuses décrites dans ce guide. Tous les habillages sont réalisés au moyen de feuilles de style en cascade (CSS) personnalisées.

Voir [Référence de commande commune à toutes les visionneuses - Attributs de configuration](../../r-html5-viewer-20-cmdref-configattrib/r-html5-viewer-20-cmdref-configattrib.md#concept-850e0f2c49b949deb7cfbfd330d329bd) et [Référence de commande commune à toutes les visionneuses - URL](../../c-html5-aem-asset-viewers/c-html5-aem-video360/c-html5-aem-video360-cmdref-url/c-html5-aem-video360-cmdref-url.md#concept-9b337f349b7b406b8c33c7ee96b3e226)

Le contenu vidéo 360 nécessite des paramètres de codage plus élevés que la vidéo non-360 standard. En d’autres termes, le contenu 360 doit être présenté à une résolution supérieure à la vidéo non-360 pour obtenir la même qualité perceptible. Il est recommandé de tenir compte des paramètres prédéfinis de vidéo adaptative suivants pour la vidéo 360 :

* 720p, 2 500 kbit/s
* 1080p, 5 000 kbit/s
* 1440p, 6 600 kbit/s

Notez toutefois que la diffusion de vidéos codées avec des paramètres de haute qualité nécessite une connexion haut débit sur le périphérique d’un utilisateur final.

## Interaction avec la visionneuse de vidéos 360 {#section-642e66ca38cd4032992840ec6c0b0cd2}

La visionneuse de vidéos HTML5 Video360 fournit un ensemble de commandes standard de l’interface utilisateur pour la lecture vidéo, telles que le bouton Lecture/Pause, la bulle de temps vidéo de la barre de défilement vidéo, l’indicateur de temps de lecture/total, le contrôle du volume et le bouton Plein écran. Tous ces contrôles sont regroupés dans la barre de contrôle située tout en bas de l’interface utilisateur du lecteur de contenu.

Notez que sur les périphériques tactiles, le contrôle de volume est masqué dans l&#39;interface utilisateur, car il est possible de contrôler le volume uniquement à l&#39;aide des boutons matériels du périphérique.

Lorsque le lecteur fonctionne en mode contextuel, aucun bouton plein écran n’est disponible dans l’interface utilisateur.

Le lecteur prend également en charge divers outils de partage sur les réseaux sociaux. Ils sont disponibles sous la forme d’un bouton unique dans l’interface utilisateur qui se développe dans une barre d’outils de partage lorsque l’utilisateur clique ou appuie dessus. La barre d’outils de partage contient une icône pour chaque type de canal de partage pris en charge, tel que Facebook, Twitter, le partage de courrier électronique, le partage de code incorporé et le partage de liens. Lorsque des outils de partage de courrier électronique, de partage incorporé ou de partage de liens sont activés, le lecteur affiche une boîte de dialogue modale avec un formulaire de saisie de données correspondant. Lorsque Facebook ou Twitter sont appelés, le lecteur redirige l’utilisateur vers une boîte de dialogue de partage standard à partir d’un service de médias sociaux. En outre, lorsqu’un outil de partage est activé, la lecture vidéo est automatiquement suspendue. Les outils de partage ne sont pas disponibles en mode plein écran en raison des restrictions de sécurité du navigateur Web.

Le lecteur prend en charge la lecture vidéo 360 sur des écouteurs VR (comme Oculus Go et Oculus Rift), des supports HMD VR (à tête fixe) (comme Google Cardboard) et des périphériques non-VR (comme les navigateurs de bureau, les tablettes et les téléphones mobiles non connectés aux supports VR HMD).

Aucune configuration supplémentaire n&#39;est nécessaire pour le contenu vidéo de la vue 360 sur le casque VR. Le lecteur détecte automatiquement la présence du casque VR et affiche le bouton &quot;VR&quot; au-dessus du contenu vidéo. L’activation de ce bouton &quot;VR&quot; bascule le rendu vidéo en mode VR. Le lecteur prend en charge le rendu VR uniquement dans les navigateurs prenant en charge WebVR.

Pour utiliser VR HMD monte le modificateur `Video360Player.vrrender` doit être défini sur `1` dans la configuration du lecteur, ce qui force le rendu stéréoscopique.

Sur les casques VR et les supports HMD VR se produisent des changements de point de vue en réponse au mouvement du casque, pas d&#39;autre contrôle de lecture n&#39;est fourni en mode VR.

Lorsque vous regardez une vidéo 360 sur des périphériques non compatibles VR, l’utilisateur final peut utiliser la souris, le toucher ou le clavier pour contrôler la lecture vidéo et le point de vue.

Le lecteur prend en charge les entrées tactiles et de souris sur les périphériques Windows dotés d’un écran tactile et d’une souris. Toutefois, cette prise en charge est limitée aux navigateurs Web Chrome, Internet Explorer 11 et Edge.

Le lecteur est entièrement accessible au clavier. Voir [Accessibilité du clavier et navigation](../../c-keyboard-accessibility.md#topic-f5650e9493404e55a3627c8d1366b861).

## Incorporation de la visionneuse vidéo 360 {#section-6bb5d3c502544ad18a58eafe12a13435}

Différentes pages Web ont des besoins différents en ce qui concerne le comportement des visiteurs. Il arrive qu’une page Web fournisse un lien qui, lorsqu’un utilisateur clique dessus, ouvre le lecteur dans une fenêtre de navigateur distincte. Dans d’autres cas, il est nécessaire d’incorporer la visionneuse directement sur la page d’hébergement. Dans ce dernier cas, la page Web peut avoir une mise en page statique ou utiliser une conception adaptée qui s’affiche différemment sur différents périphériques ou pour différentes tailles de fenêtre de navigateur. Pour répondre à ces besoins, le lecteur prend en charge trois modes de fonctionnement Principaux : fenêtre contextuelle, incorporation de taille fixe et incorporation de conception adaptée.

L’incorporation de plusieurs vidéos sur une même page est prise en charge sur les tablettes et les périphériques mobiles. Dans la plupart des cas, une seule vidéo peut être lue à la fois. Lorsqu’un utilisateur début la lecture d’une vidéo, puis tente de la lire, la première vidéo est automatiquement mise en pause. La vidéo en pause automatique mémorise son heure de lecture actuelle, de sorte que l’utilisateur puisse toujours y revenir et reprendre la lecture. La seule exception à cette règle est le navigateur Chrome sur les appareils Android 4.x, qui peuvent lire des vidéos en parallèle.

**A propos du mode contextuel**

En mode contextuel, le lecteur s’ouvre dans une fenêtre ou un onglet distinct du navigateur Web. Il prend toute la zone de la fenêtre du navigateur et s’ajuste au cas où le navigateur serait redimensionné ou où l’orientation du périphérique serait modifiée.

Ce mode est le plus courant pour les périphériques mobiles. La page Web charge la visionneuse à l’aide de l’appel JavaScript `window.open()`, d’un élément HTML `A` correctement configuré ou de toute autre méthode appropriée.

Il est recommandé d’utiliser une page HTML prête à l’emploi pour le mode d’opération contextuel. Il s’appelle [!DNL Video360Viewer.html] et se trouve sous le sous-dossier [!DNL html5/] de votre déploiement des visionneuses IS standard :

[!DNL <s7viewers_root>/html5/Video360Viewer.html]

Vous pouvez réaliser la personnalisation visuelle en appliquant une page CSS personnalisée.

Voici un exemple de code HTML qui ouvre la visionneuse dans une nouvelle fenêtre :

```
<a href="https://s7d9.scene7.com/s7viewers/html5/Video360Viewer.html?asset=Viewers/space_station_360-AVS" target="_blank">Open popup viewer</a>
```

**A propos du mode d&#39;incorporation de taille fixe et du mode d&#39;incorporation de conception réactif**

En mode incorporé, le lecteur est ajouté à la page Web existante, qui peut déjà contenir du contenu client qui n’est pas lié au lecteur. En règle générale, le lecteur occupe uniquement une partie de l’espace d’une page Web.

Les cas d&#39;utilisation Principaux sont les pages Web orientées vers les ordinateurs de bureau ou les tablettes, ainsi que les pages adaptées qui ajustent automatiquement la mise en page en fonction du type de périphérique.

L’incorporation de taille fixe est utilisée lorsque la visionneuse ne change pas de taille après le chargement initial. Il s’agit du meilleur choix pour les pages Web présentant une disposition statique.

L’incorporation de la conception réactive suppose que la visionneuse doit peut-être être redimensionnée au moment de l’exécution en réponse au changement de taille de son conteneur `DIV`. Le cas d’utilisation le plus courant consiste à ajouter une visionneuse à une page Web qui utilise une disposition de page souple.

En mode d’incorporation de conceptions réactives, le lecteur se comporte différemment selon la manière dont la page Web dimensionne son conteneur `DIV`. Si la page Web ne définit que la largeur du conteneur `DIV`, en ne limitant pas sa hauteur, le lecteur sélectionne automatiquement sa hauteur en fonction des proportions du fichier utilisé. Cette fonctionnalité permet de s’assurer que la ressource s’intègre parfaitement à la vue sans remplissage sur les côtés. Ce cas d’utilisation est le plus courant pour les pages Web utilisant des structures de mise en page de conception Web réactives telles que Bootstrap, Foundation, etc.

Sinon, si la page Web définit à la fois la largeur et la hauteur du conteneur `DIV` du lecteur, celui-ci remplit cette zone et suit la taille fournie par la mise en page Web. Un bon exemple est l’incorporation de la visionneuse dans une incrustation modale, où l’incrustation est dimensionnée en fonction de la taille de la fenêtre du navigateur Web.

**Incorporation de taille fixe**

Pour ajouter la visionneuse à une page Web, procédez comme suit :

1. Ajouter le fichier JavaScript de la visionneuse sur votre page Web.
1. Définition du conteneur `DIV`.
1. Définition de la taille de la visionneuse.
1. Création et initialisation de la visionneuse.

1. Ajouter le fichier JavaScript de la visionneuse sur votre page Web.

   Pour créer une visionneuse, vous devez ajouter une balise de script dans l’en-tête HTML. Avant de pouvoir utiliser l’API du lecteur de contenu, veillez à inclure [!DNL Video360Viewer.js]. Le fichier [!DNL Video360Viewer.js] se trouve sous le sous-dossier [!DNL html5/js/] de votre déploiement des visionneuses IS standard :

[!DNL <s7viewers_root>/etc/dam/viewers/s7viewers/html5/js/Video360Viewer.js]

Vous pouvez utiliser un chemin relatif si la visionneuse est déployée sur l’un des serveurs Dynamic Media Classic de l’Adobe et qu’elle est diffusée à partir du même domaine. Sinon, vous spécifiez un chemin d’accès complet à l’un des serveurs Dynamic Media Classic Adobe sur lesquels les visionneuses IS sont installées.

Le chemin relatif ressemble à ce qui suit :

```
<script language="javascript" type="text/javascript" src="/etc/dam/viewers/s7viewers/html5/js/InteractiveVideoViewer.js"></script>
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

   Pour que la fonction plein écran fonctionne correctement dans Internet Explorer, assurez-vous qu’aucun autre élément du modèle DOM ne présente un ordre d’empilement supérieur à celui de votre espace réservé `DIV`.

   Voici un exemple d’élément d’espace réservé défini `DIV` :

   ```
   <div id="s7viewer" style="position:relative;width:640px;height:360px;"></div>
   ```

1. Définition de la taille de la visionneuse

   Vous pouvez définir la taille statique de la visionneuse en la déclarant pour la classe CSS de niveau supérieur `.s7video360viewer` en unités absolues ou en utilisant le modificateur `stagesize`.

   Vous pouvez placer le dimensionnement en CSS directement sur la page HTML ou dans un fichier CSS de visionneuse personnalisée, qui est ensuite affecté à un enregistrement de paramètre prédéfini de visionneuse en AEM Assets - à la demande ou transmis explicitement à l’aide de la commande `style`.

   Voir [Personnalisation de la visionneuse de vidéos 360](../../c-html5-aem-asset-viewers/c-html5-aem-video360/c-html5-aem-video360-customizingviewer/c-html5-aem-video360-customizingviewer.md#concept-73a8546acdb444a387c49969ceca57d0) pour plus d’informations sur la mise en forme de la visionneuse à l’aide de CSS.

   Voici un exemple de définition de la taille d’une visionneuse statique dans la page HTML :

   ```
   #s7viewer.s7video360viewer { 
    width: 640px; 
    height: 640px; 
   }
   ```

   Vous pouvez définir le modificateur `stagesize` dans l’enregistrement de paramètre prédéfini de la visionneuse à AEM Assets - on-demand. Vous pouvez également le transmettre explicitement avec le code d’initialisation de la visionneuse avec la collection `params`, ou en tant qu’appel d’API comme décrit dans la section Référence de commande, comme suit :

   ```
   video360viewer.setParam("stagesize", "640,640");
   ```

   Une approche CSS est recommandée et est utilisée dans cet exemple.

1. Création et initialisation de la visionneuse.

   Une fois les étapes ci-dessus terminées, vous créez une instance de classe `s7viewers.Video360Viewer`, transmettez toutes les informations de configuration à son constructeur et appelez la méthode `init()` sur une instance de lecteur. Les informations de configuration sont transmises au constructeur sous la forme d’un objet JSON. Au minimum, cet objet doit comporter un champ `containerId` contenant le nom de l’identifiant de conteneur de la visionneuse et l’objet JSON `params` imbriqué avec les paramètres de configuration pris en charge par la visionneuse.

   Dans ce cas, l’objet `params` doit avoir au moins la propriété Image Serving URL transmise en tant que propriété `serverUrl` et la ressource initiale en tant que paramètre `asset`. L’API d’initialisation basée sur JSON vous permet de créer et de début la visionneuse avec une seule ligne de code, l’URL du serveur vidéo transmise en tant que propriété `videoserverurl`, la ressource initiale en tant que paramètre `asset` et les données interactives en tant que propriété `interactivedata`. L’API d’initialisation basée sur JSON vous permet de créer et de début le lecteur avec une seule ligne de code.

   Il est important que le conteneur de la visionneuse soit ajouté au modèle DOM afin que le code de la visionneuse puisse trouver l’élément de conteneur en fonction de son identifiant. Certains navigateurs retardent la création du modèle DOM jusqu’à la fin de la page Web. Pour une compatibilité maximale, appelez la méthode `init()` juste avant la balise de fermeture `BODY` ou sur le événement body `onload()`.

   Dans le même temps, l’élément conteneur ne doit pas nécessairement faire partie de la mise en page de la page Web pour le moment. Par exemple, il peut être masqué à l’aide du style `display:none` qui lui est affecté. Dans ce cas, le lecteur retarde son processus d’initialisation jusqu’au moment où la page Web ramène l’élément de conteneur à la mise en page. Dans ce cas, le chargement du lecteur reprend automatiquement.

   Voici un exemple de création d’une instance de visionneuse, de transmission des options de configuration minimales nécessaires au constructeur et d’appel de la méthode `init()`. Cet exemple suppose les éléments suivants :

   * L’instance de lecteur est `video360Viewer`.
   * Le nom de l’espace réservé `DIV` est `s7viewer`.
   * L’URL de diffusion d’images est `https://s7d9.scene7.com/is/image`.
   * L’URL du serveur vidéo est `https://s7d9.scene7.com/is/content`.
   * La ressource est `Viewers/space_station_360-AVS`.

   ```
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

   Le code suivant est un exemple complet d’une page Web triviale qui incorpore la visionneuse de vidéos 360 avec une taille fixe :

   ```
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

**Incorporation de conception réactive avec une hauteur libre**

Avec l’incorporation de conceptions réactives, la page Web dispose normalement d’une sorte de disposition souple qui détermine la taille d’exécution du conteneur `DIV` du lecteur. Pour l’exemple suivant, supposons que la page Web permette au conteneur `DIV` du lecteur de prendre 40 % de la taille de la fenêtre du navigateur Web, en laissant sa hauteur libre. Le code HTML de la page Web se présenterait comme suit :

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
1. Définition de la balise DIV de conteneur.
1. Création et initialisation de la visionneuse.

Toutes les étapes ci-dessus sont identiques à celles de l’incorporation de taille fixe. Ajoutez le conteneur DIV sur le `"holder"` DIV existant. Le code suivant est un exemple complet. Notez comment la taille de la visionneuse change lorsque le navigateur est redimensionné et comment les proportions de la visionneuse correspondent à la ressource.

```
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

**Incorporation réactive avec définition de largeur et de hauteur**

En cas d’incorporation réactive avec définition de la largeur et de la hauteur, le style de la page Web est différent. Il fournit les deux tailles à la balise `"holder"` DIV et le centre dans la fenêtre du navigateur. En outre, la page Web définit la taille des éléments `HTML` et `BODY` sur 100 %.

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

Au lieu d’utiliser l’initialisation basée sur JSON, il est possible d’utiliser une API basée sur un setter et un constructeur sans args. L&#39;utilisation de ce constructeur d&#39;API ne prend aucun paramètre et les paramètres de configuration sont spécifiés à l&#39;aide des méthodes d&#39;API `setContainerId()`, `setParam()` et `setAsset()` avec des appels JavaScript distincts.

L’exemple suivant illustre l’utilisation de l’incorporation de tailles fixes avec l’API basée sur un setter :

```
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

