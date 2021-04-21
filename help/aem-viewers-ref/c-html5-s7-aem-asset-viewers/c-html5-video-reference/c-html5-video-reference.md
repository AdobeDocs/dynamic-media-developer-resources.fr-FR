---
description: La visionneuse vidéo est un lecteur vidéo qui lit la lecture en flux continu et la vidéo progressive codée au format H.264. Il est livré à partir de Dynamic Media Classic ou de AEM Dynamic Media.
keywords: réactif
solution: Experience Manager
title: Vidéo
feature: Dynamic Media Classic,Viewers,SDK/API,Video
role: Developer,Business Practitioner
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '2383'
ht-degree: 0%

---


# Vidéo{#video}

La visionneuse vidéo est un lecteur vidéo qui lit la lecture en flux continu et la vidéo progressive codée au format H.264. Il est livré à partir de Dynamic Media Classic ou de AEM Dynamic Media.

Voir [Configuration système requise et configuration requise](../../c-system-requirements-and-prerequisites.md#concept-9282e5b777de42cdaf72ef7ebd646842).

Les visionneuses de vidéos uniques et adaptatives sont prises en charge. En outre, le lecteur prend en charge l’utilisation de flux vidéo et HLS progressifs hébergés sur des emplacements externes. Il est conçu pour fonctionner à la fois sur les navigateurs Web mobiles et de bureau qui prennent en charge les vidéos HTML5. Cette visionneuse prend également en charge les sous-titres en option qui s’affichent au-dessus du contenu vidéo, de la navigation dans les chapitres vidéo et des outils de partage sur les réseaux sociaux.

La visionneuse vidéo utilise la lecture vidéo en flux continu HTML5 au format HLS dans sa configuration par défaut chaque fois que le système sous-jacent la prend en charge. Sur les systèmes qui ne prennent pas en charge la diffusion en flux continu HTML5, la visionneuse revient à la diffusion vidéo progressive HTML5.

Type de visionneuse 506.

## URL de la démonstration {#section-e1c3106f5b3e445d9b95be337c2f94e2}

[https://s7d9.scene7.com/s7viewers/html5/VideoViewer.html?asset=Scene7SharedAssets/Glacier_Climber_MP4](https://s7d9.scene7.com/s7viewers/html5/VideoViewer.html?asset=Scene7SharedAssets/Glacier_Climber_MP4)

## Utilisation de la visionneuse de vidéos {#section-f21ac23d3f6449ad9765588d69584772}

La visionneuse de vidéos représente un fichier JavaScript principal et un ensemble de fichiers d’aide : un seul fichier JavaScript inclut tous les composants du SDK de la visionneuse utilisés par cette visionneuse, les ressources et les fichiers CSS téléchargés par la visionneuse au moment de l’exécution.

Vous pouvez utiliser la visionneuse de vidéos en mode contextuel à l’aide de la page HTML prête pour la production fournie avec les visionneuses IS. Vous pouvez également utiliser le lecteur en mode intégré, où il est intégré dans une page Web de cible à l’aide de l’API documentée.

La tâche de configuration et d’habillage de la visionneuse est similaire à celle des autres visionneuses. L’habillage est effectué au moyen d’une page CSS personnalisée.

Voir [Référence de commande commune à toutes les visionneuses - Attributs de configuration](../../r-html5-viewer-20-cmdref-configattrib/r-html5-viewer-20-cmdref-configattrib.md#concept-850e0f2c49b949deb7cfbfd330d329bd) et [Référence de commande commune à toutes les visionneuses - URL](../../c-html5-viewer-20-cmdref-url/c-html5-viewer-20-cmdref-url.md#concept-9b337f349b7b406b8c33c7ee96b3e226)

## Interaction avec la visionneuse de vidéos {#section-ab66eb6955aa4a8aa6d14a3b3acfed3f}

La visionneuse de vidéos fournit un ensemble de commandes standard de l’interface utilisateur pour la lecture vidéo, telles qu’un bouton de lecture/pause, une bulle de temps vidéo de la barre de défilement vidéo, un indicateur de temps de lecture/temps total, un contrôle du volume, un bouton plein écran et un bouton de sous-titrage fermé. Tous ces contrôles sont regroupés dans une barre de contrôle au bas de l’interface utilisateur du lecteur de contenu.

Sur les périphériques tactiles, le contrôle du volume est masqué dans l&#39;interface utilisateur, car il est possible de contrôler uniquement le volume à l&#39;aide des boutons matériels.

Lorsque le lecteur fonctionne en mode contextuel, le bouton plein écran n’est pas disponible dans l’interface utilisateur.

Il est possible de parcourir rapidement le contenu d’une vidéo lorsque le chapitre vidéo est activé. Les chapitres vidéo s’affichent sous la forme de marqueurs dans la piste de défilement vidéo et affichent le titre du chapitre et la description associée lors d’un roulement de la souris ou d’un simple appui sur les systèmes tactiles. Les utilisateurs peuvent rechercher un chapitre particulier en cliquant sur un marqueur de chapitre ou en appuyant sur la bulle de description de chapitre.

Le lecteur prend en charge les entrées tactiles et de souris sur les périphériques Windows dotés d’un écran tactile et d’une souris. Toutefois, cette prise en charge est limitée aux navigateurs Web Chrome, Internet Explorer 11 et Edge uniquement.

Cette visionneuse est entièrement accessible au clavier.

Voir [Accessibilité du clavier et navigation](../../c-keyboard-accessibility.md#topic-f5650e9493404e55a3627c8d1366b861).

## Outils de partage sur les réseaux sociaux avec la visionneuse de vidéos {#section-907d316fe1da4b87abb9775f02464704}

La visionneuse de vidéos prend en charge les outils de partage sur les réseaux sociaux. Elle est disponible sous la forme d’un bouton unique dans l’interface utilisateur, qui s’étend dans une barre d’outils de partage lorsque l’utilisateur clique ou appuie dessus.

La barre d’outils de partage contient une icône pour chaque type de canal de partage pris en charge, tel que Facebook, Twitter, le partage de courrier électronique, le partage de code incorporé et le partage de liens. Lorsque des outils de partage de courrier électronique, de partage incorporé ou de partage de liens sont activés, le lecteur affiche une boîte de dialogue modale avec un formulaire de saisie de données correspondant. Lorsque Facebook ou Twitter sont appelés, le lecteur redirige l’utilisateur vers une boîte de dialogue de partage standard à partir d’un service de médias sociaux. En outre, lorsqu’un outil de partage est activé, la lecture vidéo est automatiquement suspendue.

Les outils de partage ne sont pas disponibles en mode plein écran en raison des restrictions de sécurité du navigateur Web.

## Incorporation de la visionneuse vidéo {#section-6bb5d3c502544ad18a58eafe12a13435}

Différentes pages Web ont des besoins différents en ce qui concerne le comportement des visiteurs. Il arrive qu’une page Web fournisse un lien qui, lorsqu’un utilisateur clique dessus, ouvre le lecteur dans une fenêtre de navigateur distincte. Dans d’autres cas, il est nécessaire d’incorporer la visionneuse directement sur la page d’hébergement. Dans ce dernier cas, la page Web peut avoir une mise en page statique ou utiliser une conception adaptée qui s’affiche différemment sur différents périphériques ou pour différentes tailles de fenêtre de navigateur. Pour répondre à ces besoins, le lecteur prend en charge trois modes de fonctionnement Principaux : fenêtre contextuelle, incorporation de taille fixe et incorporation de conception adaptée.

L’incorporation de plusieurs vidéos sur une même page est prise en charge sur les tablettes et les périphériques mobiles. Dans la plupart des cas, une seule vidéo peut être lue à la fois. Lorsqu’un utilisateur début la lecture d’une vidéo, puis tente de la lire, la première vidéo est automatiquement mise en pause. La vidéo en pause automatique mémorise son heure de lecture actuelle, de sorte que l’utilisateur puisse toujours y revenir et reprendre la lecture. La seule exception à cette règle est le navigateur Chrome sur les appareils Android 4.x, qui peuvent lire des vidéos en parallèle.

**A propos du mode contextuel**

En mode contextuel, le lecteur s’ouvre dans une fenêtre ou un onglet distinct du navigateur Web. Il prend toute la zone de la fenêtre du navigateur et s’ajuste au cas où le navigateur serait redimensionné ou où l’orientation du périphérique serait modifiée.

Ce mode est le plus courant pour les périphériques mobiles. La page Web charge la visionneuse à l’aide de l’appel JavaScript `window.open()`, d’un élément HTML `A` correctement configuré ou de toute autre méthode appropriée.

Il est recommandé d’utiliser une page HTML prête à l’emploi pour le mode d’opération contextuel. Il s’appelle [!DNL VideoViewer.html] et se trouve sous le sous-dossier [!DNL html5/] de votre déploiement des visionneuses IS standard :

[!DNL <s7viewers_root>/html5/VideoViewer.html]

Vous pouvez réaliser la personnalisation visuelle en appliquant une page CSS personnalisée.

Voici un exemple de code HTML qui ouvre la visionneuse dans une nouvelle fenêtre :

```
<a href="http://s7d1.scene7.com/s7viewers/html5/VideoViewer.html?asset=Scene7SharedAssets/Glacier_Climber_MP4" target="_blank">Open popup viewer</a>
```

**A propos du mode d&#39;incorporation de taille fixe et du mode d&#39;incorporation réactif**

En mode incorporé, le lecteur est ajouté à la page Web existante, qui peut déjà contenir du contenu client qui n’est pas lié au lecteur. En règle générale, le lecteur n’occupe qu’une partie de l’espace de la page Web.

Les cas d’utilisation Principaux sont les pages Web orientées vers les ordinateurs de bureau ou les tablettes, ainsi que les pages de conception réactives qui ajustent automatiquement la mise en page en fonction du type de périphérique.

L’incorporation de taille fixe est utilisée lorsque la visionneuse ne change pas de taille après le chargement initial. Ce choix est le meilleur pour les pages Web présentant une mise en page statique.

L’incorporation de la conception réactive suppose que la visionneuse doit peut-être être redimensionnée au moment de l’exécution en raison du changement de taille de son conteneur `DIV`. Le cas d’utilisation le plus courant consiste à ajouter la visionneuse à une page Web qui utilise une disposition de page souple.

En mode d’incorporation des conceptions réactives, le lecteur se comporte différemment selon la manière dont la page Web dimensionne son conteneur `DIV`. Si la page Web ne définit que la largeur du conteneur `DIV`, en ne limitant pas sa hauteur, le lecteur sélectionne automatiquement sa hauteur en fonction des proportions du fichier utilisé. Cette méthode permet de s’assurer que la ressource s’intègre parfaitement à la vue sans remplissage sur les côtés. Ce cas d’utilisation est le plus courant pour les pages Web qui utilisent une structure de mise en page adaptée telle que Bootstrap, Foundation, etc.

Dans le cas contraire, si la page Web définit à la fois la largeur et la hauteur du conteneur du lecteur `DIV`, celui-ci remplit cette zone et suit la taille indiquée par la disposition de la page Web. Un bon exemple est l’incorporation de la visionneuse dans une incrustation modale, où l’incrustation est dimensionnée en fonction de la taille de la fenêtre du navigateur Web.

**Incorporation de taille fixe**

Pour ajouter la visionneuse à une page Web, procédez comme suit :

1. Ajouter le fichier JavaScript de la visionneuse sur votre page Web.
1. Définition du conteneur `DIV`.
1. Définition de la taille de la visionneuse.
1. Création et initialisation de la visionneuse.

1. Ajouter le fichier JavaScript de la visionneuse sur votre page Web.

   Pour créer une visionneuse, vous devez ajouter une balise de script dans l’en-tête HTML. Avant de pouvoir utiliser l’API du lecteur de contenu, veillez à inclure [!DNL FlyoutViewer.js]. Le fichier [!DNL FlyoutViewer.js] se trouve sous le sous-dossier [!DNL html5/js/] de votre déploiement des visionneuses IS standard :

[!DNL <s7viewers_root>/html5/js/FlyoutViewer.js]

Vous pouvez utiliser un chemin relatif si la visionneuse est déployée sur l’un des serveurs Dynamic Media Classic de l’Adobe et qu’elle est diffusée à partir du même domaine. Sinon, vous spécifiez un chemin d’accès complet à l’un des serveurs Dynamic Media Classic Adobe sur lesquels les visionneuses IS sont installées.

Le chemin relatif ressemble à ce qui suit :

```
<script language="javascript" type="text/javascript" src="/s7viewers/html5/js/VideoViewer.js"></script>
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
   <div id="s7viewer" style="position:relative;width:640px;height:360px;"></div> 
   ```

1. Définition de la taille de la visionneuse

   Vous pouvez définir la taille statique de la visionneuse en la déclarant pour la classe CSS de niveau supérieur `.s7videoviewer` en unités absolues ou en utilisant le modificateur `stagesize`.

   Le dimensionnement en CSS peut être placé directement sur la page HTML ou dans un fichier CSS de visionneuse personnalisée, qui est ultérieurement affecté à un enregistrement de paramètre prédéfini de visionneuse dans Dynamic Media Classic ou transmis explicitement à l’aide d’une commande de style.

   Voir [Personnalisation de la visionneuse de vidéos](../../c-html5-s7-aem-asset-viewers/c-html5-video-reference/c-html5-video-viewer-20-customizingviewer/c-html5-video-viewer-20-customizingviewer.md#concept-072a52b10b5f4c0789393dc6e2134c0e) pour plus d’informations sur le style de la visionneuse à l’aide de CSS.

   Voici un exemple de définition de la taille d’une visionneuse statique dans une page HTML :

   ```
   #s7viewer.s7videoviewer { 
    width: 640px; 
    height: 480px; 
   }
   ```

   Vous pouvez définir le modificateur `stagesize` soit dans l’enregistrement de paramètre prédéfini de la visionneuse dans Dynamic Media Classic, soit le transmettre explicitement au code d’initialisation de la visionneuse avec la collection `params`, soit en tant qu’appel d’API comme décrit dans la section de référence Commande, comme dans l’exemple suivant :

   ```
   videoViewer.setParam("stagesize", "640,480");
   ```

   Une approche CSS est recommandée et est utilisée dans cet exemple.

1. Création et initialisation de la visionneuse.

   Une fois les étapes ci-dessus terminées, vous créez une instance de classe `s7viewers.VideoViewer`, transmettez toutes les informations de configuration à son constructeur et appelez la méthode `init()` sur une instance de lecteur. Les informations de configuration sont transmises au constructeur sous la forme d’un objet JSON. Au minimum, cet objet doit comporter un champ `containerId` contenant le nom de l’ID de conteneur de la visionneuse et un objet JSON imbriqué `params` avec les paramètres de configuration pris en charge par la visionneuse. Dans ce cas, l’objet `params` doit comporter au moins la propriété Image Serving URL transmise sous la forme `serverUrl`, l’URL du serveur vidéo transmise sous la forme `videoserverurl` et le paramètre initial asset sous la forme `asset`. L’API d’initialisation basée sur JSON vous permet de créer et de début le lecteur avec une seule ligne de code.

   Il est important que le conteneur de la visionneuse soit ajouté au modèle DOM afin que le code de la visionneuse puisse trouver l’élément de conteneur en fonction de son identifiant. Certains navigateurs retardent la création du modèle DOM jusqu’à la fin de la page Web. Pour une compatibilité maximale, appelez la méthode `init()` juste avant la balise de fermeture `BODY` ou sur le événement body `onload()`.

   Dans le même temps, l’élément conteneur ne doit pas nécessairement faire partie de la mise en page de la page Web pour le moment. Par exemple, il peut être masqué à l’aide du style `display:none` qui lui est affecté. Dans ce cas, le lecteur retarde son processus d’initialisation jusqu’au moment où la page Web ramène l’élément de conteneur à la mise en page. Dans ce cas, le chargement du lecteur reprend automatiquement.

   Voici un exemple de création d’une instance de visionneuse, de transmission des options de configuration minimales nécessaires au constructeur et d’appel de la méthode `init()`. Cet exemple suppose que `videoViewer` correspond à l’instance de visionneuse, `s7viewer` au nom de l’espace réservé `DIV`, [!DNL http://s7d1.scene7.com/is/image/] à l’URL de diffusion d’images, [!DNL http://s7d1.scene7.com/is/content/] à l’URL du serveur vidéo et [!DNL Scene7SharedAssets/Glacier_Climber_MP4] à l’actif.

   ```
   <script type="text/javascript"> 
   var videoViewer = new s7viewers.VideoViewer({ 
    "containerId":"s7viewer", 
   "params":{ 
    "asset":"Scene7SharedAssets/Glacier_Climber_MP4", 
    "serverurl":"http://s7d1.scene7.com/is/image/", 
    "videoserverurl":"http://s7d1.scene7.com/is/content/" 
   } 
   }).init(); 
   </script> 
   ```

   Le code suivant est un exemple complet d’une page Web triviale qui incorpore la visionneuse de vidéos à une taille fixe :

   ```
   <!DOCTYPE html> 
   <html> 
   <head> 
   <script type="text/javascript" src="http://s7d1.scene7.com/s7viewers/html5/js/VideoViewer.js"></script> 
   <style type="text/css"> 
   #s7viewer.s7videoviewer { 
    width: 640px; 
    height: 480px; 
   } 
   </style> 
   </head> 
   <body> 
   <div id="s7viewer" style="position:relative;width:640px;height:360px;"></div> 
   <script type="text/javascript"> 
   var videoViewer = new s7viewers.VideoViewer({ 
    "containerId":"s7viewer", 
   "params":{ 
    "asset":"Scene7SharedAssets/Glacier_Climber_MP4", 
    "serverurl":"http://s7d1.scene7.com/is/image/", 
    "videoserverurl":"http://s7d1.scene7.com/is/content/" 
   } 
   }).init(); 
   </script> 
   </body> 
   </html> 
   ```

**Incorporation de conception réactive avec une hauteur libre**

Grâce à l’intégration de la conception adaptée, la page Web dispose normalement d’une sorte de disposition souple qui détermine la taille d’exécution du conteneur `DIV` du lecteur. Pour les besoins de cet exemple, supposons que la page Web permette au conteneur `DIV` du lecteur de prendre 40 % de la taille de la fenêtre du navigateur Web, en laissant sa hauteur libre. Le code HTML de la page Web se présenterait comme suit :

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

Ajouter le lecteur à une telle page est très similaire à la taille fixe incorporée ; la seule différence est que vous n’avez pas besoin de définir explicitement la taille de la visionneuse.

1. Ajouter le fichier JavaScript de la visionneuse sur votre page Web.
1. Définition de la balise DIV de conteneur.
1. Création et initialisation de la visionneuse.

Toutes les étapes ci-dessus sont identiques à celles de l’incorporation de taille fixe. Ajoutez le conteneur `DIV` au &quot; détenteur&quot; `DIV` existant. Le code suivant est un exemple complet. Vous pouvez voir comment la taille de la visionneuse change lorsque le navigateur est redimensionné et comment les proportions de la visionneuse correspondent à la ressource.

```
<!DOCTYPE html> 
<html> 
<head> 
<script type="text/javascript" src="http://s7d1.scene7.com/s7viewers/html5/js/VideoViewer.js"></script> 
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
var videoViewer = new s7viewers.VideoViewer({ 
 "containerId":"s7viewer", 
"params":{ 
 "asset":"Scene7SharedAssets/Glacier_Climber_MP4", 
 "serverurl":"http://s7d1.scene7.com/is/image/", 
 "videoserverurl":"http://s7d1.scene7.com/is/content/" 
} 
}).init(); 
</script> 
</body> 
</html> 
```

La page d’exemples suivante illustre une utilisation plus concrète de la conception adaptée incorporée avec une hauteur illimitée :

[Démonstrations en direct](https://landing.adobe.com/en/na/dynamic-media/ctir-2755/live-demos.html)

<!-- KEEP (https://marketing.adobe.com/resources/help/en_US/s7/vlist/vlist.html) -->

**Incorporation réactive de la conception avec définition de la largeur et de la hauteur**

Dans le cas d’une conception adaptée incorporée avec des valeurs de largeur et de hauteur définies, le style de la page Web est différent ; il fournit les deux tailles au &quot;détenteur&quot; `DIV` et le centre dans la fenêtre du navigateur. En outre, la page Web définit la taille des éléments `HTML` et `BODY` sur 100 % :

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

Les étapes d’incorporation restantes sont identiques à celles d’incorporation de conception adaptée avec une hauteur libre. L’exemple qui en résulte est le suivant :

```
<!DOCTYPE html> 
<html> 
<head> 
<script type="text/javascript" src="http://s7d1.scene7.com/s7viewers/html5/js/VideoViewer.js"></script> 
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
var videoViewer = new s7viewers.VideoViewer({ 
 "containerId":"s7viewer", 
"params":{ 
 "asset":"Scene7SharedAssets/Glacier_Climber_MP4", 
 "serverurl":"http://s7d1.scene7.com/is/image/", 
 "videoserverurl":"http://s7d1.scene7.com/is/content/" 
} 
}).init(); 
</script> 
</body> 
</html> 
```

**Incorporation à l’aide de l’API basée sur Setter**

Au lieu d’utiliser l’initialisation basée sur JSON, il est possible d’utiliser une API basée sur un setter et un constructeur sans args. Avec cette API, le constructeur ne prend aucun paramètre et les paramètres de configuration sont spécifiés à l&#39;aide des méthodes d&#39;API `setContainerId()`, `setParam()` et `setAsset()` avec des appels JavaScript distincts.

L’exemple suivant illustre l’incorporation de tailles fixes avec l’API basée sur un setter :

```
<!DOCTYPE html> 
<html> 
<head> 
<script type="text/javascript" src="http://s7d1.scene7.com/s7viewers/html5/js/VideoViewer.js"></script> 
<style type="text/css"> 
#s7viewer.s7videoviewer { 
 width: 640px; 
 height: 480px; 
} 
</style> 
</head> 
<body> 
<div id="s7viewer" style="position:relative;width:640px;height:360px;"></div> 
<script type="text/javascript"> 
var videoViewer = new s7viewers.VideoViewer(); 
videoViewer.setContainerId("s7viewer"); 
videoViewer.setParam("serverurl", "http://s7d1.scene7.com/is/image/"); 
videoViewer.setParam("videoserverurl", "http://s7d1.scene7.com/is/content/"); 
videoViewer.setAsset("Scene7SharedAssets/Glacier_Climber_MP4"); 
videoViewer.init(); 
</script> 
</body> 
</html> 
```

