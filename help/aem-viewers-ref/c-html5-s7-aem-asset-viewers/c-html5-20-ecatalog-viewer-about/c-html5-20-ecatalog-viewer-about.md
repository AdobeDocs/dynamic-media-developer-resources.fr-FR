---
description: Visionneuse de catalogue électronique est une visionneuse de catalogue qui affiche les brochures électroniques d’une diffusion ou page par page. Le catalogue électronique permet aux utilisateurs de parcourir le catalogue à l’aide d’éléments d’interface utilisateur supplémentaires ou de modes de miniatures dédiés. Les utilisateurs peuvent également zoomer sur chaque page pour obtenir des détails plus détaillés.
keywords: responsive
solution: Experience Manager
title: Catalogue électronique
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog
role: Developer,User
exl-id: 8e243fa5-e375-41ce-8b49-2571023130c1
source-git-commit: 191d3e7cc4cd370e1e1b6ca5d7e27acd3ded7b6c
workflow-type: tm+mt
source-wordcount: '2164'
ht-degree: 0%

---

# Catalogue électronique{#ecatalog}

Visionneuse de catalogue électronique est une visionneuse de catalogue qui affiche les brochures électroniques d’une diffusion ou page par page. Le catalogue électronique permet aux utilisateurs de parcourir le catalogue à l’aide d’éléments d’interface utilisateur supplémentaires ou de modes de miniatures dédiés. Les utilisateurs peuvent également zoomer sur chaque page pour obtenir des détails plus détaillés.

>[!NOTE]
>
>Les images qui utilisent le rendu d’image (IR) ou le contenu généré par l’utilisateur (UGC) ne sont pas prises en charge par cette visionneuse.

Type de visionneuse 507.

Voir [Configuration requise et conditions préalables](../../c-system-requirements-and-prerequisites.md#concept-9282e5b777de42cdaf72ef7ebd646842).

Cette visionneuse fonctionne avec des catalogues électroniques et prend en charge les zones cliquables et les outils de partage sur les réseaux sociaux en option. Il contient des outils de zoom, des outils de navigation de catalogue, la prise en charge du plein écran, des miniatures et un bouton de fermeture facultatif. La visionneuse prend également en charge les outils de partage sur les réseaux sociaux, l’impression, le téléchargement et les favoris. Il est conçu pour fonctionner sur les ordinateurs de bureau et les appareils mobiles.

## URL de démonstration {#section-e1c3106f5b3e445d9b95be337c2f94e2}

[https://s7d1.scene7.com/s7viewers/html5/eCatalogViewer.html?asset=Viewers/Pluralist](https://s7d1.scene7.com/s7viewers/html5/eCatalogViewer.html?asset=Viewers/Pluralist)

## Utilisation de la visionneuse de catalogue électronique {#section-e6c68406ecdc4de781df182bbd8088b4}

La visionneuse de catalogue électronique représente un fichier JavaScript principal et un ensemble de fichiers d’assistance (un seul script JavaScript comprenant tous les composants du SDK de la visionneuse utilisés par cette visionneuse, ressources et CSS particulière) téléchargés par la visionneuse au moment de l’exécution.

Vous pouvez utiliser la visionneuse de catalogue électronique en mode pop-up à l’aide d’une page HTML prête pour la production fournie avec les visionneuses IS ou en mode incorporé, où elle est intégrée à la page web cible à l’aide d’une API documentée.

La configuration et l’habillage sont similaires à ceux des autres visionneuses. L’habillage est effectué au moyen d’une feuille CSS personnalisée.

Voir [Référence de commande commune à toutes les visionneuses - Attributs de configuration](../../r-html5-viewer-20-cmdref-configattrib/r-html5-viewer-20-cmdref-configattrib.md#concept-850e0f2c49b949deb7cfbfd330d329bd) et [Référence de commande commune à toutes les visionneuses - URL](../../c-html5-viewer-20-cmdref-url/c-html5-viewer-20-cmdref-url.md#concept-9b337f349b7b406b8c33c7ee96b3e226)

## Interaction avec la visionneuse de catalogue électronique {#section-642e66ca38cd4032992840ec6c0b0cd2}

La visionneuse de catalogue électronique prend en charge les mouvements tactiles suivants, courants dans d’autres applications mobiles.

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
   <td colname="col2"> <p> Sélectionne une nouvelle miniature dans les échantillons. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Double appui </p> </td> 
   <td colname="col2"> <p> Applique un zoom à un niveau jusqu’à ce que l’agrandissement maximal soit atteint. Le geste de double pression suivant réinitialise la visionneuse à l’état d’affichage initial. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Pincement </p> </td> 
   <td colname="col2"> <p>Applique un zoom avant ou arrière. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Glissement ou clic horizontal </p> </td> 
   <td colname="col2"> <p> Fait défiler la liste des pages du catalogue si une transition de cadre de diapositive est utilisée. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Glissement ou clic vertical </p> </td> 
   <td colname="col2"> <p>Lorsque l’image est réinitialisée, elle effectue un défilement de page natif. </p> <p>Lorsque les miniatures sont principales, elles font défiler la liste des miniatures. </p> </td> 
  </tr> 
 </tbody> 
</table>

Il est possible d’activer un effet d’animation de type Symétrie de page réaliste pour naviguer entre les pages du catalogue. Dans ce cas, l’utilisateur peut maintenir le bouton de la souris enfoncé et faire glisser un coin de page et retourner la page.

Cette visionneuse prend également en charge les entrées tactile et de souris sur les périphériques Windows dotés d’un écran tactile et d’une souris. Toutefois, cette prise en charge est limitée aux navigateurs Chrome, Internet Explorer 11 et Edge uniquement.

Cette visionneuse est entièrement accessible via le clavier, comme décrit dans [Accessibilité clavier et navigation](../../c-keyboard-accessibility.md#topic-f5650e9493404e55a3627c8d1366b861).

## Outils de partage sur les médias sociaux avec la visionneuse de catalogue électronique {#section-eb575084a99647c3a9591f439f40b412}

La visionneuse de catalogue électronique prend en charge les outils de partage sur les réseaux sociaux. Ils sont disponibles sous la forme d’un bouton dans la barre de contrôle principale, qui se transforme en barre d’outils de partage lorsqu’un utilisateur clique ou appuie dessus.

La barre d’outils de partage contient des icônes pour chaque type de canal de partage pris en charge, notamment Facebook, Twitter, le partage de courrier électronique, le partage de code incorporé et le partage de lien. Lorsque des outils de partage de courrier électronique, d’intégration de partage ou de lien sont activés, la visionneuse affiche une boîte de dialogue modale avec un formulaire de saisie de données correspondant. Lorsque Facebook ou Twitter est appelé, la visionneuse redirige l’utilisateur vers une boîte de dialogue de partage standard à partir d’un service social. Les outils de partage ne sont pas disponibles en mode plein écran en raison des restrictions de sécurité du navigateur web.

## Incorporation de la visionneuse de catalogue électronique {#section-6bb5d3c502544ad18a58eafe12a13435}

Le comportement de la visionneuse varie en fonction des pages web. Il arrive qu’une page web fournisse un lien qui, en cliquant dessus, ouvre la visionneuse dans une fenêtre de navigateur distincte. Dans d’autres cas, il est nécessaire d’incorporer le droit de visionneuse dans la page d’hébergement. Dans ce cas, la page web peut avoir une mise en page statique ou utiliser une conception réactive qui s’affiche différemment sur différents appareils ou pour différentes tailles de fenêtre de navigateur. Pour répondre à ces besoins, la visionneuse prend en charge trois modes de fonctionnement Principaux : pop-up, incorporation de taille fixe et incorporation de conceptions réactives.

**A propos du mode pop-up**

En mode contextuel, la visionneuse s’ouvre dans une fenêtre ou un onglet de navigateur Web distinct. Il prend toute la zone de la fenêtre du navigateur et s’ajuste au cas où le navigateur serait redimensionné ou si l’orientation d’un appareil mobile est modifiée.

Le mode pop-up est le plus courant pour les appareils mobiles. La page web charge la visionneuse à l’aide de l’appel JavaScript `window.open()`, de l’élément HTML `A` correctement configuré ou de toute autre méthode appropriée.

Il est recommandé d’utiliser une page HTML d’usine pour le mode de fonctionnement de la fenêtre contextuelle. Dans ce cas, il est appelé [!DNL eCatalogViewer.html] et se trouve dans le sous-dossier [!DNL html5/] de votre déploiement IS-Viewers standard :

[!DNL <s7viewers_root>/html5/eCatalogViewer.html]

Vous pouvez effectuer une personnalisation visuelle en appliquant une page CSS personnalisée.

Voici un exemple de code HTML qui ouvre la visionneuse dans une nouvelle fenêtre :

```
<a href="https://s7d1.scene7.com/s7viewers/html5/eCatalogViewer.html?asset=Viewers/Pluralist" target="_blank">Open popup viewer</a>
```

**À propos du mode d’incorporation à taille fixe et du mode d’incorporation de responsive design**

En mode incorporé, la visionneuse est ajoutée à la page web existante, qui peut déjà comporter du contenu client non lié à la visionneuse. Normalement, la visionneuse occupe uniquement une partie de l’espace d’une page web.

Les cas d’utilisation Principaux sont les pages web orientées vers les ordinateurs de bureau ou les tablettes, ainsi que les pages réactives qui ajustent automatiquement la mise en page en fonction du type d’appareil.

L’incorporation des tailles fixes est utilisée lorsque la visionneuse ne modifie pas sa taille après le chargement initial. Il s’agit de la meilleure solution pour les pages web ayant une disposition statique.

L’incorporation des conceptions réactives suppose que la visionneuse doit peut-être redimensionner au moment de l’exécution en réponse au changement de taille de son conteneur `DIV`. Le cas d’utilisation le plus courant consiste à ajouter une visionneuse à une page web qui utilise une mise en page flexible.

En mode d’incorporation en responsive design, la visionneuse se comporte différemment selon la façon dont la page web dimensionne son conteneur `DIV`. Si la page web définit uniquement la largeur du conteneur `DIV`, en ne limitant pas sa hauteur, la visionneuse sélectionne automatiquement sa hauteur en fonction des proportions de la ressource utilisée. Cette fonctionnalité permet de s’assurer que la ressource s’intègre parfaitement dans la vue sans marge intérieure sur les côtés. Ce cas d’utilisation est le plus courant pour les pages web qui utilisent des structures de mise en page réactive telles que Bootstrap, Foundation, etc.

Dans le cas contraire, si la page web définit à la fois la largeur et la hauteur du conteneur de la visionneuse `DIV`, la visionneuse remplit uniquement cette zone et suit la taille fournie par la mise en page web. Un bon exemple consiste à incorporer la visionneuse dans une superposition modale, où la superposition est dimensionnée en fonction de la taille de la fenêtre du navigateur web.

**Incorporation de taille fixe**

Pour ajouter la visionneuse à une page web, procédez comme suit :

1. Ajout du fichier JavaScript de la visionneuse à votre page web.
1. Définition du conteneur DIV.
1. Définition de la taille de la visionneuse.
1. Création et initialisation de la visionneuse.

1. Ajout du fichier JavaScript de la visionneuse à votre page web.

   Pour créer une visionneuse, vous devez ajouter une balise de script dans l’en-tête HTML. Avant d’utiliser l’API de visionneuse, veillez à inclure [!DNL eCatalogViewer.js]. Le fichier [!DNL eCatalogViewer.js] se trouve sous le sous-dossier [!DNL html5/js/] de votre déploiement IS-Viewers standard :

[!DNL <s7viewers_root>/html5/js/eCatalogViewer.js]

Vous pouvez utiliser un chemin relatif si la visionneuse est déployée sur l’un des serveurs Dynamic Media Classic Adobe et qu’elle est diffusée à partir du même domaine. Dans le cas contraire, vous spécifiez un chemin d’accès complet à l’un des serveurs Dynamic Media Classic Adobe sur lesquels les visionneuses IS sont installées.

Le chemin relatif ressemble à ce qui suit :

```
<script language="javascript" type="text/javascript" src="/s7viewers/html5/js/eCatalogViewer.js"></script>
```

>[!NOTE]
>
>Vous ne devez référencer que le fichier JavaScript de la visionneuse principale `include` sur votre page. Vous ne devez pas référencer de fichiers JavaScript supplémentaires dans le code de page web qui peuvent être téléchargés selon la logique de la visionneuse au moment de l’exécution. En particulier, ne référencez pas directement la bibliothèque `Utils.js` SDK HTML5 chargée par la visionneuse à partir du chemin de contexte `/s7viewers` (appelé SDK consolidé `include`). Cela est dû au fait que l’emplacement des bibliothèques de visionneuses `Utils.js` ou d’exécution similaires est entièrement géré par la logique de la visionneuse et que l’emplacement change entre les versions de la visionneuse. Adobe ne conserve pas les anciennes versions de la visionneuse secondaire `includes` sur le serveur.
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

   Vous pouvez définir la taille statique de la visionneuse en la déclarant pour la classe CSS de niveau supérieur `.s7ecatalogviewer` en unités absolues ou en utilisant le modificateur `stagesize`.

   Vous pouvez placer le dimensionnement dans CSS directement sur la page HTML, ou dans un fichier CSS de visionneuse personnalisé, qui est ensuite affecté à un enregistrement de paramètre prédéfini de visionneuse dans Dynamic Media Classic, ou transmis explicitement à l’aide d’une commande de style.

   Voir [Personnalisation de la visionneuse de catalogue électronique](../../c-html5-s7-aem-asset-viewers/c-html5-20-ecatalog-viewer-about/c-html5-20-ecatalog-viewer-customizingviewer/c-html5-20-ecatalog-viewer-customizingviewer.md#concept-73a8546acdb444a387c49969ceca57d0) pour plus d’informations sur le style de la visionneuse avec CSS.

   Voici un exemple de définition de la taille d’une visionneuse statique dans une page HTML :

   ```
   #s7viewer.s7ecatalogviewer { 
    width: 640px; 
    height: 480px; 
   }
   ```

   Vous pouvez définir le modificateur `stagesize` dans l’enregistrement de paramètre prédéfini de visionneuse dans Dynamic Media Classic, ou le transmettre explicitement avec le code d’initialisation de la visionneuse avec la collection `params`, ou en tant qu’appel API comme décrit dans la section Référence de commande , comme suit :

   ```
   eCatalogViewer.setParam("stagesize", 
   "640,480");
   ```

1. Initialisation de la visionneuse.

   Une fois les étapes ci-dessus terminées, vous créez une instance de la classe `s7viewers.eCatalogViewer`, transmettez toutes les informations de configuration à son constructeur et appelez la méthode `init()` sur une instance de visionneuse. Les informations de configuration sont transmises au constructeur sous la forme d’un objet JSON. Au minimum, cet objet possède le champ `containerId` qui contient le nom de l’ID de conteneur de la visionneuse et l’objet JSON `params` imbriqué avec les paramètres de configuration pris en charge par la visionneuse. Dans ce cas, l’objet `params` doit avoir au moins la propriété URL de diffusion d’images transmise en tant que propriété `serverUrl` et la ressource initiale en tant que paramètre `asset`. L’API d’initialisation basée sur JSON vous permet de créer et de démarrer la visionneuse avec une seule ligne de code.

   Il est important que le conteneur de la visionneuse soit ajouté au modèle DOM afin que le code de la visionneuse puisse trouver l’élément de conteneur en fonction de son identifiant. Certains navigateurs retardent la création du DOM jusqu’à la fin de la page web. Toutefois, pour bénéficier d’une compatibilité maximale, appelez la méthode `init()` juste avant la balise de fermeture `BODY` ou sur l’événement `onload()` body .

   De même, l’élément de conteneur ne doit pas nécessairement faire partie de la mise en page de la page web pour l’instant. Par exemple, il peut être masqué à l’aide du style `display:none` qui lui est affecté. Dans ce cas, la visionneuse retarde son processus d’initialisation jusqu’au moment où la page web ramène l’élément de conteneur à la mise en page. Dans ce cas, le chargement de la visionneuse reprend automatiquement.

   Voici un exemple de création d’une instance de visionneuse, de transmission des options de configuration minimales nécessaires au constructeur et d’appel de la méthode `init()` . L’exemple suppose que `eCatalogViewer` est l’instance de visionneuse ; `s7viewer` est le nom de l’espace réservé `DIV` ; `https://s7d1.scene7.com/is/image/` est l’URL du serveur d’images et `Viewers/Pluralist` est la ressource :

   ```
   <script type="text/javascript"> 
   var eCatalogViewer = new s7viewers.eCatalogViewer({ 
    "containerId":"s7viewer", 
   "params":{ 
    "asset":"Viewers/Pluralist", 
    "serverurl":"https://s7d1.scene7.com/is/image/" 
   } 
   }).init(); 
   </script>
   ```

   Le code suivant est un exemple complet d’une page web triviale qui incorpore la visionneuse de catalogue électronique à une taille fixe :

   ```
   <!DOCTYPE html> 
   <html> 
   <head> 
   <script type="text/javascript" src="https://s7d1.scene7.com/s7viewers/html5/js/eCatalogViewer.js"></script> 
   <style type="text/css"> 
   #s7viewer.s7ecatalogviewer { 
    width: 640px; 
    height: 480px; 
   } 
   </style> 
   </head> 
   <body> 
   <div id="s7viewer" style="position:relative"></div> 
   <script type="text/javascript"> 
   var eCatalogViewer = new s7viewers.eCatalogViewer({ 
    "containerId":"s7viewer", 
   "params":{ 
    "asset":"Viewers/Pluralist", 
    "serverurl":"https://s7d1.scene7.com/is/image/" 
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
<script type="text/javascript" src="https://s7d1.scene7.com/s7viewers/html5/js/eCatalogViewer.js"></script> 
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
var eCatalogViewer = new s7viewers.eCatalogViewer({ 
 "containerId":"s7viewer", 
"params":{ 
 "asset":"Viewers/Pluralist", 
 "serverurl":"https://s7d1.scene7.com/is/image/" 
} 
}).init(); 
</script> 
</body> 
</html>
```

La page d’exemples suivante illustre d’autres cas pratiques d’incorporation de conceptions réactives avec une hauteur illimitée :

[Démonstrations en direct](https://landing.adobe.com/en/na/dynamic-media/ctir-2755/live-demos.html)

**Intégration flexible de taille avec définition de largeur et de hauteur**

Dans le cas d’une incorporation à taille flexible avec des valeurs de largeur et de hauteur définies, le style de la page web est différent. En d’autres termes, il fournit les deux tailles au &quot;détenteur&quot; `DIV` et le centre dans la fenêtre du navigateur. En outre, la page web définit la taille de l’élément `HTML` et `BODY` sur 100 % :

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
<script type="text/javascript" src="https://s7d1.scene7.com/s7viewers/html5/js/eCatalogViewer.js"></script> 
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
var eCatalogViewer = new s7viewers.eCatalogViewer({ 
 "containerId":"s7viewer", 
"params":{ 
 "asset":"Viewers/Pluralist", 
 "serverurl":"https://s7d1.scene7.com/is/image/" 
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
<script type="text/javascript" src="https://s7d1.scene7.com/s7viewers/html5/js/eCatalogViewer.js"></script> 
<style type="text/css"> 
#s7viewer.s7ecatalogviewer { 
 width: 640px; 
 height: 480px; 
} 
</style> 
</head> 
<body> 
<div id="s7viewer" style="position:relative"></div> 
<script type="text/javascript"> 
var eCatalogViewer = new s7viewers.eCatalogViewer(); 
eCatalogViewer.setContainerId("s7viewer"); 
eCatalogViewer.setParam("serverurl", "https://s7d1.scene7.com/is/image/"); 
eCatalogViewer.setAsset("Viewers/Pluralist"); 
eCatalogViewer.init(); 
</script> 
</body> 
</html>
```
