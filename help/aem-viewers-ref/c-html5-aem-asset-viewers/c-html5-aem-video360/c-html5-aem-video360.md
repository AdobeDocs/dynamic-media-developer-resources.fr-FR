---
description: La visionneuse de vidéos HTML5 Video360 est un lecteur vidéo à 360 degrés qui lit la diffusion en flux continu et la vidéo progressive à 360 degrés codée au format H.264, diffusée à partir de Scene7 Publishing System ou d’AEM Dynamic Media.
seo-description: La visionneuse de vidéos HTML5 Video360 est un lecteur vidéo à 360 degrés qui lit la diffusion en flux continu et la vidéo progressive à 360 degrés codée au format H.264, diffusée à partir de Scene7 Publishing System ou d’AEM Dynamic Media.
seo-title: Video360
solution: Experience Manager
title: Video360
topic: Dynamic media
uuid: b03e6289-e012-4c62-835f-814463a27774
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# Video360{#video}

La visionneuse de vidéos HTML5 Video360 est un lecteur vidéo à 360 degrés qui lit la diffusion en flux continu et la vidéo progressive à 360 degrés codée au format H.264, diffusée à partir de Scene7 Publishing System ou d’AEM Dynamic Media.

Les vidéos à 360 degrés, également connues sous le nom de vidéos immersives ou sphériques, sont des enregistrements vidéo où un dans toutes les directions est enregistré en même temps, tourné à l&#39;aide d&#39;une caméra omnidirectionnelle ou d&#39;une collection de caméras. La vidéo unique et les visionneuses de vidéos adaptatives sont prises en charge. Le lecteur prend également en charge l’utilisation de flux vidéo et HLS progressifs hébergés sur un emplacement externe.

Le format recommandé pour la vidéo 360 est de 2:1. Le son spatial n’est pas pris en charge. La visionneuse est conçue pour fonctionner avec la vidéo 360 uniquement ; une tentative de lecture d’une vidéo non-360 entraîne une lecture vidéo déformée.

La visionneuse est conçue pour fonctionner sur les navigateurs Web mobiles et de bureau qui prennent en charge la vidéo HTML5. Le lecteur prend en charge les outils de partage sur les réseaux sociaux en option.

La visionneuse Video360 utilise la lecture vidéo en flux continu HTML5 au format HLS dans sa configuration par défaut chaque fois que le système sous-jacent le prend en charge. Sur les systèmes qui ne prennent pas en charge la diffusion en flux continu HTML5, la visionneuse revient au vidéo progressif HTML5.

Le type de lecteur est 517.

## URL de démonstration {#section-c0ad383db6a444979dc7eeb1ec4cf54d}

[https://s7d9.scene7.com/s7viewers/html5/Video360Viewer.html?asset=Viewers/space_station_360-AVS](https://s7d9.scene7.com/s7viewers/html5/Video360Viewer.html?asset=Viewers/space_station_360-AVS)

## Configuration système requise {#section-b7270cc4290043399681dc504f043609}

Voir [Configuration requise](../../c-system-requirements-and-prerequisites.md#concept-9282e5b777de42cdaf72ef7ebd646842).

## Utilisation de la visionneuse Video360 {#section-e6c68406ecdc4de781df182bbd8088b4}

La visionneuse de vidéos HTML5 360 représente un fichier JavaScript principal et un ensemble de fichiers d’aide (un seul code JavaScript inclut tous les composants du kit de développement de la visionneuse HTML5 utilisés par cette visionneuse, ressources, CSS en particulier) téléchargés par la visionneuse au moment de l’exécution.

La visionneuse de vidéos HTML5 Video360 peut être utilisée à la fois en mode contextuel à l’aide d’une page HTML prête à l’emploi fournie avec des visionneuses IS ou en mode intégré, où elle est intégrée dans une page Web  à l’aide d’une API documentée.

La configuration et l’habillage sont similaires à ceux des autres visionneuses décrites dans ce guide. Tous les habillages sont réalisés au moyen de feuilles de style en cascade (CSS) personnalisées.

Voir Référence [de commande commune à toutes les visionneuses - Attributs](../../r-html5-viewer-20-cmdref-configattrib/r-html5-viewer-20-cmdref-configattrib.md#concept-850e0f2c49b949deb7cfbfd330d329bd) de configuration et référence de [commande commune à toutes les visionneuses - URL](../../c-html5-aem-asset-viewers/c-html5-aem-video360/c-html5-aem-video360-cmdref-url/c-html5-aem-video360-cmdref-url.md#concept-9b337f349b7b406b8c33c7ee96b3e226)

Le contenu vidéo 360 requiert des paramètres de codage plus élevés que la vidéo non 360 standard. En d&#39;autres termes, 360 contenus doivent être de résolution supérieure à la vidéo non-360 pour obtenir la même qualité perceptible. Il est recommandé de prendre en compte les paramètres prédéfinis de vidéo adaptative suivants pour la vidéo 360 :

* 720p, 2 500 kbit/s
* 1080p, 5 000 kbit/s
* 1440p, 6600 kbit/s

Notez toutefois que la diffusion de vidéos codées avec des paramètres de haute qualité nécessite une connexion haut débit sur le périphérique d’un utilisateur final.

## Interaction avec le lecteur vidéo 360 {#section-642e66ca38cd4032992840ec6c0b0cd2}

La visionneuse de vidéos HTML5 Video360 fournit un ensemble de commandes standard de l’interface utilisateur pour la lecture vidéo, telles que le bouton Lecture/Pause, la bulle de temps vidéo de la barre de défilement vidéo, l’indicateur de temps de lecture/temps total, le contrôle du volume et le bouton Plein écran. Tous ces contrôles sont regroupés dans la barre de contrôle au bas de l’interface utilisateur du lecteur de contenu.

Notez que sur les périphériques tactiles, le contrôle du volume est masqué dans l&#39;interface utilisateur, car il est possible de contrôler le volume uniquement à l&#39;aide des boutons matériels du périphérique.

Lorsque le lecteur fonctionne en mode contextuel, aucun bouton plein écran n’est disponible dans l’interface utilisateur.

Le lecteur prend également en charge divers outils de partage sur les réseaux sociaux. Ils sont disponibles sous la forme d’un bouton unique dans l’interface utilisateur qui s’étend dans une barre d’outils de partage lorsque l’utilisateur clique ou appuie dessus. La barre d’outils de partage contient une icône pour chaque type de de partage pris en charge, comme Facebook, Twitter, le partage de courrier électronique, le partage de code incorporé et le partage de liens. Lorsque des outils de partage de courrier électronique, de partage incorporé ou de partage de liens sont activés, le lecteur affiche une boîte de dialogue modale avec un formulaire de saisie de données correspondant. Lorsque Facebook ou Twitter sont appelés, le lecteur redirige l’utilisateur vers une boîte de dialogue de partage standard à partir d’un service de médias sociaux. En outre, lorsqu’un outil de partage est activé, la lecture vidéo est mise en pause automatiquement. Les outils de partage ne sont pas disponibles en mode plein écran en raison des restrictions de sécurité du navigateur Web.

Le lecteur prend en charge la lecture vidéo 360 sur des écouteurs VR (comme Oculus Go et Oculus Rift), des supports HMD (à la tête) VR (comme Google Cardboard) et des périphériques non-VR (comme les navigateurs de bureau, les tablettes et les téléphones mobiles non connectés aux supports RV HMD).

Aucune configuration supplémentaire n’est nécessaire pour de contenu vidéo 360 sur le casque VR. Le lecteur détecte automatiquement la présence du casque VR et affiche le bouton &quot;VR&quot; au-dessus du contenu vidéo. L’activation de ce bouton &quot;VR&quot; bascule le rendu vidéo en mode VR. Le lecteur prend en charge le rendu VR uniquement dans les navigateurs prenant en charge WebVR.

Pour utiliser les supports VR HMD, le `Video360Player.vrrender` modificateur doit être défini sur `1` dans la configuration du lecteur, ce qui force le rendu stéréoscopique.

Sur les écouteurs VR et les supports HMD VR, le point de montage du change en réponse au mouvement du casque, pas d&#39;autre contrôle de lecture n&#39;est fourni en mode VR.

Lorsque vous regardez une vidéo 360 sur des périphériques non compatibles VR, l’utilisateur final peut utiliser la souris, le toucher ou le clavier pour contrôler la lecture vidéo et le point d’ du.

Le lecteur prend en charge la saisie tactile et la saisie de la souris sur les périphériques Windows dotés d’un écran tactile et d’une souris ; toutefois, cette prise en charge est limitée aux navigateurs Web Chrome, Internet Explorer 11 et Edge uniquement.

Le lecteur est entièrement accessible au clavier. Voir Accessibilité [du clavier et navigation](../../c-keyboard-accessibility.md#topic-f5650e9493404e55a3627c8d1366b861).

## Incorporation de la visionneuse vidéo 360 {#section-6bb5d3c502544ad18a58eafe12a13435}

Le comportement des visiteurs varie selon les pages Web. Il arrive qu’une page Web fournisse un lien qui, lorsqu’un utilisateur clique dessus, ouvre le lecteur dans une fenêtre de navigateur distincte. Dans d’autres cas, il est nécessaire d’incorporer le lecteur directement sur la page d’hébergement. Dans ce dernier cas, la page Web peut avoir une mise en page statique, ou utiliser une conception adaptée qui s’affiche différemment sur différents périphériques ou pour différentes tailles de fenêtre de navigateur. Pour répondre à ces besoins, le lecteur prend en charge trois modes de fonctionnement principaux : fenêtre contextuelle, incorporation de taille fixe et incorporation de conception adaptée.

L’incorporation de plusieurs vidéos sur une même page est prise en charge sur les tablettes et les périphériques mobiles. Dans la plupart des cas, une seule vidéo peut être lue à la fois. Lorsqu’un utilisateur  une vidéo, puis tente de la lire, la première vidéo est automatiquement mise en pause. La vidéo en pause automatique mémorise son temps de lecture actuel, de sorte que l’utilisateur puisse toujours y revenir et reprendre la lecture. La seule exception à cette règle est le navigateur Chrome sur les appareils Android 4.x, qui peuvent lire des vidéos en parallèle.

**A propos du mode contextuel**

En mode contextuel, le lecteur s’ouvre dans une fenêtre ou un onglet distinct du navigateur Web. Il prend toute la zone de la fenêtre du navigateur et s’ajuste au cas où le navigateur serait redimensionné ou où l’orientation du périphérique serait modifiée.

Ce mode est le plus courant pour les périphériques mobiles. La page Web charge le lecteur à l’aide d’un appel `window.open()` JavaScript, d’un élément `A` HTML correctement configuré ou de toute autre méthode appropriée.

Il est recommandé d’utiliser une page HTML prête à l’emploi pour le mode d’opération contextuel. Elle est appelée [!DNL Video360Viewer.html] et se trouve sous le [!DNL html5/] sous-dossier du déploiement des visionneuses IS standard :

[!DNL <s7viewers_root>/html5/Video360Viewer.html]

Vous pouvez réaliser la personnalisation visuelle en appliquant une page CSS personnalisée.

Voici un exemple de code HTML qui ouvre la visionneuse dans une nouvelle fenêtre :

```
<a href="https://s7d9.scene7.com/s7viewers/html5/Video360Viewer.html?asset=Viewers/space_station_360-AVS" target="_blank">Open popup viewer</a>
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
1. Définition du  de `DIV`.
1. Définition de la taille de la visionneuse.
1. Création et initialisation de la visionneuse.

1. Ajout du fichier JavaScript de la visionneuse à votre page Web.

   Pour créer une visionneuse, vous devez ajouter une balise de script dans l’en-tête HTML. Avant d’utiliser l’API du lecteur de contenu, veillez à inclure [!DNL Video360Viewer.js]. Le [!DNL Video360Viewer.js] fichier se trouve sous le [!DNL html5/js/] sous-dossier du déploiement des visionneuses IS standard :

[!DNL <s7viewers_root>/etc/dam/viewers/s7viewers/html5/js/Video360Viewer.js]

Vous pouvez utiliser un chemin relatif si le lecteur est déployé sur l’un des serveurs Adobe Dynamic Media Classic et qu’il est diffusé à partir du même domaine. Dans le cas contraire, vous spécifiez un chemin d’accès complet à l’un des serveurs Adobe Dynamic Media Classic sur lesquels les visionneuses IS sont installées.

Le chemin relatif ressemble à ce qui suit :

```
<script language="javascript" type="text/javascript" src="/etc/dam/viewers/s7viewers/html5/js/InteractiveVideoViewer.js"></script>
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

   Pour que la fonction plein écran fonctionne correctement dans Internet Explorer, assurez-vous qu’aucun autre élément du modèle DOM ne présente un ordre d’empilement supérieur à celui de votre espace réservé `DIV`.

   Voici un exemple d’élément d’espace réservé défini `DIV` :

   ```
   <div id="s7viewer" style="position:relative;width:640px;height:360px;"></div>
   ```

1. Définition de la taille de la visionneuse

   Vous pouvez définir la taille statique de la visionneuse en la déclarant pour la classe CSS de `.s7video360viewer` niveau supérieur en unités absolues ou en utilisant le modificateur `stagesize` .

   Vous pouvez placer le dimensionnement en CSS directement sur la page HTML ou dans un fichier CSS de lecteur personnalisé, qui est ensuite affecté à un enregistrement de paramètre prédéfini de visionneuse dans AEM Assets - à la demande ou transmis explicitement à l’aide de `style` la commande.

   Voir [Personnalisation de la visionneuse](../../c-html5-aem-asset-viewers/c-html5-aem-video360/c-html5-aem-video360-customizingviewer/c-html5-aem-video360-customizingviewer.md#concept-73a8546acdb444a387c49969ceca57d0) vidéo360 pour plus d’informations sur le style de la visionneuse avec CSS.

   Voici un exemple de définition de la taille d’une visionneuse statique dans la page HTML :

   ```
   #s7viewer.s7video360viewer { 
    width: 640px; 
    height: 640px; 
   }
   ```

   Vous pouvez définir le `stagesize` modificateur dans l’enregistrement des paramètres prédéfinis de la visionneuse dans AEM Assets - on-demand. Vous pouvez également le transmettre explicitement avec le code d’initialisation de la visionneuse avec la `params` collection, ou en tant qu’appel API comme décrit dans la section Référence de commande, comme suit :

   ```
   video360viewer.setParam("stagesize", "640,640");
   ```

   Une approche CSS est recommandée et utilisée dans cet exemple.

1. Création et initialisation de la visionneuse.

   Une fois les étapes ci-dessus terminées, vous créez une instance de `s7viewers.Video360Viewer` classe, vous transmettez toutes les informations de configuration à son constructeur, puis vous appelez `init()` la méthode sur une instance de visionneuse. Les informations de configuration sont transmises au constructeur sous forme d’objet JSON. Au minimum, cet objet doit avoir `containerId` un champ contenant le nom de l’ID de  de la visionneuse et l’objet `params` JSON imbriqué avec les paramètres de configuration pris en charge par la visionneuse.

   Dans ce cas, l’ `params` objet doit comporter au moins l’URL de diffusion d’images transmise en tant que `serverUrl` propriété et le fichier initial en tant que `asset` paramètre. L’API d’initialisation basée sur JSON vous permet de créer et de  le lecteur avec une seule ligne de code, l’URL du serveur vidéo transmise en tant que `videoserverurl` propriété, la ressource initiale en tant que `asset` paramètre et les données interactives en tant que `interactivedata` propriété. L’API d’initialisation basée sur JSON vous permet de créer et de  le lecteur avec une seule ligne de code.

   Il est important que le de la visionneuse soit ajouté au modèle DOM afin que le code de la visionneuse puisse trouver l’élément  par son identifiant. Certains navigateurs retardent la création du modèle DOM jusqu’à la fin de la page Web. Pour une compatibilité maximale, appelez la `init()` méthode juste avant la `BODY` balise de fermeture ou sur le  du corps `onload()` .

   De même, l’élément  du ne doit pas nécessairement faire partie de la mise en page de la page Web pour le moment. Par exemple, il peut être masqué à l’aide du `display:none` style qui lui est affecté. Dans ce cas, le lecteur de contenu retarde son processus d’initialisation jusqu’au moment où la page Web ramène l’élément  du à la mise en page. Dans ce cas, le chargement du lecteur reprend automatiquement.

   Voici un exemple de création d’une instance de visionneuse, de transmission des options de configuration minimales nécessaires au constructeur et d’appel de la `init()` méthode. L’exemple suppose ce qui suit :

   * L’instance de lecteur est `video360Viewer`.
   * Le nom de l’espace réservé `DIV` est `s7viewer`.
   * L’URL de diffusion d’images est `https://s7d9.scene7.com/is/image`.
   * L’URL du serveur vidéo est `https://s7d9.scene7.com/is/content`.
   * Le fichier est `Viewers/space_station_360-AVS`.

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

En cas d’incorporation réactive avec définition de la largeur et de la hauteur, le style de la page Web est différent. Il fournit les deux tailles à la `"holder"` balise DIV et le centre dans la fenêtre du navigateur. En outre, la page Web définit la taille de l’ `HTML` `BODY` élément et de l’élément sur 100 %.

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

Au lieu d’utiliser l’initialisation basée sur JSON, il est possible d’utiliser une API basée sur un setter et un constructeur sans args. L’utilisation de ce constructeur d’API ne prend aucun paramètre et les paramètres de configuration sont spécifiés à l’aide `setContainerId()`, `setParam()`et `setAsset()` des méthodes API avec des appels JavaScript distincts.

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

