---
description: La visionneuse de vidéos interactive est un lecteur vidéo qui lit la diffusion en flux continu et la vidéo progressive codée au format H.264.
seo-description: La visionneuse de vidéos interactive est un lecteur vidéo qui lit la diffusion en flux continu et la vidéo progressive codée au format H.264.
seo-title: Vidéo interactive
solution: Experience Manager
title: Vidéo interactive
topic: Dynamic media
uuid: 116c6b40-2490-4f1a-9c76-e06082069cc8
translation-type: tm+mt
source-git-commit: 16838d04b005224fad6df215ab5bf8c25ef86fc7

---


# Vidéo interactive{#interactive-video}

La visionneuse de vidéos interactive est un lecteur vidéo qui lit la diffusion en flux continu et la vidéo progressive codée au format H.264.

Le lecteur de contenu affiche également des échantillons de produit interactifs en regard du contenu vidéo. La vidéo unique et les visionneuses de vidéos adaptatives sont prises en charge. Il est conçu pour fonctionner sur les navigateurs Web mobiles et de bureau qui prennent en charge la vidéo HTML5. Le lecteur prend en charge les sous-titres en option affichés au-dessus du contenu vidéo, de la navigation dans les chapitres vidéo et des outils de partage sur les réseaux sociaux. L’objectif de cette visionneuse est de vous aider à mettre en oeuvre une expérience de &quot;vidéo pouvant faire l’objet d’un achat&quot;. En d’autres termes, les utilisateurs peuvent sélectionner une nuance associée à une région de temps vidéo spécifique et être redirigés vers une  rapide ou une page de détails sur un produit sur le site Web du client.

Le type de lecteur est 510.

## URL de démonstration {#section-c0ad383db6a444979dc7eeb1ec4cf54d}

[https://marketing.adobe.com/resources/help/en_US/dm/shoppable-video/glacier/InteractiveVideoViewerDemo.html](https://marketing.adobe.com/resources/help/en_US/dm/shoppable-video/glacier/InteractiveVideoViewerDemo.html)

et

[https://marketing.adobe.com/resources/help/en_US/dm/shoppable-video/AXIS/index.html](https://marketing.adobe.com/resources/help/en_US/dm/shoppable-video/AXIS/index.html)

## Configuration système requise {#section-b7270cc4290043399681dc504f043609}

Voir [Configuration requise](../../c-system-requirements-and-prerequisites.md#concept-9282e5b777de42cdaf72ef7ebd646842).

## Utilisation de la visionneuse de vidéos interactive {#section-e6c68406ecdc4de781df182bbd8088b4}

La visionneuse de vidéos interactive représente un fichier JavaScript principal et un ensemble de fichiers d’aide (un seul code JavaScript inclut tous les composants du SDK de la visionneuse utilisés par cette visionneuse, ressources et CSS en particulier) téléchargés par la visionneuse au moment de l’exécution.

La visionneuse de vidéos interactive peut être utilisée en mode contextuel à l’aide d’une page HTML prête à être produite, fournie avec les visionneuses de diffusion d’images. Il peut également être utilisé en mode intégré, où il est intégré dans la page Web ciblée à l’aide de l’API documentée.

La configuration et l’habillage sont similaires à ceux des autres visionneuses décrites dans ce guide. Tous les habillages sont réalisés au moyen de feuilles de style en cascade (CSS) personnalisées.

Voir Référence [de commande commune à toutes les visionneuses - Attributs](../../r-html5-viewer-20-cmdref-configattrib/r-html5-viewer-20-cmdref-configattrib.md#concept-850e0f2c49b949deb7cfbfd330d329bd) de configuration et référence de [commande commune à toutes les visionneuses - URL](../../c-html5-viewer-20-cmdref-url/c-html5-viewer-20-cmdref-url.md#concept-9b337f349b7b406b8c33c7ee96b3e226)

## Interaction avec la visionneuse de vidéos interactive {#section-642e66ca38cd4032992840ec6c0b0cd2}

La visionneuse de vidéos interactive fournit un ensemble de commandes standard de l’interface utilisateur pour la lecture vidéo, telles qu’un bouton Lecture/Pause, la barre de défilement vidéo, la bulle d’heure de la vidéo, l’indicateur de temps de lecture/total, le contrôle du volume, le bouton Plein écran et la bascule de sous-titrage. Tous ces contrôles sont regroupés dans une barre de contrôle directement sous la  principale.

Notez que sur les périphériques tactiles, le contrôle du volume est masqué dans l&#39;interface utilisateur, car il est possible de contrôler le volume uniquement à l&#39;aide des boutons matériels du périphérique.

Lorsque le lecteur fonctionne en mode contextuel, aucun bouton plein écran n’est disponible dans l’interface utilisateur.

La visionneuse affiche un panneau avec des échantillons interactifs à droite de la zone de visualisation vidéo. Le  des échantillons avance automatiquement au fur et à mesure de la lecture de la vidéo, de sorte que les échantillons correspondant à la région de la vidéo active s’affichent. Un clic ou un appui sur une nuance déclenche une action associée à cette nuance pendant l’heure de création. Selon la manière dont vous l’avez configuré, le déclencheur peut rediriger vers une autre page du site Web ou transmettre les informations sur le produit à la logique de la page Web, ce qui peut à son tour déclencher l’ouverture d’un  rapide qui affiche le contenu du produit associé.

Il est possible de naviguer rapidement dans le contenu vidéo lorsque le chapitre vidéo est activé. Les chapitres vidéo s’affichent sous forme de marqueurs dans la piste de défilement vidéo et affichent le titre et la description du chapitre lors du survol (ou lors d’un appui sur les systèmes tactiles). Le client peut &quot;rechercher&quot; un chapitre particulier en cliquant sur un marqueur de chapitre ou en appuyant sur une bulle de description de chapitre.

Le lecteur prend également en charge divers outils de partage sur les réseaux sociaux. Ils sont disponibles sous la forme d’un bouton unique dans l’interface utilisateur qui s’étend dans une barre d’outils de partage lorsque l’utilisateur clique ou appuie dessus. La barre d’outils de partage contient une icône pour chaque type de de partage pris en charge, comme Facebook, Twitter, le partage de courrier électronique, le partage de code incorporé et le partage de liens. Lorsque des outils de partage de courrier électronique, de partage incorporé ou de partage de liens sont activés, le lecteur affiche une boîte de dialogue modale avec un formulaire de saisie de données correspondant. Lorsque Facebook ou Twitter sont appelés, le lecteur redirige l’utilisateur vers une boîte de dialogue de partage standard à partir d’un service de médias sociaux. En outre, lorsqu’un outil de partage est activé, la lecture vidéo est mise en pause automatiquement. Les outils de partage ne sont pas disponibles en mode plein écran en raison des restrictions de sécurité du navigateur Web.

Le lecteur est entièrement accessible au clavier. Voir Accessibilité [du clavier et navigation](../../c-keyboard-accessibility.md#topic-f5650e9493404e55a3627c8d1366b861).

## Incorporation de la visionneuse de vidéos interactives {#section-6bb5d3c502544ad18a58eafe12a13435}

La visionneuse de vidéos interactive est conçue pour être incorporée à la page d’hébergement. Une telle page Web peut avoir une disposition statique ou être &quot;adaptée&quot; et s’afficher différemment sur différents périphériques ou selon la taille des fenêtres du navigateur.

Pour répondre à ces besoins, le lecteur prend en charge deux modes de fonctionnement principaux : incorporation de taille fixe et incorporation réactive.

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

   Pour créer une visionneuse, vous devez ajouter une balise de script dans l’en-tête HTML. Avant d’utiliser l’API du lecteur de contenu, veillez à inclure [!DNL InterativeVideoViewer.js]. Le [!DNL InteractiveVideoViewer.js] fichier se trouve sous le [!DNL html5/js/] sous-dossier du déploiement des visionneuses IS standard :

[!DNL <s7viewers_root>/etc/dam/viewers/s7viewers/html5/js/InteractiveVideoViewer.js]

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
   <div id="s7viewer" style="position:relative"></div>
   ```

1. Définition de la taille de la visionneuse

   Vous pouvez définir la taille statique de la visionneuse en la déclarant pour la classe CSS de `.s7interactivevideoviewer` niveau supérieur en unités absolues ou en utilisant le modificateur `stagesize` .

   Vous pouvez placer le dimensionnement en CSS directement sur la page HTML ou dans un fichier CSS de lecteur personnalisé, qui est ensuite affecté à un enregistrement de paramètre prédéfini de visionneuse dans AEM Assets - à la demande ou transmis explicitement à l’aide de `style` la commande.

   Voir [Personnalisation de la visionneuse](../../c-html5-aem-asset-viewers/c-html5-aem-int-video/c-html5-aem-int-video-customizingviewer/c-html5-aem-int-video-customizingviewer.md#concept-73a8546acdb444a387c49969ceca57d0) de vidéos interactives pour plus d’informations sur le style de la visionneuse avec CSS.

   Voici un exemple de définition de la taille d’une visionneuse statique dans la page HTML :

   ```
   #s7viewer.s7interactivevideoviewer { 
    width: 640px; 
    height: 640px; 
   }
   ```

   Vous pouvez définir le `stagesize` modificateur dans l’enregistrement des paramètres prédéfinis de la visionneuse dans AEM Assets - on-demand. Vous pouvez également le transmettre explicitement avec le code d’initialisation de la visionneuse avec la `params` collection, ou en tant qu’appel API comme décrit dans la section Référence de commande, comme suit :

   ```
   interactivevideoviewer.setParam("stagesize", "640,640");
   ```

   Une approche CSS est recommandée et utilisée dans cet exemple.

1. Création et initialisation de la visionneuse.

   Une fois les étapes ci-dessus terminées, vous créez une instance de `s7viewers.InteractiveVideoViewer` classe, vous transmettez toutes les informations de configuration à son constructeur, puis vous appelez `init()` la méthode sur une instance de visionneuse. Les informations de configuration sont transmises au constructeur sous forme d’objet JSON. Au minimum, cet objet doit avoir `containerId` un champ contenant le nom de l’ID de  de la visionneuse et l’objet `params` JSON imbriqué avec les paramètres de configuration pris en charge par la visionneuse.

   Dans ce cas, l’ `params` objet doit comporter au moins l’URL de diffusion d’images transmise en tant que `serverUrl` propriété et le fichier initial en tant que `asset` paramètre. L’API d’initialisation basée sur JSON vous permet de créer et de  le lecteur avec une seule ligne de code, l’URL du serveur vidéo transmise en tant que `videoserverurl` propriété, la ressource initiale en tant que `asset` paramètre et les données interactives en tant que `interactivedata` propriété. L’API d’initialisation basée sur JSON vous permet de créer et de  le lecteur avec une seule ligne de code.

   Il est important que le de la visionneuse soit ajouté au modèle DOM afin que le code de la visionneuse puisse trouver l’élément  par son identifiant. Certains navigateurs retardent la création du modèle DOM jusqu’à la fin de la page Web. Pour une compatibilité maximale, appelez la `init()` méthode juste avant la `BODY` balise de fermeture ou sur le  du corps `onload()` .

   De même, l’élément  du ne doit pas nécessairement faire partie de la mise en page de la page Web pour le moment. Par exemple, il peut être masqué à l’aide du `display:none` style qui lui est affecté. Dans ce cas, le lecteur de contenu retarde son processus d’initialisation jusqu’au moment où la page Web ramène l’élément  du à la mise en page. Ce qui se produit, le chargement du lecteur reprend automatiquement.

   Voici un exemple de création d’une instance de visionneuse, de transmission des options de configuration minimales nécessaires au constructeur et d’appel de la `init()` méthode. L’exemple suppose ce qui suit :

   * L’instance de lecteur est `interactiveVideoViewer`.
   * Le nom de l’espace réservé `DIV` est `s7viewer`.
   * L’URL de diffusion d’images est `https://aodmarketingna.assetsadobe.com/is/image/`.
   * L’URL du serveur vidéo est `https://gateway-na.assetsadobe.com/DMGateway/public/aodmarketingna`.
   * L’URL du contenu est `https://aodmarketingna.assetsadobe.com/`.
   * Le fichier est `/content/dam/mac/aodmarketingna/dm-viewers-content/video/Glacier.mp4`.
   * Les données interactives sont `is/content/content/dam/mac/aodmarketingna/_VTT/dm-viewers-content/video/Glacier.mp4.svideo.vtt`.

   ```
   <script type="text/javascript"> 
   var interactiveVideoViewer = new s7viewers.InteractiveVideoViewer({ 
    "containerId":"s7viewer", 
   "params":{ 
    "asset":"/content/dam/mac/aodmarketingna/dm-viewers-content/video/Glacier.mp4", 
   "config":"/etc/dam/presets/viewer/Shoppable_Video_Dark", 
    "serverurl":"https://aodmarketingna.assetsadobe.com/is/image/", 
    "videoserverurl":"https://gateway-na.assetsadobe.com/DMGateway/public/aodmarketingna", 
    "contenturl":"https://aodmarketingna.assetsadobe.com/", 
   "interactivedata":"is/content/content/dam/mac/aodmarketingna/_VTT/dm-viewers-content/video/Glacier.mp4.svideo.vtt" 
   } 
   }).init(); 
   </script>
   ```

   Le code suivant est un exemple complet d’une page Web triviale qui incorpore la visionneuse de vidéos interactives avec une taille fixe :

   ```
   <!DOCTYPE html> 
   <html> 
   <head> 
   <script type="text/javascript" src="https://aodmarketingna.assetsadobe.com/etc/dam/viewers/s7viewers/html5/js/InteractiveVideoViewer.js"></script> 
   <style type="text/css"> 
   #s7viewer.s7interactivevideoviewer { 
    width: 640px; 
    height: 480px; 
   } 
   </style> 
   </head> 
   <body> 
   <div id="s7viewer" style="position:relative;"></div> 
   <script type="text/javascript"> 
   var interactiveVideoViewer = new s7viewers.InteractiveVideoViewer({ 
    "containerId":"s7viewer", 
   "params":{ 
    "asset":"/content/dam/mac/aodmarketingna/dm-viewers-content/video/Glacier.mp4", 
   "config":"/etc/dam/presets/viewer/Shoppable_Video_Dark", 
    "serverurl":"https://aodmarketingna.assetsadobe.com/is/image/", 
    "videoserverurl":"https://gateway-na.assetsadobe.com/DMGateway/public/aodmarketingna", 
    "contenturl":"https://aodmarketingna.assetsadobe.com/", 
   "interactivedata":"is/content/content/dam/mac/aodmarketingna/_VTT/dm-viewers-content/video/Glacier.mp4.svideo.vtt" 
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
<script type="text/javascript" src="https://aodmarketingna.assetsadobe.com/etc/dam/viewers/s7viewers/html5/js/InteractiveVideoViewer.js"></script> 
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
var interactiveVideoViewer = new s7viewers.InteractiveVideoViewer({ 
 "containerId":"s7viewer", 
"params":{ 
 "asset":"/content/dam/mac/aodmarketingna/dm-viewers-content/video/Glacier.mp4", 
"config":"/etc/dam/presets/viewer/Shoppable_Video_Dark", 
 "serverurl":"https://aodmarketingna.assetsadobe.com/is/image/", 
 "videoserverurl":"https://gateway-na.assetsadobe.com/DMGateway/public/aodmarketingna", 
 "contenturl":"https://aodmarketingna.assetsadobe.com/", 
"interactivedata":"is/content/content/dam/mac/aodmarketingna/_VTT/dm-viewers-content/video/Glacier.mp4.svideo.vtt" 
} 
}).init(); 
</script> 
</body> 
</html>
```

La page d’exemples suivante illustre d’autres utilisations réelles de la conception adaptée incorporée à une hauteur illimitée :

[https://marketing.adobe.com/resources/help/en_US/s7/vlist/vlist.html](https://marketing.adobe.com/resources/help/en_US/s7/vlist/vlist.html)

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
<script type="text/javascript" src="https://aodmarketingna.assetsadobe.com/etc/dam/viewers/s7viewers/html5/js/InteractiveVideoViewer.js"></script> 
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
var interactiveVideoViewer = new s7viewers.InteractiveVideoViewer({ 
 "containerId":"s7viewer", 
"params":{ 
 "asset":"/content/dam/mac/aodmarketingna/dm-viewers-content/video/Glacier.mp4", 
"config":"/etc/dam/presets/viewer/Shoppable_Video_Dark", 
 "serverurl":"https://aodmarketingna.assetsadobe.com/is/image/", 
 "videoserverurl":"https://gateway-na.assetsadobe.com/DMGateway/public/aodmarketingna", 
 "contenturl":"https://aodmarketingna.assetsadobe.com/", 
"interactivedata":"is/content/content/dam/mac/aodmarketingna/_VTT/dm-viewers-content/video/Glacier.mp4.svideo.vtt" 
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
<script type="text/javascript" src="https://aodmarketingna.assetsadobe.com/etc/dam/viewers/s7viewers/html5/js/InteractiveVideoViewer.js"></script> 
<style type="text/css"> 
#s7viewer.s7interactivevideoviewer { 
 width: 640px; 
 height: 480px; 
} 
</style> 
</head> 
<body> 
<div id="s7viewer" style="position:relative;width:640px;height:360px;"></div> 
<script type="text/javascript"> 
var interactiveVideoViewer = new s7viewers.InteractiveVideoViewer(); 
interactiveVideoViewer.setContainerId("s7viewer"); 
interactiveVideoViewer.setParam("config", "/etc/dam/presets/viewer/Shoppable_Video_Dark"); 
interactiveVideoViewer.setParam("serverurl", "https://aodmarketingna.assetsadobe.com/is/image/"); 
interactiveVideoViewer.setParam("videoserverurl", "https://gateway-na.assetsadobe.com/DMGateway/public/aodmarketingna"); 
interactiveVideoViewer.setParam("contenturl", "https://aodmarketingna.assetsadobe.com/"); 
interactiveVideoViewer.setParam("interactivedata", "is/content/content/dam/mac/aodmarketingna/_VTT/dm-viewers-content/video/Glacier.mp4.svideo.vtt"); 
interactiveVideoViewer.setAsset("/content/dam/mac/aodmarketingna/dm-viewers-content/video/Glacier.mp4"); 
interactiveVideoViewer.init(); 
</script> 
</body> 
</html>
```

