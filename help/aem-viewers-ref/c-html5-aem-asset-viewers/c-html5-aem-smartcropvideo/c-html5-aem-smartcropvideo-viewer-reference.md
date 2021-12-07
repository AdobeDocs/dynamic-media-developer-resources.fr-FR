---
title: Recadrage intelligent de la visionneuse vidéo
description: La visionneuse de vidéos de recadrage intelligent est un lecteur vidéo qui lit la vidéo en flux continu et progressive codée au format H.264 avec l’ajout de la prise en charge du recadrage intelligent. Elle est fournie à partir de Dynamic Media Classic ou d’Adobe Experience Manager avec Dynamic Media.
keywords: responsive
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Smart Crop,Video
role: Developer,User
source-git-commit: 2dc7b92da6c73a328a82c50dc5a052a3351ee2dc
workflow-type: tm+mt
source-wordcount: '2413'
ht-degree: 0%

---

# Recadrage intelligent de la vidéo{#smart-crop-video}

La visionneuse de vidéos de recadrage intelligent est un lecteur vidéo qui lit la vidéo en flux continu et progressive codée au format H.264 avec l’ajout de la prise en charge du recadrage intelligent. Elle est fournie à partir de Dynamic Media Classic ou de Experience Manager avec Dynamic Media.

Voir [Configuration requise et conditions préalables](../../c-system-requirements-and-prerequisites.md#concept-9282e5b777de42cdaf72ef7ebd646842).

Les visionneuses de vidéos uniques et adaptatives sont prises en charge. En outre, la visionneuse prend en charge l’utilisation de flux vidéo progressive et HLS hébergés sur des emplacements externes. Il est conçu pour fonctionner à la fois sur les navigateurs de bureau et les navigateurs Web mobiles qui prennent en charge la vidéo HTML5. Cette visionneuse prend également en charge les sous-titres facultatifs qui s’affichent au-dessus du contenu vidéo, de la navigation dans les chapitres vidéo et des outils de partage sur les médias sociaux.

La visionneuse de vidéos avec recadrage intelligent utilise la lecture vidéo en continu HTML5 au format HLS dans sa configuration par défaut chaque fois que le système sous-jacent la prend en charge. Sur les systèmes qui ne prennent pas en charge la diffusion HTML5, la visionneuse revient à la diffusion vidéo progressive par HTML5.

Type de visionneuse 518.

## URL de démonstration {#section-e1c3106f5b3e445d9b95be337c2f94e2}

[https://s7d9.scene7.com/s7viewers/html5/SmartCropVideoViewer.html?asset=html5automation/frisbee-AVS](https://s7d9.scene7.com/s7viewers/html5/SmartCropVideoViewer.html?asset=html5automation/frisbee-AVS)

## Utilisation de la visionneuse de vidéos avec recadrage intelligent {#section-f21ac23d3f6449ad9765588d69584772}

La visionneuse vidéo avec recadrage intelligent représente un fichier JavaScript principal et un ensemble de fichiers d’assistance, un seul code JavaScript comprenant tous les composants du SDK de la visionneuse utilisés par cette visionneuse, ces ressources et les fichiers CSS téléchargés par la visionneuse au moment de l’exécution.

Vous pouvez utiliser la visionneuse de vidéos de recadrage intelligent en mode pop-up à l’aide de la page de HTML prête pour la production fournie avec les visionneuses IS. Vous pouvez également utiliser la visionneuse en mode incorporé, où elle est intégrée dans une page web cible à l’aide de l’API documentée.

La configuration et l’habillage de la visionneuse sont similaires à d’autres visionneuses. L’habillage est effectué au moyen d’une feuille CSS personnalisée.

Voir [Référence de commande commune à toutes les visionneuses - Attributs de configuration](../../r-html5-viewer-20-cmdref-configattrib/r-html5-viewer-20-cmdref-configattrib.md#concept-850e0f2c49b949deb7cfbfd330d329bd) et [Référence de commande commune à toutes les visionneuses - URL](../../c-html5-viewer-20-cmdref-url/c-html5-viewer-20-cmdref-url.md#concept-9b337f349b7b406b8c33c7ee96b3e226)

## Interaction avec la visionneuse de vidéos avec recadrage intelligent {#section-ab66eb6955aa4a8aa6d14a3b3acfed3f}

La visionneuse de vidéos avec recadrage intelligent fournit un ensemble de commandes d’interface utilisateur standard pour la lecture vidéo, telles que :

* Bouton Lecture/Pause .
* Blocage vidéo : bulle de temps vidéo.
* Indicateur de temps de lecture/temps total.
* Contrôle du volume.
* Bouton Plein écran.
* Bascule des sous-titres codés.

Tous ces contrôles sont regroupés dans une barre de contrôle au bas de l’interface utilisateur de la visionneuse.

Sur les périphériques tactiles, la commande de volume est masquée dans l’interface utilisateur, car il est uniquement possible de contrôler le volume à l’aide des boutons matériels.

Lorsque la visionneuse fonctionne en mode pop-up, le bouton plein écran n’est pas disponible dans l’interface utilisateur.

Il est possible de parcourir rapidement le contenu d’une vidéo lorsque le chapitre vidéo est activé. Les chapitres vidéo s’affichent sous la forme de marqueurs dans le suivi de la barre de défilement vidéo et affichent le titre du chapitre et la description associée au survol d’une souris ou en appuyant une seule fois sur les systèmes tactiles. Les utilisateurs peuvent accéder à un chapitre spécifique en sélectionnant un marqueur de chapitre ou en sélectionnant la bulle de description du chapitre.

La visionneuse prend en charge les entrées tactile et de souris sur les périphériques Windows dotés d’un écran tactile et d’une souris. Toutefois, cette prise en charge est limitée aux navigateurs Chrome, Internet Explorer 11 et Edge uniquement.

Cette visionneuse est entièrement accessible au clavier.

Voir [Accessibilité du clavier et navigation](../../c-keyboard-accessibility.md#topic-f5650e9493404e55a3627c8d1366b861).

## Outils de partage sur les médias sociaux avec la visionneuse vidéo avec recadrage intelligent {#section-907d316fe1da4b87abb9775f02464704}

La visionneuse vidéo avec recadrage intelligent prend en charge les outils de partage sur les médias sociaux. Ils sont disponibles sous la forme d’un bouton unique dans l’interface utilisateur qui se développe dans une barre d’outils de partage lorsque l’utilisateur clique ou appuie dessus.

La barre d’outils de partage contient une icône pour chaque type de canal de partage pris en charge, tel que Facebook, Twitter, partage d’email, partage de code incorporé et partage de lien. Lorsque des outils de partage de courrier électronique, d’intégration de partage ou de lien sont activés, la visionneuse affiche une boîte de dialogue modale avec un formulaire de saisie de données correspondant. Lors de l’appel de Facebook ou Twitter, la visionneuse redirige l’utilisateur vers une boîte de dialogue de partage standard à partir d’un service de médias sociaux. En outre, lorsqu’un outil de partage est activé, la lecture vidéo est automatiquement suspendue.

Les outils de partage ne sont pas disponibles en mode plein écran en raison des restrictions de sécurité du navigateur web.

## Incorporation de la visionneuse de vidéos avec recadrage intelligent {#section-6bb5d3c502544ad18a58eafe12a13435}

Le comportement de la visionneuse varie en fonction des pages web. Il arrive qu’une page web fournisse un lien qui, lorsqu’il est sélectionné, ouvre la visionneuse dans une fenêtre de navigateur distincte. Dans d’autres cas, il est nécessaire d’incorporer directement la visionneuse sur la page d’hébergement. Dans ce cas, la page web peut avoir une mise en page statique ou utiliser une conception réactive qui s’affiche différemment sur différents appareils ou pour différentes tailles de fenêtre de navigateur. Pour répondre à ces besoins, la visionneuse prend en charge trois modes de fonctionnement Principaux : fenêtre contextuelle, incorporation de taille fixe et incorporation de conceptions réactives.

L’incorporation de plusieurs vidéos sur la même page est prise en charge sur les tablettes et les appareils mobiles. En règle générale, une seule vidéo peut être lue à la fois. Lorsqu’un utilisateur commence la lecture d’une vidéo, puis tente de la lire, la première vidéo est automatiquement suspendue. La vidéo qui a été mise en pause automatique mémorise son temps de lecture actuel, de sorte que l’utilisateur puisse toujours y revenir et reprendre la lecture. La seule exception à cette règle est le navigateur Chrome sur les appareils Android™ 4.x, qui peuvent lire des vidéos en parallèle.

**A propos du mode pop-up**

En mode contextuel, la visionneuse s’ouvre dans une fenêtre ou un onglet de navigateur Web distinct. Il prend toute la zone de la fenêtre du navigateur et s’ajuste au cas où le navigateur serait redimensionné ou où l’orientation du périphérique serait modifiée.

Ce mode est le plus courant pour les appareils mobiles. La page web charge la visionneuse à l’aide de `window.open()` Appel JavaScript, correctement configuré `A` élément de HTML ou toute autre méthode appropriée.

Il est recommandé d’utiliser une page de HTML d’usine pour le mode de fonctionnement de la fenêtre contextuelle. Elle s’appelle [!DNL SmartCropVideoViewer.html] et se trouve sous le noeud [!DNL html5/] sous-dossier de votre déploiement IS-Viewers standard :

[!DNL <s7viewers_root>/html5/SmartCropVideoViewer.html]

Vous pouvez effectuer une personnalisation visuelle en appliquant une page CSS personnalisée.

Voici un exemple de code de HTML qui ouvre la visionneuse dans une nouvelle fenêtre :

```
<a href="http://s7d1.scene7.com/s7viewers/html5/SmartCropVideoViewer.html?asset=html5automation/frisbee-AVS" target="_blank">Open popup viewer</a>
```

**À propos du mode d’incorporation à taille fixe et du mode d’incorporation réactif**

En mode incorporé, la visionneuse est ajoutée à la page web existante, qui peut déjà comporter du contenu client non lié à la visionneuse. Normalement, la visionneuse n’occupe qu’une partie de l’emplacement de la page web.

Les cas d’utilisation Principaux sont les pages web orientées vers les ordinateurs de bureau ou les tablettes, ainsi que les pages de conception réactive qui ajustent automatiquement la mise en page en fonction du type d’appareil.

L’incorporation des tailles fixes est utilisée lorsque la visionneuse ne modifie pas sa taille après le chargement initial. Ce choix est idéal pour les pages web ayant une mise en page statique.

L’incorporation de conceptions réactives suppose que la visionneuse doit être redimensionnée au moment de l’exécution en réponse au changement de taille de son conteneur. `DIV`. Le cas d’utilisation le plus courant consiste à ajouter la visionneuse à une page web qui utilise une mise en page flexible.

En mode d’incorporation de responsive design, la visionneuse se comporte différemment selon la manière dont la page web dimensionne son conteneur. `DIV`. Si la page web définit uniquement la largeur du conteneur `DIV`, sans restriction de hauteur, la visionneuse choisit automatiquement sa hauteur en fonction des proportions de la ressource utilisée. Cette méthode permet de s’assurer que la ressource s’intègre parfaitement dans la vue sans marge intérieure sur les côtés. Ce cas d’utilisation est le plus courant pour les pages web qui utilisent une structure de mise en page en responsive design telle que Bootstrap ou Foundation.

Sinon, si la page web définit la largeur et la hauteur du conteneur de la visionneuse. `DIV`, la visionneuse remplit cette zone et suit la taille fournie par la mise en page web. Un bon exemple consiste à incorporer la visionneuse dans une superposition modale, où la superposition est dimensionnée en fonction de la taille de la fenêtre du navigateur web.

**Incorporation de taille fixe**

Pour ajouter la visionneuse à une page web, procédez comme suit :

1. Ajout du fichier JavaScript de la visionneuse à votre page web.
1. Définir le conteneur `DIV`.
1. Définition de la taille de la visionneuse.
1. Création et initialisation de la visionneuse.

1. Ajout du fichier JavaScript de la visionneuse à votre page web.

   Pour créer une visionneuse, vous devez ajouter une balise de script dans l’en-tête du HTML. Avant d’utiliser l’API de visionneuse, veillez à inclure [!DNL SmartCropVideoViewer.js]. Le [!DNL SmartCropVideoViewer.js] se trouve sous le fichier [!DNL html5/js/] sous-dossier de votre déploiement IS-Viewers standard :

[!DNL <s7viewers_root>/html5/js/SmartCropVideoViewer.js]

Vous pouvez utiliser un chemin relatif si la visionneuse est déployée sur l’un des serveurs Adobe Dynamic Media Classic et qu’elle est diffusée à partir du même domaine. Dans le cas contraire, vous spécifiez un chemin d’accès complet à l’un des serveurs Adobe Dynamic Media Classic sur lesquels les visionneuses IS sont installées.

Le chemin relatif ressemble à ce qui suit :

```
<script language="javascript" type="text/javascript" src="/s7viewers/html5/js/SmartCropVideoViewer.js"></script>
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

   ```
   <div id="s7viewer" style="position:relative;width:640px;height:360px;"></div> 
   ```

1. Définition de la taille de la visionneuse

   Vous pouvez définir la taille statique de la visionneuse en la déclarant pour `.s7videoviewer` classe CSS de niveau supérieur en unités absolues ou en utilisant le modificateur `stagesize`.

   Vous pouvez placer le dimensionnement dans CSS directement sur la page de HTML ou dans un fichier CSS de visionneuse personnalisé. Il est ensuite affecté à un enregistrement de paramètre prédéfini de visionneuse dans Dynamic Media Classic ou transmis explicitement à l’aide d’une commande de style.

   Voir [Personnalisation de la visionneuse de vidéos avec recadrage intelligent](../../c-html5-s7-aem-asset-viewers/c-html5-video-reference/c-html5-video-viewer-20-customizingviewer/c-html5-video-viewer-20-customizingviewer.md#concept-072a52b10b5f4c0789393dc6e2134c0e) pour plus d’informations sur le style de la visionneuse à l’aide de CSS.

   Voici un exemple de définition d’une taille de visionneuse statique dans une page de HTML :

   ```
   #s7viewer.s7videoviewer { 
    width: 640px; 
    height: 480px; 
   }
   ```

   Vous pouvez définir `stagesize` modifier soit dans l’enregistrement de paramètre prédéfini de visionneuse dans Dynamic Media Classic, soit le transmettre explicitement avec le code d’initialisation de la visionneuse avec `params` collection. Ou, sous la forme d’un appel API, comme décrit dans la section Référence de commande, comme dans l’exemple suivant :

   ```
   smartCropVideoViewer.setParam("stagesize", "640,480");
   ```

   Une approche basée sur CSS est recommandée et est utilisée dans cet exemple.

1. Création et initialisation de la visionneuse.

   Une fois les étapes ci-dessus terminées, vous créez une instance de `s7viewers.SmartCropVideoViewer` , transmettez toutes les informations de configuration à son constructeur, et appelez `init()` sur une instance de visionneuse. Les informations de configuration sont transmises au constructeur sous la forme d’un objet JSON. Au minimum, cet objet doit avoir la valeur `containerId` champ contenant le nom de l’identifiant de conteneur de la visionneuse et imbriqué `params` Objet JSON avec des paramètres de configuration pris en charge par la visionneuse. Dans ce cas, `params` doit comporter au moins l’URL du serveur d’images transmise comme `serverUrl` propriété, URL du serveur vidéo transmise en tant que `videoserverurl` et la ressource initiale en tant que `asset` . L’API d’initialisation basée sur JSON vous permet de créer et de démarrer la visionneuse avec une seule ligne de code.

   Il est important que le conteneur de la visionneuse soit ajouté au modèle DOM afin que le code de la visionneuse puisse trouver l’élément de conteneur en fonction de son identifiant. Certains navigateurs retardent la création du DOM jusqu’à la fin de la page web. Pour une compatibilité maximale, appelez la méthode `init()` juste avant la fermeture `BODY` ou sur le corps `onload()` .

   Dans le même temps, l’élément de conteneur ne doit pas nécessairement faire partie de la mise en page web pour l’instant. Par exemple, il peut être masqué à l’aide de `display:none` style qui lui est affecté. Dans ce cas, la visionneuse retarde son processus d’initialisation jusqu’au moment où la page web ramène l’élément de conteneur à la mise en page. Lorsque cette action se produit, le chargement de la visionneuse reprend automatiquement.

   Voici un exemple de création d’une instance de visionneuse, de transmission des options de configuration minimales nécessaires au constructeur et d’appel de la fonction `init()` . Cet exemple suppose que `smartCropVideoViewer` est l’instance de visionneuse, `s7viewer` est le nom de l’espace réservé. `DIV`, [!DNL http://s7d1.scene7.com/is/image/] est l’URL du serveur d’images, [!DNL http://s7d1.scene7.com/is/content/] est l’URL du serveur vidéo, et [!DNL html5automation/frisbee-AVS] est la ressource.

   ```
   <script type="text/javascript"> 
   var smartCropVideoViewer = new s7viewers.SmartCropVideoViewer({ 
    "containerId":"s7viewer", 
   "params":{ 
    "asset":"html5automation/frisbee-AVS", 
    "serverurl":"http://s7d1.scene7.com/is/image/", 
    "videoserverurl":"http://s7d1.scene7.com/is/content/" 
   } 
   }).init(); 
   </script> 
   ```

   Le code suivant est un exemple complet d’une page web triviale qui incorpore la visionneuse vidéo avec recadrage intelligent avec une taille fixe :

   ```
   <!DOCTYPE html> 
   <html> 
   <head> 
   <script type="text/javascript" src="http://s7d1.scene7.com/s7viewers/html5/js/SmartCropVideoViewer.js"></script> 
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
   var smartCropVideoViewer = new s7viewers.SmartCropVideoViewer({ 
    "containerId":"s7viewer", 
   "params":{ 
    "asset":"html5automation/frisbee-AVS", 
    "serverurl":"http://s7d1.scene7.com/is/image/", 
    "videoserverurl":"http://s7d1.scene7.com/is/content/" 
   } 
   }).init(); 
   </script> 
   </body> 
   </html> 
   ```

**Intégration de conception réactive avec une hauteur libre**

Avec l’intégration de la conception réactive, la page web dispose normalement d’une sorte de disposition flexible qui détermine la taille d’exécution du conteneur de la visionneuse. `DIV`. Dans cet exemple, supposons que la page web autorise le conteneur de la visionneuse. `DIV` pour prendre 40 % de la taille de la fenêtre du navigateur web, sans restriction de sa hauteur. Le code de HTML de la page web se présente comme suit :

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

L’ajout de la visionneuse à une telle page est similaire à l’incorporation de tailles fixes ; la seule différence est que vous n’avez pas besoin de définir explicitement la taille de la visionneuse.

1. Ajout du fichier JavaScript de la visionneuse à votre page web.
1. Définition du conteneur DIV.
1. Création et initialisation de la visionneuse.

Toutes les étapes ci-dessus sont identiques à l’incorporation de tailles fixes. Ajouter un conteneur `DIV` au &quot;détenteur&quot; existant `DIV`. Le code suivant est un exemple complet. Vous pouvez voir comment la taille de la visionneuse change lorsque le navigateur est redimensionné et comment le rapport d’aspect de la visionneuse correspond à la ressource.

```
<!DOCTYPE html> 
<html> 
<head> 
<script type="text/javascript" src="http://s7d1.scene7.com/s7viewers/html5/js/SmartCropVideoViewer.js"></script> 
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
var smartCropVideoViewer = new s7viewers.SmartCropVideoViewer({ 
 "containerId":"s7viewer", 
"params":{ 
 "asset":"html5automation/frisbee-AVS", 
 "serverurl":"http://s7d1.scene7.com/is/image/", 
 "videoserverurl":"http://s7d1.scene7.com/is/content/" 
} 
}).init(); 
</script> 
</body> 
</html> 
```

La page d’exemples suivante illustre une utilisation plus concrète de l’incorporation de conceptions réactives avec une hauteur illimitée :

[Démonstrations en direct](https://landing.adobe.com/en/na/dynamic-media/ctir-2755/live-demos.html)

[Autre emplacement de démonstration](https://experienceleague.adobe.com/tools/dynamic-media-demo/vlist/vlist.html)

**Intégration de conception réactive avec définition de la largeur et de la hauteur**

Si une conception réactive est incorporée avec des valeurs de largeur et de hauteur définies, le style de la page web est différent ; il fournit les deux tailles au &quot;détenteur&quot; `DIV` et centrez-le dans la fenêtre du navigateur. En outre, la page web définit la taille de la variable `HTML` et `BODY` à 100 % :

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
<script type="text/javascript" src="http://s7d1.scene7.com/s7viewers/html5/js/SmartCropVideoViewer.js"></script> 
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
var smartCropVideoViewer = new s7viewers.SmartCropVideoViewer({ 
 "containerId":"s7viewer", 
"params":{ 
 "asset":"html5automation/frisbee-AVS", 
 "serverurl":"http://s7d1.scene7.com/is/image/", 
 "videoserverurl":"http://s7d1.scene7.com/is/content/" 
} 
}).init(); 
</script> 
</body> 
</html> 
```

**Incorporation à l’aide d’une API basée sur Setter**

Au lieu d’utiliser l’initialisation basée sur JSON, il est possible d’utiliser une API basée sur un setter et un constructeur sans args. Avec cette API, le constructeur ne prend aucun paramètre et les paramètres de configuration sont spécifiés à l’aide de `setContainerId()`, `setParam()`, et `setAsset()` Méthodes d’API avec des appels JavaScript distincts.

L’exemple suivant illustre l’incorporation de tailles fixes avec l’API basée sur setter :

```
<!DOCTYPE html> 
<html> 
<head> 
<script type="text/javascript" src="http://s7d1.scene7.com/s7viewers/html5/js/SmartCropVideoViewer.js"></script> 
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
var smartCropVideoViewer = new s7viewers.SmartCropVideoViewer(); 
smartCropVideoViewer.setContainerId("s7viewer"); 
smartCropVideoViewer.setParam("serverurl", "http://s7d1.scene7.com/is/image/"); 
smartCropVideoViewer.setParam("videoserverurl", "http://s7d1.scene7.com/is/content/"); 
smartCropVideoViewer.setAsset("html5automation/frisbee-AVS"); 
smartCropVideoViewer.init(); 
</script> 
</body> 
</html> 
```
