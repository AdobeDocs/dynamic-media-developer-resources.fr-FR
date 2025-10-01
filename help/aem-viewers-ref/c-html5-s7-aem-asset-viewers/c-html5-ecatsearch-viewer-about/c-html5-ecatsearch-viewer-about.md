---
description: La visionneuse de recherche de catalogue électronique est une visionneuse de catalogue qui affiche les brochures électroniques sous la forme d’une répartition par page ou page par page. Le catalogue électronique permet aux utilisateurs de parcourir le catalogue à l’aide d’éléments d’interface utilisateur supplémentaires ou d’un mode de miniatures dédié. Les utilisateurs peuvent également effectuer un zoom avant sur chaque page pour plus de détails.
keywords: réactif
solution: Experience Manager
title: Recherche catalogue électronique
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog Search
role: Developer,User
exl-id: 915e628e-65e7-44c6-a2aa-d4ae7ed03b8e
source-git-commit: baf8015dc93cfa6be0a841243a7e3524f06f1639
workflow-type: tm+mt
source-wordcount: '2058'
ht-degree: 0%

---

# Recherche catalogue électronique{#ecatalog-search}

La visionneuse de recherche de catalogue électronique est une visionneuse de catalogue qui affiche les brochures électroniques sous la forme d’une répartition par page ou page par page. Le catalogue électronique permet aux utilisateurs de parcourir le catalogue à l’aide d’éléments d’interface utilisateur supplémentaires ou d’un mode de miniatures dédié. Les utilisateurs peuvent également effectuer un zoom avant sur chaque page pour plus de détails.

Cette visionneuse fonctionne avec des catalogues électroniques et prend en charge les zones cliquables facultatives et les outils de partage sur les réseaux sociaux. Elle comprend des outils de zoom, des outils de navigation de catalogue, une prise en charge du plein écran, des miniatures et un bouton de fermeture facultatif. La visionneuse prend également en charge les outils de partage sur les réseaux sociaux, l’impression, le téléchargement et les favoris. Il est conçu pour fonctionner sur les ordinateurs de bureau et les appareils mobiles.

L’utilisateur peut également effectuer une recherche par mot-clé ou expression sur le contenu du catalogue.

>[!NOTE]
>
>Les images qui utilisent le rendu d’image (IR) ou le contenu créé par l’utilisateur (UGC) ne sont pas pris en charge par cette visionneuse.

Type de visionneuse 513.

Voir [Configuration requise et conditions préalables](../../c-system-requirements-and-prerequisites.md#concept-9282e5b777de42cdaf72ef7ebd646842).

<!--
## Demo URL {#section-e1c3106f5b3e445d9b95be337c2f94e2}

[https://s7d9.scene7.com/s7viewers/html5/eCatalogSearchViewer.html?emailurl=https://s7d9.scene7.com/s7/emailFriend&serverUrl=https://s7d9.scene7.com/is/image/&config=Scene7SharedAssets/Universal_HTML5_eCatalog_Search&contenturl=https://s7d9.scene7.com/skins/&asset=Viewers/Pluralist&searchserverurl=https://s7search1.scene7.com/s7search/](https://s7d9.scene7.com/s7viewers/html5/eCatalogSearchViewer.html?emailurl=https://s7d9.scene7.com/s7/emailFriend&serverUrl=https://s7d9.scene7.com/is/image/&config=Scene7SharedAssets/Universal_HTML5_eCatalog_Search&contenturl=https://s7d9.scene7.com/skins/&asset=Viewers/Pluralist&searchserverurl=https://s7search1.scene7.com/s7search/)

-->

## Utilisation de la visionneuse de catalogue électronique {#section-e6c68406ecdc4de781df182bbd8088b4}

La visionneuse de recherche de catalogue électronique représente un fichier JavaScript principal et un ensemble de fichiers d’assistance (un seul JavaScript inclus avec tous les composants SDK de la visionneuse utilisés par cette visionneuse particulière, ressources, CSS) téléchargés par la visionneuse au moment de l’exécution

Vous pouvez utiliser la visionneuse de recherche de catalogue électronique en mode pop-up à l’aide d’une page HTML prête pour l’exploitation fournie avec des visionneuses IS ou en mode intégré, où elle est intégrée à la page web cible à l’aide d’une API documentée.

La configuration et l’habillage sont similaires à ceux des autres visionneuses. Toute application de la peau est réalisée au moyen d’un CSS personnalisé.

Voir [ Référence des commandes commune à toutes les visionneuses - Attributs de configuration ](../../r-html5-viewer-20-cmdref-configattrib/r-html5-viewer-20-cmdref-configattrib.md#concept-850e0f2c49b949deb7cfbfd330d329bd) et [ Référence des commandes commune à toutes les visionneuses - URL](../../c-html5-viewer-20-cmdref-url/c-html5-viewer-20-cmdref-url.md#concept-9b337f349b7b406b8c33c7ee96b3e226)

## Interaction avec la visionneuse de recherche de catalogue électronique {#section-642e66ca38cd4032992840ec6c0b0cd2}

La visionneuse de recherche de catalogue électronique prend en charge les gestes tactiles suivants, courants dans d’autres applications mobiles.

<table id="table_ED747CC7178448919C34A4FCD18922D0"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>Mouvement </p> </th> 
   <th colname="col2" class="entry"> <p>Description </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>Clic unique </p> </td> 
   <td colname="col2"> <p> Sélectionne la nouvelle miniature dans les échantillons. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Appuyer deux fois </p> </td> 
   <td colname="col2"> <p> Effectue un zoom d’un niveau jusqu’à ce que le zoom maximal soit atteint. Le mouvement de double appui suivant réinitialise la visionneuse à l’état d’affichage initial. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Pincer </p> </td> 
   <td colname="col2"> <p>Effectue un zoom avant ou arrière. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Balayage horizontal ou clic </p> </td> 
   <td colname="col2"> <p>Fait défiler la liste des pages du catalogue si une transition de cadre de diapositives est utilisée. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Balayage vertical ou battement </p> </td> 
   <td colname="col2"> <p>Lorsque l’image est réinitialisée, elle effectue un défilement natif de la page. </p> <p>Lorsque les miniatures sont actives, elles font défiler la liste. </p> </td> 
  </tr> 
 </tbody> 
</table>

Il est possible d’activer un effet d’animation réaliste de basculement de page pour naviguer entre les pages du catalogue. Dans ce cas, l’utilisateur peut tenir et faire glisser un coin de page et retourner la page.

Cette visionneuse prend également en charge l’entrée tactile et l’entrée souris sur les appareils Windows dotés d’un écran tactile et d’une souris. Cette prise en charge se limite toutefois aux navigateurs web Chrome, Internet Explorer 11 et Edge uniquement.

## Outils de partage sur les médias sociaux avec la visionneuse de recherche de catalogue électronique {#section-eb575084a99647c3a9591f439f40b412}

La visionneuse de recherche de catalogue électronique prend en charge les outils de partage sur les réseaux sociaux. Ils sont disponibles sous la forme d’un bouton dans la barre de contrôle principale, qui se développe en barre d’outils de partage lorsqu’un utilisateur clique ou appuie dessus.

La barre d’outils de partage contient des icônes pour chaque type de canal de partage pris en charge, qui comprend Facebook, Twitter, le partage d’e-mail, le partage de code intégré et le partage de lien. Lorsque les outils de partage d’e-mail, de partage intégré ou de partage de lien sont activés, la visionneuse affiche une boîte de dialogue modale avec un formulaire de saisie de données correspondant. Lorsque Facebook ou Twitter est appelé, la visionneuse redirige l’utilisateur vers une boîte de dialogue de partage standard d’un service social. Les outils de partage ne sont pas disponibles en mode plein écran en raison de restrictions de sécurité du navigateur web.

La fonction de recherche de la visionneuse est disponible sous la forme d’une icône en forme de glace dans la barre d’outils principale. Cliquer ou appuyer sur l’icône active le panneau de recherche avec un champ de saisie. Après avoir saisi un mot-clé ou une expression et appuyé sur Entrée, la visionneuse affiche les résultats de la recherche dans le panneau et met en surbrillance les mots trouvés dans la vue principale.

## Incorporation de la visionneuse de recherche de catalogue électronique {#section-6bb5d3c502544ad18a58eafe12a13435}

Les différentes pages web ont des besoins différents en termes de comportement des observateurs. Parfois, une page web fournit un lien qui, lorsqu’il est sélectionné, ouvre la visionneuse dans une fenêtre de navigateur distincte. Dans d’autres cas, il est nécessaire d’incorporer la visionneuse directement dans la page d’hébergement. Dans ce dernier cas, la page web peut avoir une mise en page statique ou utiliser une conception réactive qui s’affiche différemment sur différents appareils ou pour différentes tailles de fenêtre du navigateur. Pour répondre à ces besoins, la visionneuse prend en charge trois modes de fonctionnement principaux : pop-up, incorporation de taille fixe et incorporation de conception réactive.

**À propos du mode pop-up**

En mode pop-up, la visionneuse s’ouvre dans une fenêtre ou un onglet distinct du navigateur web. Elle occupe toute la zone de la fenêtre du navigateur et s’ajuste au cas où le navigateur serait redimensionné ou si l’orientation d’un appareil mobile était modifiée.

Le mode pop-up est le plus courant pour les appareils mobiles. La page web charge la visionneuse à l’aide de `window.open()`’appel JavaScript, correctement configuré `A` l’élément HTML ou de toute autre méthode appropriée.

Il est recommandé d’utiliser une page HTML prête à l’emploi pour le mode de fonctionnement des fenêtres pop-up. Dans ce cas, il s’appelle [!DNL eCatalogSearchViewer.html] et se trouve dans le sous-dossier [!DNL html5/] de votre déploiement d’observateurs IS standard :

[!DNL <s7viewers_root>/html5/eCatalogSearchViewer.html]

Vous pouvez effectuer une personnalisation visuelle en appliquant un CSS personnalisé.

<!--
The following is an example of HTML code that opens the viewer in a new window:

```html {.line-numbers}
<a href="https://s7d9.scene7.com/s7viewers/html5/eCatalogSearchViewer.html?emailurl=https://s7d9.scene7.com/s7/emailFriend&serverUrl=https://s7d9.scene7.com/is/image/&config=Scene7SharedAssets/Universal_HTML5_eCatalog_Search&contenturl=https://s7d9.scene7.com/skins/&asset=Viewers/Pluralist&searchserverurl=https://s7search1.scene7.com/s7search/" target="_blank">Open pop-up viewer</a>
```
-->

**À propos du mode d’incorporation de taille fixe et du mode d’incorporation de conception réactive**

En mode incorporé, la visionneuse est ajoutée à la page web existante, qui peut déjà comporter du contenu client non lié à la visionneuse. L’observateur n’occupe normalement qu’une partie de l’espace d’une page web.

Les principaux cas d’utilisation sont des pages web orientées pour les ordinateurs de bureau ou les tablettes, ainsi que des pages conçues en responsive design qui ajustent automatiquement la disposition en fonction du type d’appareil.

L’incorporation de taille fixe est utilisée lorsque la visionneuse ne modifie pas sa taille après le chargement initial. Il s’agit du meilleur choix pour les pages web avec une disposition statique.

L’incorporation de conception réactive suppose que la visionneuse doit être redimensionnée au moment de l’exécution en réponse au changement de taille de son `DIV` de conteneur. Le cas d’utilisation le plus courant consiste à ajouter une visionneuse à une page web qui utilise une disposition de page flexible.

En mode d’incorporation de responsive design, la visionneuse se comporte différemment selon la manière dont la page web dimensionne son `DIV` de conteneur. Si la page web définit uniquement la largeur du `DIV` de conteneur, sans restriction de hauteur, la visionneuse choisit automatiquement sa hauteur en fonction des proportions de la ressource utilisée. Cette fonctionnalité garantit que la ressource s’adapte parfaitement à la vue sans marge intérieure sur les côtés. Ce cas d’utilisation est le plus courant pour les pages web utilisant des structures de disposition réactives telles que Bootstrap, Foundation, etc.

Dans le cas contraire, si la page web définit à la fois la largeur et la hauteur du `DIV` de conteneur de la visionneuse, celle-ci remplit exactement cette zone et suit la taille fournie par la disposition de la page web. Un bon exemple consiste à incorporer la visionneuse dans une superposition modale, où la superposition est dimensionnée en fonction de la taille de la fenêtre du navigateur web.

**Incorporation de taille fixe**

Ajoutez la visionneuse à une page web en procédant comme suit :

1. Ajout du fichier JavaScript de la visionneuse à votre page web.
1. Définition du DIV du conteneur.
1. Définition de la taille de la visionneuse.
1. Création et initialisation de la visionneuse.

1. Ajout du fichier JavaScript de la visionneuse à votre page web.

   La création d’une visionneuse nécessite l’ajout d’une balise de script dans l’en-tête HTML. Avant de pouvoir utiliser l’API de visionneuse, veillez à inclure [!DNL eCatalogSearchViewer.js]. Le fichier [!DNL eCatalogSearchViewer.js] se trouve sous le sous-dossier [!DNL html5/js/] de votre déploiement d’observateurs IS standard :

[!DNL <s7viewers_root>/html5/js/eCatalogSearchViewer.js]

Vous pouvez utiliser un chemin d’accès relatif si la visionneuse est déployée sur l’un des serveurs Dynamic Media d’Adobe et qu’elle est diffusée à partir du même domaine. Sinon, vous spécifiez un chemin d’accès complet à l’un des serveurs Dynamic Media Adobe sur lesquels les visionneuses IS sont installées.

Le chemin d’accès relatif ressemble à ce qui suit :

```html {.line-numbers}
<script language="javascript" type="text/javascript" src="/s7viewers/html5/js/eCatalogSearchViewer.js"></script>
```

1. Définition du DIV du conteneur.

   Ajoutez un élément DIV vide à la page sur laquelle vous souhaitez que la visionneuse apparaisse. L’identifiant de l’élément DIV doit être défini, car cet identifiant est transmis ultérieurement à l’API de visionneuse.

   L’espace réservé DIV est un élément positionné, ce qui signifie que la propriété CSS `position` est définie sur `relative` ou `absolute`.

   Exemple d’élément DIV d’espace réservé défini :

   ```html {.line-numbers}
   <div id="s7viewer" style="position:relative"></div>
   ```

1. Définition de la taille de la visionneuse

   Vous pouvez définir la taille statique de la visionneuse en la déclarant pour `.s7ecatalogsearchviewer` classe CSS de niveau supérieur dans des unités absolues ou à l’aide du modificateur `stagesize`.

   Vous pouvez définir le dimensionnement dans CSS directement sur la page HTML ou dans un fichier CSS de visionneuse personnalisé, qui est ensuite attribué à un enregistrement de paramètre prédéfini de visionneuse dans Dynamic Media Classic, ou transmis explicitement à l’aide d’une commande de style.

   Consultez [Personnalisation de la visionneuse de catalogue électronique](../../c-html5-s7-aem-asset-viewers/c-html5-20-ecatalog-viewer-about/c-html5-20-ecatalog-viewer-customizingviewer/c-html5-20-ecatalog-viewer-customizingviewer.md#concept-73a8546acdb444a387c49969ceca57d0) pour plus d’informations sur la mise en forme de la visionneuse avec CSS.

   Voici un exemple de définition d’une taille de visionneuse statique dans une page HTML :

   ```html {.line-numbers}
   #s7viewer.s7ecatalogsearchviewer { 
    width: 640px; 
    height: 480px; 
   }
   ```

   Vous pouvez définir le modificateur `stagesize` dans l’enregistrement du paramètre prédéfini de la visionneuse dans Dynamic Media Classic ou le transmettre explicitement avec le code d’initialisation de la visionneuse avec `params` collection, ou sous la forme d’un appel API, comme décrit dans la section Référence des commandes , comme suit :

   ```html {.line-numbers}
   eCatalogSearchViewer.setParam("stagesize", 
   "640,480");
   ```

1. Initialisation de la visionneuse.

   Une fois les étapes ci-dessus terminées, vous créez une instance de `s7viewers.eCatalogSearchViewer` classe, transmettez toutes les informations de configuration à son constructeur et appelez `init()` méthode sur une instance de visionneuse. Les informations de configuration sont transmises au constructeur en tant qu’objet JSON. Au minimum, cet objet comporte le champ `containerId` qui contient le nom de l’ID de conteneur de visionneuse et de l’objet JSON `params` imbriqué avec les paramètres de configuration pris en charge par la visionneuse. Dans ce cas, l’objet `params` doit comporter au moins l’URL du service d’images transmise en tant que propriété `serverUrl`, et la ressource initiale en tant que paramètre `asset`. L’API d’initialisation basée sur JSON vous permet de créer et de démarrer la visionneuse avec une seule ligne de code.

   Il est important d’ajouter le conteneur de visionneuse au DOM afin que le code de la visionneuse puisse trouver l’élément de conteneur à l’aide de son identifiant. Certains navigateurs retardent la création du DOM jusqu’à la fin de la page web. Toutefois, pour une compatibilité maximale, appelez la méthode `init()` juste avant la balise de `BODY` de fermeture ou sur l’événement de `onload()` du corps.

   Dans le même temps, l’élément de conteneur ne doit pas nécessairement faire tout de suite partie de la mise en page web. Par exemple, elle peut être masquée à l’aide `display:none` style qui lui est affecté. Dans ce cas, la visionneuse retarde son processus d’initialisation jusqu’au moment où la page web ramène l’élément de conteneur dans la mise en page. Dans ce cas, le chargement de la visionneuse reprend automatiquement.

   Voici un exemple de création d’une instance de visionneuse, de transmission des options de configuration minimales nécessaires au constructeur et d’appel de la méthode `init()`. L’exemple suppose que `eCatalogSearchViewer` est l’instance de visionneuse, `s7viewer` est le nom de l’espace réservé `DIV`, `https://s7d1.scene7.com/is/image/` est l’URL du service d’images et `Viewers/Pluralist` est la ressource :

   ```html {.line-numbers}
   <script type="text/javascript"> 
   var eCatalogSearchViewer = new s7viewers.eCatalogSearchViewer({ 
    "containerId":"s7viewer", 
   "params":{ 
    "asset":"Viewers/Pluralist", 
    "serverurl":"https://s7d1.scene7.com/is/image/", 
    "searchserverurl":"https://s7search1.scene7.com/s7search/" 
   } 
   }).init(); 
   </script>
   ```

   Le code suivant est un exemple complet de page web triviale qui incorpore la visionneuse de recherche de catalogue électronique avec une taille fixe :

   ```html {.line-numbers}
   <!DOCTYPE html> 
   <html> 
   <head> 
   <script type="text/javascript" src="https://s7d1.scene7.com/s7viewers/html5/js/eCatalogSearchViewer.js"></script> 
   <style type="text/css"> 
   #s7viewer.s7ecatalogsearchviewer { 
    width: 640px; 
    height: 480px; 
   } 
   </style> 
   </head> 
   <body> 
   <div id="s7viewer" style="position:relative"></div> 
   <script type="text/javascript"> 
   var eCatalogSearchViewer = new s7viewers.eCatalogSearchViewer({ 
    "containerId":"s7viewer", 
   "params":{ 
    "asset":"Viewers/Pluralist", 
    "serverurl":"https://s7d1.scene7.com/is/image/", 
    "searchserverurl":"https://s7search1.scene7.com/s7search/" 
   } 
   }).init(); 
   </script> 
   </body> 
   </html>
   ```

**Incorporation de conception réactive avec hauteur illimitée**

Avec l’incorporation de responsive design, la page web dispose normalement d’un type de disposition flexible qui détermine la taille d’exécution du `DIV` de conteneur de la visionneuse. Pour les besoins de cet exemple, supposons que la page web permette au `DIV` de conteneur de la visionneuse de prendre 40 % de la taille de la fenêtre du navigateur web, sans restriction de hauteur. Le code HTML de la page web qui en résulte ressemble à ce qui suit :

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

L’ajout de la visionneuse à une telle page est similaire à l’incorporation de taille fixe, la seule différence étant que vous n’avez pas besoin de définir explicitement la taille de la visionneuse.

1. Ajout du fichier JavaScript de la visionneuse à votre page web.
1. Définition du DIV du conteneur.
1. Création et initialisation de la visionneuse.

Toutes les étapes ci-dessus sont identiques à celles de l’incorporation à taille fixe. Ajoutez l’`DIV` de conteneur au `DIV` « holder » existant. Le code suivant en est un exemple complet. Vous pouvez voir comment la taille de la visionneuse change lorsque le navigateur est redimensionné et comment les proportions de la visionneuse correspondent à la ressource.

```html {.line-numbers}
<!DOCTYPE html> 
<html> 
<head> 
<script type="text/javascript" src="https://s7d1.scene7.com/s7viewers/html5/js/eCatalogSearchViewer.js"></script> 
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
var eCatalogSearchViewer = new s7viewers.eCatalogSearchViewer({ 
 "containerId":"s7viewer", 
"params":{ 
 "asset":"Viewers/Pluralist", 
 "serverurl":"https://s7d1.scene7.com/is/image/", 
 "searchserverurl":"https://s7search1.scene7.com/s7search/" 
} 
}).init(); 
</script> 
</body> 
</html>
```

La page d’exemples suivante illustre d’autres cas d’utilisation réels d’incorporation de conception réactive avec une hauteur non limitée :

[Démonstrations en direct](https://landing.adobe.com/en/na/dynamic-media/ctir-2755/live-demos.html)

**Incorporation de taille flexible avec largeur et hauteur définies**

Dans le cas d’une incorporation de taille flexible avec une largeur et une hauteur définies, le style de la page web est différent. En d’autres termes, il fournit les deux tailles au `DIV` « holder » et le centre dans la fenêtre du navigateur. En outre, la page web définit la taille de l’élément `HTML` et `BODY` sur 100 % :

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

Les étapes d’incorporation restantes sont identiques à l’incorporation de conception réactive avec une hauteur illimitée. L’exemple qui en résulte est le suivant :

```html {.line-numbers}
<!DOCTYPE html> 
<html> 
<head> 
<script type="text/javascript" src="https://s7d1.scene7.com/s7viewers/html5/js/eCatalogSearchViewer.js"></script> 
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
var eCatalogSearchViewer = new s7viewers.eCatalogSearchViewer({ 
 "containerId":"s7viewer", 
"params":{ 
 "asset":"Viewers/Pluralist", 
 "serverurl":"https://s7d1.scene7.com/is/image/", 
 "searchserverurl":"https://s7search1.scene7.com/s7search/" 
} 
}).init(); 
</script> 
</body> 
</html>
```

**Incorporation à l’aide de l’API Setter**

Au lieu d’utiliser l’initialisation basée sur JSON, il est possible d’utiliser l’API basée sur setter et le constructeur sans args. Avec ce constructeur d’API, aucun paramètre n’est pris et les paramètres de configuration sont spécifiés à l’aide des méthodes d’API `setContainerId()`, `setParam()` et `setAsset()` avec des appels JavaScript distincts.

L’exemple suivant illustre l’incorporation à taille fixe avec l’API basée sur setter :

```html {.line-numbers}
<!DOCTYPE html> 
<html> 
<head> 
<script type="text/javascript" src="https://s7d1.scene7.com/s7viewers/html5/js/eCatalogSearchViewer.js"></script> 
<style type="text/css"> 
#s7viewer.s7ecatalogsearchviewer { 
 width: 640px; 
 height: 480px; 
} 
</style> 
</head> 
<body> 
<div id="s7viewer" style="position:relative"></div> 
<script type="text/javascript"> 
var eCatalogSearchViewer = new s7viewers.eCatalogSearchViewer(); 
eCatalogSearchViewer.setContainerId("s7viewer"); 
eCatalogSearchViewer.setParam("serverurl", "https://s7d1.scene7.com/is/image/"); 
eCatalogSearchViewer.setParam("searchserverurl", "https://s7search1.scene7.com/s7search/"); 
eCatalogSearchViewer.setAsset("Viewers/Pluralist"); 
eCatalogSearchViewer.init(); 
</script> 
</body> 
</html>
```
