---
title: Mixte
description: La visionneuse de supports variés est une visionneuse de médias. Il prend en charge les visionneuses de supports qui contiennent des images, des séries d’échantillons, des visionneuses à 360°, des vidéos et des visionneuses de vidéos adaptatives.
keywords: sensible
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Mixed Media Sets
role: Developer,User
exl-id: 65a54308-f9db-4458-a9c3-ccb1433af43c
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '2581'
ht-degree: 0%

---

# Mixte{#mixed-media}

La visionneuse de supports variés est une visionneuse de médias. Elle prend en charge les visionneuses de médias qui contiennent des images, des visionneuses d’échantillons, des visionneuses à 360°, des vidéos et des visionneuses de vidéos adaptatives.

Une miniature dans la partie inférieure de la visionneuse représente chaque élément de visionneuse de médias, ainsi que son indicateur de type de ressource. Lorsqu’un élément d’échantillon est sélectionné, une deuxième ligne d’échantillons semble permettre la sélection de la variation de couleur dans l’échantillon. Les images et les éléments d’échantillon prennent en charge le zoom en mode continu ou en ligne ; les visionneuses à 360° prennent en charge le zoom et la rotation. Les vidéos et les visionneuses de vidéos adaptatives prennent en charge tous les contrôles de lecture de base à condition que les sous-titres facultatifs s’affichent au-dessus du contenu vidéo. Un utilisateur peut basculer vers le plein écran à tout moment en cliquant sur le bouton Plein écran . La visionneuse dispose d’un bouton de fermeture facultatif. Il est conçu pour fonctionner sur les ordinateurs de bureau et les appareils mobiles.

La visionneuse de médias mixtes utilise la lecture vidéo en flux continu HTML5 au format HLS dans sa configuration par défaut chaque fois que le système sous-jacent le prend en charge. Sur les systèmes qui ne prennent pas en charge la diffusion en flux continu HTML5, la visionneuse revient à la diffusion vidéo progressive HTML5.

>[!NOTE]
>
>Les images qui utilisent IR (Image Rendering) ou UGC (User-Generated Content) ne sont pas prises en charge par cette visionneuse.

Type de visionneuse 505.

Voir [Configuration requise et conditions préalables](../../c-system-requirements-and-prerequisites.md#concept-9282e5b777de42cdaf72ef7ebd646842).

## URL de démonstration {#section-e1c3106f5b3e445d9b95be337c2f94e2}

[https://s7d9.scene7.com/s7viewers/html5/MixedMediaViewer.html?asset=Scene7SharedAssets/Mixed_Media_Set_Sample](https://s7d9.scene7.com/s7viewers/html5/MixedMediaViewer.html?asset=Scene7SharedAssets/Mixed_Media_Set_Sample)

## Utilisation de la visionneuse de supports variés {#section-f21ac23d3f6449ad9765588d69584772}

La visionneuse de supports variés représente un fichier de JavaScript principal et un ensemble de fichiers d’assistance (une seule JavaScript inclure avec tous les composants SDK de la visionneuse utilisés par cette visionneuse particulière, ressources, CSS) téléchargés par la visionneuse au moment de l’exécution.

Vous pouvez utiliser la visionneuse de supports variés en mode pop-up à l’aide d’une page HTML prête pour la production fournie avec IS-Viewers. Vous pouvez également utiliser la visionneuse en mode intégré, où elle est intégrée dans une page Web cible à l’aide de l’API documentée.

La tâche de configuration et d’habillage de la visionneuse est similaire à celle des autres visionneuses. Tout l’habillage est réalisé par le biais d’une feuille de style CSS personnalisée.

Voir [Référence de commande commune à tous les visualiseurs - Attributs](../../r-html5-viewer-20-cmdref-configattrib/r-html5-viewer-20-cmdref-configattrib.md#concept-850e0f2c49b949deb7cfbfd330d329bd) de configuration et [Référence de commande communs à tous les visualiseurs - URL](../../c-html5-viewer-20-cmdref-url/c-html5-viewer-20-cmdref-url.md#concept-9b337f349b7b406b8c33c7ee96b3e226)

## Interaction avec la visionneuse de supports variés {#section-ab66eb6955aa4a8aa6d14a3b3acfed3f}

La visionneuse de supports variés prend en charge les gestes tactiles et multipoints courants dans d’autres applications mobiles. Lorsque le spectateur ne peut pas traiter le mouvement de glissement d’un utilisateur, il transfère l’événement au navigateur Web pour effectuer un défilement de page natif. Cette fonctionnalité permet à un utilisateur de naviguer dans la page même si la visionneuse occupe la majeure partie de la zone d’écran de l’appareil.

<table id="table_ED747CC7178448919C34A4FCD18922D0"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>Mouvement </p> </th> 
   <th colname="col2" class="entry"> <p>Description </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>Robinet unique </p> </td> 
   <td colname="col2"> <p> Active la vue déroulante ou passe du niveau de zoom principal au niveau de zoom secondaire. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Double appui </p> </td> 
   <td colname="col2"> <p>Lorsque vous êtes en <span class="codeph"> mode zoom continu </span> , zoome d’un niveau jusqu’à ce que le grossissement maximal soit atteint, le geste de double appui suivant se réinitialise à l’état initial. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Toucher et maintenir </p> </td> 
   <td colname="col2"> <p> Lorsque le mode de zoom intégré <span class="codeph"> est sélectionné</span>, l’image zoomée est activée. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Pincer </p> </td> 
   <td colname="col2"> <p>Lorsque vous passez en mode zoom continu, applique un zoom avant ou arrière sur l’image. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Glissement horizontal </p> </td> 
   <td colname="col2"> <p> Lorsque la ressource active est une visionneuse à 360° et que l’image est dans un état de réinitialisation, elle tourne horizontalement dans la visionneuse à 360°. </p> <p> Lorsque la ressource active est une visionneuse à 360° ou une image et que l’image est zoomée, elle déplace l’image horizontalement. Si l’image est déplacée vers le bord de la vue et que le balayage est toujours effectué dans cette direction, le mouvement effectue un défilement de page natif. </p> <p> Fait défiler la liste des nuances dans la barre d’échantillons. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Balayage vertical </p> </td> 
   <td colname="col2"> <p> Si l’image est dans un état de réinitialisation, cela change l’angle de vue vertical en cas d’utilisation d’une visionneuse à 360° multidimensionnelle. Dans une visionneuse à 360° unidimensionnelle, ou lorsqu’une visionneuse à 360° multidimensionnelle se trouve sur le dernier ou le premier axe, de sorte que le balayage vertical n’entraîne pas de modification de l’angle de vue vertical, le mouvement effectue le défilement natif de la page. </p> <p> Lorsque la ressource active est une visionneuse à 360° ou une image et que l’image fait l’objet d’un zoom, déplace l’image verticalement. Si l’image est déplacée vers le bord de la vue et que le balayage est toujours effectué dans cette direction, le mouvement effectue le défilement de la page native. </p> <p> Si le mouvement est effectué dans la zone d’échantillons, il effectue un défilement de page natif. </p> </td> 
  </tr> 
 </tbody> 
</table>

La visionneuse prend également en charge l’entrée tactile et l’entrée souris sur les appareils Windows dotés d’un écran tactile et d’une souris. Cette prise en charge est toutefois limitée aux navigateurs Web Chrome, Internet Explorer 11 et Edge uniquement.

Cette visionneuse est entièrement accessible à l’aide du clavier.

Voir [Accessibilité clavier et navigation](../../c-keyboard-accessibility.md#topic-f5650e9493404e55a3627c8d1366b861).

## Incorporation d’une visionneuse de supports variés {#section-6bb5d3c502544ad18a58eafe12a13435}

Les différentes pages web ont des besoins différents en ce qui concerne le comportement des spectateurs. Parfois, une page Web fournit un lien qui, lorsqu’il est sélectionné, ouvre la visionneuse dans une fenêtre de navigateur distincte. Dans d’autres cas, il est nécessaire d’intégrer la visionneuse directement sur la page d’hébergement. Dans ce dernier cas, la page Web peut avoir une mise en page statique ou utiliser un design réactif qui s’affiche différemment sur différents appareils ou pour différentes tailles de fenêtre de navigateur. Pour répondre à ces besoins, la visionneuse prend en charge trois modes de fonctionnement principaux : pop-up, incorporation de taille fixe et incorporation de conception réactive.

## A propos du mode pop-up {#section-77d5aa03b8b94566958a179b1a2cd474}

En mode pop-up, la visionneuse est ouverte dans une fenêtre ou un onglet de navigateur Web distinct. Il prend toute la zone de la fenêtre du navigateur et s’ajuste en cas de redimensionnement du navigateur ou de changement d’orientation d’un appareil mobile.

Le mode pop-up est le plus courant pour les appareils mobiles. La page Web charge la visionneuse à l’aide `window.open()` d’JavaScript appel, d’un élément HTML correctement configuré `A` ou de toute autre méthode appropriée.

Il est recommandé d’utiliser une page HTML prête à l’emploi pour le mode de fonctionnement contextuel. Dans ce cas, il est appelé [!DNL MixedMediaViewer.html] et se trouve dans le [!DNL html5/] sous-dossier de votre déploiement IS-Viewers standard :

[!DNL <s7viewers_root>/html5/MixedMediaViewer.html]

Vous pouvez obtenir une personnalisation visuelle en appliquant une feuille de style CSS personnalisée.

Voici un exemple de code HTML qui ouvre la visionneuse dans une nouvelle fenêtre :

```html {.line-numbers}
<a href="http://s7d1.scene7.com/s7viewers/html5/MixedMediaViewer.html?asset=Scene7SharedAssets/Mixed_Media_Set_Sample" target="_blank">Open popup viewer</a>
```

## A propos de la taille fixe et de l’incorporation de la conception réactive {#section-ec86b100ba5943d0b16694268520bbde}

En mode intégré, la visionneuse est ajoutée à la page Web existante, qui peut déjà contenir du contenu client non lié à la visionneuse. Le spectateur n’occupe normalement qu’une partie de l’espace d’une page Web.

Les principaux cas d’utilisation sont les pages Web orientées vers les ordinateurs de bureau ou les tablettes, ainsi que les pages de conception réactive qui ajustent automatiquement la mise en page en fonction du type d’appareil.

L’incorporation de taille fixe est utilisée lorsque la visionneuse ne modifie pas sa taille après le chargement initial. Cette action constitue le meilleur choix pour les pages Web dotées d’une disposition statique.

L’incorporation de conception réactive suppose que la visionneuse doit se redimensionner au moment de l’exécution en réponse au changement de taille de son conteneur `DIV`. Le cas d’utilisation le plus courant consiste à ajouter une visionneuse à une page web qui utilise une disposition de page flexible.

En mode d’incorporation de responsive design, la visionneuse se comporte différemment selon la manière dont la page web dimensionne son `DIV` de conteneur. Si la page web définit uniquement la largeur du `DIV` de conteneur, sans restriction de hauteur, la visionneuse choisit automatiquement sa hauteur en fonction des proportions de la ressource utilisée. Cette fonctionnalité garantit que la ressource s’adapte parfaitement à la vue sans marge intérieure sur les côtés. Ce cas d’utilisation est le plus courant pour les pages web utilisant des structures de disposition en responsive design telles que Bootstrap ou Foundation.

Dans le cas contraire, si la page web définit à la fois la largeur et la hauteur du `DIV` de conteneur de la visionneuse, celle-ci remplit exactement cette zone et suit la taille fournie par la disposition de la page web. Un bon exemple consiste à incorporer la visionneuse dans une superposition modale, où la superposition est dimensionnée en fonction de la taille de la fenêtre du navigateur web.

## Incorporation de taille fixe {#section-17d162f76ffa4804b27928f51e7bea1d}

Pour ajouter la visionneuse à une page Web, procédez comme suit :

1. Ajout du fichier JavaScript de visionneuse à votre page Web.
1. Définition du conteneur `DIV`.
1. Définition de la taille de la visionneuse.
1. Création et initialisation de la visionneuse.

1. Ajout du fichier JavaScript de visionneuse à votre page Web.

   Pour créer une visionneuse, vous devez ajouter une balise de script dans l’en-tête HTML. Avant de pouvoir utiliser l’API de visionneuse, veillez à inclure [!DNL MixedMediaViewer.js]le fichier . Le [!DNL MixedMediaViewer.js] fichier se trouve dans le [!DNL html5/js/] sous-dossier de votre déploiement IS-Viewers standard :

[!DNL <s7viewers_root>/html5/js/MixedMediaViewer.js]

Vous pouvez utiliser un chemin d’accès relatif si la visionneuse est déployée sur l’un des serveurs Adobe Dynamic Media Classic et qu’elle est diffusée à partir du même domaine. Sinon, vous spécifiez un chemin d’accès complet à l’un des serveurs Adobe Dynamic Media Classic sur lesquels les IS-Viewers sont installés.

Le chemin d’accès relatif ressemble à ce qui suit :

```html {.line-numbers}
<script language="javascript" type="text/javascript" src="/s7viewers/html5/js/MixedMediaViewer.js"></script>
```

>[!NOTE]
>
>Référencez uniquement le fichier JavaScript `include` de visionneuse principal sur votre page. Ne référencez pas de fichiers JavaScript supplémentaires dans le code de la page Web qui pourraient être téléchargés par la logique du visualiseur au moment de l’exécution. En particulier, ne référencez pas directement la bibliothèque SDK `Utils.js` HTML5 chargée par la visionneuse à partir du chemin d’accès `/s7viewers` au contexte (SDK `include`consolidé). La raison en est que l’emplacement des bibliothèques d’exécution ou des bibliothèques de `Utils.js` visionneuse similaires est entièrement géré par la logique de la visionneuse et que l’emplacement change entre les versions de la visionneuse. Adobe ne conserve pas les anciennes versions de la visionneuse `includes` secondaire sur le serveur.
>
>
>Par conséquent, le fait de placer une référence directe à une JavaScript `include` secondaire utilisée par l’utilisateur sur la page interrompt la fonctionnalité de la visionneuse à l’avenir lorsqu’une nouvelle version du produit est déployée.

1. Définition du conteneur DIV.

   Ajoutez un élément DIV vide à la page dans laquelle vous souhaitez que la visionneuse apparaisse. L’ID de l’élément DIV doit être défini, car cet identifiant est transmis ultérieurement à l’API de visionneuse. La taille de la DIV est spécifiée via CSS.

   L’espace réservé DIV est un élément positionné, ce qui signifie que la `position` propriété CSS est définie sur `relative` ou `absolute`.

   Assurez-vous que la fonctionnalité Plein écran fonctionne correctement dans Internet Explorer. Vérifiez qu’aucun autre élément dans le DOM n’a un ordre d’empilement supérieur à celui de votre balise div d’espace réservé.

   Voici un exemple d’élément DIV d’espace réservé défini :

   ```html {.line-numbers}
   <div id="s7viewer" style="position:relative"></div> 
   ```

1. Définition de la taille de la visionneuse

   Cette visionneuse affiche des miniatures lorsque vous travaillez avec des visionneuses multi-éléments. Sur les ordinateurs de bureau, des miniatures sont placées sous la vue principale. Dans le même temps, la visionneuse permet l’échange de la ressource principale pendant l’exécution à l’aide d’API `setAsset()` . En tant que développeur, vous contrôlez la façon dont la visionneuse gère la zone des vignettes en bas lorsque la nouvelle ressource ne comporte qu’un seul élément. Il est possible de garder la taille de la visionneuse extérieure intacte et de laisser la vue principale augmenter sa hauteur et occuper la zone des vignettes. Vous pouvez également conserver la taille de la vue principale statique et réduire la zone extérieure de la visionneuse, ce qui permet au contenu de la page Web de se déplacer vers le haut. Ensuite, utilisez l’espace de page gratuit qui reste des miniatures.

   Pour conserver les limites extérieures de la visionneuse, définissez la taille de `.s7mixedmediaviewer` la classe CSS de niveau supérieur en unités absolues. Le dimensionnement dans CSS peut être placé directement sur la page HTML ou dans un fichier CSS de visionneuse personnalisé, puis affecté à un enregistrement de paramètre prédéfini de visionneuse dans Dynamic Media Classic, ou transmis explicitement à l’aide de la commande de style.

   Voir [Personnalisation de la visionneuse](../../c-html5-s7-aem-asset-viewers/c-html5-mixedmedia-viewer-about/c-html5-mixedmedia-viewer-customizingviewer/c-html5-mixedmedia-viewer-customizingviewer.md#concept-61b3410f187c4bf3af09ec813c649bf4) de supports variés pour plus d’informations sur le style de la visionneuse avec CSS.

   Voici un exemple de définition de la taille statique de la visionneuse externe dans une page HTML :

   ```html {.line-numbers}
   #s7viewer.s7mixedmediaviewer { 
    width: 640px; 
    height: 480px; 
   }
   ```

   Vous pouvez voir le comportement avec une zone de visionneuse extérieure fixe sur l’exemple de page suivant. Notez que lorsque vous basculez entre des visionneuses, la taille extérieure de la visionneuse ne change pas :

   [https://experienceleague.adobe.com/tools/dynamic-media-demo/viewers-ref/mixedmedia/MixedMediaViewer-fixed-outer-area.html?lang=fr](https://experienceleague.adobe.com/tools/dynamic-media-demo/viewers-ref/mixedmedia/MixedMediaViewer-fixed-outer-area.html?lang=fr)

   Pour rendre les dimensions de la vue principale statiques, définissez la taille de la visionneuse en unités absolues pour le composant SDK interne `Container` à l’aide `.s7mixedmediaviewer .s7container` du sélecteur CSS ou à l’aide `stagesize` du modificateur.

   Voici un exemple de définition de la taille de la visionneuse pour le composant SDK interne `Container` afin que la zone d’affichage principale ne modifie pas sa taille lors du changement de ressource :

   ```html {.line-numbers}
   #s7viewer.s7mixedmediaviewer .s7container { 
    width: 640px; 
    height: 480px; 
   }
   ```

   L’exemple de page suivant montre le comportement d’un observateur avec une taille d’affichage principal fixe. Notez que lorsque vous basculez entre des visionneuses, la vue principale reste statique et le contenu de la page Web se déplace verticalement :

   [https://experienceleague.adobe.com/tools/dynamic-media-demo/viewers-ref/mixedmedia/MixedMediaViewer-fixed-main-view.html?lang=fr](https://experienceleague.adobe.com/tools/dynamic-media-demo/viewers-ref/mixedmedia/MixedMediaViewer-fixed-main-view.html?lang=fr)

   Vous pouvez définir le `stagesize` modificateur dans l’enregistrement du paramètre prédéfini de la visionneuse dans Dynamic Media Classic ou le transmettre explicitement avec le code d’initialisation de la visionneuse avec `params` collection. Ou, en tant qu’appel d’API comme décrit dans la section Référence des commandes de cette aide, comme dans ce qui suit :

   ```html {.line-numbers}
   mixedMediaViewer.setParam("stagesize", "640,480");
   ```

   Une approche basée sur le code CSS est recommandée et est utilisée dans cet exemple.

1. Création et initialisation de la visionneuse.

   Lorsque vous avez terminé les étapes ci-dessus, vous créez une instance de classe, transmettez toutes les informations de configuration à son constructeur et appelez `s7viewers.MixedMediaViewer` la méthode sur une instance de `init()` visionneuse. Les informations de configuration sont transmises au constructeur sous la forme d’un objet JSON. Au minimum, cet objet doit avoir le `containerId` champ qui contient le nom de l’ID de conteneur de la visionneuse et de l’objet JSON imbriqué `params` avec les paramètres de configuration pris en charge par la visionneuse. Dans ce cas, l’objet `params` doit avoir au moins l’URL Image Serving transmise en tant que propriété, l’URL du serveur vidéo transmise en propriété et la ressource initiale en tant que `serverUrl` `videoserverurl` `asset` paramètre. L’API d’initialisation basée sur JSON vous permet de créer et de démarrer la visionneuse avec une seule ligne de code.

   Il est important d’ajouter le conteneur de visionneuse au DOM afin que le code de visionneuse puisse trouver l’élément conteneur par son identifiant. Certains navigateurs retardent la création de DOM jusqu’à la fin de la page Web. Pour une compatibilité maximale, appelez la `init()` méthode juste avant la balise de fermeture `BODY` , ou sur l’événement body `onload()` .

   Dans le même temps, l’élément conteneur ne doit pas nécessairement faire partie de la mise en page Web pour le moment. Par exemple, il peut être masqué à l’aide `display:none` du style qui lui est attribué. Dans ce cas, la visionneuse retarde son processus d’initialisation jusqu’au moment où la page Web ramène l’élément conteneur à la mise en page. Lorsque cette action se produit, le chargement de la visionneuse reprend automatiquement.

   Voici un exemple de création d’une instance de visionneuse, de transmission des options de configuration minimales nécessaires au constructeur et d’appel de la `init()` méthode. L’exemple suppose `mixedMediaViewer` est l’instance de visionneuse, `s7viewer` est le nom de l’espace réservé`DIV`[!DNL http://s7d1.scene7.com/is/image/], est l’URL [!DNL http://s7d1.scene7.com/is/content/] du serveur d’images, est l’URL du serveur vidéo et [!DNL Scene7SharedAssets/Mixed_Media_Set_Sample] est la ressource :

```html {.line-numbers}
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

Le code suivant est un exemple complet de page Web triviale qui intègre la visionneuse de médias mixtes avec une taille fixe :

```html {.line-numbers}
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

## Intégration réactive avec une hauteur illimitée {#section-056cb574713c4d07be6d07cf3c598839}

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

1. Ajout du fichier JavaScript de la visionneuse à votre page web.
1. Définition du DIV du conteneur.
1. Création et initialisation de la visionneuse.

Toutes les étapes ci-dessus sont identiques à l’incorporation de taille fixe. Ajoutez le conteneur DIV au DIV `"holder"` existant. Le code suivant en est un exemple complet. Notez comment la taille de la visionneuse change lorsque le navigateur est redimensionné et comment les proportions de la visionneuse correspondent à la ressource.

```html {.line-numbers}
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

La page d’exemples suivante illustre d’autres utilisations réelles de l’incorporation de conception réactive avec une hauteur illimitée :

[Démonstrations en direct](https://landing.adobe.com/en/na/dynamic-media/ctir-2755/live-demos.html)

[Autre emplacement de démonstration](https://experienceleague.adobe.com/tools/dynamic-media-demo/vlist/vlist.html?lang=fr)

## Intégration de taille flexible avec largeur et hauteur définies {#section-0a329016f9414d199039776645c693de}

S’il existe un incorporation de taille flexible avec la largeur et la hauteur définies, le style de la page Web est différent. Il fournit les deux tailles au DIV `"holder"` et le centre dans la fenêtre du navigateur. En outre, la page Web définit la taille de l’élément `HTML` et `BODY` sur 100 %.

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

Le reste des étapes d’incorporation sont identiques aux étapes utilisées pour l’incorporation de conception réactive avec une hauteur illimitée. L’exemple résultant est le suivant :

```html {.line-numbers}
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

Au lieu d’utiliser l’initialisation basée sur JSON, il est possible d’utiliser l’API basée sur setter et le constructeur no-args. L’utilisation de ce constructeur d’API ne prend aucun paramètre et les paramètres de configuration sont spécifiés à l’aide de `setContainerId()`, `setParam()`et `setAsset()` des méthodes d’API, avec des appels JavaScript distincts.

L’exemple suivant illustre l’utilisation de l’incorporation de taille fixe avec l’API basée sur setter :

```html {.line-numbers}
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
