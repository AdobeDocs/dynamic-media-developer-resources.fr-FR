---
title: Vidéo interactive
description: La visionneuse de vidéos interactive est un lecteur vidéo qui lit la diffusion en continu et la vidéo progressive codée au format H.264.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Interactive Videos
role: Developer,User
exl-id: e54b0b1f-b015-4592-82e2-99f5080543e3
source-git-commit: b89ca96947f751b750623e1f18d2a5d86f0cd759
workflow-type: tm+mt
source-wordcount: '2211'
ht-degree: 0%

---

# Vidéo interactive{#interactive-video}

La visionneuse de vidéos interactive est un lecteur vidéo qui lit la diffusion en continu et la vidéo progressive codée au format H.264.

La visionneuse affiche également des échantillons de produits interactifs en regard du contenu vidéo. Les visionneuses de vidéos uniques et adaptatives sont prises en charge. Il est conçu pour fonctionner à la fois sur les navigateurs de bureau et les navigateurs Web mobiles qui prennent en charge la vidéo HTML5. La visionneuse prend en charge les sous-titres fermés facultatifs affichés au-dessus du contenu vidéo, de la navigation dans les chapitres vidéo et des outils de partage sur les réseaux sociaux. L’objectif de cette visionneuse est de vous aider à mettre en oeuvre une expérience &quot;vidéo Shoppable&quot;. En d’autres termes, les utilisateurs peuvent sélectionner un échantillon associé à une région de temps vidéo spécifique et être redirigés vers un aperçu rapide ou une page des détails du produit sur le site web du client.

Le type de visionneuse est 510.

## URL de démonstration {#section-c0ad383db6a444979dc7eeb1ec4cf54d}

[https://experienceleague.adobe.com/tools/dynamic-media-demo/shoppable-video/glacier/InteractiveVideoViewerDemo.html](https://experienceleague.adobe.com/tools/dynamic-media-demo/shoppable-video/glacier/InteractiveVideoViewerDemo.html)

Et

[https://experienceleague.adobe.com/tools/dynamic-media-demo/shoppable-video/AXIS/index.html](https://experienceleague.adobe.com/tools/dynamic-media-demo/shoppable-video/AXIS/index.html)

## Configuration système requise {#section-b7270cc4290043399681dc504f043609}

Voir [Configuration requise](../../c-system-requirements-and-prerequisites.md#concept-9282e5b777de42cdaf72ef7ebd646842).

## Utilisation de la visionneuse de vidéo interactive {#section-e6c68406ecdc4de781df182bbd8088b4}

La visionneuse de vidéos interactive représente un fichier JavaScript principal et un ensemble de fichiers d’assistance téléchargés par la visionneuse au moment de l’exécution. Un seul code JavaScript est inclus avec tous les composants du SDK de la visionneuse utilisés par cette visionneuse, ces ressources et cette page CSS particulière.

La visionneuse de vidéo interactive peut être utilisée en mode pop-up à l’aide de la page de HTML prête pour la production fournie avec les visionneuses de diffusion d’images. Il peut également être utilisé en mode incorporé, où il est intégré à la page web ciblée à l’aide de l’API documentée.

La configuration et l’habillage sont similaires à ceux des autres visionneuses décrites dans ce guide. L’ensemble de l’habillage est réalisé au moyen de feuilles de style en cascade (CSS) personnalisées.

Voir [Référence de commande commune à toutes les visionneuses - Attributs de configuration](../../r-html5-viewer-20-cmdref-configattrib/r-html5-viewer-20-cmdref-configattrib.md#concept-850e0f2c49b949deb7cfbfd330d329bd) et [Référence de commande commune à toutes les visionneuses - URL](../../c-html5-viewer-20-cmdref-url/c-html5-viewer-20-cmdref-url.md#concept-9b337f349b7b406b8c33c7ee96b3e226)

## Interaction avec la visionneuse de vidéo interactive {#section-642e66ca38cd4032992840ec6c0b0cd2}

La visionneuse de vidéos interactive fournit un ensemble de commandes standard de l’interface utilisateur pour la lecture vidéo, telles qu’un bouton Lecture/Pause, la barre de défilement vidéo, la bulle de temps vidéo, l’indicateur de temps de lecture/durée totale, le contrôle du volume, le bouton Plein écran et le bouton de sous-titrage fermé. Tous ces contrôles sont regroupés dans une barre de contrôle directement sous la vue principale.

Sur les périphériques tactiles, la commande de volume est masquée dans l’interface utilisateur, car il est uniquement possible de contrôler le volume à l’aide des boutons matériels de l’appareil.

Lorsque la visionneuse fonctionne en mode pop-up, un bouton plein écran n’est pas disponible dans l’interface utilisateur.

La visionneuse affiche un panneau avec des échantillons interactifs à droite de la zone d’affichage vidéo. La liste des échantillons avance automatiquement au fur et à mesure de la lecture de la vidéo, de sorte que les échantillons correspondant à la zone de la vidéo active s’affichent. Cliquer ou appuyer sur un échantillon déclenche une action associée à cet échantillon pendant l’heure de création. Selon la configuration utilisée, le déclencheur peut rediriger vers une autre page du site web. Il peut également renvoyer les informations sur les produits à la logique de la page web, ce qui peut à son tour déclencher l’ouverture d’un aperçu rapide qui affiche le contenu des produits associés.

Il est possible de parcourir rapidement le contenu vidéo lorsque le chapitre vidéo est activé. Les chapitres vidéo s’affichent sous la forme de marqueurs dans le suivi de la barre de défilement vidéo et affichent le titre et la description du chapitre au survol (ou en appuyant une seule fois sur les systèmes tactiles). Le client peut &quot;rechercher&quot; un chapitre spécifique en cliquant sur un marqueur de chapitre ou en appuyant sur une bulle de description de chapitre.

Le spectateur prend également en charge divers outils de partage sur les médias sociaux. Ils sont disponibles sous la forme d’un bouton unique dans l’interface utilisateur qui se développe dans une barre d’outils de partage lorsque l’utilisateur clique ou appuie dessus. La barre d’outils de partage contient une icône pour chaque type de canal de partage pris en charge, tel que Facebook, Twitter, partage de courrier électronique, partage de code intégré et partage de lien. Lorsque des outils de partage de courrier électronique, d’intégration de partage ou de lien sont activés, la visionneuse affiche une boîte de dialogue modale avec un formulaire de saisie de données correspondant. Lors de l’appel de Facebook ou Twitter, la visionneuse redirige l’utilisateur vers une boîte de dialogue de partage standard à partir d’un service de médias sociaux. En outre, lorsqu’un outil de partage est activé, la lecture vidéo est automatiquement suspendue. Les outils de partage ne sont pas disponibles en mode plein écran en raison des restrictions de sécurité du navigateur web.

La visionneuse est entièrement accessible au clavier. Voir [Accessibilité du clavier et navigation](../../c-keyboard-accessibility.md#topic-f5650e9493404e55a3627c8d1366b861).

## Incorporation de la visionneuse de vidéos interactives {#section-6bb5d3c502544ad18a58eafe12a13435}

La visionneuse de vidéo interactive est incorporée dans la page d’hébergement. Une telle page web peut avoir une mise en page statique ou être &quot;réactive&quot; et s’afficher différemment sur différents appareils ou pour différentes tailles de fenêtre de navigateur.

Pour répondre à ces besoins, la visionneuse prend en charge deux modes de fonctionnement Principaux : incorporation de taille fixe et incorporation réactive.

**À propos du mode d’incorporation à taille fixe et du mode d’incorporation de responsive design**

En mode incorporé, la visionneuse est ajoutée à la page web existante, qui peut déjà comporter du contenu client non lié à la visionneuse. Normalement, la visionneuse occupe uniquement une partie de l’espace d’une page web.

Les cas d’utilisation Principaux sont les pages web orientées vers les ordinateurs de bureau ou les tablettes, ainsi que les pages réactives qui ajustent automatiquement la mise en page en fonction du type d’appareil.

L’incorporation des tailles fixes est utilisée lorsque la visionneuse ne modifie pas sa taille après le chargement initial. Cette fonctionnalité est la meilleure solution pour les pages web avec une disposition statique.

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

   Pour créer une visionneuse, vous devez ajouter une balise de script dans l’en-tête du HTML. Avant d’utiliser l’API de visionneuse, veillez à inclure [!DNL InterativeVideoViewer.js]. Le [!DNL InteractiveVideoViewer.js] se trouve sous le fichier [!DNL html5/js/] sous-dossier de votre déploiement IS-Viewers standard :

[!DNL <s7viewers_root>/etc/dam/viewers/s7viewers/html5/js/InteractiveVideoViewer.js]

Vous pouvez utiliser un chemin relatif si la visionneuse est déployée sur l’un des serveurs Adobe Dynamic Media Classic et qu’elle est diffusée à partir du même domaine. Dans le cas contraire, vous spécifiez un chemin d’accès complet à l’un des serveurs Adobe Dynamic Media Classic sur lesquels les visionneuses IS sont installées.

Le chemin relatif ressemble à ce qui suit :

```html {.line-numbers}
<script language="javascript" type="text/javascript" src="/etc/dam/viewers/s7viewers/html5/js/InteractiveVideoViewer.js"></script>
```

>[!NOTE]
>
>Ne référencez que le code JavaScript de la visionneuse principale `include` sur votre page. Ne référencez pas de fichiers JavaScript supplémentaires dans le code de page web qui pourraient être téléchargés par la logique de la visionneuse au moment de l’exécution. En particulier, ne référencez pas directement le SDK HTML5. `Utils.js` bibliothèque chargée par la visionneuse depuis `/s7viewers` chemin d’accès au contexte (appelé SDK consolidé) `include`). La raison en est que l’emplacement de la variable `Utils.js` ou des bibliothèques de visionneuses d’exécution similaires sont entièrement gérées par la logique de la visionneuse et l’emplacement change entre les versions de la visionneuse. Adobe ne conserve pas les anciennes versions de la visionneuse secondaire `includes` sur le serveur.
>
>
>Par conséquent, l’insertion d’une référence directe à tout JavaScript secondaire `include` utilisé par la visionneuse sur la page rompt la fonctionnalité de visionneuse à l’avenir lorsqu’une nouvelle version de produit est déployée.

1. Définir le conteneur `DIV`.

   Ajouter un champ vide `DIV` sur la page dans laquelle vous souhaitez que la visionneuse s’affiche. Le `DIV` L’ID de l’élément doit être défini, car cet ID est transmis ultérieurement à l’API de visionneuse. La taille du DIV est spécifiée via CSS.

   Espace réservé `DIV` est un élément positionné, ce qui signifie que la variable `position` La propriété CSS est définie sur `relative` ou `absolute`.

   Pour que la fonction plein écran fonctionne correctement dans Internet Explorer, assurez-vous qu’aucun autre élément du DOM n’a un ordre d’empilement supérieur à celui de votre espace réservé. `DIV`.

   Voici un exemple d’espace réservé défini `DIV` element:

   ```html {.line-numbers}
   <div id="s7viewer" style="position:relative"></div>
   ```

1. Définition de la taille de la visionneuse

   Vous pouvez définir la taille statique de la visionneuse en la déclarant pour `.s7interactivevideoviewer` classe CSS de niveau supérieur en unités absolues ou en utilisant `stagesize` modifier.

   Vous pouvez placer le dimensionnement dans CSS directement sur la page de HTML. Vous pouvez également le placer dans un fichier CSS de visionneuse personnalisé, qui est ensuite affecté à un enregistrement de paramètre prédéfini de visionneuse dans Adobe Experience Manager Assets - On-demand ou transmis explicitement à l’aide de `style` .

   Voir [Personnalisation de la visionneuse de vidéo interactive](../../c-html5-aem-asset-viewers/c-html5-aem-int-video/c-html5-aem-int-video-customizingviewer/c-html5-aem-int-video-customizingviewer.md#concept-73a8546acdb444a387c49969ceca57d0) pour plus d’informations sur le style de la visionneuse avec CSS.

   Voici un exemple de définition d’une taille de visionneuse statique dans la page de HTML :

   ```html {.line-numbers}
   #s7viewer.s7interactivevideoviewer { 
    width: 640px; 
    height: 640px; 
   }
   ```

   Vous pouvez définir la variable `stagesize` modification dans l’enregistrement de paramètre prédéfini de visionneuse dans Experience Manager Assets - On-demand. Vous pouvez également le transmettre explicitement avec le code d’initialisation de la visionneuse avec `params` ou sous la forme d’un appel API, comme décrit dans la section Référence de commande, comme suit :

   ```html {.line-numbers}
   interactivevideoviewer.setParam("stagesize", "640,640");
   ```

   Une approche basée sur CSS est recommandée et est utilisée dans cet exemple.

1. Création et initialisation de la visionneuse.

   Une fois les étapes ci-dessus terminées, vous créez une instance de `s7viewers.InteractiveVideoViewer` , transmettez toutes les informations de configuration à son constructeur, et appelez `init()` sur une instance de visionneuse. Les informations de configuration sont transmises au constructeur sous la forme d’un objet JSON. Au minimum, cet objet doit avoir la valeur `containerId` champ contenant le nom de l’identifiant de conteneur de la visionneuse et imbriqué `params` Objet JSON avec des paramètres de configuration pris en charge par la visionneuse.

   Dans ce cas, la variable `params` doit comporter au moins l’URL du serveur d’images transmise comme `serverUrl` et la ressource initiale en tant que `asset` . L’API d’initialisation basée sur JSON vous permet de créer et de démarrer la visionneuse avec une seule ligne de code, l’URL du serveur vidéo transmise comme `videoserverurl` propriété, ressource initiale en tant que `asset` et données interactives sous la forme `interactivedata` . L’API d’initialisation basée sur JSON vous permet de créer et de démarrer la visionneuse avec une seule ligne de code.

   Il est important que le conteneur de la visionneuse soit ajouté au modèle DOM afin que le code de la visionneuse puisse trouver l’élément de conteneur en fonction de son identifiant. Certains navigateurs retardent la création du DOM jusqu’à la fin de la page web. Pour une compatibilité maximale, appelez la méthode `init()` juste avant la fermeture `BODY` ou sur le corps `onload()` .

   De même, l’élément de conteneur ne fait pas encore nécessairement partie de la mise en page de la page web. Par exemple, il peut être masqué à l’aide de `display:none` style qui lui est affecté. Dans ce cas, la visionneuse retarde son processus d’initialisation jusqu’au moment où la page web ramène l’élément de conteneur à la mise en page. Ce qui se produit, le chargement de la visionneuse reprend automatiquement.

   Voici un exemple de création d’une instance de visionneuse, de transmission des options de configuration minimales nécessaires au constructeur et d’appel de la fonction `init()` . L’exemple suppose les éléments suivants :

   * L’instance de visionneuse est `interactiveVideoViewer`.
   * Nom de l’espace réservé `DIV` is `s7viewer`.
   * L’URL du serveur d’images est `https://aodmarketingna.assetsadobe.com/is/image/`.
   * L’URL du serveur vidéo est `https://gateway-na.assetsadobe.com/DMGateway/public/aodmarketingna`.
   * L’URL de contenu est `https://aodmarketingna.assetsadobe.com/`.
   * La ressource est `/content/dam/mac/aodmarketingna/dm-viewers-content/video/Glacier.mp4`.
   * Les données interactives sont les suivantes : `is/content/content/dam/mac/aodmarketingna/_VTT/dm-viewers-content/video/Glacier.mp4.svideo.vtt`.

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

   Le code suivant est un exemple complet d’une page web triviale qui incorpore la visionneuse de vidéos interactives à une taille fixe :

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

**Intégration de conception réactive avec une hauteur libre**

Avec l’incorporation de responsive design, la page web dispose normalement d’une sorte de disposition flexible qui détermine la taille d’exécution du conteneur de la visionneuse. `DIV`. Dans l’exemple suivant, supposons que la page web autorise le conteneur de la visionneuse. `DIV` pour prendre 40 % de la taille de la fenêtre du navigateur web, sans restriction de sa hauteur. Le code de HTML de la page web se présente comme suit :

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

La page d’exemples suivante illustre d’autres utilisations réelles de l’incorporation en responsive design avec une hauteur illimitée :

[Démonstrations en direct](https://landing.adobe.com/en/na/dynamic-media/ctir-2755/live-demos.html)

[Autre emplacement de démonstration](https://experienceleague.adobe.com/tools/dynamic-media-demo/vlist/vlist.html)

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

Au lieu d’utiliser l’initialisation basée sur JSON, il est possible d’utiliser une API basée sur un setter et un constructeur sans args. L’utilisation de ce constructeur d’API ne prend aucun paramètre et les paramètres de configuration sont spécifiés à l’aide de `setContainerId()`, `setParam()`, et `setAsset()` Méthodes d’API avec des appels JavaScript distincts.

L’exemple suivant illustre l’utilisation de l’incorporation de tailles fixes avec l’API basée sur setter :

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
