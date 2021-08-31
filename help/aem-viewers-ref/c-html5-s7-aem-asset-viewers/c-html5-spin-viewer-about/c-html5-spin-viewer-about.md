---
description: Visionneuse à 360° est une visionneuse d’images qui fournit une vue à 360 degrés de l’image, voire multidimensionnelle, si une visionneuse à 360° appropriée est utilisée. Il comporte des outils de zoom et de rotation, une prise en charge du plein écran et un bouton de fermeture facultatif. Il est conçu pour fonctionner sur les ordinateurs de bureau et les appareils mobiles.
keywords: responsive
solution: Experience Manager
title: Spin
feature: Dynamic Media Classic,Viewers,SDK/API,Spin Sets
role: Developer,User
exl-id: 4c802d42-ea5b-4f28-b6ef-2689aa16839d
source-git-commit: 191d3e7cc4cd370e1e1b6ca5d7e27acd3ded7b6c
workflow-type: tm+mt
source-wordcount: '2130'
ht-degree: 0%

---

# Rotation{#spin}

Visionneuse à 360° est une visionneuse d’images qui fournit une vue à 360 degrés de l’image, voire multidimensionnelle, si une visionneuse à 360° appropriée est utilisée. Il comporte des outils de zoom et de rotation, une prise en charge du plein écran et un bouton de fermeture facultatif. Il est conçu pour fonctionner sur les ordinateurs de bureau et les appareils mobiles.

>[!NOTE]
>
>Les images qui utilisent IR (Image Rendering) ou UGC (User-Generated Content) ne sont pas prises en charge par cette visionneuse.

Type de visionneuse 503.

Voir [Configuration requise et conditions préalables](../../c-system-requirements-and-prerequisites.md#concept-9282e5b777de42cdaf72ef7ebd646842).

## URL de démonstration {#section-e1c3106f5b3e445d9b95be337c2f94e2}

[https://s7d9.scene7.com/s7viewers/html5/SpinViewer.html?asset=Scene7SharedAssets/SpinSet_Sample&amp;stagesize=500,400](https://s7d9.scene7.com/s7viewers/html5/SpinViewer.html?asset=Scene7SharedAssets/SpinSet_Sample&amp;stagesize=500,400)

## Utilisation de la visionneuse à 360° {#section-e6c68406ecdc4de781df182bbd8088b4}

Visionneuse à 360° représente un fichier JavaScript principal et un ensemble de fichiers d’assistance (un seul fichier JavaScript est inclus avec tous les composants du SDK de la visionneuse utilisés par cette visionneuse, ressources et CSS particulière) téléchargés par la visionneuse au moment de l’exécution.

La visionneuse à 360° peut être utilisée en mode pop-up à l’aide d’une page HTML prête pour la production fournie avec les visionneuses IS ou en mode incorporé, où elle est intégrée à la page web cible à l’aide d’une API documentée.

La configuration et l’habillage sont similaires à ceux des autres visionneuses. L’ensemble de l’habillage peut être réalisé via une page CSS personnalisée.

Voir [Référence de commande commune à toutes les visionneuses - Attributs de configuration](../../r-html5-viewer-20-cmdref-configattrib/r-html5-viewer-20-cmdref-configattrib.md#concept-850e0f2c49b949deb7cfbfd330d329bd) et [Référence de commande commune à toutes les visionneuses - URL](../../c-html5-viewer-20-cmdref-url/c-html5-viewer-20-cmdref-url.md#concept-9b337f349b7b406b8c33c7ee96b3e226)

## Interaction avec la visionneuse à 360° {#section-642e66ca38cd4032992840ec6c0b0cd2}

La visionneuse à 360° prend en charge les mouvements tactiles suivants, courants dans d’autres applications mobiles. Lorsque la visionneuse ne peut pas traiter le mouvement de glissement d’un utilisateur, elle transfère l’événement vers le navigateur web pour effectuer un défilement de page natif. Cette fonctionnalité permet à l’utilisateur de parcourir la page même si la visionneuse occupe la majeure partie de la zone d’écran de l’appareil.

<table id="table_ED747CC7178448919C34A4FCD18922D0"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>Mouvement </p> </th> 
   <th colname="col2" class="entry"> <p>Description </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>Double appui </p> </td> 
   <td colname="col2"> <p> Applique un zoom à un niveau jusqu’à ce que l’agrandissement maximal soit atteint. Le geste de double pression suivant réinitialise la visionneuse à l’état d’affichage initial. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Pincement </p> </td> 
   <td colname="col2"> <p>Applique un zoom avant ou arrière à l’image. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Glissement ou clic horizontal </p> </td> 
   <td colname="col2"> <p> Si l’image est à l’état réinitialisé, elle passe sur la visionneuse horizontalement. </p> <p> Si l’image est agrandie, elle se déplace horizontalement. Si l’image est déplacée vers le bord de la vue et qu’un glissement est toujours effectué dans cette direction, le mouvement effectue un défilement de page natif. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Glissement ou clic vertical </p> </td> 
   <td colname="col2"> <p> Si l’image est à l’état réinitialisé, l’angle d’affichage vertical est modifié en cas d’utilisation d’une visionneuse à 360° multidimensionnelle. Dans une visionneuse à 360° unidimensionnelle, le mouvement effectue un défilement de page natif. Ou, lorsqu’une visionneuse à 360° multidimensionnelle se trouve sur le dernier ou le premier axe de sorte que le glissement vertical n’entraîne pas de changement de l’angle d’affichage vertical, le mouvement effectue également un défilement de page natif. </p> <p> Si l’image est agrandie, elle bouge l’image verticalement. Si l’image est déplacée vers le bord de la vue et qu’un glissement est toujours effectué dans cette direction, le mouvement effectue un défilement de page natif. </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>La visionneuse prend également en charge les entrées tactile et de souris sur les appareils Windows dotés d’un écran tactile et d’une souris. Toutefois, cette prise en charge est limitée aux navigateurs Chrome, Internet Explorer 11 et Edge uniquement.

Cette visionneuse est entièrement accessible au clavier.

Voir [Accessibilité clavier et navigation](../../c-keyboard-accessibility.md#topic-f5650e9493404e55a3627c8d1366b861).

## Incorporation de la visionneuse à 360° {#section-6bb5d3c502544ad18a58eafe12a13435}

Le comportement de la visionneuse varie en fonction des pages web. Il arrive qu’une page web fournisse un lien qui, en cliquant dessus, ouvre la visionneuse dans une fenêtre de navigateur distincte. Dans d’autres cas, il est nécessaire d’incorporer le droit de visionneuse dans la page d’hébergement. Dans ce cas, la page web peut avoir une mise en page statique ou utiliser une conception réactive qui s’affiche différemment sur différents appareils ou pour différentes tailles de fenêtre de navigateur. Pour répondre à ces besoins, la visionneuse prend en charge trois modes de fonctionnement Principaux : pop-up, incorporation de taille fixe et incorporation de conceptions réactives.

**A propos du mode pop-up**

En mode contextuel, la visionneuse s’ouvre dans une fenêtre ou un onglet de navigateur Web distinct. Il prend toute la zone de la fenêtre du navigateur et s’ajuste au cas où le navigateur serait redimensionné ou si l’orientation d’un appareil mobile est modifiée.

Le mode pop-up est le plus courant pour les appareils mobiles. La page web charge la visionneuse à l’aide de l’appel JavaScript `window.open()`, de l’élément HTML `A` correctement configuré ou de toute autre méthode appropriée.

Il est recommandé d’utiliser une page HTML d’usine pour le mode de fonctionnement de la fenêtre contextuelle. Dans ce cas, il est appelé [!DNL SpinViewer.html] et se trouve dans le sous-dossier [!DNL html5/] de votre déploiement IS-Viewers standard :

[!DNL <s7viewers_root>/html5/SpinViewer.html]

Vous pouvez effectuer une personnalisation visuelle en appliquant une page CSS personnalisée.

Voici un exemple de code HTML qui ouvre la visionneuse dans une nouvelle fenêtre :

```
<a 
href="https://s7d1.scene7.com/s7viewers/html5/SpinViewer.html?asset=Scene7SharedAssets/SpinSet_Sample&stagesize=500,400" 
target="_blank">Open popup viewer</a>
```

**À propos du mode d’incorporation à taille fixe et du mode d’incorporation de responsive design**

En mode incorporé, la visionneuse est ajoutée à la page web existante, qui peut déjà comporter du contenu client non lié à la visionneuse. Normalement, la visionneuse occupe uniquement une partie de l’espace d’une page web.

Les cas d’utilisation Principaux sont les pages web orientées vers les ordinateurs de bureau ou les tablettes, ainsi que les pages de conception réactive qui ajustent automatiquement la mise en page en fonction du type d’appareil.

L’incorporation des tailles fixes est utilisée lorsque la visionneuse ne modifie pas sa taille après le chargement initial. Cette action est la meilleure solution pour les pages web avec une disposition statique.

L’incorporation des conceptions réactives suppose que la visionneuse doit être redimensionnée au moment de l’exécution en réponse au changement de taille de son conteneur `DIV`. Le cas d’utilisation le plus courant consiste à ajouter une visionneuse à une page web qui utilise une mise en page flexible.

En mode d’incorporation en responsive design, la visionneuse se comporte différemment selon la façon dont la page web dimensionne son conteneur `DIV`. Si la page web définit uniquement la largeur du conteneur `DIV`, en ne limitant pas sa hauteur, la visionneuse sélectionne automatiquement sa hauteur en fonction des proportions de la ressource utilisée. Cette fonctionnalité permet de s’assurer que la ressource s’intègre parfaitement dans la vue sans marge intérieure sur les côtés. Ce cas d’utilisation est le plus courant pour les pages web qui utilisent des structures de mise en page en responsive design comme Bootstrap ou Foundation.

Dans le cas contraire, si la page web définit à la fois la largeur et la hauteur du conteneur de la visionneuse `DIV`, la visionneuse remplit uniquement cette zone et suit la taille fournie par la mise en page web. Un bon exemple peut être l’incorporation de la visionneuse dans une superposition modale, où la superposition est dimensionnée en fonction de la taille de la fenêtre du navigateur web.

**Incorporation de taille fixe**

Pour ajouter la visionneuse à 360° à une page web, procédez comme suit :

1. Ajout du fichier JavaScript de la visionneuse à votre page web.
1. Définition du conteneur `DIV`.
1. Définition de la taille de la visionneuse.
1. Création et initialisation de la visionneuse.

1. Ajout du fichier JavaScript de la visionneuse à votre page web.

   Pour créer une visionneuse, vous devez ajouter une balise de script dans l’en-tête HTML. Avant de pouvoir utiliser l’API de visionneuse, veillez à inclure `SpinViewer.js`. `SpinViewer.js` se trouve sous le  [!DNL html5/js/] sous-dossier de votre déploiement IS-Viewers standard :

   `<s7viewers_root>/html5/js/SpinViewer.js`

   Vous pouvez utiliser un chemin relatif si la visionneuse est déployée sur l’un des serveurs Dynamic Media Adobe et qu’elle est diffusée à partir du même domaine. Dans le cas contraire, vous spécifiez un chemin d’accès complet à l’un des serveurs Dynamic Media Adobe sur lesquels les visionneuses IS sont installées.

   Le chemin relatif ressemble à ce qui suit :

   ```
    <script language="javascript" type="text/javascript" src="/s7viewers/html5/js/SpinViewer.js"></script>
   ```

   >[!NOTE]
   >
   >Ne référencez que le fichier JavaScript de la visionneuse principale `include` sur votre page. Ne référencez pas de fichiers JavaScript supplémentaires dans le code de page web qui pourraient être téléchargés par la logique de la visionneuse au moment de l’exécution. En particulier, ne référencez pas directement la bibliothèque `Utils.js` SDK HTML5 chargée par la visionneuse à partir du chemin de contexte `/s7viewers` (appelé SDK consolidé `include`). Cela est dû au fait que l’emplacement des bibliothèques de visionneuses `Utils.js` ou d’exécution similaires est entièrement géré par la logique de la visionneuse et que l’emplacement change entre les versions de la visionneuse. Adobe ne conserve pas les anciennes versions de la visionneuse secondaire `includes` sur le serveur.
   >
   >
   >Par conséquent, l’insertion d’une référence directe à tout JavaScript secondaire `include` utilisé par la visionneuse sur la page rompt la fonctionnalité de visionneuse à l’avenir lorsqu’une nouvelle version de produit est déployée.

1. Définition du conteneur DIV.

   Ajoutez un élément DIV vide à la page sur laquelle vous souhaitez que la visionneuse apparaisse. L’ID de l’élément DIV doit être défini, car cet ID est transmis ultérieurement à l’API de visionneuse.

   L’espace réservé DIV est un élément positionné, ce qui signifie que la propriété CSS `position` est définie sur `relative` ou `absolute`.

   Voici un exemple d’élément DIV d’espace réservé défini :

   ```
   <div id="s7viewer" style="position:relative"></div>
   ```

1. Définition de la taille de la visionneuse

   Vous pouvez définir la taille statique de la visionneuse en la déclarant pour la classe CSS de niveau supérieur `.s7spinviewer` en unités absolues ou en utilisant le modificateur `stagesize`.

   Vous pouvez placer le dimensionnement dans CSS directement sur la page HTML ou dans un fichier CSS de visionneuse personnalisé. Il est ensuite affecté à un enregistrement de paramètre prédéfini de visionneuse dans Dynamic Media Classic ou transmis explicitement à l’aide d’une commande de style.

   Voir [Personnalisation de la visionneuse à 360°](../../c-html5-s7-aem-asset-viewers/c-html5-spin-viewer-about/c-html5-spin-viewer-customizingviewer/c-html5-spin-viewer-customizingviewer.md#concept-464f3bfa55764bc09c92d8c7480b0b55) pour plus d’informations sur le style de la visionneuse avec CSS.

   Voici un exemple de définition de la taille d’une visionneuse statique dans une page HTML :

   ```
   #s7viewer.s7spinviewer { 
    width: 640px; 
    height: 480px; 
   }
   ```

   Vous pouvez définir le modificateur `stagesize` dans l’enregistrement de paramètre prédéfini de visionneuse dans Dynamic Media Classic. Vous pouvez également le transmettre explicitement avec le code d’initialisation de la visionneuse avec la collection `params` ou sous la forme d’un appel API, comme décrit dans la section Référence de commande, comme suit :

   ```
    spinViewer.setParam("stagesize", 
   "640,480");
   ```

   Une approche basée sur CSS est recommandée et est utilisée dans cet exemple.

1. Création et initialisation de la visionneuse.

   Une fois les étapes ci-dessus terminées, vous créez une instance de la classe `s7viewers.SpinViewer`, transmettez toutes les informations de configuration à son constructeur et appelez la méthode `init()` sur une instance de visionneuse. Les informations de configuration sont transmises au constructeur sous la forme d’un objet JSON. Au minimum, ce champ d’objet contient `containerId` le nom de l’ID de conteneur de la visionneuse et l’objet JSON `params` imbriqué avec les paramètres de configuration pris en charge par la visionneuse. Dans ce cas d’objet `params`, l’URL de diffusion d’images doit au moins être transmise comme propriété `serverUrl` et la ressource initiale comme paramètre `asset`. L’API d’initialisation basée sur JSON vous permet de créer et de démarrer la visionneuse avec une seule ligne de code.

   Il est important que le conteneur de la visionneuse soit ajouté au modèle DOM afin que le code de la visionneuse puisse trouver l’élément de conteneur en fonction de son identifiant. Certains navigateurs retardent la création du DOM jusqu’à la fin de la page web. Pour bénéficier d’une compatibilité maximale, appelez la méthode `init()` juste avant la balise `BODY` de fermeture ou sur l’événement `onload()` body .

   Dans le même temps, l’élément de conteneur ne doit pas nécessairement faire partie de la mise en page de la page web pour l’instant. Par exemple, il peut être masqué à l’aide du style `display:none` qui lui est affecté. Dans ce cas, la visionneuse retarde son processus d’initialisation jusqu’au moment où la page web ramène l’élément de conteneur à la mise en page. Lorsque cette action se produit, le chargement de la visionneuse reprend automatiquement.

   Voici un exemple de création d’une instance de visionneuse, en transmettant les options de configuration minimales nécessaires au constructeur et en appelant la méthode `init()` . L’exemple suppose que `spinViewer` est l’instance de visionneuse, `s7viewer` est le nom de l’espace réservé `DIV`, [!DNL http://s7d1.scene7.com/is/image/] est l’URL de diffusion d’images et [!DNL Scene7SharedAssets/SpinSet_Sample] est la ressource.

   ```
   <script type="text/javascript"> 
   var spinViewer = new s7viewers.SpinViewer({ 
    "containerId":"s7viewer", 
   "params":{ 
    "asset":"Scene7SharedAssets/SpinSet_Sample", 
    "serverurl":"http://s7d1.scene7.com/is/image/" 
   } 
   }).init(); 
   </script>
   ```

   Le code suivant est un exemple complet d’une page web triviale qui incorpore la visionneuse à 360° avec une taille fixe :

   ```
   <!DOCTYPE html> 
   <html> 
   <head> 
   <script type="text/javascript" src="http://s7d1.scene7.com/s7viewers/html5/js/SpinViewer.js"></script> 
   <style type="text/css"> 
   #s7viewer.s7spinviewer { 
    width: 640px; 
    height: 480px; 
   } 
   </style> 
   </head> 
   <body> 
   <div id="s7viewer" style="position:relative"></div> 
   <script type="text/javascript"> 
   var spinViewer = new s7viewers.SpinViewer({ 
    "containerId":"s7viewer", 
   "params":{ 
    "asset":"Scene7SharedAssets/SpinSet_Sample", 
    "serverurl":"http://s7d1.scene7.com/is/image/" 
   } 
   }).init(); 
   </script> 
   </body> 
   </html>
   ```

**Intégration de conception réactive avec une hauteur libre**

Avec l’incorporation de responsive design, la page web dispose normalement d’une sorte de disposition flexible qui détermine la taille d’exécution du conteneur de la visionneuse `DIV`. Pour les besoins de cet exemple, supposons que la page web permette au conteneur de la visionneuse `DIV` de prendre 40 % de la taille de la fenêtre du navigateur web, en ne restreignant pas sa hauteur. Le code HTML de page web obtenu ressemble à ce qui suit :

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

L’ajout de la visionneuse à une telle page est similaire à l’incorporation d’une taille fixe, la seule différence étant que vous n’avez pas besoin de définir explicitement la taille de la visionneuse.

1. Ajout du fichier JavaScript de la visionneuse à votre page web.
1. Définition du conteneur DIV.
1. Création et initialisation de la visionneuse.

Toutes les étapes ci-dessus sont identiques à l’incorporation à taille fixe. Ajoutez le conteneur `DIV` au &quot; détenteur&quot; `DIV` existant. Le code suivant est un exemple complet. Vous pouvez voir comment la taille de la visionneuse change lorsque le navigateur est redimensionné et comment le rapport d’aspect de la visionneuse correspond à la ressource.

```
<!DOCTYPE html> 
<html> 
<head> 
<script type="text/javascript" src="http://s7d1.scene7.com/s7viewers/html5/js/SpinViewer.js"></script> 
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
var spinViewer = new s7viewers.SpinViewer({ 
 "containerId":"s7viewer", 
"params":{ 
 "asset":"Scene7SharedAssets/SpinSet_Sample", 
 "serverurl":"http://s7d1.scene7.com/is/image/" 
} 
}).init(); 
</script> 
</body> 
</html>
```

La page d’exemples suivante illustre d’autres cas pratiques d’incorporation de conceptions réactives avec une hauteur illimitée :

[Démonstrations en direct](https://landing.adobe.com/en/na/dynamic-media/ctir-2755/live-demos.html)

[Autre emplacement de démonstration](https://experienceleague.adobe.com/tools/dynamic-media-demo/vlist/vlist.html)

**Intégration flexible de taille avec définition de largeur et de hauteur**

Si l’incorporation de tailles flexibles avec largeur et hauteur est définie, le style de la page web est différent. En d’autres termes, il fournit les deux tailles au &quot;détenteur&quot; `DIV` et le centre dans la fenêtre du navigateur. En outre, la page web définit la taille de l’élément `HTML` et `BODY` sur 100 % :

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

Les étapes d’incorporation restantes sont identiques à l’incorporation en responsive design avec une hauteur libre. L’exemple qui en résulte est le suivant :

```
<!DOCTYPE html> 
<html> 
<head> 
<script type="text/javascript" src="http://s7d1.scene7.com/s7viewers/html5/js/SpinViewer.js"></script> 
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
var spinViewer = new s7viewers.SpinViewer({ 
 "containerId":"s7viewer", 
"params":{ 
 "asset":"Scene7SharedAssets/SpinSet_Sample", 
 "serverurl":"http://s7d1.scene7.com/is/image/" 
} 
}).init(); 
</script> 
</body> 
</html>
```

**Incorporation à l’aide d’une API basée sur Setter**

Au lieu d’utiliser l’initialisation basée sur JSON, il est possible d’utiliser une API basée sur un setter et un constructeur sans argument. Avec cette API, le constructeur ne prend aucun paramètre et les paramètres de configuration sont spécifiés à l’aide des méthodes d’API `setContainerId()`, `setParam()` et `setAsset()` avec des appels JavaScript distincts.

L’exemple suivant illustre l’incorporation de tailles fixes avec une API basée sur setter :

```
<!DOCTYPE html> 
<html> 
<head> 
<script type="text/javascript" src="http://s7d1.scene7.com/s7viewers/html5/js/SpinViewer.js"></script> 
<style type="text/css"> 
#s7viewer.s7spinviewer { 
 width: 640px; 
 height: 480px; 
} 
</style> 
</head> 
<body> 
<div id="s7viewer" style="position:relative"></div> 
<script type="text/javascript"> 
var spinViewer = new s7viewers.SpinViewer(); 
spinViewer.setContainerId("s7viewer"); 
spinViewer.setParam("serverurl", "http://s7d1.scene7.com/is/image/"); 
spinViewer.setAsset("Scene7SharedAssets/SpinSet_Sample"); 
spinViewer.init(); 
</script> 
</body> 
</html>
```
