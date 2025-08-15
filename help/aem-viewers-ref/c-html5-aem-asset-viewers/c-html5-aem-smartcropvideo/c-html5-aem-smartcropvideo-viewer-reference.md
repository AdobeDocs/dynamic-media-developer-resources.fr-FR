---
title: Visionneuse de vidéo avec recadrage intelligent
description: La visionneuse de vidéos avec recadrage intelligent lit des vidéos en streaming et progressives codées au format H.264 avec l’ajout de la prise en charge du recadrage intelligent. Elle est diffusée à partir d’Dynamic Media Classic ou Adobe Experience Manager avec Dynamic Media.
keywords: sensible
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Smart Crop,Video
role: Developer,User
exl-id: 937be8a2-307e-47bb-9fc8-d354f780a214
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '2368'
ht-degree: 0%

---

# Recadrage intelligent de la vidéo{#smart-crop-video}

La visionneuse de vidéos avec recadrage intelligent lit des vidéos en streaming et progressives codées au format H.264 avec l’ajout de la prise en charge du recadrage intelligent. Elle est diffusée à partir d’Dynamic Media Classic ou Experience Manager avec Dynamic Media.

Voir [Configuration requise et conditions préalables](../../c-system-requirements-and-prerequisites.md#concept-9282e5b777de42cdaf72ef7ebd646842).

Les visionneuses de vidéos uniques et adaptatives sont prises en charge. En outre, la visionneuse prend en charge le travail avec des flux vidéo progressifs et HLS hébergés sur des emplacements externes. Il est conçu pour fonctionner sur les navigateurs Web de bureau et mobiles qui prennent en charge la vidéo HTML5. Cette visionneuse prend également en charge les sous-titres codés facultatifs qui s’affichent au-dessus du contenu vidéo, de la navigation par chapitre vidéo et des outils de partage sur les réseaux sociaux.

La visionneuse de vidéos avec recadrage intelligent utilise la lecture vidéo en flux continu HTML5 au format HLS dans sa configuration par défaut chaque fois que le système sous-jacent la prend en charge. Sur les systèmes qui ne prennent pas en charge la diffusion en flux continu HTML5, la visionneuse revient à la diffusion vidéo progressive HTML5.

Type de visionneuse 518.

## URL de démonstration {#section-e1c3106f5b3e445d9b95be337c2f94e2}

[https://s7d9.scene7.com/s7viewers/html5/SmartCropVideoViewer.html?asset=html5automation/frisbee-AVS](https://s7d9.scene7.com/s7viewers/html5/SmartCropVideoViewer.html?asset=html5automation/frisbee-AVS)

## Utilisation de la visionneuse de vidéos avec recadrage intelligent {#section-f21ac23d3f6449ad9765588d69584772}

La visionneuse de vidéos avec recadrage intelligent représente un fichier JavaScript principal et un ensemble de fichiers d’assistance (un seul JavaScript inclure avec tous les composants SDK de la visionneuse utilisés par cette visionneuse, les ressources et les CSS particuliers téléchargés par la visionneuse au moment de l’exécution.

Vous pouvez utiliser la visionneuse de vidéos avec recadrage intelligent en mode pop-up à l’aide d’une page HTML prête pour la production fournie avec IS-Viewers. Vous pouvez également utiliser la visionneuse en mode intégré, où elle est intégrée dans une page Web cible à l’aide de l’API documentée.

La tâche de configuration et d’habillage de la visionneuse est similaire à celle des autres visionneuses. Toute application de la peau est réalisée au moyen d’un CSS personnalisé.

Voir [ Référence des commandes commune à toutes les visionneuses - Attributs de configuration ](../../r-html5-viewer-20-cmdref-configattrib/r-html5-viewer-20-cmdref-configattrib.md#concept-850e0f2c49b949deb7cfbfd330d329bd) et [ Référence des commandes commune à toutes les visionneuses - URL](../../c-html5-viewer-20-cmdref-url/c-html5-viewer-20-cmdref-url.md#concept-9b337f349b7b406b8c33c7ee96b3e226)

## Interaction avec la visionneuse de vidéo avec recadrage intelligent {#section-ab66eb6955aa4a8aa6d14a3b3acfed3f}

La visionneuse de vidéos avec recadrage intelligent fournit un ensemble de commandes d’interface utilisateur standard pour la lecture vidéo, telles que :

* Bouton Lecture/Pause.
* Vidéo de défilement vidéo bulle temporelle.
* Indicateur de temps de lecture/temps total.
* Contrôle du volume.
* bouton plein écran.
* Bouton bascule des sous-titres.

Toutes ces commandes sont regroupées dans une barre de commandes située dans la partie inférieure de l’interface utilisateur de la visionneuse.

Sur les appareils tactiles, le contrôle du volume est masqué dans l’interface utilisateur, car il n’est possible de le contrôler qu’à l’aide des boutons matériels.

Lorsque la visionneuse fonctionne en mode pop-up, le bouton Plein écran n’est pas disponible dans l’interface utilisateur.

Il est possible de naviguer rapidement dans le contenu d’une vidéo lorsque le chapitre vidéo est activé. Les chapitres vidéo sont affichés sous forme de marqueurs dans la piste de défilement vidéo et affichent le titre du chapitre et la description associée au survol de la souris ou en appuyant simplement sur les systèmes tactiles. Les utilisateurs peuvent rechercher un chapitre particulier en sélectionnant un marqueur de chapitre ou en sélectionnant la bulle de description du chapitre.

La visionneuse prend en charge l’entrée tactile et l’entrée souris sur les appareils Windows avec écran tactile et souris. Cette prise en charge est toutefois limitée aux navigateurs Web Chrome, Internet Explorer 11 et Edge uniquement.

Cette visionneuse est entièrement accessible à l’aide du clavier.

Voir [Accessibilité clavier et navigation](../../c-keyboard-accessibility.md#topic-f5650e9493404e55a3627c8d1366b861).

## Outils de partage sur les médias sociaux avec la visionneuse de vidéos avec recadrage intelligent {#section-907d316fe1da4b87abb9775f02464704}

La visionneuse de vidéos avec recadrage intelligent prend en charge les outils de partage sur les médias sociaux. Ils sont disponibles sous la forme d’un seul bouton dans l’interface utilisateur, qui se développe en barre d’outils de partage lorsque l’utilisateur clique ou appuie dessus.

La barre d’outils de partage contient une icône pour chaque type de canal de partage pris en charge, tel que Facebook, Twitter, le partage d’e-mail, le partage de code intégré et le partage de lien. Lorsque les outils de partage d’e-mail, de partage intégré ou de partage de lien sont activés, la visionneuse affiche une boîte de dialogue modale avec un formulaire de saisie de données correspondant. Lorsque Facebook ou Twitter sont appelés, le spectateur redirige l’utilisateur vers une boîte de dialogue de partage standard à partir d’un service de médias sociaux. De plus, lorsqu’un outil de partage est activé, la lecture vidéo est automatiquement interrompue.

Les outils de partage ne sont pas disponibles en mode plein écran en raison des restrictions de sécurité du navigateur Web.

## Intégration de la visionneuse de vidéo avec recadrage intelligent {#section-6bb5d3c502544ad18a58eafe12a13435}

Les différentes pages web ont des besoins différents en ce qui concerne le comportement des spectateurs. Parfois, une page Web fournit un lien qui, lorsqu’il est sélectionné, ouvre la visionneuse dans une fenêtre de navigateur distincte. Dans d’autres cas, il est nécessaire d’intégrer la visionneuse directement sur la page d’hébergement. Dans ce dernier cas, la page Web peut avoir une mise en page statique ou utiliser un design réactif qui s’affiche différemment sur différents appareils ou pour différentes tailles de fenêtre de navigateur. Pour répondre à ces besoins, la visionneuse prend en charge trois modes de fonctionnement principaux : popup, incorporation de taille fixe et incorporation de conception réactive.

L’incorporation de plusieurs vidéos sur la même page est prise en charge sur les tablettes et les appareils mobiles. En règle générale, une seule vidéo peut être lue à la fois. Lorsqu’un utilisateur ou une utilisatrice commence la lecture d’une vidéo, puis tente de lire une autre vidéo, la première vidéo est automatiquement mise en pause. La vidéo qui a été mise en pause automatique se souvient de son heure de lecture actuelle, de sorte que l’utilisateur peut toujours y revenir et reprendre la lecture. La seule exception à cette règle est dans le navigateur Chrome sur les appareils Android™ 4.x, qui peuvent lire des vidéos en parallèle.

**A propos du mode pop-up**

En mode pop-up, la visionneuse est ouverte dans une fenêtre ou un onglet de navigateur Web distinct. Il prend toute la zone de la fenêtre du navigateur et s’ajuste en cas de redimensionnement du navigateur ou de modification de l’orientation de l’appareil.

Ce mode est le plus courant pour les appareils mobiles. La page Web charge la visionneuse à l’aide `window.open()` d’JavaScript appel, d’un élément HTML correctement configuré `A` ou de toute autre méthode appropriée.

Il est recommandé d’utiliser une page HTML prête à l’emploi pour le mode de fonctionnement contextuel. Il s’appelle [!DNL SmartCropVideoViewer.html] et se trouve sous le sous-dossier [!DNL html5/] de votre déploiement d’observateurs IS standard :

[!DNL <s7viewers_root>/html5/SmartCropVideoViewer.html]

Vous pouvez effectuer une personnalisation visuelle en appliquant un CSS personnalisé.

Voici un exemple de code HTML qui permet d’ouvrir la visionneuse dans une nouvelle fenêtre :

```html {.line-numbers}
<a href="http://s7d1.scene7.com/s7viewers/html5/SmartCropVideoViewer.html?asset=html5automation/frisbee-AVS" target="_blank">Open popup viewer</a>
```

**A propos du mode d’incorporation de taille fixe et du mode d’incorporation réactif**

En mode intégré, la visionneuse est ajoutée à la page Web existante, qui peut déjà contenir du contenu client non lié à la visionneuse. Le spectateur n’occupe normalement qu’une partie de l’espace de la page Web.

Les principaux cas d’utilisation sont les pages Web orientées vers les ordinateurs de bureau ou les tablettes, ainsi que les pages de conception réactive qui ajustent automatiquement la mise en page en fonction du type d’appareil.

L’incorporation de taille fixe est utilisée lorsque la visionneuse ne modifie pas sa taille après le chargement initial. Cette sélection est la meilleure pour les pages Web qui ont une mise en page statique.

L’incorporation de conception réactive suppose que la visionneuse doit se redimensionner en exécution en réponse au changement de taille de son conteneur `DIV`. Le cas d’utilisation le plus courant est l’ajout de la visionneuse à une page Web qui utilise une mise en page flexible.

En mode d’incorporation de conception réactive, la visionneuse se comporte différemment selon la façon dont la page Web dimensionne son conteneur `DIV`. Si la page Web définit uniquement la largeur du conteneur `DIV`, en laissant sa hauteur illimitée, le visualisateur choisit automatiquement sa hauteur en fonction du format de la ressource utilisée. Cette méthode garantit que l’actif s’intègre parfaitement dans la vue sans aucun rembourrage sur les côtés. Ce cas d’utilisation est le plus courant pour les pages Web qui utilisent une structure de mise en page de conception réactive comme Bootstrap ou Foundation.

Sinon, si la page Web définit à la fois la largeur et la hauteur du conteneur `DIV`de la visionneuse, celle-ci remplit uniquement cette zone et suit la taille fournie par la mise en page Web. Un bon exemple est l’intégration de la visionneuse dans une superposition modale, où la superposition est dimensionnée en fonction de la taille de la fenêtre du navigateur Web.

**Incorporation de taille fixe**

Pour ajouter la visionneuse à une page Web, procédez comme suit :

1. Ajout du fichier JavaScript de visionneuse à votre page Web.
1. Définition du conteneur `DIV`.
1. Définition de la taille de la visionneuse.
1. Création et initialisation de la visionneuse.

1. Ajout du fichier JavaScript de visionneuse à votre page Web.

   Pour créer une visionneuse, vous devez ajouter une balise de script dans l’en-tête HTML. Avant de pouvoir utiliser l’API de visionneuse, veillez à inclure [!DNL SmartCropVideoViewer.js]le fichier . Le [!DNL SmartCropVideoViewer.js] fichier se trouve dans le [!DNL html5/js/] sous-dossier de votre déploiement IS-Viewers standard :

[!DNL <s7viewers_root>/html5/js/SmartCropVideoViewer.js]

Vous pouvez utiliser un chemin d’accès relatif si la visionneuse est déployée sur l’un des serveurs Adobe Dynamic Media Classic et qu’elle est diffusée à partir du même domaine. Sinon, vous spécifiez un chemin d’accès complet à l’un des serveurs Adobe Dynamic Media Classic sur lesquels les IS-Viewers sont installés.

Le chemin d’accès relatif ressemble à ce qui suit :

```html {.line-numbers}
<script language="javascript" type="text/javascript" src="/s7viewers/html5/js/SmartCropVideoViewer.js"></script>
```

>[!NOTE]
>
>Référencez uniquement le fichier de `include` JavaScript de la visionneuse principale sur votre page. Ne référencez aucun fichier JavaScript supplémentaire dans le code de page web qui pourrait être téléchargé par la logique de la visionneuse au moment de l’exécution. En particulier, ne référencez pas directement la bibliothèque de `Utils.js` SDK HTML5 chargée par la visionneuse à partir `/s7viewers` chemin de contexte (appelé `include` consolidée de SDK). La raison en est que l’emplacement des bibliothèques d’exécution ou des bibliothèques de `Utils.js` visionneuse similaires est entièrement géré par la logique de la visionneuse et que l’emplacement change entre les versions de la visionneuse. Adobe ne conserve pas les anciennes versions de la visionneuse `includes` secondaire sur le serveur.
>
>
>Par conséquent, le fait de placer une référence directe à une JavaScript `include` secondaire utilisée par l’utilisateur sur la page interrompt la fonctionnalité de la visionneuse à l’avenir lorsqu’une nouvelle version du produit est déployée.

1. Définition du conteneur DIV.

   Ajoutez un élément DIV vide à la page sur laquelle vous souhaitez que la visionneuse apparaisse. L’identifiant de l’élément DIV doit être défini, car cet identifiant est transmis ultérieurement à l’API de visionneuse. La taille du DIV est spécifiée via CSS.

   L’espace réservé DIV est un élément positionné, ce qui signifie que la propriété CSS `position` est définie sur `relative` ou `absolute`.

   Assurez-vous que la fonction Plein écran fonctionne correctement dans Internet Explorer. Vérifiez qu’aucun autre élément du DOM n’a un ordre d’empilement supérieur à celui de votre DIV d’espace réservé.

   Exemple d’élément DIV d’espace réservé défini :

   ```html {.line-numbers}
   <div id="s7viewer" style="position:relative;width:640px;height:360px;"></div> 
   ```

1. Définition de la taille de la visionneuse

   Vous pouvez définir la taille statique de la visionneuse en la déclarant pour `.s7videoviewer` classe CSS de niveau supérieur dans des unités absolues ou à l’aide du `stagesize` de modificateur.

   Vous pouvez placer le dimensionnement dans CSS directement sur la page HTML ou dans un fichier CSS de visionneuse personnalisé. Il est ensuite attribué à un enregistrement de paramètre prédéfini de visionneuse dans Dynamic Media Classic ou transmis explicitement à l’aide d’une commande de style.

   Voir [Personnalisation de la visionneuse](../../c-html5-s7-aem-asset-viewers/c-html5-video-reference/c-html5-video-viewer-20-customizingviewer/c-html5-video-viewer-20-customizingviewer.md#concept-072a52b10b5f4c0789393dc6e2134c0e) de vidéos avec recadrage intelligent pour plus d’informations sur le style de la visionneuse à l’aide de CSS.

   Voici un exemple de définition d’une taille de visionneuse statique dans une page HTML :

   ```html {.line-numbers}
   #s7viewer.s7videoviewer { 
    width: 640px; 
    height: 480px; 
   }
   ```

   Vous pouvez définir `stagesize` un modificateur dans l’enregistrement du paramètre prédéfini de la visionneuse dans Dynamic Media Classic ou le transmettre explicitement avec le code d’initialisation de la visionneuse avec `params` collection. Ou, en tant qu’appel d’API comme décrit dans la section Référence de commande, comme dans ce qui suit :

   ```html {.line-numbers}
   smartCropVideoViewer.setParam("stagesize", "640,480");
   ```

   Une approche basée sur CSS est recommandée et est utilisée dans cet exemple.

1. Création et initialisation de la visionneuse.

   Lorsque vous avez terminé les étapes ci-dessus, vous créez une instance de classe, transmettez toutes les informations de configuration à son constructeur et appelez `s7viewers.SmartCropVideoViewer` la méthode sur une instance de `init()` visionneuse. Les informations de configuration sont transmises au constructeur sous la forme d’un objet JSON. Au minimum, cet objet doit avoir `containerId` un champ qui contient le nom de l’ID de conteneur de la visionneuse et l’objet JSON imbriqué `params` avec les paramètres de configuration pris en charge par la visionneuse. Dans ce cas, `params` l’objet doit avoir au moins l’URL Image Serving transmise en tant que propriété, l’URL du serveur vidéo transmise en tant que propriété et la ressource initiale en tant que `serverUrl` `videoserverurl` `asset` paramètre. L’API d’initialisation basée sur JSON vous permet de créer et de démarrer la visionneuse avec une seule ligne de code.

   Il est important d’ajouter le conteneur de visionneuse au DOM afin que le code de la visionneuse puisse trouver l’élément de conteneur à l’aide de son identifiant. Certains navigateurs retardent la création du DOM jusqu’à la fin de la page web. Pour une compatibilité maximale, appelez la méthode `init()` juste avant la balise `BODY` de fermeture ou sur l’événement body `onload()`.

   Dans le même temps, l’élément de conteneur ne doit pas nécessairement encore faire partie de la mise en page web. Par exemple, elle peut être masquée à l’aide `display:none` style qui lui est affecté. Dans ce cas, la visionneuse retarde son processus d’initialisation jusqu’au moment où la page web ramène l’élément de conteneur dans la mise en page. Lorsque cette action se produit, le chargement de la visionneuse reprend automatiquement.

   Voici un exemple de création d’une instance de visionneuse, de transmission des options de configuration minimales nécessaires au constructeur et d’appel de la méthode `init()`. Cet exemple suppose que `smartCropVideoViewer` est l’instance de visionneuse, `s7viewer` est le nom de l’espace réservé `DIV`, [!DNL http://s7d1.scene7.com/is/image/] est l’URL du service d’images, [!DNL http://s7d1.scene7.com/is/content/] est l’URL du serveur vidéo et [!DNL html5automation/frisbee-AVS] est la ressource.

   ```html {.line-numbers}
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

   Le code suivant est un exemple complet de page web triviale qui intègre la visionneuse de vidéos avec recadrage intelligent avec une taille fixe :

   ```html {.line-numbers}
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

**Incorporation de conception réactive avec hauteur illimitée**

Avec l’incorporation de responsive design, la page web dispose normalement d’un certain type de disposition flexible en place qui détermine la taille d’exécution du `DIV` de conteneur de la visionneuse. Pour les besoins de cet exemple, supposons que la page Web autorise le conteneur `DIV` du spectateur à prendre 40 % de la taille de la fenêtre du navigateur Web, en laissant sa hauteur sans restriction. Le code HTML de la page Web doit ressembler à ce qui suit :

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

L’ajout de la visionneuse à une telle page est similaire à l’incorporation de taille fixe ; La seule différence réside dans le fait que vous n’avez pas besoin de définir explicitement la taille de la visionneuse.

1. Ajout du fichier JavaScript de visionneuse à votre page Web.
1. Définition du conteneur DIV.
1. Création et initialisation de la visionneuse.

Toutes les étapes ci-dessus sont identiques à l’incorporation de taille fixe. Ajoutez des `DIV` de conteneur au `DIV` « holder » existant. Le code suivant en est un exemple complet. Vous pouvez voir comment la taille de la visionneuse change lorsque le navigateur est redimensionné et comment le format de la visionneuse correspond à la ressource.

```html {.line-numbers}
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

La page d’exemples suivante illustre une utilisation plus réelle de l’incorporation de conception réactive avec une hauteur illimitée :

[Démonstrations en direct](https://landing.adobe.com/en/na/dynamic-media/ctir-2755/live-demos.html)

[Autre emplacement de démonstration](https://experienceleague.adobe.com/tools/dynamic-media-demo/vlist/vlist.html?lang=fr)

**Intégration de conception réactive avec largeur et hauteur définies**

S’il existe un design réactif intégrant une largeur et une hauteur définies, le style de la page Web est différent ; Il fournit les deux tailles au « titulaire » `DIV` et le centre dans la fenêtre du navigateur. En outre, la page web définit la taille de l’élément `HTML` ET `BODY` sur 100 % :

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

**Incorporation à l’aide de l’API basée sur Setter**

Au lieu d’utiliser l’initialisation basée sur JSON, il est possible d’utiliser l’API basée sur setter et le constructeur no-args. Avec cette API, le constructeur ne prend aucun paramètre et les paramètres de configuration sont spécifiés à l’aide de `setContainerId()`, `setParam()`et `setAsset()` des méthodes API avec des appels JavaScript distincts.

L’exemple suivant illustre l’incorporation de taille fixe avec l’API basée sur setter :

```html {.line-numbers}
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
