---
description: Mixed Media Viewer est une visionneuse de supports. Il prend en charge les visionneuses de supports qui contiennent des images, des séries d’échantillons, des visionneuses à 360°, des vidéos et des visionneuses de vidéos adaptatives.
keywords: réactif
solution: Experience Manager
title: Supports variés
feature: Dynamic Media Classic,Viewers,SDK/API,Mix Media Sets
role: Developer,Business Practitioner
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '2673'
ht-degree: 0%

---


# Supports variés{#mixed-media}

Mixed Media Viewer est une visionneuse de supports. Il prend en charge les visionneuses de supports qui contiennent des images, des séries d’échantillons, des visionneuses à 360°, des vidéos et des visionneuses de vidéos adaptatives.

Une miniature au bas de la visionneuse représente chaque élément de visionneuse de supports, ainsi que son indicateur de type de fichier. Lorsqu’un élément de série d’échantillons est sélectionné, une ligne secondaire de nuances s’affiche pour permettre la sélection de variations de couleur dans l’ensemble d’échantillons. Les images et les éléments d’ensemble d’échantillons prennent en charge le zoom en mode continu ou intégré ; les visionneuses à 360° prennent en charge le zoom et la rotation. Les vidéos et les visionneuses de vidéos adaptatives prennent en charge toutes les commandes de lecture de base tant que les sous-titres éventuellement fermés s’affichent au-dessus du contenu vidéo. Un utilisateur peut à tout moment passer en mode plein écran en cliquant sur le bouton plein écran. Le lecteur de contenu dispose d’un bouton de fermeture facultatif. Il est conçu pour fonctionner sur les ordinateurs de bureau et les périphériques mobiles.

La visionneuse de supports variés utilise la lecture vidéo en flux continu HTML5 au format HLS dans sa configuration par défaut chaque fois que le système sous-jacent le prend en charge. Sur les systèmes qui ne prennent pas en charge la diffusion en flux continu HTML5, la visionneuse revient à la diffusion vidéo progressive HTML5.

>[!NOTE]
>
>Cette visionneuse ne prend pas en charge les images qui utilisent la fonction IR (Image Rendering) ou UGC (User-Generated Content).

Type de visionneuse 505.

Voir [Configuration système requise et configuration requise](../../c-system-requirements-and-prerequisites.md#concept-9282e5b777de42cdaf72ef7ebd646842).

## URL de la démonstration {#section-e1c3106f5b3e445d9b95be337c2f94e2}

[https://s7d9.scene7.com/s7viewers/html5/MixedMediaViewer.html?asset=Scene7SharedAssets/Mixed_Media_Set_Sample](https://s7d9.scene7.com/s7viewers/html5/MixedMediaViewer.html?asset=Scene7SharedAssets/Mixed_Media_Set_Sample)

## Utilisation de la visionneuse de supports variés {#section-f21ac23d3f6449ad9765588d69584772}

Mixed Media Viewer représente un fichier JavaScript principal et un ensemble de fichiers d’aide (un seul fichier JavaScript est inclus avec tous les composants du SDK de la visionneuse utilisés par cette visionneuse, ressources et CSS) téléchargés par la visionneuse au moment de l’exécution.

Vous pouvez utiliser la visionneuse de supports variés en mode contextuel à l’aide de la page HTML prête à l’emploi fournie avec les visionneuses IS. Vous pouvez également utiliser le lecteur en mode intégré, où il est intégré dans une page Web de cible à l’aide de l’API documentée.

La tâche de configuration et d’habillage de la visionneuse est similaire à celle des autres visionneuses. L’habillage est effectué au moyen d’une page CSS personnalisée.

Voir [Référence de commande commune à toutes les visionneuses - Attributs de configuration](../../r-html5-viewer-20-cmdref-configattrib/r-html5-viewer-20-cmdref-configattrib.md#concept-850e0f2c49b949deb7cfbfd330d329bd) et [Référence de commande commune à toutes les visionneuses - URL](../../c-html5-viewer-20-cmdref-url/c-html5-viewer-20-cmdref-url.md#concept-9b337f349b7b406b8c33c7ee96b3e226)

## Interaction avec la visionneuse de supports variés {#section-ab66eb6955aa4a8aa6d14a3b3acfed3f}

Mixed Media Viewer prend en charge les mouvements tactiles simples et multipoints courants dans d’autres applications mobiles. Lorsque le lecteur ne peut pas traiter le mouvement de glissement d’un utilisateur, il transfère le événement vers le navigateur Web pour effectuer un défilement de page natif. Cette fonctionnalité permet à un utilisateur de parcourir la page même si le lecteur occupe la majeure partie de l’écran du périphérique.

<table id="table_ED747CC7178448919C34A4FCD18922D0"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>Mouvement </p> </th> 
   <th colname="col2" class="entry"> <p>Description </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>Touche unique </p> </td> 
   <td colname="col2"> <p> Active la vue de la fenêtre déroulante ou les modifications entre le niveau de zoom Principal et le niveau de zoom secondaire. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Doublon </p> </td> 
   <td colname="col2"> <p>En mode de zoom <span class="codeph"> continu </span>, effectue un zoom dans un niveau jusqu’à ce que le facteur de zoom maximal soit atteint, le mouvement de pression du doublon suivant se réinitialise à l’état initial. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Toucher et maintenir </p> </td> 
   <td colname="col2"> <p> En mode de zoom intégré <span class="codeph"> </span>, active l’image agrandie. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Pincer </p> </td> 
   <td colname="col2"> <p>En mode de zoom continu, effectue un zoom avant ou arrière sur l’image. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Glissement ou clic horizontal </p> </td> 
   <td colname="col2"> <p> Lorsque le fichier actif est une visionneuse à 360° et que l’image est à l’état de réinitialisation, il tourne horizontalement dans la visionneuse à 360°. </p> <p> Lorsque le fichier actif est une visionneuse à 360° ou une image et que l’image est zoomée, il déplace l’image horizontalement. Si l’image est déplacée vers le bord de la vue et que le glissement est toujours effectué dans cette direction, le mouvement effectue un défilement de page natif. </p> <p> Fait défiler la liste des nuances dans la barre d’échantillons. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Glissement ou clic vertical </p> </td> 
   <td colname="col2"> <p> Si l’image est à l’état reset, elle modifie l’angle de vue vertical en cas d’utilisation d’une visionneuse à 360° multidimensionnelle. Dans une visionneuse à 360° unidimensionnelle, ou lorsqu’une visionneuse à 360° multidimensionnelle se trouve sur le dernier ou le premier axe, de sorte que le glissement vertical n’entraîne pas de changement de l’angle de vue vertical, le mouvement effectue le défilement de page natif. </p> <p> Lorsque le fichier actif est une visionneuse à 360° ou une image et que l’image est zoomée, déplace l’image verticalement. Si l’image est déplacée vers le bord de la vue et que le glissement est toujours effectué dans cette direction, le mouvement effectue le défilement natif de la page. </p> <p> Si le mouvement est effectué dans la zone des échantillons, il effectue un défilement de page natif. </p> </td> 
  </tr> 
 </tbody> 
</table>

Le lecteur prend également en charge les entrées tactiles et de souris sur les périphériques Windows dotés d’un écran tactile et d’une souris. Toutefois, cette prise en charge est limitée aux navigateurs Web Chrome, Internet Explorer 11 et Edge uniquement.

Cette visionneuse est entièrement accessible au clavier.

Voir [Accessibilité du clavier et navigation](../../c-keyboard-accessibility.md#topic-f5650e9493404e55a3627c8d1366b861).

## Incorporation de la visionneuse de supports variés {#section-6bb5d3c502544ad18a58eafe12a13435}

Différentes pages Web ont des besoins différents en ce qui concerne le comportement des visiteurs. Il arrive qu’une page Web fournisse un lien qui, lorsqu’un utilisateur clique dessus, ouvre le lecteur dans une fenêtre de navigateur distincte. Dans d’autres cas, il est nécessaire d’incorporer le droit du lecteur dans la page d’hébergement. Dans ce dernier cas, la page Web peut avoir une mise en page statique, ou utiliser une conception adaptée qui s’affiche différemment sur différents périphériques ou pour différentes tailles de fenêtre de navigateur. Pour répondre à ces besoins, le lecteur prend en charge trois modes de fonctionnement Principaux : fenêtre contextuelle, incorporation de tailles fixes et incorporation de conceptions réactives.

## A propos du mode contextuel {#section-77d5aa03b8b94566958a179b1a2cd474}

En mode contextuel, le lecteur s’ouvre dans une fenêtre ou un onglet distinct du navigateur Web. Elle prend toute la zone de la fenêtre du navigateur et s’ajuste au cas où le navigateur serait redimensionné ou où l’orientation d’un périphérique mobile serait modifiée.

Le mode contextuel est le plus courant pour les périphériques mobiles. La page Web charge la visionneuse à l’aide de l’appel JavaScript `window.open()`, d’un élément HTML `A` correctement configuré ou de toute autre méthode appropriée.

Il est recommandé d’utiliser une page HTML prête à l’emploi pour le mode d’opération contextuel. Dans ce cas, il s’appelle [!DNL MixedMediaViewer.html] et se trouve dans le sous-dossier [!DNL html5/] de votre déploiement des visionneuses IS standard :

[!DNL <s7viewers_root>/html5/MixedMediaViewer.html]

Vous pouvez réaliser la personnalisation visuelle en appliquant une page CSS personnalisée.

Voici un exemple de code HTML qui ouvre la visionneuse dans une nouvelle fenêtre :

```
<a href="http://s7d1.scene7.com/s7viewers/html5/MixedMediaViewer.html?asset=Scene7SharedAssets/Mixed_Media_Set_Sample" target="_blank">Open popup viewer</a>
```

## À propos de la taille fixe et de l’incorporation de la conception adaptée {#section-ec86b100ba5943d0b16694268520bbde}

En mode incorporé, le lecteur est ajouté à la page Web existante, qui peut déjà contenir du contenu client qui n’est pas lié au lecteur. En règle générale, le lecteur occupe uniquement une partie de l’espace d’une page Web.

Les cas d&#39;utilisation Principaux sont les pages Web orientées vers les ordinateurs de bureau ou les tablettes, ainsi que les pages de conception réactives qui ajustent automatiquement la mise en page en fonction du type de périphérique.

L’incorporation de taille fixe est utilisée lorsque la visionneuse ne change pas de taille après le chargement initial. Il s’agit du meilleur choix pour les pages Web présentant une disposition statique.

L’incorporation de la conception réactive suppose que la visionneuse doit peut-être être redimensionnée au moment de l’exécution en réponse au changement de taille de son conteneur `DIV`. Le cas d’utilisation le plus courant consiste à ajouter une visionneuse à une page Web qui utilise une disposition de page souple.

En mode d’incorporation de conceptions réactives, le lecteur se comporte différemment selon la manière dont la page Web dimensionne son conteneur `DIV`. Si la page Web ne définit que la largeur du conteneur `DIV`, en ne limitant pas sa hauteur, le lecteur sélectionne automatiquement sa hauteur en fonction des proportions du fichier utilisé. Cette fonctionnalité permet de s’assurer que la ressource s’intègre parfaitement à la vue sans remplissage sur les côtés. Ce cas d’utilisation est le plus courant pour les pages Web qui utilisent des structures de mise en page réactives telles que Bootstrap, Foundation, etc.

Sinon, si la page Web définit à la fois la largeur et la hauteur du conteneur `DIV` du lecteur, celui-ci remplit cette zone et suit la taille fournie par la mise en page Web. Un bon exemple est l’incorporation de la visionneuse dans une incrustation modale, où l’incrustation est dimensionnée en fonction de la taille de la fenêtre du navigateur Web.

## Incorporation de taille fixe {#section-17d162f76ffa4804b27928f51e7bea1d}

Pour ajouter la visionneuse à une page Web, procédez comme suit :

1. Ajouter le fichier JavaScript de la visionneuse sur votre page Web.
1. Définition du conteneur `DIV`.
1. Définition de la taille de la visionneuse.
1. Création et initialisation de la visionneuse.

1. Ajouter le fichier JavaScript de la visionneuse sur votre page Web.

   Pour créer une visionneuse, vous devez ajouter une balise de script dans l’en-tête HTML. Avant de pouvoir utiliser l’API du lecteur de contenu, veillez à inclure [!DNL MixedMediaViewer.js]. Le fichier [!DNL MixedMediaViewer.js] se trouve sous le sous-dossier [!DNL html5/js/] de votre déploiement des visionneuses IS standard :

[!DNL <s7viewers_root>/html5/js/MixedMediaViewer.js]

Vous pouvez utiliser un chemin relatif si la visionneuse est déployée sur l’un des serveurs Dynamic Media Classic de l’Adobe et qu’elle est diffusée à partir du même domaine. Sinon, vous spécifiez un chemin d’accès complet à l’un des serveurs Dynamic Media Classic Adobe sur lesquels les visionneuses IS sont installées.

Le chemin relatif ressemble à ce qui suit :

```
<script language="javascript" type="text/javascript" src="/s7viewers/html5/js/MixedMediaViewer.js"></script>
```

>[!NOTE]
>
>Vous ne devez référencer que le fichier JavaScript du lecteur principal `include` sur votre page. Vous ne devez pas référencer de fichiers JavaScript supplémentaires dans le code de la page Web qui pourraient être téléchargés selon la logique du lecteur au moment de l’exécution. En particulier, ne référencez pas directement la bibliothèque HTML5 SDK `Utils.js` chargée par la visionneuse à partir du chemin de contexte `/s7viewers` (appelé SDK consolidé `include`). La raison en est que l’emplacement des bibliothèques de lecteurs de contenu d’exécution `Utils.js` ou similaires est entièrement géré par la logique du lecteur et que l’emplacement change entre les versions du lecteur. Adobe ne conserve pas les anciennes versions du lecteur secondaire `includes` sur le serveur.
>
>
>Par conséquent, le fait de placer une référence directe à tout script JavaScript secondaire `include` utilisé par le lecteur sur la page rompt la fonctionnalité du lecteur à l’avenir lorsqu’une nouvelle version du produit est déployée.

1. Définition de la balise DIV de conteneur.

   Ajoutez un élément DIV vide sur la page où doit apparaître le lecteur de contenu. L’identifiant de l’élément DIV doit être défini, car il est transmis ultérieurement à l’API du lecteur de contenu. La taille du DIV est spécifiée par le biais de CSS.

   L’espace réservé DIV est un élément positionné, ce qui signifie que la propriété CSS `position` est définie sur `relative` ou `absolute`.

   Assurez-vous que la fonction plein écran fonctionne correctement dans Internet Explorer. Vérifiez qu’aucun autre élément du modèle DOM ne présente un ordre d’empilement supérieur à celui de votre balise d’emplacement DIV.

   Voici un exemple d’élément DIV d’espace réservé défini :

   ```
   <div id="s7viewer" style="position:relative"></div> 
   ```

1. Définition de la taille de la visionneuse

   Cette visionneuse affiche des miniatures lorsque vous travaillez avec des jeux d’éléments multiples. Sur les systèmes de bureau, les miniatures sont placées sous la vue principale. En même temps, le lecteur permet la permutation de la ressource principale lors de l’exécution à l’aide de l’API `setAsset()`. En tant que développeur, vous avez le contrôle sur la manière dont le lecteur gère la zone des vignettes en bas lorsque la nouvelle ressource ne comporte qu’un seul élément. Il est possible de garder intacte la taille de la visionneuse extérieure et de laisser la vue principale augmenter sa hauteur et occuper la zone des vignettes. Vous pouvez également maintenir la taille de la vue principale statique et réduire la zone extérieure du lecteur de contenu, en laissant le contenu de la page Web monter, puis utiliser l’espace de la page libre qui reste des miniatures.

   Pour que les limites extérieures de la visionneuse restent intactes, définissez la taille de la classe CSS de niveau supérieur `.s7mixedmediaviewer` en unités absolues. Le dimensionnement en CSS peut être placé directement sur la page HTML ou dans un fichier CSS de visionneuse personnalisée, qui est ultérieurement affecté à un enregistrement de paramètre prédéfini de visionneuse dans Dynamic Media Classic, ou transmis explicitement à l’aide de la commande de style.

   Voir [Personnalisation de la visionneuse de supports variés](../../c-html5-s7-aem-asset-viewers/c-html5-mixedmedia-viewer-about/c-html5-mixedmedia-viewer-customizingviewer/c-html5-mixedmedia-viewer-customizingviewer.md#concept-61b3410f187c4bf3af09ec813c649bf4) pour plus d’informations sur la mise en forme de la visionneuse à l’aide de CSS.

   Voici un exemple de définition de la taille de la visionneuse externe statique dans une page HTML :

   ```
   #s7viewer.s7mixedmediaviewer { 
    width: 640px; 
    height: 480px; 
   }
   ```

   Vous pouvez voir le comportement avec une zone de visionneuse externe fixe sur l’exemple de page suivant. Notez que lorsque vous passez d’un jeu à l’autre, la taille de la visionneuse externe ne change pas :

   [https://marketing.adobe.com/resources/help/en_US/s7/viewers_ref/samples/MixedMediaViewer-fixed-outer-area.html](https://marketing.adobe.com/resources/help/en_US/s7/viewers_ref/samples/MixedMediaViewer-fixed-outer-area.html)

   Pour rendre statiques les dimensions de la vue principale, définissez la taille de la visionneuse en unités absolues pour le composant SDK interne `Container` à l’aide du sélecteur CSS `.s7mixedmediaviewer .s7container` ou en utilisant le modificateur `stagesize`.

   Voici un exemple de définition de la taille de la visionneuse pour le composant SDK interne `Container` de sorte que la zone de vue principale ne change pas sa taille lors du changement de fichier :

   ```
   #s7viewer.s7mixedmediaviewer .s7container { 
    width: 640px; 
    height: 480px; 
   }
   ```

   L’exemple de page suivant montre le comportement de la visionneuse avec une taille de vue principale fixe. Notez que lorsque vous passez d’un jeu à l’autre, la vue principale reste statique et le contenu de la page Web se déplace verticalement :

   [https://marketing.adobe.com/resources/help/en_US/s7/viewers_ref/samples/MixedMediaViewer-fixed-main-view.html](https://marketing.adobe.com/resources/help/en_US/s7/viewers_ref/samples/MixedMediaViewer-fixed-main-view.html)

   Vous pouvez définir le modificateur `stagesize` soit dans l’enregistrement de paramètre prédéfini de la visionneuse dans Dynamic Media Classic, soit le transmettre explicitement au code d’initialisation de la visionneuse avec la collection `params`, soit en tant qu’appel d’API comme décrit dans la section Référence de commandes de cette aide, comme dans l’exemple suivant :

   ```
   mixedMediaViewer.setParam("stagesize", "640,480");
   ```

   Une approche CSS est recommandée et est utilisée dans cet exemple.

1. Création et initialisation de la visionneuse.

   Une fois les étapes ci-dessus terminées, vous créez une instance de classe `s7viewers.MixedMediaViewer`, vous transmettez toutes les informations de configuration à son constructeur et vous appelez la méthode `init()` sur une instance de lecteur. Les informations de configuration sont transmises au constructeur sous la forme d’un objet JSON. Au minimum, cet objet doit avoir le champ `containerId` qui contient le nom de l’ID de conteneur de la visionneuse et l’objet JSON imbriqué `params` avec les paramètres de configuration pris en charge par la visionneuse. Dans ce cas, l’objet `params` doit avoir au moins la propriété Image Serving URL transmise en tant que propriété `serverUrl`, l’URL du serveur vidéo transmise en tant que propriété `videoserverurl` et la ressource initiale en tant que paramètre `asset`. L’API d’initialisation basée sur JSON vous permet de créer et de début le lecteur avec une seule ligne de code.

   Il est important que le conteneur de la visionneuse soit ajouté au modèle DOM afin que le code de la visionneuse puisse trouver l’élément de conteneur en fonction de son identifiant. Certains navigateurs retardent la création du modèle DOM jusqu’à la fin de la page Web. Pour une compatibilité maximale, appelez la méthode `init()` juste avant la balise de fermeture `BODY` ou sur le événement body `onload()`.

   Dans le même temps, l’élément conteneur ne doit pas nécessairement faire partie de la mise en page de la page Web pour le moment. Par exemple, il peut être masqué à l’aide du style `display:none` qui lui est affecté. Dans ce cas, le lecteur retarde son processus d’initialisation jusqu’au moment où la page Web ramène l’élément de conteneur à la mise en page. Dans ce cas, le chargement du lecteur reprend automatiquement.

   Voici un exemple de création d’une instance de visionneuse, de transmission des options de configuration minimales nécessaires au constructeur et d’appel de la méthode `init()`. L’exemple suppose que `mixedMediaViewer` correspond à l’instance de visionneuse ; `s7viewer` est le nom de l&#39;espace réservé `DIV`; [!DNL http://s7d1.scene7.com/is/image/] correspond à l’URL de diffusion d’images ; [!DNL http://s7d1.scene7.com/is/content/] correspond à l’URL du serveur vidéo ; et [!DNL Scene7SharedAssets/Mixed_Media_Set_Sample] est l&#39;actif :

```
<script type="text/javascript"> 
var mixedMediaViewer = new s7viewers.MixedMediaViewer({ 
 "containerId":"s7viewer", 
"params":{ 
 "asset":"Scene7SharedAssets/Mixed_Media_Set_Sample", 
 "serverurl":"http://s7d1.scene7.com/is/image/", 
 "videoserverurl":"http://s7d1.scene7.com/is/content/" 
} 
}).init(); 
</script> 
<script type="text/javascript"> 
mixedMediaViewer.init(); 
</script>
```

Le code suivant est un exemple complet d’une page Web triviale qui incorpore la visionneuse de supports variés avec une taille fixe :

```
<!DOCTYPE html> 
<html> 
<head> 
<script type="text/javascript" src="http://s7d1.scene7.com/s7viewers/html5/js/MixedMediaViewer.js"></script> 
<style type="text/css"> 
#s7viewer.s7mixedmediaviewer { 
 width: 640px; 
 height: 480px; 
} 
</style> 
</head> 
<body> 
<div id="s7viewer" style="position:relative"></div> 
<script type="text/javascript"> 
var mixedMediaViewer = new s7viewers.MixedMediaViewer({ 
 "containerId":"s7viewer", 
"params":{ 
 "asset":"Scene7SharedAssets/Mixed_Media_Set_Sample", 
 "serverurl":"http://s7d1.scene7.com/is/image/", 
 "videoserverurl":"http://s7d1.scene7.com/is/content/" 
} 
}).init(); 
</script> 
</body> 
</html>
```

## Incorporation réactive avec une hauteur sans restriction {#section-056cb574713c4d07be6d07cf3c598839}

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
<script type="text/javascript" src="http://s7d1.scene7.com/s7viewers/html5/js/MixedMediaViewer.js"></script> 
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
var mixedMediaViewer = new s7viewers.MixedMediaViewer({ 
 "containerId":"s7viewer", 
"params":{ 
 "asset":"Scene7SharedAssets/Mixed_Media_Set_Sample", 
 "serverurl":"http://s7d1.scene7.com/is/image/", 
 "videoserverurl":"http://s7d1.scene7.com/is/content/" 
} 
}).init(); 
</script> 
</body> 
</html>
```

La page d’exemples suivante illustre d’autres utilisations réelles de l’incorporation de conceptions réactives avec une hauteur libre :

[Démonstrations en direct](https://landing.adobe.com/en/na/dynamic-media/ctir-2755/live-demos.html)

<!-- KEEP (https://marketing.adobe.com/resources/help/en_US/s7/vlist/vlist.html) -->

## Taille flexible incorporée avec largeur et hauteur définies {#section-0a329016f9414d199039776645c693de}

Dans le cas d’une incorporation de taille flexible avec des valeurs de largeur et de hauteur définies, le style de la page Web est différent. Il fournit les deux tailles à la balise `"holder"` DIV et le centre dans la fenêtre du navigateur. En outre, la page Web définit la taille des éléments `HTML` et `BODY` sur 100 %.

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

Le reste des étapes d&#39;incorporation est identique aux étapes utilisées pour l&#39;incorporation de conceptions réactives avec une hauteur libre. L’exemple qui en résulte est le suivant :

```
<!DOCTYPE html> 
<html> 
<head> 
<script type="text/javascript" src="http://s7d1.scene7.com/s7viewers/html5/js/MixedMediaViewer.js"></script> 
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
var mixedMediaViewer = new s7viewers.MixedMediaViewer({ 
 "containerId":"s7viewer", 
"params":{ 
 "asset":"Scene7SharedAssets/Mixed_Media_Set_Sample", 
 "serverurl":"http://s7d1.scene7.com/is/image/", 
 "videoserverurl":"http://s7d1.scene7.com/is/content/" 
} 
}).init(); 
</script> 
</body> 
</html>
```

## Incorporation à l’aide de l’API basée sur Setter {#section-af26f0cc2e5140e8a9bfd0c6a841a6d1}

Au lieu d’utiliser l’initialisation basée sur JSON, il est possible d’utiliser une API basée sur un setter et un constructeur sans args. L&#39;utilisation de ce constructeur d&#39;API ne prend aucun paramètre et les paramètres de configuration sont spécifiés à l&#39;aide des méthodes d&#39;API `setContainerId()`, `setParam()` et `setAsset()`, avec des appels JavaScript distincts.

L’exemple suivant illustre l’utilisation de l’incorporation de tailles fixes avec l’API basée sur un setter :

```
<!DOCTYPE html> 
<html> 
<head> 
<script type="text/javascript" src="http://s7d1.scene7.com/s7viewers/html5/js/MixedMediaViewer.js"></script> 
<style type="text/css"> 
#s7viewer.s7mixedmediaviewer { 
 width: 640px; 
 height: 480px; 
} 
</style> 
</head> 
<body> 
<div id="s7viewer" style="position:relative"></div> 
<script type="text/javascript"> 
var mixedMediaViewer = new s7viewers.MixedMediaViewer(); 
mixedMediaViewer.setContainerId("s7viewer"); 
mixedMediaViewer.setParam("serverurl", "http://s7d1.scene7.com/is/image/"); 
mixedMediaViewer.setAsset("Scene7SharedAssets/Mixed_Media_Set_Sample"); 
mixedMediaViewer.init(); 
</script> 
</body> 
</html>
```

