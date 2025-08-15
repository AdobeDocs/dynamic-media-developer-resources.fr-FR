---
title: Vidéo 360
description: La visionneuse HTML5 Video360 est un lecteur vidéo à 360 degrés qui lit des vidéos 360 en streaming et progressives encodées au format H.264, diffusées à partir de Dynamic Media Classic ou de Adobe Experience Manager, Dynamic Media.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,360 VR Video
role: Developer,User
exl-id: 74dca3f6-ce89-4c5b-8459-c2c4ca8ed27c
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '2561'
ht-degree: 0%

---

# Vidéo 360{#video}

La visionneuse HTML5 Video360 est un lecteur vidéo à 360 degrés qui lit des vidéos 360 en streaming et progressives encodées au format H.264, diffusées à partir de Dynamic Media Classic ou de Adobe Experience Manager, Dynamic Media.

Les vidéos à 360 degrés, également appelées vidéos immersives ou vidéos sphériques, sont des enregistrements vidéo dans lesquels une vue dans chaque direction est enregistrée en même temps, tournée à l’aide d’une caméra omnidirectionnelle ou d’un ensemble de caméras. Les visionneuses de vidéos uniques et adaptatives sont prises en charge. La visionneuse prend également en charge le travail avec des flux vidéo progressifs et HLS hébergés sur un emplacement externe.

Le rapport d’aspect recommandé pour une vidéo 360 est 2:1. Le son spatial n’est pas pris en charge. La visionneuse est conçue pour fonctionner avec la vidéo 360 uniquement ; Toute tentative de lecture d’une vidéo non 360 entraîne une distorsion de la lecture de la vidéo.

La visionneuse est conçue pour fonctionner sur les navigateurs Web de bureau et mobiles qui prennent en charge la vidéo HTML5. La visionneuse prend en charge les outils facultatifs de partage sur les réseaux sociaux.

La visionneuse Video360 utilise la lecture vidéo en flux continu HTML5 au format HLS dans sa configuration par défaut chaque fois que le système sous-jacent le prend en charge. Sur les systèmes qui ne prennent pas en charge la diffusion en flux continu HTML5, la visionneuse revient à la diffusion vidéo progressive HTML5.

Type de visionneuse : 517.

## URL de démonstration {#section-c0ad383db6a444979dc7eeb1ec4cf54d}

[https://s7d9.scene7.com/s7viewers/html5/Video360Viewer.html?asset=Viewers/space_station_360-AVS](https://s7d9.scene7.com/s7viewers/html5/Video360Viewer.html?asset=Viewers/space_station_360-AVS)

## Configuration système requise {#section-b7270cc4290043399681dc504f043609}

Voir [Configuration requise](../../c-system-requirements-and-prerequisites.md#concept-9282e5b777de42cdaf72ef7ebd646842).

## Utilisation de la visionneuse Video360 {#section-e6c68406ecdc4de781df182bbd8088b4}

La visionneuse HTML5 Video360 représente un fichier JavaScript principal et un ensemble de fichiers d’assistance (une seule JavaScript inclure avec tous les composants SDK de la visionneuse HTML5 utilisés par cette visionneuse, ressources, CSS) téléchargés par la visionneuse au moment de l’exécution.

HTML5 Video360 Viewer peut être utilisé à la fois en mode popup à l’aide d’une page HTML prête pour la production fournie avec IS-Viewers ou en mode intégré, où il est intégré dans la page Web cible à l’aide d’une API documentée.

La configuration et l’habillage sont similaires à ceux des autres visionneuses décrites dans ce guide. Tous les skins sont réalisés au moyen de feuilles de style en cascade personnalisées (CSS).

Voir [Référence de commande commune à tous les visualiseurs - Attributs](../../r-html5-viewer-20-cmdref-configattrib/r-html5-viewer-20-cmdref-configattrib.md#concept-850e0f2c49b949deb7cfbfd330d329bd) de configuration et [Référence de commande communs à tous les visualiseurs - URL](../../c-html5-aem-asset-viewers/c-html5-aem-video360/c-html5-aem-video360-cmdref-url/c-html5-aem-video360-cmdref-url.md#concept-9b337f349b7b406b8c33c7ee96b3e226)

Le contenu vidéo 360 nécessite des paramètres de codage plus élevés que la vidéo non 360 standard. En d’autres termes, le contenu 360 doit avoir une résolution supérieure à celle de la vidéo non 360 afin d’obtenir la même qualité perceptible. Il est recommandé de prendre en compte les paramètres prédéfinis suivants de vidéo adaptative pour la vidéo 360 :

* 720p, 2 500 Kbits/s
* 1080p, 5 000 Kbits/s
* 1440p, 6600 Kbits/s

Notez toutefois que la diffusion de vidéos codées avec de tels paramètres de haute qualité nécessite une connexion à large bande passante sur le périphérique d’un utilisateur final.

## Interaction avec la visionneuse Video360 {#section-642e66ca38cd4032992840ec6c0b0cd2}

La visionneuse HTML5 Video360 fournit un ensemble de commandes d’interface utilisateur standard pour la lecture vidéo, telles que le bouton lecture/pause, la bulle temporelle vidéo de découpe vidéo, l’indicateur de durée de lecture/durée totale, le contrôle du volume et le bouton plein écran. Tous ces contrôles sont regroupés dans la barre de contrôle au bas de l’interface utilisateur de la visionneuse.

Sur les appareils tactiles, le contrôle du volume est masqué de l’interface utilisateur, car il n’est possible de contrôler le volume qu’à l’aide des boutons matériels de l’appareil.

Lorsque la visionneuse fonctionne en mode pop-up, aucun bouton plein écran n’est disponible dans l’interface utilisateur.

La visionneuse prend également en charge divers outils de partage sur les réseaux sociaux. Ils sont disponibles sous la forme d’un seul bouton dans l’interface utilisateur qui se développe dans une barre d’outils de partage lorsque l’utilisateur clique ou appuie dessus. La barre d’outils de partage contient une icône pour chaque type de canal de partage pris en charge, tel que Facebook, Twitter, le partage d’e-mails, le partage de code intégré et le partage de lien. Lorsque les outils de partage de courrier électronique, de partage intégré ou de partage de lien sont activés, la visionneuse affiche une boîte de dialogue modale avec un formulaire de saisie de données correspondant. Lorsque Facebook ou Twitter sont appelés, le spectateur redirige l’utilisateur vers une boîte de dialogue de partage standard à partir d’un service de médias sociaux. En outre, lorsqu’un outil de partage est activé, la lecture vidéo est automatiquement interrompue. Les outils de partage ne sont pas disponibles en mode plein écran en raison des restrictions de sécurité du navigateur Web.

La visionneuse prend en charge la lecture vidéo 360 sur les éléments suivants :

* Casques VR (comme Oculus Go et Oculus Rift)
* Supports VR HMD (casque) (comme Google Cardboard)
* Appareils non compatibles VR (tels que les navigateurs de bureau, les tablettes et les téléphones mobiles non connectés aux supports de HMD VR)

Aucune configuration supplémentaire n’est nécessaire pour afficher du contenu vidéo 360 sur un casque VR. Le spectateur détecte automatiquement la présence d’un casque VR et affiche le bouton « VR » au-dessus du contenu vidéo. L’activation de ce bouton « VR » fait basculer le rendu vidéo en mode VR. La visionneuse prend en charge le rendu VR uniquement dans les navigateurs prenant en charge WebVR.

Pour utiliser les supports VR HMD, le `Video360Player.vrrender` modificateur doit être réglé sur `1` dans la configuration de la visionneuse, ce qui force le rendu stéréoscopique.

Sur les casques VR et les supports de casque VR HMD, le changement de point de vue se produit en réponse au mouvement du casque, aucun autre contrôle de lecture n’est fourni en mode VR.

Lorsqu’il regarde une vidéo 360 sur des appareils non compatibles VR, l’utilisateur final peut utiliser la souris, le toucher ou le clavier pour contrôler la lecture vidéo et le point de vue.

La visionneuse prend en charge l’entrée tactile et l’entrée souris sur les appareils Windows avec écran tactile et souris, cette prise en charge est toutefois limitée aux navigateurs Web Chrome, Internet Explorer 11 et Edge uniquement.

La visionneuse est entièrement accessible à l’aide du clavier. Voir [Accessibilité clavier et navigation](../../c-keyboard-accessibility.md#topic-f5650e9493404e55a3627c8d1366b861).

## Intégration de la visionneuse Video360 {#section-6bb5d3c502544ad18a58eafe12a13435}

Les différentes pages web ont des besoins différents en ce qui concerne le comportement des spectateurs. Parfois, une page Web fournit un lien qui, lorsqu’il est sélectionné, ouvre la visionneuse dans une fenêtre de navigateur distincte. Dans d’autres cas, il est nécessaire d’intégrer la visionneuse directement sur la page d’hébergement. Dans ce dernier cas, la page Web peut avoir une mise en page statique ou utiliser un design réactif qui s’affiche différemment sur différents appareils ou pour différentes tailles de fenêtre de navigateur. Pour répondre à ces besoins, la visionneuse prend en charge trois modes de fonctionnement principaux : popup, incorporation de taille fixe et incorporation de conception réactive.

L’intégration de plusieurs vidéos sur la même page est prise en charge sur les tablettes et les appareils mobiles. Habituellement, une seule vidéo peut être lue à la fois. Lorsqu’un utilisateur commence à lire une vidéo, puis tente de lire une autre vidéo, la première vidéo est automatiquement mise en pause. La vidéo qui a été mise en pause automatiquement se souvient de sa durée de lecture actuelle, de sorte que l’utilisateur peut toujours y revenir et reprendre la lecture. La seule exception à cette règle est dans le navigateur Chrome sur les appareils Android™ 4.x, qui peuvent lire des vidéos en parallèle.

**A propos du mode pop-up**

En mode pop-up, la visionneuse est ouverte dans une fenêtre ou un onglet de navigateur Web distinct. Il prend toute la zone de la fenêtre du navigateur et s’ajuste en cas de redimensionnement du navigateur ou de modification de l’orientation de l’appareil.

Ce mode est le plus courant pour les appareils mobiles. La page Web charge la visionneuse à l’aide `window.open()` d’JavaScript appel, d’un élément HTML correctement configuré `A` ou de toute autre méthode appropriée.

Il est recommandé d’utiliser une page HTML prête à l’emploi pour le mode de fonctionnement contextuel. Il est appelé [!DNL Video360Viewer.html] et il se trouve dans le [!DNL html5/] sous-dossier de votre déploiement IS-Viewers standard :

[!DNL <s7viewers_root>/html5/Video360Viewer.html]

Vous pouvez obtenir une personnalisation visuelle en appliquant une feuille de style CSS personnalisée.

Voici un exemple de code HTML qui ouvre la visionneuse dans une nouvelle fenêtre :

```html {.line-numbers}
<a href="https://s7d9.scene7.com/s7viewers/html5/Video360Viewer.html?asset=Viewers/space_station_360-AVS" target="_blank">Open popup viewer</a>
```

**A propos du mode d’incorporation de taille fixe et du mode d’incorporation de conception réactive**

En mode intégré, la visionneuse est ajoutée à la page Web existante, qui peut déjà contenir du contenu client non lié à la visionneuse. Le spectateur n’occupe normalement qu’une partie de l’espace d’une page Web.

Les principaux cas d’utilisation sont les pages Web orientées vers les ordinateurs de bureau ou les tablettes, ainsi que les pages réactives qui ajustent automatiquement la mise en page en fonction du type d’appareil.

L’incorporation de taille fixe est utilisée lorsque la visionneuse ne modifie pas sa taille après le chargement initial. Cette méthode est le meilleur choix pour les pages Web qui ont une disposition statique.

L’incorporation de conception réactive suppose que la visionneuse doit se redimensionner au moment de l’exécution en réponse au changement de taille de son conteneur `DIV`. Le cas d’utilisation le plus courant est l’ajout d’une visionneuse à une page Web qui utilise une mise en page flexible.

En mode d’incorporation de conception réactive, la visionneuse se comporte différemment selon la façon dont la page Web dimensionne son conteneur `DIV`. Si la page Web définit uniquement la largeur du conteneur `DIV`, en laissant sa hauteur illimitée, le visualisateur choisit automatiquement sa hauteur en fonction du format de la ressource utilisée. Cette fonctionnalité garantit que l’actif s’intègre parfaitement dans la vue sans aucun rembourrage sur les côtés. Ce cas d’utilisation est le plus courant pour les pages Web utilisant des cadres de mise en page de conception Web réactive tels que Bootstrap et Foundation.

Sinon, si la page Web définit à la fois la largeur et la hauteur du conteneur `DIV`de la visionneuse, celle-ci remplit uniquement cette zone et suit la taille fournie par la mise en page Web. Un bon exemple est l’intégration de la visionneuse dans une superposition modale, où la superposition est dimensionnée en fonction de la taille de la fenêtre du navigateur Web.

**Incorporation de taille fixe**

Pour ajouter la visionneuse à une page Web, procédez comme suit :

1. Ajout du fichier JavaScript de visionneuse à votre page Web.
1. Définition du conteneur `DIV`.
1. Définition de la taille de la visionneuse.
1. Création et initialisation de la visionneuse.

1. Ajout du fichier JavaScript de visionneuse à votre page Web.

   Pour créer une visionneuse, vous devez ajouter une balise de script dans l’en-tête HTML. Avant de pouvoir utiliser l’API de visionneuse, veillez à inclure [!DNL Video360Viewer.js]le fichier . Le [!DNL Video360Viewer.js] fichier se trouve dans le [!DNL html5/js/] sous-dossier de votre déploiement IS-Viewers standard :

[!DNL <s7viewers_root>/etc/dam/viewers/s7viewers/html5/js/Video360Viewer.js]

Vous pouvez utiliser un chemin d’accès relatif si la visionneuse est déployée sur l’un des serveurs Adobe Dynamic Media Classic et qu’elle est diffusée à partir du même domaine. Sinon, vous spécifiez un chemin d’accès complet à l’un des serveurs Adobe Dynamic Media Classic sur lesquels les IS-Viewers sont installés.

Le chemin d’accès relatif ressemble à ce qui suit :

```html {.line-numbers}
<script language="javascript" type="text/javascript" src="/etc/dam/viewers/s7viewers/html5/js/InteractiveVideoViewer.js"></script>
```

>[!NOTE]
>
>Référencez uniquement le fichier JavaScript `include` de visionneuse principal sur votre page. Ne référencez pas de fichiers JavaScript supplémentaires dans le code de la page Web qui pourraient être téléchargés par la logique du visualiseur au moment de l’exécution. En particulier, ne référencez pas directement la bibliothèque SDK `Utils.js` HTML5 chargée par la visionneuse à partir du chemin d’accès `/s7viewers` au contexte (SDK `include`consolidé). La raison en est que l’emplacement des bibliothèques d’exécution ou des bibliothèques de `Utils.js` visionneuse similaires est entièrement géré par la logique de la visionneuse et que l’emplacement change entre les versions de la visionneuse. Adobe ne conserve pas les anciennes versions de la visionneuse `includes` secondaire sur le serveur.
>
>
>Par conséquent, le fait de placer une référence directe à une JavaScript `include` secondaire utilisée par l’utilisateur sur la page interrompt la fonctionnalité de la visionneuse à l’avenir lorsqu’une nouvelle version du produit est déployée.

1. Définition du conteneur `DIV`.

   Ajoutez un élément vide `DIV` à la page dans laquelle vous souhaitez que la visionneuse apparaisse. L’ID `DIV` doit être défini pour l’élément, car cet identifiant est transmis ultérieurement à l’API de visionneuse. La taille de la DIV est spécifiée via CSS.

   L’espace réservé `DIV` est un élément positionné, ce qui signifie que la `position` propriété CSS est définie sur `relative` ou `absolute`.

   Pour que la fonctionnalité plein écran fonctionne correctement dans Internet Explorer, assurez-vous qu’aucun autre élément dans le DOM n’a un ordre d’empilement supérieur à celui de votre espace réservé `DIV`.

   Voici un exemple d’élément d’espace réservé `DIV` défini :

   ```html {.line-numbers}
   <div id="s7viewer" style="position:relative;width:640px;height:360px;"></div>
   ```

1. Définition de la taille de la visionneuse

   Vous pouvez définir la taille statique de la visionneuse en la déclarant pour `.s7video360viewer` la classe CSS de niveau supérieur en unités absolues ou en utilisant le `stagesize` modificateur.

   Vous pouvez placer le dimensionnement dans CSS directement sur la page HTML ou dans un fichier CSS de visionneuse personnalisé, qui est ensuite attribué à un enregistrement prédéfini de visionneuse dans Adobe Experience Manager Assets - À la demande, ou transmis explicitement à l’aide `style` de la commande.

   Voir [Personnalisation de la visionneuse](../../c-html5-aem-asset-viewers/c-html5-aem-video360/c-html5-aem-video360-customizingviewer/c-html5-aem-video360-customizingviewer.md#concept-73a8546acdb444a387c49969ceca57d0) Video360 pour plus d’informations sur le style de la visionneuse avec CSS.

   Voici un exemple de définition d’une taille de visionneuse statique dans la page HTML :

   ```html {.line-numbers}
   #s7viewer.s7video360viewer { 
    width: 640px; 
    height: 640px; 
   }
   ```

   Vous pouvez définir le `stagesize` modificateur dans l’enregistrement des paramètres prédéfinis de la visionneuse dans AEM Assets - à la demande. Vous pouvez également le transmettre explicitement avec le code d’initialisation de la visionneuse avec `params` collection, ou sous la forme d’un appel d’API comme décrit dans la section Référence des commandes, comme ceci :

   ```html {.line-numbers}
   video360viewer.setParam("stagesize", "640,640");
   ```

   Une approche basée sur le code CSS est recommandée et est utilisée dans cet exemple.

1. Création et initialisation de la visionneuse.

   Lorsque vous avez terminé les étapes ci-dessus, vous créez une instance de classe, transmettez toutes les informations de configuration à son constructeur et appelez `s7viewers.Video360Viewer` la méthode sur une instance de `init()` visionneuse. Les informations de configuration sont transmises au constructeur sous la forme d’un objet JSON. Au minimum, cet objet doit avoir `containerId` un champ qui contient le nom de l’ID de conteneur de la visionneuse et de l’objet JSON imbriqué `params` avec les paramètres de configuration pris en charge par la visionneuse.

   Dans ce cas, l’objet `params` doit avoir au moins l’URL Image Serving transmise en tant que propriété et la ressource initiale en tant que `serverUrl` `asset` paramètre. L’API d’initialisation basée sur JSON vous permet de créer et de démarrer la visionneuse avec une seule ligne de code, l’URL du serveur vidéo transmise en tant que propriété, la ressource initiale en tant que `videoserverurl` paramètre et les données interactives en tant que `asset` `interactivedata` propriété. L’API d’initialisation basée sur JSON vous permet de créer et de démarrer la visionneuse avec une seule ligne de code.

   Il est important d’ajouter le conteneur de visionneuse au DOM afin que le code de visionneuse puisse trouver l’élément conteneur par son identifiant. Certains navigateurs retardent la création de DOM jusqu’à la fin de la page Web. Pour une compatibilité maximale, appelez la `init()` méthode juste avant la balise de fermeture `BODY` , ou sur l’événement body `onload()` .

   Dans le même temps, l’élément conteneur ne doit pas nécessairement faire partie de la mise en page Web pour le moment. Par exemple, il peut être masqué à l’aide `display:none` du style qui lui est attribué. Dans ce cas, la visionneuse retarde son processus d’initialisation jusqu’au moment où la page Web ramène l’élément conteneur à la mise en page. Lorsque cela se produit, le chargement de la visionneuse reprend automatiquement.

   Voici un exemple de création d’une instance de visionneuse, en transmettant les options de configuration minimales nécessaires au constructeur et en appelant la `init()` méthode. L’exemple suppose ce qui suit :

   * L’instance de visionneuse est `video360Viewer`.
   * Le nom de l’espace réservé `DIV` est `s7viewer`.
   * L’URL du serveur d’images est `https://s7d9.scene7.com/is/image`.
   * L’URL du serveur vidéo est `https://s7d9.scene7.com/is/content`.
   * L’actif est `Viewers/space_station_360-AVS`.

   ```html {.line-numbers}
   <script type="text/javascript"> 
   var video360Viewer = new s7viewers.Video360Viewer({ 
    "containerId":"s7viewer", 
   "params":{ 
    "asset":"Viewers/space_station_360-AVS", 
    "serverurl":"https://s7d9.scene7.com/is/image/", 
    "videoserverurl":"https://s7d9.scene7.com/is/content/" 
   } 
   }).init(); 
   </script>
   ```

   Le code suivant est un exemple complet de page Web triviale qui intègre la visionneuse Video360 avec une taille fixe :

   ```html {.line-numbers}
   <!DOCTYPE html> 
   <html> 
   <head> 
   <script type="text/javascript" src="https://s7d9.scene7.com/s7viewers/html5/js/Video360Viewer.js"></script> 
   <style type="text/css"> 
   #s7viewer.s7video360viewer { 
    width: 640px; 
    height: 480px; 
   } 
   </style> 
   </head> 
   <body> 
   <div id="s7viewer" style="position:relative;width:640px;height:360px;"></div> 
   <script type="text/javascript"> 
   var video360Viewer = new s7viewers.Video360Viewer({ 
    "containerId":"s7viewer", 
   "params":{ 
    "asset":"Viewers/space_station_360-AVS", 
    "serverurl":"https://s7d9.scene7.com/is/image/", 
    "videoserverurl":"https://s7d9.scene7.com/is/content/" 
   } 
   }).init(); 
   </script> 
   </body> 
   </html>
   ```

**Intégration de conception réactive avec une hauteur illimitée**

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

1. Ajout du fichier JavaScript de visionneuse à votre page Web.
1. Définition du conteneur DIV.
1. Création et initialisation de la visionneuse.

Toutes les étapes ci-dessus sont identiques à celles de l’incorporation de taille fixe. Ajoutez la balise DIV conteneur à la balise DIV existante `"holder"` . Le code suivant est un exemple complet. Notez comment la taille de la visionneuse change lorsque le navigateur est redimensionné et comment le rapport d’aspect de la visionneuse correspond à la ressource.

```html {.line-numbers}
<!DOCTYPE html> 
<html> 
<head> 
<script type="text/javascript" src="https://s7d9.scene7.com/s7viewers/html5/js/Video360Viewer.js"></script> 
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
var video360Viewer = new s7viewers.Video360Viewer({ 
 "containerId":"s7viewer", 
"params":{ 
 "asset":"Viewers/space_station_360-AVS", 
 "serverurl":"https://s7d9.scene7.com/is/image/", 
 "videoserverurl":"https://s7d9.scene7.com/is/content/" 
} 
}).init(); 
</script> 
</body> 
</html>
```

**Incorporation réactive avec largeur et hauteur définies**

S’il existe un incorporation réactive avec la largeur et la hauteur définies, le style de la page Web est différent. Il fournit les deux tailles au `"holder"` DIV et le centre dans la fenêtre du navigateur. En outre, la page Web définit la taille de l’élément `HTML` et `BODY` sur 100 %.

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

Le reste des étapes d’incorporation sont identiques aux étapes utilisées pour l’incorporation réactive avec une hauteur illimitée. L’exemple résultant est le suivant :

```html {.line-numbers}
<!DOCTYPE html> 
<html> 
<head> 
<script type="text/javascript" src="https://s7d9.scene7.com/s7viewers/html5/js/Video360Viewer.js"></script> 
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
var video360Viewer = new s7viewers.Video360Viewer({ 
 "containerId":"s7viewer", 
"params":{ 
 "asset":"Viewers/space_station_360-AVS", 
 "serverurl":"https://s7d9.scene7.com/is/image/", 
 "videoserverurl":"https://s7d9.scene7.com/is/content/" 
} 
}).init(); 
</script> 
</body> 
</html>
```

**Incorporation à l’aide de l’API basée sur Setter**

Au lieu d’utiliser l’initialisation basée sur JSON, il est possible d’utiliser l’API basée sur setter et le constructeur no-args. L’utilisation de ce constructeur d’API ne prend aucun paramètre et les paramètres de configuration sont spécifiés à l’aide de `setContainerId()`, `setParam()`et `setAsset()` des méthodes API avec des appels JavaScript distincts.

L’exemple suivant illustre l’utilisation de l’incorporation de taille fixe avec l’API basée sur setter :

```html {.line-numbers}
<!DOCTYPE html> 
<html> 
<head> 
<script type="text/javascript" src="https://s7d9.scene7.com/s7viewers/html5/js/Video360Viewer.js"></script> 
<style type="text/css"> 
#s7viewer.s7video360viewer { 
 width: 640px; 
 height: 480px; 
} 
</style> 
</head> 
<body> 
<div id="s7viewer" style="position:relative;width:640px;height:360px;"></div> 
<script type="text/javascript"> 
var video360Viewer = new s7viewers.Video360Viewer(); 
video360Viewer.setContainerId("s7viewer"); 
video360Viewer.setParam("serverurl", "https://s7d9.scene7.com/is/image/"); 
video360Viewer.setParam("videoserverurl", "https://s7d9.scene7.com/is/content/"); 
video360Viewer.setAsset("Viewers/space_station_360-AVS"); 
video360Viewer.init(); 
</script> 
</body> 
</html>
```
