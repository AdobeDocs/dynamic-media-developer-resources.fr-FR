---
title: Vidéo interactive
description: La visionneuse de vidéos interactive est un lecteur vidéo qui lit des vidéos en streaming et progressives encodées au format H.264.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Interactive Videos
role: Developer,User
exl-id: e54b0b1f-b015-4592-82e2-99f5080543e3
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '2180'
ht-degree: 0%

---

# Vidéo interactive{#interactive-video}

La visionneuse de vidéos interactive est un lecteur vidéo qui lit des vidéos en streaming et progressives encodées au format H.264.

La visionneuse affiche également des échantillons interactifs de produits en regard du contenu vidéo. Les visionneuses de vidéos uniques et adaptatives sont prises en charge. Il est conçu pour fonctionner sur les navigateurs Web de bureau et mobiles qui prennent en charge la vidéo HTML5. La visionneuse prend en charge les sous-titres facultatifs affichés au-dessus du contenu vidéo, la navigation dans les chapitres vidéo et les outils de partage social. L’objectif de cette visionneuse est de vous aider à mettre en œuvre une expérience de « vidéo achetable ». Autrement dit, les utilisateurs peuvent sélectionner une nuance associée à une région horaire vidéo particulière et être redirigés vers un aperçu rapide ou une page détaillée du produit sur le site Web du client.

Type de visionneuse : 510.

## URL de démonstration {#section-c0ad383db6a444979dc7eeb1ec4cf54d}

[https://experienceleague.adobe.com/tools/dynamic-media-demo/shoppable-video/glacier/InteractiveVideoViewerDemo.html](https://experienceleague.adobe.com/tools/dynamic-media-demo/shoppable-video/glacier/InteractiveVideoViewerDemo.html)

Et

[https://experienceleague.adobe.com/tools/dynamic-media-demo/shoppable-video/AXIS/index.html](https://experienceleague.adobe.com/tools/dynamic-media-demo/shoppable-video/AXIS/index.html)

## Configuration système requise {#section-b7270cc4290043399681dc504f043609}

Voir [Configuration requise](../../c-system-requirements-and-prerequisites.md#concept-9282e5b777de42cdaf72ef7ebd646842).

## Utilisation de la visionneuse de vidéos interactives {#section-e6c68406ecdc4de781df182bbd8088b4}

La visionneuse de vidéos interactives représente un fichier JavaScript principal et un ensemble de fichiers d’assistance téléchargés par la visionneuse au moment de l’exécution. Un seul JavaScript est inclus avec tous les composants SDK de visionneuse utilisés par cette visionneuse, ces ressources et ce code CSS.

La visionneuse de vidéos interactives peut être utilisée en mode pop-up à l’aide d’une page HTML prête pour la production fournie avec les visionneuses Image Serving. Il peut également être utilisé en mode intégré, où il est intégré dans la page Web ciblée à l’aide de l’API documentée.

La configuration et l’habillage sont similaires à ceux des autres visionneuses décrites dans ce guide. Tous les skins sont réalisés au moyen de feuilles de style en cascade personnalisées (CSS).

Voir [Référence de commande commune à tous les visualiseurs - Attributs](../../r-html5-viewer-20-cmdref-configattrib/r-html5-viewer-20-cmdref-configattrib.md#concept-850e0f2c49b949deb7cfbfd330d329bd) de configuration et [Référence de commande communs à tous les visualiseurs - URL](../../c-html5-viewer-20-cmdref-url/c-html5-viewer-20-cmdref-url.md#concept-9b337f349b7b406b8c33c7ee96b3e226)

## Interaction avec la visionneuse de vidéos interactive {#section-642e66ca38cd4032992840ec6c0b0cd2}

La visionneuse de vidéos interactives fournit un ensemble de commandes d’interface utilisateur standard pour la lecture vidéo, telles qu’un bouton Lecture/Pause, un laveur vidéo, une bulle temporelle vidéo, un indicateur de durée de lecture/durée totale, un contrôle du volume, un bouton plein écran et une bascule de sous-titrage. Tous ces contrôles sont regroupés dans une barre de contrôle directement sous la vue principale.

Sur les appareils tactiles, le contrôle du volume est masqué de l’interface utilisateur, car il n’est possible de contrôler le volume qu’à l’aide des boutons matériels de l’appareil.

Lorsque la visionneuse fonctionne en mode pop-up, aucun bouton plein écran n’est disponible dans l’interface utilisateur.

La visionneuse affiche un panneau avec des échantillons interactifs à droite de la zone de visualisation vidéo. La liste des échantillons avance automatiquement au fur et à mesure de la lecture de la vidéo, de sorte que les échantillons correspondant à la région vidéo actuelle sont affichés. Le fait de cliquer ou de taper sur une nuance déclenche une action associée à cette nuance pendant le temps de création. Selon la façon dont vous le configurez, le déclencheur peut rediriger vers une autre page du site Web. Ou, il peut renvoyer des informations sur le produit à la logique de la page Web, ce qui peut déclencher l’ouverture d’un aperçu rapide qui affiche le contenu du produit associé.

Il est possible de naviguer rapidement dans le contenu vidéo lorsque le chapitre vidéo est activé. Les chapitres vidéo sont affichés sous forme de marqueurs dans la piste de défilement vidéo et affichent le titre et la description du chapitre au survol (ou en un seul clic sur les systèmes tactiles). Le client peut « rechercher » un chapitre particulier en cliquant sur un marqueur de chapitre ou en appuyant sur une bulle de description du chapitre.

La visionneuse prend également en charge divers outils de partage sur les réseaux sociaux. Ils sont disponibles sous la forme d’un seul bouton dans l’interface utilisateur qui se développe dans une barre d’outils de partage lorsque l’utilisateur clique ou appuie dessus. La barre d’outils de partage contient une icône pour chaque type de canal de partage pris en charge, tel que Facebook, Twitter, le partage d’e-mails, le partage de code intégré et le partage de lien. Lorsque les outils de partage de courrier électronique, de partage intégré ou de partage de lien sont activés, la visionneuse affiche une boîte de dialogue modale avec un formulaire de saisie de données correspondant. Lorsque Facebook ou Twitter sont appelés, le spectateur redirige l’utilisateur vers une boîte de dialogue de partage standard à partir d’un service de médias sociaux. En outre, lorsqu’un outil de partage est activé, la lecture vidéo est automatiquement interrompue. Les outils de partage ne sont pas disponibles en mode plein écran en raison des restrictions de sécurité du navigateur Web.

La visionneuse est entièrement accessible à l’aide du clavier. Voir [Accessibilité clavier et navigation](../../c-keyboard-accessibility.md#topic-f5650e9493404e55a3627c8d1366b861).

## Intégration d’une visionneuse de vidéos interactive {#section-6bb5d3c502544ad18a58eafe12a13435}

La visionneuse de vidéos interactive est intégrée à la page d’hébergement. Une telle page Web peut avoir une mise en page statique, ou elle peut être « réactive » et s’afficher différemment sur différents appareils ou pour différentes tailles de fenêtre de navigateur.

Pour répondre à ces besoins, la visionneuse prend en charge deux modes de fonctionnement principaux : l’incorporation de taille fixe et l’incorporation réactive.

**A propos du mode d’incorporation de taille fixe et du mode d’incorporation de conception réactive**

En mode intégré, la visionneuse est ajoutée à la page Web existante, qui peut déjà contenir du contenu client non lié à la visionneuse. Le spectateur n’occupe normalement qu’une partie de l’espace d’une page Web.

Les principaux cas d’utilisation sont les pages Web orientées vers les ordinateurs de bureau ou les tablettes, ainsi que les pages réactives qui ajustent automatiquement la mise en page en fonction du type d’appareil.

L’incorporation de taille fixe est utilisée lorsque la visionneuse ne modifie pas sa taille après le chargement initial. Cette fonctionnalité est le meilleur choix pour les pages Web qui ont une disposition statique.

L’incorporation de conception réactive suppose que la visionneuse doit se redimensionner au moment de l’exécution en réponse au changement de taille de son conteneur `DIV`. Le cas d’utilisation le plus courant est l’ajout d’une visionneuse à une page Web qui utilise une mise en page flexible.

En mode d’incorporation de conception réactive, la visionneuse se comporte différemment selon la façon dont la page Web dimensionne son conteneur `DIV`. Si la page Web définit uniquement la largeur du conteneur `DIV`, en laissant sa hauteur illimitée, le visualisateur choisit automatiquement sa hauteur en fonction du format de la ressource utilisée. Cette fonctionnalité garantit que l’actif s’intègre parfaitement dans la vue sans aucun rembourrage sur les côtés. Ce cas d’utilisation est le plus courant pour les pages Web utilisant des cadres de mise en page de conception Web réactive tels que Bootstrap et Foundation.

Sinon, si la page Web définit à la fois la largeur et la hauteur du conteneur `DIV`de la visionneuse, celle-ci remplit uniquement cette zone et suit la taille fournie par la mise en page Web. Un bon exemple est l’intégration de la visionneuse dans une superposition modale, où la superposition est dimensionnée en fonction de la taille de la fenêtre du navigateur Web.

**Incorporation de taille fixe**

Pour ajouter la visionneuse à une page Web, procédez comme suit :

1. Ajout du fichier JavaScript de visionneuse à votre page Web.
1. Définition du conteneur `DIV`.
1. Définition de la taille de la visionneuse.
1. Création et initialisation de la visionneuse.

1. Ajout du fichier JavaScript de visionneuse à votre page Web.

   Pour créer une visionneuse, vous devez ajouter une balise de script dans l’en-tête HTML. Avant de pouvoir utiliser l’API de visionneuse, veillez à inclure [!DNL InterativeVideoViewer.js]le fichier . Le [!DNL InteractiveVideoViewer.js] fichier se trouve dans le [!DNL html5/js/] sous-dossier de votre déploiement IS-Viewers standard :

[!DNL <s7viewers_root>/etc/dam/viewers/s7viewers/html5/js/InteractiveVideoViewer.js]

Vous pouvez utiliser un chemin d’accès relatif si la visionneuse est déployée sur l’un des serveurs Adobe Dynamic Media Classic et qu’elle est diffusée à partir du même domaine. Sinon, vous spécifiez un chemin d’accès complet à l’un des serveurs Adobe Dynamic Media Classic sur lesquels les IS-Viewers sont installés.

Le chemin d’accès relatif ressemble à ce qui suit :

```html {.line-numbers}
<script language="javascript" type="text/javascript" src="/etc/dam/viewers/s7viewers/html5/js/InteractiveVideoViewer.js"></script>
```

>[!NOTE]
>
>Référencez uniquement le fichier JavaScript `include` de visionneuse principal sur votre page. Ne référencez pas de fichiers JavaScript supplémentaires dans le code de la page Web qui pourraient être téléchargés par la logique du visualiseur au moment de l’exécution. En particulier, ne référencez pas directement la bibliothèque SDK `Utils.js` HTML5 chargée par la visionneuse à partir du chemin d’accès `/s7viewers` au contexte (SDK `include`consolidé). La raison en est que l’emplacement des bibliothèques d’exécution ou des bibliothèques de `Utils.js` visionneuse similaires est entièrement géré par la logique de la visionneuse et que l’emplacement change entre les versions de la visionneuse. Adobe ne conserve pas les anciennes versions de la visionneuse `includes` secondaire sur le serveur.
>
>
>Par conséquent, le fait de placer une référence directe à une JavaScript `include` secondaire utilisée par l’utilisateur sur la page interrompt la fonctionnalité de la visionneuse à l’avenir lorsqu’une nouvelle version du produit est déployée.

1. Définition du conteneur `DIV`.

   Ajoutez un élément vide `DIV` à la page dans laquelle vous souhaitez que la visionneuse apparaisse. L’ID `DIV` doit être défini pour l’élément, car cet identifiant est transmis ultérieurement à l’API de visionneuse. La taille de la DIV est spécifiée via CSS.

   L’espace réservé `DIV` est un élément positionné, ce qui signifie que la `position` propriété CSS est définie sur `relative` ou `absolute`.

   Pour que la fonctionnalité plein écran fonctionne correctement dans Internet Explorer, assurez-vous qu’aucun autre élément dans le DOM n’a un ordre d’empilement supérieur à celui de votre espace réservé `DIV`.

   Voici un exemple d’élément d’espace réservé `DIV` défini :

   ```html {.line-numbers}
   <div id="s7viewer" style="position:relative"></div>
   ```

1. Définition de la taille de la visionneuse

   Vous pouvez définir la taille statique de la visionneuse en la déclarant pour `.s7interactivevideoviewer` la classe CSS de niveau supérieur en unités absolues ou en utilisant le `stagesize` modificateur.

   Vous pouvez placer le dimensionnement dans CSS directement sur la page HTML. Vous pouvez également le placer dans un fichier CSS de visionneuse personnalisé, qui est ensuite attribué à un enregistrement de paramètre prédéfini de visionneuse dans Adobe Experience Manager Assets - À la demande, ou transmis explicitement à l’aide `style` de la commande.

   Voir [Personnalisation de la visionneuse](../../c-html5-aem-asset-viewers/c-html5-aem-int-video/c-html5-aem-int-video-customizingviewer/c-html5-aem-int-video-customizingviewer.md#concept-73a8546acdb444a387c49969ceca57d0) de vidéos interactives pour plus d’informations sur le style de la visionneuse avec CSS.

   Voici un exemple de définition d’une taille de visionneuse statique dans la page HTML :

   ```html {.line-numbers}
   #s7viewer.s7interactivevideoviewer { 
    width: 640px; 
    height: 640px; 
   }
   ```

   Vous pouvez définir le `stagesize` modificateur dans l’enregistrement des paramètres prédéfinis de la visionneuse dans Experience Manager Assets - À la demande. Vous pouvez également le transmettre explicitement avec le code d’initialisation de la visionneuse avec `params` collection, ou sous la forme d’un appel d’API comme décrit dans la section Référence des commandes, comme ceci :

   ```html {.line-numbers}
   interactivevideoviewer.setParam("stagesize", "640,640");
   ```

   Une approche basée sur le code CSS est recommandée et est utilisée dans cet exemple.

1. Création et initialisation de la visionneuse.

   Lorsque vous avez terminé les étapes ci-dessus, vous créez une instance de classe, transmettez toutes les informations de configuration à son constructeur et appelez `s7viewers.InteractiveVideoViewer` la méthode sur une instance de `init()` visionneuse. Les informations de configuration sont transmises au constructeur sous la forme d’un objet JSON. Au minimum, cet objet doit avoir `containerId` un champ qui contient le nom de l’ID de conteneur de la visionneuse et de l’objet JSON imbriqué `params` avec les paramètres de configuration pris en charge par la visionneuse.

   Dans ce cas, l’objet `params` doit avoir au moins l’URL Image Serving transmise en tant que propriété et la ressource initiale en tant que `serverUrl` `asset` paramètre. L’API d’initialisation basée sur JSON vous permet de créer et de démarrer la visionneuse avec une seule ligne de code, l’URL du serveur vidéo transmise en tant que propriété, la ressource initiale en tant que `videoserverurl` paramètre et les données interactives en tant que `asset` `interactivedata` propriété. L’API d’initialisation basée sur JSON vous permet de créer et de démarrer la visionneuse avec une seule ligne de code.

   Il est important d’ajouter le conteneur de visionneuse au DOM afin que le code de visionneuse puisse trouver l’élément conteneur par son identifiant. Certains navigateurs retardent la création de DOM jusqu’à la fin de la page Web. Pour une compatibilité maximale, appelez la `init()` méthode juste avant la balise de fermeture `BODY` , ou sur l’événement body `onload()` .

   De même, l’élément conteneur ne fait pas encore nécessairement partie de la mise en page web. Par exemple, il peut être masqué à l’aide `display:none` du style qui lui est attribué. Dans ce cas, la visionneuse retarde son processus d’initialisation jusqu’au moment où la page Web ramène l’élément conteneur à la mise en page. Dans ce cas, le chargement de la visionneuse reprend automatiquement.

   Voici un exemple de création d’une instance de visionneuse, en transmettant les options de configuration minimales nécessaires au constructeur et en appelant la `init()` méthode. L’exemple suppose ce qui suit :

   * L’instance de visionneuse est `interactiveVideoViewer`.
   * Le nom de l’espace réservé `DIV` est `s7viewer`.
   * L’URL du serveur d’images est `https://aodmarketingna.assetsadobe.com/is/image/`.
   * L’URL du serveur vidéo est `https://gateway-na.assetsadobe.com/DMGateway/public/aodmarketingna`.
   * L’URL de contenu est `https://aodmarketingna.assetsadobe.com/`.
   * L’actif est `/content/dam/mac/aodmarketingna/dm-viewers-content/video/Glacier.mp4`.
   * Les données interactives sont `is/content/content/dam/mac/aodmarketingna/_VTT/dm-viewers-content/video/Glacier.mp4.svideo.vtt`.

   ```html {.line-numbers}
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

   Le code suivant est un exemple complet de page Web triviale qui intègre la visionneuse de vidéos interactives avec une taille fixe :

   ```html {.line-numbers}
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

**Intégration de conception réactive avec une hauteur illimitée**

Avec l’intégration de conception réactive, la page Web a normalement une sorte de mise en page flexible en place qui dicte la taille d’exécution du conteneur `DIV`de la visionneuse. Pour l’exemple suivant, supposons que la page Web autorise le conteneur `DIV` de la visionneuse à prendre 40 % de la taille de la fenêtre du navigateur Web, en laissant sa hauteur sans restriction. Le code HTML de la page Web doit ressembler à ce qui suit :

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

L’ajout de la visionneuse à une telle page est similaire aux étapes d’incorporation de taille fixe. La seule différence réside dans le fait que vous n’avez pas besoin de définir explicitement la taille de la visionneuse.

1. Ajout du fichier JavaScript de visionneuse à votre page Web.
1. Définition du conteneur DIV.
1. Création et initialisation de la visionneuse.

Toutes les étapes ci-dessus sont identiques à celles de l’incorporation de taille fixe. Ajoutez la balise DIV conteneur à la balise DIV existante `"holder"` . Le code suivant est un exemple complet. Notez comment la taille de la visionneuse change lorsque le navigateur est redimensionné et comment le rapport d’aspect de la visionneuse correspond à la ressource.

```html {.line-numbers}
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

La page d’exemples suivante illustre d’autres utilisations réelles de l’incorporation de conception réactive avec une hauteur illimitée :

[Démonstrations en direct](https://landing.adobe.com/en/na/dynamic-media/ctir-2755/live-demos.html)

[Autre emplacement de démonstration](https://experienceleague.adobe.com/tools/dynamic-media-demo/vlist/vlist.html)

**Incorporation réactive avec largeur et hauteur définies**

S’il existe un incorporation réactive avec la largeur et la hauteur définies, le style de la page Web est différent. Il fournit les deux tailles au `"holder"` DIV et le centre dans la fenêtre du navigateur. En outre, la page Web définit la taille de l’élément `HTML` et `BODY` sur 100 %.

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

**Incorporation à l’aide de l’API basée sur Setter**

Au lieu d’utiliser l’initialisation basée sur JSON, il est possible d’utiliser l’API basée sur setter et le constructeur no-args. L’utilisation de ce constructeur d’API ne prend aucun paramètre et les paramètres de configuration sont spécifiés à l’aide de `setContainerId()`, `setParam()`et `setAsset()` des méthodes API avec des appels JavaScript distincts.

L’exemple suivant illustre l’utilisation de l’incorporation de taille fixe avec l’API basée sur setter :

```html {.line-numbers}
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
