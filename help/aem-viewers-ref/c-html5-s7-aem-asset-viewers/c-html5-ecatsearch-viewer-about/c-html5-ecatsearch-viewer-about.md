---
description: La visionneuse de recherche de catalogue électronique est une visionneuse de catalogue qui affiche les brochures électroniques sous la forme d’une répartition par page ou page par page. Le catalogue électronique permet aux utilisateurs de parcourir le catalogue à l’aide d’éléments d’interface utilisateur supplémentaires ou d’un mode de miniatures dédié. Les utilisateurs peuvent également effectuer un zoom avant sur chaque page pour plus de détails.
keywords: réactif
solution: Experience Manager
title: Recherche catalogue électronique
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog Search
role: Developer,User
exl-id: 915e628e-65e7-44c6-a2aa-d4ae7ed03b8e
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '2078'
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

## URL de démonstration {#section-e1c3106f5b3e445d9b95be337c2f94e2}

[https://s7d9.scene7.com/s7viewers/html5/eCatalogSearchViewer.html?emailurl=https://s7d9.scene7.com/s7/emailFriend&amp;serverUrl=https://s7d9.scene7.com/is/image/&amp;config=Scene7SharedAssets/Universal_HTML5_eCatalog_Search&amp;contenturl=https://s7d9.scene7.com/skins/&amp;asset=Viewers/Pluralist&amp;searchserverurl=https://s7search1.scene7.com/s7search/](https://s7d9.scene7.com/s7viewers/html5/eCatalogSearchViewer.html?emailurl=https://s7d9.scene7.com/s7/emailFriend&serverUrl=https://s7d9.scene7.com/is/image/&config=Scene7SharedAssets/Universal_HTML5_eCatalog_Search&contenturl=https://s7d9.scene7.com/skins/&asset=Viewers/Pluralist&searchserverurl=https://s7search1.scene7.com/s7search/)

## Utilisation de la visionneuse de catalogue électronique {#section-e6c68406ecdc4de781df182bbd8088b4}

La visionneuse de recherche de catalogue électronique représente un fichier JavaScript principal et un ensemble de fichiers d’assistance (un seul JavaScript inclus avec tous les composants SDK de la visionneuse utilisés par cette visionneuse particulière, ressources, CSS) téléchargés par la visionneuse au moment de l’exécution

Vous pouvez utiliser la visionneuse de recherche de catalogue électronique en mode pop-up à l’aide d’une page HTML prête pour l’exploitation fournie avec des visionneuses IS ou en mode intégré, où elle est intégrée à la page web cible à l’aide d’une API documentée.

La configuration et l’habillage sont similaires à ceux des autres visionneuses. Tout l’habillage est réalisé par le biais d’une feuille de style CSS personnalisée.

Voir [Référence de commande commune à tous les visualiseurs - Attributs](../../r-html5-viewer-20-cmdref-configattrib/r-html5-viewer-20-cmdref-configattrib.md#concept-850e0f2c49b949deb7cfbfd330d329bd) de configuration et [Référence de commande communs à tous les visualiseurs - URL](../../c-html5-viewer-20-cmdref-url/c-html5-viewer-20-cmdref-url.md#concept-9b337f349b7b406b8c33c7ee96b3e226)

## Interaction avec la visionneuse de catalogue électronique Search {#section-642e66ca38cd4032992840ec6c0b0cd2}

La visionneuse de Search de catalogue électronique prend en charge les gestes tactiles suivants qui sont courants dans d’autres applications mobiles.

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
   <td colname="col2"> <p> Sélectionne une nouvelle miniature dans les échantillons. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Double appui </p> </td> 
   <td colname="col2"> <p> Applique un zoom sur un niveau jusqu’à ce que le facteur d’agrandissement maximal soit atteint. Le mouvement de double appui suivant réinitialise la visionneuse à son état d’affichage initial. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Pincer </p> </td> 
   <td colname="col2"> <p>Applique un zoom avant ou arrière. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Glissement horizontal </p> </td> 
   <td colname="col2"> <p>Fait défiler la liste des pages du catalogue si une transition de cadre de diapositives est utilisée. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Balayage vertical ou battement </p> </td> 
   <td colname="col2"> <p>Lorsque l’image est réinitialisée, elle effectue un défilement natif de la page. </p> <p>Lorsque les miniatures sont actives, elles font défiler la liste des miniatures. </p> </td> 
  </tr> 
 </tbody> 
</table>

Il est possible d’activer un effet d’animation de retournement de page réaliste pour naviguer entre les pages du catalogue. Dans ce cas, un utilisateur peut maintenir et faire glisser un coin de page et retourner la page.

Cette visionneuse prend également en charge l’entrée tactile et l’entrée souris sur les appareils Windows dotés d’un écran tactile et d’une souris. Cette prise en charge est toutefois limitée aux navigateurs Web Chrome, Internet Explorer 11 et Edge uniquement.

## Social des outils de partage de médias avec la visionneuse de catalogue électronique Search {#section-eb575084a99647c3a9591f439f40b412}

La visionneuse Search catalogue électronique prend en charge les outils de partage sur les réseaux sociaux. Ils sont disponibles sous la forme d’un bouton dans la barre de contrôle principale, qui se développe en barre d’outils de partage lorsqu’un utilisateur clique ou appuie dessus.

La barre d’outils de partage contient des icônes pour chaque type de canal de partage pris en charge, qui comprend Facebook, Twitter, le partage d’e-mail, le partage de code intégré et le partage de lien. Lorsque les outils de partage d’e-mail, de partage intégré ou de partage de lien sont activés, la visionneuse affiche une boîte de dialogue modale avec un formulaire de saisie de données correspondant. Lorsque Facebook ou Twitter est appelé, la visionneuse redirige l’utilisateur vers une boîte de dialogue de partage standard d’un service social. Les outils de partage ne sont pas disponibles en mode plein écran en raison de restrictions de sécurité du navigateur web.

La fonction de recherche de la visionneuse est disponible sous la forme d’une icône en forme de glace dans la barre d’outils principale. Cliquer ou appuyer sur l’icône active le panneau de recherche avec un champ de saisie. Après avoir saisi un mot-clé ou une expression et appuyé sur Entrée, la visionneuse affiche les résultats de la recherche dans le panneau et met en surbrillance les mots trouvés dans la vue principale.

## Incorporation de la visionneuse de recherche de catalogue électronique {#section-6bb5d3c502544ad18a58eafe12a13435}

Les différentes pages web ont des besoins différents en ce qui concerne le comportement des spectateurs. Parfois, une page Web fournit un lien qui, lorsqu’il est sélectionné, ouvre la visionneuse dans une fenêtre de navigateur distincte. Dans d’autres cas, il est nécessaire d’intégrer la visionneuse directement sur la page d’hébergement. Dans ce dernier cas, la page Web peut avoir une mise en page statique ou utiliser un design réactif qui s’affiche différemment sur différents appareils ou pour différentes tailles de fenêtre de navigateur. Pour répondre à ces besoins, la visionneuse prend en charge trois modes de fonctionnement principaux : pop-up, incorporation de taille fixe et incorporation de conception réactive.

**A propos du mode pop-up**

En mode pop-up, la visionneuse est ouverte dans une fenêtre ou un onglet de navigateur Web distinct. Il prend toute la zone de la fenêtre du navigateur et s’ajuste en cas de redimensionnement du navigateur ou de changement d’orientation d’un appareil mobile.

Le mode pop-up est le plus courant pour les appareils mobiles. La page Web charge la visionneuse à l’aide `window.open()` d’JavaScript appel, d’un élément HTML correctement configuré `A` ou de toute autre méthode appropriée.

Il est recommandé d’utiliser une page HTML prête à l’emploi pour le mode de fonctionnement contextuel. Dans ce cas, il est appelé [!DNL eCatalogSearchViewer.html] et se trouve dans le [!DNL html5/] sous-dossier de votre déploiement IS-Viewers standard :

[!DNL <s7viewers_root>/html5/eCatalogSearchViewer.html]

Vous pouvez obtenir une personnalisation visuelle en appliquant une feuille de style CSS personnalisée.

Voici un exemple de code HTML qui ouvre la visionneuse dans une nouvelle fenêtre :

```html {.line-numbers}
<a href="https://s7d9.scene7.com/s7viewers/html5/eCatalogSearchViewer.html?emailurl=https://s7d9.scene7.com/s7/emailFriend&serverUrl=https://s7d9.scene7.com/is/image/&config=Scene7SharedAssets/Universal_HTML5_eCatalog_Search&contenturl=https://s7d9.scene7.com/skins/&asset=Viewers/Pluralist&searchserverurl=https://s7search1.scene7.com/s7search/" target="_blank">Open pop-up viewer</a>
```

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

1. Définition du conteneur DIV.

   Ajoutez un élément DIV vide à la page dans laquelle vous souhaitez que la visionneuse apparaisse. L’ID de l’élément DIV doit être défini, car cet identifiant est transmis ultérieurement à l’API de visionneuse.

   L’espace réservé DIV est un élément positionné, ce qui signifie que la `position` propriété CSS est définie sur `relative` ou `absolute`.

   Voici un exemple d’élément DIV d’espace réservé défini :

   ```html {.line-numbers}
   <div id="s7viewer" style="position:relative"></div>
   ```

1. Définition de la taille de la visionneuse

   Vous pouvez définir la taille statique de la visionneuse en la déclarant pour `.s7ecatalogsearchviewer` la classe CSS de niveau supérieur en unités absolues ou en utilisant le `stagesize` modificateur.

   Vous pouvez placer le dimensionnement dans CSS directement sur la page HTML ou dans un fichier CSS de visionneuse personnalisé, qui est ensuite affecté à un enregistrement de paramètre prédéfini de visionneuse dans Dynamic Media Classic, ou transmis explicitement à l’aide d’une commande de style.

   Voir [Personnalisation de la visionneuse](../../c-html5-s7-aem-asset-viewers/c-html5-20-ecatalog-viewer-about/c-html5-20-ecatalog-viewer-customizingviewer/c-html5-20-ecatalog-viewer-customizingviewer.md#concept-73a8546acdb444a387c49969ceca57d0) de catalogue électronique pour plus d’informations sur le style de la visionneuse avec CSS.

   Voici un exemple de définition d’une taille de visionneuse statique sur une page HTML :

   ```html {.line-numbers}
   #s7viewer.s7ecatalogsearchviewer { 
    width: 640px; 
    height: 480px; 
   }
   ```

   Vous pouvez définir le `stagesize` modificateur dans l’enregistrement du paramètre prédéfini de la visionneuse dans Dynamic Media Classic, ou le transmettre explicitement avec le code d’initialisation de la visionneuse avec `params` collection, ou en tant qu’appel d’API comme décrit dans la section Référence de la commande, comme suit :

   ```html {.line-numbers}
   eCatalogSearchViewer.setParam("stagesize", 
   "640,480");
   ```

1. Initialisation de la visionneuse.

   Lorsque vous avez terminé les étapes ci-dessus, vous créez une instance de classe, transmettez toutes les informations de configuration à son constructeur et appelez `s7viewers.eCatalogSearchViewer` la méthode sur une instance de `init()` visionneuse. Les informations de configuration sont transmises au constructeur sous la forme d’un objet JSON. Au minimum, cet objet comporte le `containerId` champ qui contient le nom de l’ID de conteneur de la visionneuse et de l’objet JSON imbriqué `params` avec les paramètres de configuration pris en charge par la visionneuse. Dans ce cas, l’objet `params` doit comporter au moins l’URL du service d’images transmise en tant que propriété `serverUrl`, et la ressource initiale en tant que paramètre `asset`. L’API d’initialisation basée sur JSON vous permet de créer et de démarrer la visionneuse avec une seule ligne de code.

   Il est important d’ajouter le conteneur de visionneuse au DOM afin que le code de la visionneuse puisse trouver l’élément de conteneur à l’aide de son identifiant. Certains navigateurs retardent la création du DOM jusqu’à la fin de la page web. Toutefois, pour une compatibilité maximale, appelez la méthode `init()` juste avant la balise de `BODY` de fermeture ou sur l’événement de `onload()` du corps.

   En même temps, l’élément conteneur ne doit pas nécessairement faire partie de la mise en page Web pour le moment. Par exemple, il peut être masqué à l’aide `display:none` du style qui lui est attribué. Dans ce cas, la visionneuse retarde son processus d’initialisation jusqu’au moment où la page Web ramène l’élément conteneur à la mise en page. Lorsque cela se produit, le chargement de la visionneuse reprend automatiquement.

   Voici un exemple de création d’une instance de visionneuse, de transmission des options de configuration minimales nécessaires au constructeur et d’appel de la `init()` méthode. L’exemple suppose `eCatalogSearchViewer` est l’instance de visionneuse ; `s7viewer` est le nom de l’espace `DIV`réservé ; `https://s7d1.scene7.com/is/image/` est l’URL du serveur d’images et `Viewers/Pluralist` est l’actif :

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

   Le code suivant est un exemple complet de page Web triviale qui intègre la visionneuse de catalogue électronique Search une taille fixe :

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

**Intégration de conception réactive avec une hauteur illimitée**

Avec l’intégration de conception réactive, la page Web a normalement une sorte de mise en page flexible en place qui dicte la taille d’exécution du conteneur `DIV`de la visionneuse. Pour les besoins de cet exemple, supposons que la page Web autorise le conteneur `DIV` du spectateur à prendre 40 % de la taille de la fenêtre du navigateur Web, en laissant sa hauteur sans restriction. Le code HTML résultant de la page Web ressemble à ce qui suit :

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

L’ajout de la visionneuse à une telle page est similaire à l’incorporation de taille fixe, à la seule différence que vous n’avez pas besoin de définir explicitement la taille de la visionneuse.

1. Ajout du fichier JavaScript de visionneuse à votre page Web.
1. Définition du conteneur DIV.
1. Création et initialisation de la visionneuse.

Toutes les étapes ci-dessus sont identiques à celles d’un incorporation de taille fixe. Ajoutez le conteneur `DIV` au « support » `DIV`existant. Le code suivant est un exemple complet. Vous pouvez voir comment la taille de la visionneuse change lorsque le navigateur est redimensionné et comment le format de la visionneuse correspond à la ressource.

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

La page d’exemples suivante illustre d’autres cas réels d’incorporation de conception réactive avec une hauteur illimitée :

[Démonstrations en direct](https://landing.adobe.com/en/na/dynamic-media/ctir-2755/live-demos.html)

**Intégration de taille flexible avec largeur et hauteur définies**

En cas d’incorporation de taille flexible avec la largeur et la hauteur définies, le style de la page Web est différent. C’est-à-dire qu’il fournit les deux tailles au « titulaire » `DIV` et le centre dans la fenêtre du navigateur. En outre, la page web définit la taille de l’élément `HTML` ET `BODY` sur 100 % :

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

Les étapes d’incorporation restantes sont identiques à l’incorporation de conception réactive avec une hauteur illimitée. L’exemple résultant est le suivant :

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

**Incorporation à l’aide de l’API basée sur Setter**

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
