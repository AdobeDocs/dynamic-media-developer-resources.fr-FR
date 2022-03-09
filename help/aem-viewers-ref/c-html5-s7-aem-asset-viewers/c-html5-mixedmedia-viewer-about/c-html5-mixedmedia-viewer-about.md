---
title: Supports variés
description: Visionneuse de médias mixtes est une visionneuse de médias. Il prend en charge les visionneuses de médias qui contiennent des images, des visionneuses d’échantillons, des visionneuses à 360°, des vidéos et des visionneuses de vidéos adaptatives.
keywords: responsive
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Mixed Media Sets
role: Developer,User
exl-id: 65a54308-f9db-4458-a9c3-ccb1433af43c
source-git-commit: b89ca96947f751b750623e1f18d2a5d86f0cd759
workflow-type: tm+mt
source-wordcount: '2645'
ht-degree: 0%

---

# Supports variés{#mixed-media}

Visionneuse de médias mixtes est une visionneuse de médias. Il prend en charge les visionneuses de médias qui contiennent des images, des visionneuses d’échantillons, des visionneuses à 360°, des vidéos et des visionneuses de vidéos adaptatives.

Une miniature au bas de la visionneuse représente chaque élément de visionneuse de médias, ainsi que son indicateur de type de ressource. Lorsqu’un élément d’ensemble d’échantillons est sélectionné, une deuxième ligne d’échantillons s’affiche pour permettre la sélection de la variation de couleur dans l’ensemble d’échantillons. Les images et les éléments d’ensemble d’échantillons prennent en charge le zoom en mode continu ou intégré ; les visionneuses à 360° prennent en charge le zoom et la rotation. Les vidéos et les visionneuses de vidéos adaptatives prennent en charge toutes les commandes de lecture de base tant que les sous-titres fermés facultatifs s’affichent au-dessus du contenu vidéo. Un utilisateur peut passer en mode Plein écran à tout moment en cliquant sur le bouton Plein écran. La visionneuse comporte un bouton de fermeture facultatif. Il est conçu pour fonctionner sur les ordinateurs de bureau et les appareils mobiles.

La visionneuse de supports variés utilise la lecture vidéo en flux continu HTML5 au format HLS dans sa configuration par défaut chaque fois que le système sous-jacent la prend en charge. Sur les systèmes qui ne prennent pas en charge la diffusion HTML5, la visionneuse revient à la diffusion vidéo progressive par HTML5.

>[!NOTE]
>
>Les images qui utilisent IR (Image Rendering) ou UGC (User-Generated Content) ne sont pas prises en charge par cette visionneuse.

Type de visionneuse 505.

Voir [Configuration requise et conditions préalables](../../c-system-requirements-and-prerequisites.md#concept-9282e5b777de42cdaf72ef7ebd646842).

## URL de démonstration {#section-e1c3106f5b3e445d9b95be337c2f94e2}

[https://s7d9.scene7.com/s7viewers/html5/MixedMediaViewer.html?asset=Scene7SharedAssets/Mixed_Media_Set_Sample](https://s7d9.scene7.com/s7viewers/html5/MixedMediaViewer.html?asset=Scene7SharedAssets/Mixed_Media_Set_Sample)

## Utilisation de la visionneuse de supports variés {#section-f21ac23d3f6449ad9765588d69584772}

La visionneuse de médias mixtes représente un fichier JavaScript principal et un ensemble de fichiers d’assistance (un seul script JavaScript inclus avec tous les composants du SDK de la visionneuse utilisés par cette visionneuse, ressources et CSS particulière) téléchargés par la visionneuse au moment de l’exécution.

Vous pouvez utiliser la visionneuse de supports variés en mode pop-up à l’aide de la page de HTML prête pour la production fournie avec les visionneuses IS. Vous pouvez également utiliser la visionneuse en mode incorporé, où elle est intégrée dans une page web cible à l’aide de l’API documentée.

La configuration et l’habillage de la visionneuse sont similaires à d’autres visionneuses. L’habillage est effectué au moyen d’une feuille CSS personnalisée.

Voir [Référence de commande commune à toutes les visionneuses - Attributs de configuration](../../r-html5-viewer-20-cmdref-configattrib/r-html5-viewer-20-cmdref-configattrib.md#concept-850e0f2c49b949deb7cfbfd330d329bd) et [Référence de commande commune à toutes les visionneuses - URL](../../c-html5-viewer-20-cmdref-url/c-html5-viewer-20-cmdref-url.md#concept-9b337f349b7b406b8c33c7ee96b3e226)

## Interaction avec la visionneuse de supports variés {#section-ab66eb6955aa4a8aa6d14a3b3acfed3f}

La visionneuse de supports variés prend en charge les gestes tactiles simples et multipoints communs aux autres applications mobiles. Lorsque la visionneuse ne peut pas traiter le mouvement de glissement d’un utilisateur, elle transfère l’événement vers le navigateur web pour effectuer un défilement de page natif. Cette fonctionnalité permet à l’utilisateur de parcourir la page même si la visionneuse occupe la majeure partie de la zone d’écran de l’appareil.

<table id="table_ED747CC7178448919C34A4FCD18922D0"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>Mouvement </p> </th> 
   <th colname="col2" class="entry"> <p>Description </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>Appuyer une seule fois </p> </td> 
   <td colname="col2"> <p> Active la vue déroulante ou modifie le niveau de zoom Principal et secondaire. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Double appui </p> </td> 
   <td colname="col2"> <p>Dans <span class="codeph"> continue </span> mode zoom, zoome à un niveau jusqu’à ce que l’agrandissement maximal soit atteint, le prochain geste double d’appui réinitialise l’état initial. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Toucher et maintenir </p> </td> 
   <td colname="col2"> <p> Dans <span class="codeph"> inline </span> mode zoom , active l’image agrandie. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Pincement </p> </td> 
   <td colname="col2"> <p>En mode zoom continu, permet d’effectuer un zoom avant ou arrière sur l’image. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Glissement ou clic horizontal </p> </td> 
   <td colname="col2"> <p> Lorsque la ressource active est une visionneuse à 360° et que l’image est à l’état réinitialisé, elle tourne à travers la visionneuse à 360° horizontalement. </p> <p> Lorsque la ressource active est une visionneuse à 360° ou une image avec un zoom avant, l’image est déplacée horizontalement. Si l’image est déplacée vers le bord de la vue et que le glissement est toujours effectué dans cette direction, le mouvement effectue un défilement de page natif. </p> <p> Fait défiler la liste des échantillons dans la barre d’échantillons. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Glissement ou clic vertical </p> </td> 
   <td colname="col2"> <p> Si l’image est à l’état réinitialisé, l’angle d’affichage vertical est modifié en cas d’utilisation d’une visionneuse à 360° multidimensionnelle. Dans une visionneuse à 360° unidimensionnelle, ou lorsqu’une visionneuse à 360° multidimensionnelle se trouve sur le dernier ou le premier axe, de sorte que le glissement vertical n’entraîne pas de changement de l’angle d’affichage vertical, le mouvement effectue un défilement de page natif. </p> <p> Lorsque la ressource active est une visionneuse à 360° ou une image avec un zoom avant, l’image est déplacée verticalement. Si l’image est déplacée vers le bord de la vue et que le glissement est toujours effectué dans cette direction, le mouvement effectue un défilement de page natif. </p> <p> Si le mouvement est effectué dans la zone des échantillons, il effectue un défilement de page natif. </p> </td> 
  </tr> 
 </tbody> 
</table>

La visionneuse prend également en charge les entrées tactile et de souris sur les périphériques Windows dotés d’un écran tactile et d’une souris. Toutefois, cette prise en charge est limitée aux navigateurs Chrome, Internet Explorer 11 et Edge uniquement.

Cette visionneuse est entièrement accessible au clavier.

Voir [Accessibilité du clavier et navigation](../../c-keyboard-accessibility.md#topic-f5650e9493404e55a3627c8d1366b861).

## Intégration de la visionneuse de supports variés {#section-6bb5d3c502544ad18a58eafe12a13435}

Le comportement de la visionneuse varie en fonction des pages web. Il arrive qu’une page web fournisse un lien qui, lorsqu’il est sélectionné, ouvre la visionneuse dans une fenêtre de navigateur distincte. Dans d’autres cas, il est nécessaire d’incorporer le droit de visionneuse dans la page d’hébergement. Dans ce cas, la page web peut avoir une mise en page statique ou utiliser une conception réactive qui s’affiche différemment sur différents appareils ou pour différentes tailles de fenêtre de navigateur. Pour répondre à ces besoins, la visionneuse prend en charge trois modes de fonctionnement Principaux : pop-up, incorporation de taille fixe et incorporation de conceptions réactives.

## A propos du mode pop-up {#section-77d5aa03b8b94566958a179b1a2cd474}

En mode contextuel, la visionneuse s’ouvre dans une fenêtre ou un onglet de navigateur Web distinct. Il prend toute la zone de la fenêtre du navigateur et s’ajuste au cas où le navigateur serait redimensionné ou si l’orientation d’un appareil mobile est modifiée.

Le mode pop-up est le plus courant pour les appareils mobiles. La page web charge la visionneuse à l’aide de `window.open()` Appel JavaScript, correctement configuré `A` élément de HTML ou toute autre méthode appropriée.

Il est recommandé d’utiliser une page de HTML d’usine pour le mode de fonctionnement de la fenêtre contextuelle. Dans ce cas, il est appelé [!DNL MixedMediaViewer.html] et se trouve dans la variable [!DNL html5/] sous-dossier de votre déploiement IS-Viewers standard :

[!DNL <s7viewers_root>/html5/MixedMediaViewer.html]

Vous pouvez effectuer une personnalisation visuelle en appliquant une page CSS personnalisée.

Voici un exemple de code de HTML qui ouvre la visionneuse dans une nouvelle fenêtre :

```html {.line-numbers}
<a href="http://s7d1.scene7.com/s7viewers/html5/MixedMediaViewer.html?asset=Scene7SharedAssets/Mixed_Media_Set_Sample" target="_blank">Open popup viewer</a>
```

## À propos de la taille fixe et de l’incorporation des conceptions réactives {#section-ec86b100ba5943d0b16694268520bbde}

En mode incorporé, la visionneuse est ajoutée à la page web existante, qui peut déjà comporter du contenu client non lié à la visionneuse. Normalement, la visionneuse occupe uniquement une partie de l’espace d’une page web.

Les cas d’utilisation Principaux sont les pages web orientées vers les ordinateurs de bureau ou les tablettes, ainsi que les pages de conception réactive qui ajustent automatiquement la mise en page en fonction du type d’appareil.

L’incorporation des tailles fixes est utilisée lorsque la visionneuse ne modifie pas sa taille après le chargement initial. Cette action est la meilleure solution pour les pages web avec une disposition statique.

L’incorporation de conceptions réactives suppose que la visionneuse doit être redimensionnée au moment de l’exécution en réponse au changement de taille de son conteneur. `DIV`. Le cas d’utilisation le plus courant consiste à ajouter une visionneuse à une page web qui utilise une mise en page flexible.

En mode d’incorporation de responsive design, la visionneuse se comporte différemment selon la manière dont la page web dimensionne son conteneur. `DIV`. Si la page web définit uniquement la largeur du conteneur `DIV`, sans restriction de hauteur, la visionneuse choisit automatiquement sa hauteur en fonction des proportions de la ressource utilisée. Cette fonctionnalité permet de s’assurer que la ressource s’intègre parfaitement dans la vue sans marge intérieure sur les côtés. Ce cas d’utilisation est le plus courant pour les pages web qui utilisent des structures de mise en page en responsive design comme Bootstrap ou Foundation.

Sinon, si la page web définit la largeur et la hauteur du conteneur de la visionneuse. `DIV`, la visionneuse remplit uniquement cette zone et suit la taille fournie par la mise en page web. Un bon exemple consiste à incorporer la visionneuse dans une superposition modale, où la superposition est dimensionnée en fonction de la taille de la fenêtre du navigateur web.

## Incorporation de taille fixe {#section-17d162f76ffa4804b27928f51e7bea1d}

Pour ajouter la visionneuse à une page web, procédez comme suit :

1. Ajout du fichier JavaScript de la visionneuse à votre page web.
1. Définir le conteneur `DIV`.
1. Définition de la taille de la visionneuse.
1. Création et initialisation de la visionneuse.

1. Ajout du fichier JavaScript de la visionneuse à votre page web.

   Pour créer une visionneuse, vous devez ajouter une balise de script dans l’en-tête du HTML. Avant d’utiliser l’API de visionneuse, veillez à inclure [!DNL MixedMediaViewer.js]. Le [!DNL MixedMediaViewer.js] se trouve sous le fichier [!DNL html5/js/] sous-dossier de votre déploiement IS-Viewers standard :

[!DNL <s7viewers_root>/html5/js/MixedMediaViewer.js]

Vous pouvez utiliser un chemin relatif si la visionneuse est déployée sur l’un des serveurs Adobe Dynamic Media Classic et qu’elle est diffusée à partir du même domaine. Dans le cas contraire, vous spécifiez un chemin d’accès complet à l’un des serveurs Adobe Dynamic Media Classic sur lesquels les visionneuses IS sont installées.

Le chemin relatif ressemble à ce qui suit :

```html {.line-numbers}
<script language="javascript" type="text/javascript" src="/s7viewers/html5/js/MixedMediaViewer.js"></script>
```

>[!NOTE]
>
>Ne référencez que le code JavaScript de la visionneuse principale `include` sur votre page. Ne référencez pas de fichiers JavaScript supplémentaires dans le code de page web qui pourraient être téléchargés par la logique de la visionneuse au moment de l’exécution. En particulier, ne référencez pas directement le SDK HTML5. `Utils.js` bibliothèque chargée par la visionneuse depuis `/s7viewers` chemin d’accès au contexte (appelé SDK consolidé) `include`). La raison en est que l’emplacement de la variable `Utils.js` ou des bibliothèques de visionneuses d’exécution similaires sont entièrement gérées par la logique de la visionneuse et l’emplacement change entre les versions de la visionneuse. Adobe ne conserve pas les anciennes versions de la visionneuse secondaire `includes` sur le serveur.
>
>
>Par conséquent, l’insertion d’une référence directe à tout JavaScript secondaire `include` utilisé par la visionneuse sur la page rompt la fonctionnalité de visionneuse à l’avenir lorsqu’une nouvelle version de produit est déployée.

1. Définition du conteneur DIV.

   Ajoutez un élément DIV vide à la page sur laquelle vous souhaitez que la visionneuse apparaisse. L’ID de l’élément DIV doit être défini, car cet ID est transmis ultérieurement à l’API de visionneuse. La taille du DIV est spécifiée via CSS.

   L’espace réservé DIV est un élément positionné, ce qui signifie que la variable `position` La propriété CSS est définie sur `relative` ou `absolute`.

   Assurez-vous que la fonction Plein écran fonctionne correctement dans Internet Explorer. Vérifiez qu’il n’existe aucun autre élément DOM dont l’ordre d’empilement est plus élevé que votre balise DIV d’espace réservé.

   Voici un exemple d’élément DIV d’espace réservé défini :

   ```html {.line-numbers}
   <div id="s7viewer" style="position:relative"></div> 
   ```

1. Définition de la taille de la visionneuse

   Cette visionneuse affiche des miniatures lorsque vous utilisez des jeux de plusieurs éléments. Sur les systèmes de bureau, les miniatures sont placées sous la vue principale. En même temps, la visionneuse permet la permutation de la ressource principale lors de l’exécution à l’aide de `setAsset()` API. En tant que développeur, vous contrôlez la manière dont la visionneuse gère la zone des miniatures située en bas lorsque la nouvelle ressource ne comporte qu’un seul élément. Il est possible de conserver la taille de la visionneuse externe intacte et de laisser la vue principale augmenter sa hauteur et occuper la zone des miniatures. Vous pouvez également conserver la taille d’affichage principale statique et réduire la zone de la visionneuse externe, ce qui permet au contenu de la page web de se déplacer vers le haut. Ensuite, utilisez l’espace libre de la page qui est laissé dans les miniatures.

   Pour conserver les limites de la visionneuse externe intactes, définissez la taille de `.s7mixedmediaviewer` classe CSS de niveau supérieur en unités absolues. Le dimensionnement en CSS peut être directement placé sur la page de HTML ou dans un fichier CSS de visionneuse personnalisé, puis affecté à un enregistrement de paramètre prédéfini de visionneuse dans Dynamic Media Classic, ou transmis explicitement à l’aide de la commande de style.

   Voir [Personnalisation de la visionneuse de supports variés](../../c-html5-s7-aem-asset-viewers/c-html5-mixedmedia-viewer-about/c-html5-mixedmedia-viewer-customizingviewer/c-html5-mixedmedia-viewer-customizingviewer.md#concept-61b3410f187c4bf3af09ec813c649bf4) pour plus d’informations sur le style de la visionneuse avec CSS.

   Voici un exemple de définition de la taille statique de la visionneuse externe dans une page de HTML :

   ```html {.line-numbers}
   #s7viewer.s7mixedmediaviewer { 
    width: 640px; 
    height: 480px; 
   }
   ```

   Vous pouvez voir le comportement avec une zone de visionneuse externe fixe sur l’exemple de page suivant. Notez que lorsque vous passez d’un ensemble à l’autre, la taille de la visionneuse externe ne change pas :

   [https://experienceleague.adobe.com/tools/dynamic-media-demo/viewers-ref/mixedmedia/MixedMediaViewer-fixed-outer-area.html](https://experienceleague.adobe.com/tools/dynamic-media-demo/viewers-ref/mixedmedia/MixedMediaViewer-fixed-outer-area.html)

   Pour rendre les dimensions d’affichage principales statiques, définissez la taille de la visionneuse en unités absolues pour le contenu `Container` Composant SDK à l’aide de `.s7mixedmediaviewer .s7container` sélecteur CSS ou à l’aide de `stagesize` modifier.

   Voici un exemple de définition de la taille de la visionneuse pour le contenu `Container` Le composant SDK de sorte que la zone d’affichage principale ne modifie pas sa taille lors du changement de ressource :

   ```html {.line-numbers}
   #s7viewer.s7mixedmediaviewer .s7container { 
    width: 640px; 
    height: 480px; 
   }
   ```

   L’exemple de page suivant montre le comportement de la visionneuse avec une taille d’affichage principale fixe. Notez que lorsque vous basculez entre deux ensembles, la vue principale reste statique et le contenu de la page web se déplace verticalement :

   [https://experienceleague.adobe.com/tools/dynamic-media-demo/viewers-ref/mixedmedia/MixedMediaViewer-fixed-main-view.html](https://experienceleague.adobe.com/tools/dynamic-media-demo/viewers-ref/mixedmedia/MixedMediaViewer-fixed-main-view.html)

   Vous pouvez définir la variable `stagesize` modifier soit dans l’enregistrement de paramètre prédéfini de visionneuse dans Dynamic Media Classic, soit le transmettre explicitement avec le code d’initialisation de la visionneuse avec `params` collection. Ou, comme appel API, comme décrit dans la section Référence de commande de cette aide, comme dans l’exemple suivant :

   ```html {.line-numbers}
   mixedMediaViewer.setParam("stagesize", "640,480");
   ```

   Une approche basée sur CSS est recommandée et est utilisée dans cet exemple.

1. Création et initialisation de la visionneuse.

   Une fois les étapes ci-dessus terminées, vous créez une instance de `s7viewers.MixedMediaViewer` , transmettez toutes les informations de configuration à son constructeur et appelez . `init()` sur une instance de visionneuse. Les informations de configuration sont transmises au constructeur sous la forme d’un objet JSON. Au minimum, cet objet doit avoir la propriété `containerId` champ contenant le nom de l’identifiant de conteneur de la visionneuse et imbriqué `params` Objet JSON avec des paramètres de configuration pris en charge par la visionneuse. Dans ce cas, la variable `params` doit comporter au moins l’URL du serveur d’images transmise comme `serverUrl` , l’URL du serveur vidéo transmise comme `videoserverurl` et la ressource initiale en tant que `asset` . L’API d’initialisation basée sur JSON vous permet de créer et de démarrer la visionneuse avec une seule ligne de code.

   Il est important que le conteneur de la visionneuse soit ajouté au modèle DOM afin que le code de la visionneuse puisse trouver l’élément de conteneur en fonction de son identifiant. Certains navigateurs retardent la création du DOM jusqu’à la fin de la page web. Pour une compatibilité maximale, appelez la méthode `init()` juste avant la fermeture `BODY` ou sur le corps `onload()` .

   Dans le même temps, l’élément de conteneur ne doit pas nécessairement faire partie de la mise en page web pour l’instant. Par exemple, il peut être masqué à l’aide de `display:none` style qui lui est affecté. Dans ce cas, la visionneuse retarde son processus d’initialisation jusqu’au moment où la page web ramène l’élément de conteneur à la mise en page. Lorsque cette action se produit, le chargement de la visionneuse reprend automatiquement.

   Voici un exemple de création d’une instance de visionneuse, de transmission des options de configuration minimales nécessaires au constructeur et d’appel de la fonction `init()` . L’exemple suppose que `mixedMediaViewer` est l’instance de visionneuse ; `s7viewer` est le nom de l’espace réservé. `DIV`; [!DNL http://s7d1.scene7.com/is/image/] est l’URL du serveur d’images ; [!DNL http://s7d1.scene7.com/is/content/] est l’URL du serveur vidéo ; et [!DNL Scene7SharedAssets/Mixed_Media_Set_Sample] est la ressource :

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

Le code suivant est un exemple complet d’une page web triviale qui incorpore la visionneuse de médias mixtes avec une taille fixe :

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

## Intégration réactive avec une hauteur libre {#section-056cb574713c4d07be6d07cf3c598839}

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

La page d’exemples suivante illustre d’autres utilisations réelles de l’incorporation en responsive design avec une hauteur illimitée :

[Démonstrations en direct](https://landing.adobe.com/en/na/dynamic-media/ctir-2755/live-demos.html)

[Autre emplacement de démonstration](https://experienceleague.adobe.com/tools/dynamic-media-demo/vlist/vlist.html)

## Intégration flexible de taille avec définition de largeur et de hauteur {#section-0a329016f9414d199039776645c693de}

Si l’incorporation de tailles flexibles avec largeur et hauteur est définie, le style de la page web est différent. Elle fournit les deux tailles au `"holder"` DIV et le centre dans la fenêtre du navigateur. En outre, la page web définit la taille de la variable `HTML` et `BODY` à 100 %.

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

Les autres étapes d’incorporation sont identiques aux étapes utilisées pour l’incorporation en responsive design avec une hauteur illimitée. L’exemple qui en résulte est le suivant :

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

## Incorporation à l’aide d’une API basée sur Setter {#section-af26f0cc2e5140e8a9bfd0c6a841a6d1}

Au lieu d’utiliser l’initialisation basée sur JSON, il est possible d’utiliser une API basée sur un setter et un constructeur sans args. L’utilisation de ce constructeur d’API ne prend aucun paramètre et les paramètres de configuration sont spécifiés à l’aide de `setContainerId()`, `setParam()`, et `setAsset()` méthodes d’API, avec des appels JavaScript distincts.

L’exemple suivant illustre l’utilisation de l’incorporation de tailles fixes avec une API basée sur setter :

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
