---
description: La visionneuse de recherche de catalogue électronique est une visionneuse de catalogue qui affiche les brochures électroniques dans une diffusion ou page par page. Elle permet aux utilisateurs de parcourir le catalogue à l’aide d’éléments d’interface utilisateur supplémentaires ou de modes de miniatures dédiés. Les utilisateurs peuvent également zoomer sur chaque page pour obtenir des détails plus détaillés.
keywords: responsive
solution: Experience Manager
title: Recherche catalogue électronique
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog Search
role: Developer,User
exl-id: 915e628e-65e7-44c6-a2aa-d4ae7ed03b8e
source-git-commit: b89ca96947f751b750623e1f18d2a5d86f0cd759
workflow-type: tm+mt
source-wordcount: '2180'
ht-degree: 0%

---

# Recherche catalogue électronique{#ecatalog-search}

La visionneuse de recherche de catalogue électronique est une visionneuse de catalogue qui affiche les brochures électroniques dans une diffusion ou page par page. Elle permet aux utilisateurs de parcourir le catalogue à l’aide d’éléments d’interface utilisateur supplémentaires ou de modes de miniatures dédiés. Les utilisateurs peuvent également zoomer sur chaque page pour obtenir des détails plus détaillés.

Cette visionneuse fonctionne avec des catalogues électroniques et prend en charge les zones cliquables et les outils de partage sur les réseaux sociaux en option. Il contient des outils de zoom, des outils de navigation de catalogue, la prise en charge du plein écran, des miniatures et un bouton de fermeture facultatif. La visionneuse prend également en charge les outils de partage sur les réseaux sociaux, l’impression, le téléchargement et les favoris. Il est conçu pour fonctionner sur les ordinateurs de bureau et les appareils mobiles.

L’utilisateur peut également effectuer une recherche par mot-clé ou par expression sur le contenu du catalogue.

>[!NOTE]
>
>Les images qui utilisent IR (Image Rendering) ou UGC (User-Generated Content) ne sont pas prises en charge par cette visionneuse.

Type de visionneuse 513.

Voir [Configuration requise et conditions préalables](../../c-system-requirements-and-prerequisites.md#concept-9282e5b777de42cdaf72ef7ebd646842).

## URL de démonstration {#section-e1c3106f5b3e445d9b95be337c2f94e2}

[https://s7d9.scene7.com/s7viewers/html5/eCatalogSearchViewer.html?emailurl=https://s7d9.scene7.com/s7/emailFriend&amp;serverUrl=https://s7d9.scene7.com/is/image/&amp;config=Scene7SharedAssets/Universal_HTML5_eCatalog_Search&amp;contenturl=https://s7d9.scene7.com/skins/&amp;asset=Viewers/Pluralist&amp;searchserverurl=https://s7search1.scene7.com/s7search/](https://s7d9.scene7.com/s7viewers/html5/eCatalogSearchViewer.html?emailurl=https://s7d9.scene7.com/s7/emailFriend&amp;serverUrl=https://s7d9.scene7.com/is/image/&amp;config=Scene7SharedAssets/Universal_HTML5_eCatalog_Search&amp;contenturl=https://s7d9.scene7.com/skins/&amp;asset=Viewers/Pluralist&amp;searchserverurl=https://s7search1.scene7.com/s7search/)

## Utilisation de la visionneuse de catalogue électronique {#section-e6c68406ecdc4de781df182bbd8088b4}

La visionneuse de recherche eCatalog représente un fichier JavaScript principal et un ensemble de fichiers d’assistance (un seul script JavaScript inclus avec tous les composants du SDK de la visionneuse utilisés par cette visionneuse, ressources, CSS) téléchargés par la visionneuse au moment de l’exécution.

Vous pouvez utiliser la visionneuse de recherche de catalogue électronique en mode pop-up à l’aide d’une page de HTML prête à l’emploi fournie avec les visionneuses IS ou en mode incorporé, où elle est intégrée à la page web cible à l’aide d’une API documentée.

La configuration et l’habillage sont similaires à ceux des autres visionneuses. L’habillage est effectué au moyen d’une feuille CSS personnalisée.

Voir [Référence de commande commune à toutes les visionneuses - Attributs de configuration](../../r-html5-viewer-20-cmdref-configattrib/r-html5-viewer-20-cmdref-configattrib.md#concept-850e0f2c49b949deb7cfbfd330d329bd) et [Référence de commande commune à toutes les visionneuses - URL](../../c-html5-viewer-20-cmdref-url/c-html5-viewer-20-cmdref-url.md#concept-9b337f349b7b406b8c33c7ee96b3e226)

## Interaction avec la visionneuse de recherche de catalogue électronique {#section-642e66ca38cd4032992840ec6c0b0cd2}

La visionneuse de recherche par catalogue électronique prend en charge les mouvements tactiles suivants, courants dans d’autres applications mobiles.

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
   <td colname="col2"> <p>Fait défiler la liste des pages du catalogue si une transition de cadre de diapositive est utilisée. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Glissement ou clic vertical </p> </td> 
   <td colname="col2"> <p>Lorsque l’image est réinitialisée, elle effectue un défilement de page natif. </p> <p>Lorsque les miniatures sont principales, elles font défiler la liste des miniatures. </p> </td> 
  </tr> 
 </tbody> 
</table>

Il est possible d’activer un effet d’animation de type Symétrie de page réaliste pour naviguer entre les pages du catalogue. Dans ce cas, l’utilisateur peut maintenir le bouton de la souris enfoncé et faire glisser un coin de page et retourner la page.

Cette visionneuse prend également en charge les entrées tactile et de souris sur les périphériques Windows dotés d’un écran tactile et d’une souris. Toutefois, cette prise en charge est limitée aux navigateurs Chrome, Internet Explorer 11 et Edge uniquement.

## Outils de partage sur les médias sociaux avec la visionneuse de recherche de catalogue électronique {#section-eb575084a99647c3a9591f439f40b412}

La visionneuse de recherche eCatalog prend en charge les outils de partage sur les réseaux sociaux. Ils sont disponibles sous forme de bouton dans la barre de contrôle principale, qui se transforme en barre d’outils de partage lorsqu’un utilisateur clique ou appuie dessus.

La barre d’outils de partage contient des icônes pour chaque type de canal de partage pris en charge, notamment Facebook, Twitter, le partage de courrier électronique, le partage de code incorporé et le partage de lien. Lorsque des outils de partage de courrier électronique, d’intégration de partage ou de lien sont activés, la visionneuse affiche une boîte de dialogue modale avec un formulaire de saisie de données correspondant. Lorsque Facebook ou Twitter est appelé, la visionneuse redirige l’utilisateur vers une boîte de dialogue de partage standard à partir d’un service social. Les outils de partage ne sont pas disponibles en mode plein écran en raison des restrictions de sécurité du navigateur web.

La fonction de recherche de la visionneuse est disponible sous la forme d’une icône en forme de vitre dans la barre d’outils principale. Cliquez ou appuyez sur l’icône pour activer le panneau Rechercher avec un champ de saisie. Après avoir saisi un mot-clé ou une expression et appuyé sur Entrée, la visionneuse effectue le rendu des résultats de recherche dans le panneau et met en surbrillance les mots trouvés dans la vue principale.

## Incorporation de la visionneuse de recherche de catalogue électronique {#section-6bb5d3c502544ad18a58eafe12a13435}

Le comportement de la visionneuse varie en fonction des pages web. Il arrive qu’une page web fournisse un lien qui, lorsqu’il est sélectionné, ouvre la visionneuse dans une fenêtre de navigateur distincte. Dans d’autres cas, il est nécessaire d’incorporer le droit de visionneuse dans la page d’hébergement. Dans ce cas, la page web peut avoir une mise en page statique ou utiliser une conception réactive qui s’affiche différemment sur différents appareils ou pour différentes tailles de fenêtre de navigateur. Pour répondre à ces besoins, la visionneuse prend en charge trois modes de fonctionnement Principaux : pop-up, incorporation de taille fixe et incorporation de conceptions réactives.

**A propos du mode pop-up**

En mode contextuel, la visionneuse s’ouvre dans une fenêtre ou un onglet de navigateur Web distinct. Il prend toute la zone de la fenêtre du navigateur et s’ajuste au cas où le navigateur serait redimensionné ou si l’orientation d’un appareil mobile est modifiée.

Le mode pop-up est le plus courant pour les appareils mobiles. La page web charge la visionneuse à l’aide de `window.open()` Appel JavaScript, correctement configuré `A` élément de HTML ou toute autre méthode appropriée.

Il est recommandé d’utiliser une page de HTML d’usine pour le mode de fonctionnement de la fenêtre contextuelle. Dans ce cas, il est appelé [!DNL eCatalogSearchViewer.html] et se trouve dans la variable [!DNL html5/] sous-dossier de votre déploiement IS-Viewers standard :

[!DNL <s7viewers_root>/html5/eCatalogSearchViewer.html]

Vous pouvez effectuer une personnalisation visuelle en appliquant une page CSS personnalisée.

Voici un exemple de code de HTML qui ouvre la visionneuse dans une nouvelle fenêtre :

```html {.line-numbers}
<a href="https://s7d9.scene7.com/s7viewers/html5/eCatalogSearchViewer.html?emailurl=https://s7d9.scene7.com/s7/emailFriend&serverUrl=https://s7d9.scene7.com/is/image/&config=Scene7SharedAssets/Universal_HTML5_eCatalog_Search&contenturl=https://s7d9.scene7.com/skins/&asset=Viewers/Pluralist&searchserverurl=https://s7search1.scene7.com/s7search/" target="_blank">Open pop-up viewer</a>
```

**À propos du mode d’incorporation à taille fixe et du mode d’incorporation de responsive design**

En mode incorporé, la visionneuse est ajoutée à la page web existante, qui peut déjà comporter du contenu client non lié à la visionneuse. Normalement, la visionneuse occupe uniquement une partie de l’espace d’une page web.

Les cas d’utilisation Principaux sont les pages web orientées vers les ordinateurs de bureau ou les tablettes, ainsi que les pages réactives qui ajustent automatiquement la mise en page en fonction du type d’appareil.

L’incorporation des tailles fixes est utilisée lorsque la visionneuse ne modifie pas sa taille après le chargement initial. Il s’agit de la meilleure solution pour les pages web ayant une disposition statique.

L’incorporation de conceptions réactives suppose que la visionneuse doit peut-être être redimensionnée au moment de l’exécution en réponse au changement de taille de son conteneur. `DIV`. Le cas d’utilisation le plus courant consiste à ajouter une visionneuse à une page web qui utilise une mise en page flexible.

En mode d’incorporation de responsive design, la visionneuse se comporte différemment selon la manière dont la page web dimensionne son conteneur. `DIV`. Si la page web définit uniquement la largeur du conteneur `DIV`, sans restriction de hauteur, la visionneuse choisit automatiquement sa hauteur en fonction des proportions de la ressource utilisée. Cette fonctionnalité permet de s’assurer que la ressource s’intègre parfaitement dans la vue sans marge intérieure sur les côtés. Ce cas d’utilisation est le plus courant pour les pages web qui utilisent des structures de mise en page réactive telles que Bootstrap, Foundation, etc.

Sinon, si la page web définit la largeur et la hauteur du conteneur de la visionneuse. `DIV`, la visionneuse remplit uniquement cette zone et suit la taille fournie par la mise en page web. Un bon exemple consiste à incorporer la visionneuse dans une superposition modale, où la superposition est dimensionnée en fonction de la taille de la fenêtre du navigateur web.

**Incorporation de taille fixe**

Pour ajouter la visionneuse à une page web, procédez comme suit :

1. Ajout du fichier JavaScript de la visionneuse à votre page web.
1. Définition du conteneur DIV.
1. Définition de la taille de la visionneuse.
1. Création et initialisation de la visionneuse.

1. Ajout du fichier JavaScript de la visionneuse à votre page web.

   Pour créer une visionneuse, vous devez ajouter une balise de script dans l’en-tête du HTML. Avant d’utiliser l’API de visionneuse, veillez à inclure [!DNL eCatalogSearchViewer.js]. Le [!DNL eCatalogSearchViewer.js] se trouve sous le fichier [!DNL html5/js/] sous-dossier de votre déploiement IS-Viewers standard :

[!DNL <s7viewers_root>/html5/js/eCatalogSearchViewer.js]

Vous pouvez utiliser un chemin relatif si la visionneuse est déployée sur l’un des serveurs Dynamic Media Adobe et qu’elle est diffusée à partir du même domaine. Dans le cas contraire, vous spécifiez un chemin d’accès complet à l’un des serveurs Dynamic Media Adobe sur lesquels les visionneuses IS sont installées.

Le chemin relatif ressemble à ce qui suit :

```html {.line-numbers}
<script language="javascript" type="text/javascript" src="/s7viewers/html5/js/eCatalogSearchViewer.js"></script>
```

1. Définition du conteneur DIV.

   Ajoutez un élément DIV vide à la page sur laquelle vous souhaitez que la visionneuse apparaisse. L’ID de l’élément DIV doit être défini, car cet ID est transmis ultérieurement à l’API de visionneuse.

   L’espace réservé DIV est un élément positionné, ce qui signifie que la variable `position` La propriété CSS est définie sur `relative` ou `absolute`.

   Voici un exemple d’élément DIV d’espace réservé défini :

   ```html {.line-numbers}
   <div id="s7viewer" style="position:relative"></div>
   ```

1. Définition de la taille de la visionneuse

   Vous pouvez définir la taille statique de la visionneuse en la déclarant pour `.s7ecatalogsearchviewer` classe CSS de niveau supérieur en unités absolues ou en utilisant `stagesize` modifier.

   Vous pouvez placer le dimensionnement dans CSS directement sur la page de HTML ou dans un fichier CSS de visionneuse personnalisé, qui est ensuite affecté à un enregistrement de paramètre prédéfini de visionneuse dans Dynamic Media Classic, ou transmis explicitement à l’aide d’une commande de style.

   Voir [Personnalisation de la visionneuse de catalogue électronique](../../c-html5-s7-aem-asset-viewers/c-html5-20-ecatalog-viewer-about/c-html5-20-ecatalog-viewer-customizingviewer/c-html5-20-ecatalog-viewer-customizingviewer.md#concept-73a8546acdb444a387c49969ceca57d0) pour plus d’informations sur le style de la visionneuse avec CSS.

   Voici un exemple de définition d’une taille de visionneuse statique dans une page de HTML :

   ```html {.line-numbers}
   #s7viewer.s7ecatalogsearchviewer { 
    width: 640px; 
    height: 480px; 
   }
   ```

   Vous pouvez définir la variable `stagesize` modifier soit dans l’enregistrement de paramètre prédéfini de visionneuse dans Dynamic Media Classic, soit le transmettre explicitement avec le code d’initialisation de la visionneuse avec `params` ou sous la forme d’un appel API, comme décrit dans la section Référence de commande , comme suit :

   ```html {.line-numbers}
   eCatalogSearchViewer.setParam("stagesize", 
   "640,480");
   ```

1. Initialisation de la visionneuse.

   Une fois les étapes ci-dessus terminées, vous créez une instance de `s7viewers.eCatalogSearchViewer` , transmettez toutes les informations de configuration à son constructeur et appelez . `init()` sur une instance de visionneuse. Les informations de configuration sont transmises au constructeur sous la forme d’un objet JSON. Au minimum, cet objet a la propriété `containerId` champ contenant le nom de l’identifiant de conteneur de la visionneuse et imbriqué `params` Objet JSON avec des paramètres de configuration pris en charge par la visionneuse. Dans ce cas, la variable `params` doit comporter au moins l’URL du serveur d’images transmise comme `serverUrl` et la ressource initiale en tant que `asset` . L’API d’initialisation basée sur JSON vous permet de créer et de démarrer la visionneuse avec une seule ligne de code.

   Il est important que le conteneur de la visionneuse soit ajouté au modèle DOM afin que le code de la visionneuse puisse trouver l’élément de conteneur en fonction de son identifiant. Certains navigateurs retardent la création du DOM jusqu’à la fin de la page web. Toutefois, pour bénéficier d’une compatibilité maximale, appelez la fonction `init()` juste avant la fermeture `BODY` ou sur le corps `onload()` .

   De même, l’élément de conteneur ne doit pas nécessairement faire partie de la mise en page de la page web pour l’instant. Par exemple, il peut être masqué à l’aide de `display:none` style qui lui est affecté. Dans ce cas, la visionneuse retarde son processus d’initialisation jusqu’au moment où la page web ramène l’élément de conteneur à la mise en page. Dans ce cas, le chargement de la visionneuse reprend automatiquement.

   Voici un exemple de création d’une instance de visionneuse, de transmission des options de configuration minimales nécessaires au constructeur et d’appel de la fonction `init()` . L’exemple suppose que `eCatalogSearchViewer` est l’instance de visionneuse ; `s7viewer` est le nom de l’espace réservé. `DIV`; `https://s7d1.scene7.com/is/image/` est l’URL du serveur d’images, et `Viewers/Pluralist` est la ressource :

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

   Le code suivant est un exemple complet d’une page web triviale qui incorpore la visionneuse de recherche de catalogue électronique avec une taille fixe :

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

**Intégration de conception réactive avec une hauteur libre**

Avec l’incorporation de responsive design, la page web dispose normalement d’une sorte de disposition flexible qui détermine la taille d’exécution du conteneur de la visionneuse. `DIV`. Dans cet exemple, supposons que la page web autorise le conteneur de la visionneuse. `DIV` pour prendre 40 % de la taille de la fenêtre du navigateur web, sans restriction de sa hauteur. Le code de HTML de page web qui en résulte ressemble à ce qui suit :

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

L’ajout de la visionneuse à une telle page est similaire à l’incorporation d’une taille fixe, la seule différence étant que vous n’avez pas besoin de définir explicitement la taille de la visionneuse.

1. Ajout du fichier JavaScript de la visionneuse à votre page web.
1. Définition du conteneur DIV.
1. Création et initialisation de la visionneuse.

Toutes les étapes ci-dessus sont identiques à l’incorporation à taille fixe. Ajouter le conteneur `DIV` au &quot;détenteur&quot; existant `DIV`. Le code suivant est un exemple complet. Vous pouvez voir comment la taille de la visionneuse change lorsque le navigateur est redimensionné et comment le rapport d’aspect de la visionneuse correspond à la ressource.

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

La page d’exemples suivante illustre d’autres cas pratiques d’incorporation de conceptions réactives avec une hauteur illimitée :

[Démonstrations en direct](https://landing.adobe.com/en/na/dynamic-media/ctir-2755/live-demos.html)

**Intégration flexible de taille avec définition de largeur et de hauteur**

Dans le cas d’une incorporation à taille flexible avec des valeurs de largeur et de hauteur définies, le style de la page web est différent. En d’autres termes, il fournit les deux tailles au &quot; détenteur &quot;. `DIV` et le centre dans la fenêtre du navigateur. En outre, la page web définit la taille de la variable `HTML` et `BODY` à 100 % :

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

Les étapes d’incorporation restantes sont identiques à l’incorporation en responsive design avec une hauteur libre. L’exemple qui en résulte est le suivant :

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

**Incorporation à l’aide d’une API basée sur Setter**

Au lieu d’utiliser l’initialisation basée sur JSON, il est possible d’utiliser une API basée sur un setter et un constructeur sans argument. Avec , le constructeur d’API ne prend aucun paramètre et les paramètres de configuration sont spécifiés à l’aide de `setContainerId()`, `setParam()`, et `setAsset()` Méthodes d’API avec des appels JavaScript distincts.

L’exemple suivant illustre l’incorporation de tailles fixes avec une API basée sur setter :

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
