---
description: Notes de mise à jour les plus récentes pour la version d’Adobe Scene7, automne 2016, de la solution Adobe Experience Manager dans Adobe Marketing Cloud.
seo-description: Notes de mise à jour les plus récentes pour la version d’Adobe Scene7, automne 2016, de la solution Adobe Experience Manager dans Adobe Marketing Cloud.
seo-title: Version de l’automne 2016 de Scene7
solution: Experience Manager
title: Version de l’automne 2016 de Scene7
topic: Dynamic media
uuid: 3fddda65-0c6e-48ec-bd60-7e0ca59421a8
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# Version de l’automne 2016 de Scene7{#scene-fall-release}

Notes de mise à jour les plus récentes pour la version d’Adobe Scene7, automne 2016, de la solution Adobe Experience Manager dans Adobe Marketing Cloud.

## Version de l’automne 2016 de Scene7 {#topic-791cdf80f91e457fbb63bfedf79f5a94}

Notes de mise à jour les plus récentes pour la version de [!DNL Adobe Scene7] l’automne 2016 de la [!DNL Adobe Experience Manager] solution dans le [!DNL Adobe Marketing Cloud].

* [Généraux](s7rnfall2016.md#section-52afeb72ecb34c1585ea67a5051825a2)
* [Scene7 Publishing System](s7rnfall2016.md#section-24487cb493444d808fb7193f0a00cdd4)
* [Visionneuses (Image Serving 5.5.3)](s7rnfall2016.md#section-1d59bcd5825d487b80b59a6d1a08ed30)
* [Visionneuses (Image Serving 5.5.2)](s7rnfall2016.md#section-9932c988cfee45749594af481dfc6476)
* [Visionneuses (Image Serving 5.5.1)](s7rnfall2016.md#section-833ab92c91c941d2bfdc27f233f582ad)
* [Kit de développement de visionneuse HTML5 Scene7 3.0.1](s7rnfall2016.md#section-30e2392859c442d1aab2766d0f1d1580)
* [Scene7 Image Serving 6.3.2 et Image Rendering 6.3.2](s7rnfall2016.md#section-19a3e96f52c74757bcdea0f8a11001f2)

## Généraux {#section-52afeb72ecb34c1585ea67a5051825a2}

Adobe est ravi d’annoncer la disponibilité des  de contenu HTTP/2 avec l’avantage global d’améliorer les performances.

Voir  [HTTP2 du FAQ](https://docs.adobe.com/content/docs/en/aem/6-2/administer/integration/marketing-cloud/scene7/http2faq.html)sur le contenu.

## Scene7 Publishing System {#section-24487cb493444d808fb7193f0a00cdd4}

Pour obtenir une documentation complète, voir [https://docs.adobe.com/content/help/en/dynamic-media-classic/using/home.html](https://docs.adobe.com/content/help/en/dynamic-media-classic/using/home.html)

**Nouvelles fonctionnalités, améliorations et correctifs**

* Suppression de la fonction de découpe vidéo de l’interface [!DNL Adobe Scene7 Publishing System] utilisateur.
* Ajout de l’authentification à tous les servlets Scene7 lorsque cela est nécessaire et possible.
* Correction de bogues impliquant le   dans la corbeille.
* Suppression de la fonctionnalité **Créer un utilisateur SPSAdmin** de User Management en raison de problèmes de sécurité.
* FTP WebAdmin prend désormais en charge l’authentification OKTA.
* Suppression de la fonctionnalité du mot de passe par défaut créé pour les nouveaux utilisateurs du portail multimédia.
* Correction d’un bogue concernant le mot de passe temporaire généré lors de l’ajout d’un nouvel utilisateur. Le mot de passe ne remplissait pas les conditions requises pour le mot de passe.
* Correction de problèmes de disque racine WebAdmin saturé.
* Correction d’un bogue en raison duquel la désactivation d’un utilisateur n’était pas immédiatement répercutée dans l’interface utilisateur.
* Correction de bogues impliquant la suppression d’un utilisateur qui ne vous permettait pas de recréer l’utilisateur ultérieurement.
* Correction d’un bogue concernant le courrier électronique de bienvenue envoyé aux nouveaux utilisateurs de Scene7 qui n’incluaient pas l’authentification pour contrôler certains paramètres.
* Correction d’un bogue suite auquel l’échec de la récupération d’un de dossiers FTP  si le nom d’un dossier contenait des caractères spéciaux.
* Configurez les OKTA pour   de de Scene7.
* Ajout de la prise en charge de l’ID d’organisation Marketing Cloud pour Viewer Analytics.
* Mise en oeuvre du client SAML Scene7.

## Visionneuses (Image Serving 5.5.3) {#section-1d59bcd5825d487b80b59a6d1a08ed30}

Pour obtenir une documentation complète, consultez le Guide [de référence des visionneuses](https://marketing.adobe.com/resources/help/en_US/s7/viewers_ref/)Scene7.

**Correctifs pour Image Serving 5.5.3**

* Compatibilité avec les bibliothèques RequireJS et DOJO.

   Mise en cache JS du SDK consolidé pendant le déploiement de la visionneuse.

## Visionneuses (Image Serving 5.5.2) {#section-9932c988cfee45749594af481dfc6476}

Pour obtenir une documentation complète, consultez le Guide [de référence des visionneuses](https://marketing.adobe.com/resources/help/en_US/s7/viewers_ref/)Scene7.

**Correctifs pour Image Serving 5.5.2**

* La lecture de la vidéo a échoué dans Internet Explorer 11 sous Windows 7.
* `initialframe` n’affectait pas le mode portrait sur les périphériques mobiles pour le catalogue électronique HTML5.

## Visionneuses (Image Serving 5.5.1) {#section-833ab92c91c941d2bfdc27f233f582ad}

Pour obtenir une documentation complète, consultez le Guide [de référence des visionneuses](https://marketing.adobe.com/resources/help/en_US/s7/viewers_ref/)Scene7.

**Nouvelles fonctionnalités, améliorations et correctifs pour Image Serving 5.5.1**

* Visionneuse de catalogue électronique HTML5 avec fonction de recherche.
* Ajout de la lecture vidéo en flux continu HLS en tant que méthode de vidéo par défaut pour la majorité des systèmes de bureau. La diffusion vidéo en flux continu HDS Flash reste disponible en tant qu’option de lecture alternative.
* Ajout de la prise en charge des périphériques dotés de la souris et d’une entrée tactile exécutant le navigateur Chrome.
* Ajout de la prise en charge de l’ID d’organisation Marketing Cloud à l’intégration d’Analytics.
* Mettez à jour la bibliothèque JavaScript AppMeasurement vers la version 1.6.1.
* Ajout de la prise en charge de l’orientation de droite à gauche dans la visionneuse de catalogue électronique.
* Correction d’un problème `tip=0,-1,0` provoquant une erreur hors plage.

**Notes de compatibilité**

* Blackberry

   * Incompatibilité avec les anciens jeux AVS. Les clients peuvent avoir besoin de recharger les visionneuses AVS pour autoriser la lecture.

* Généraux

   * La mise à l’échelle côté navigateur peut rendre l’interface utilisateur et les images floues lorsque l’utilisateur effectue un zoom sur la page. Le formatage de l’interface utilisateur peut également s’afficher incorrectement selon le zoom. Cela sera reporté en plein écran.
   * En raison de la taille limitée sur les périphériques mobiles, la visionneuse de supports variés utilise le mouvement des diapositives pour permuter des images dans des visionneuses d’images incorporées au lieu d’appuyer sur le composant de nuances incorporées. Le composant est là comme indicateur visuel.
   * Dans les navigateurs Internet Explorer et sur certains périphériques tactiles, le mode plein écran n’occupe pas l’intégralité de l’écran du périphérique. Il redimensionne l’application en fonction de la taille de la fenêtre du navigateur.
   * Le bouton Fermer ne fonctionne pas sous iOS 8.0 et 8.1, mais il ne se produit plus sous iOS 8.2.

* Galaxy SIII

   * Fuite de mémoire visible avec les visionneuses HTML5 de zoom et de catalogue électronique. Une navigation répétée dans les cadres peut entraîner le blocage du navigateur.
   *  appuyer sur le lecteur peut faire zoomer la page entière au lieu de la seule visionneuse dont la mise à l’échelle côté navigateur est activée.

* Galaxy S4

   * Périphérique détecté comme tablette en mode portrait avec le mode Plein écran coché dans les paramètres du navigateur.

* Galaxy Nexus

   *  appuyer sur le lecteur peut faire zoomer la page entière au lieu de la seule visionneuse dont la mise à l’échelle côté navigateur est activée.

* Galaxy Nexus 10 et tablette Galaxy

   * Catalogue électronique montrant une planche de page incorrecte avec des orientations portrait et paysage.

* Périphériques mobiles HTC

   * Les périphériques mobiles HTC que nous avons découvert montrent que l&#39;incapacité à désactiver le zoom-pincement natif est une &quot;fonctionnalité&quot; de l&#39;enveloppe HTC UI wrapper (HTC Sense). Cela peut entraîner un zoom sur toute la page lors de l’utilisation du mouvement &quot;Pincer pour zoomer&quot; sur la visionneuse. Suggérez d’utiliser -appuyer plutôt.
   * Les icônes de zone cliquable peuvent se chevaucher si les zones cliquables sont petites et rapprochées.

* Vidéo HTML5

   * Internet Explorer 9 : les images d’affiche personnalisées ne s’affichent pas.
   * `IntialBitRate` est uniquement pris en charge avec la lecture HLS du logiciel et HDS Flash. Cela ne fonctionne pas lorsque la lecture utilise le lecteur natif.
   * La lecture progressive OGG et WebM n’est pas prise en charge pour le moment.
   * La mise à l’échelle du navigateur peut entraîner l’affichage du lecteur vidéo à une taille incorrecte (inclut les paramètres d’affichage du panneau de configuration Windows OS).
   * La recherche de vidéos en flux continu HLS sur Safari peut être incohérente.

* Internet Explorer

   * Le mode Quirks n’est pas pris en charge pour le moment.
   * Le mode de compatibilité n’est pas pris en charge pour le moment.
   * Internet Explorer sur mobile n’est pas pris en charge pour le moment.

* iOS

   * Les catalogues électroniques volumineux peuvent entraîner un blocage du navigateur sur l’iPad 2.
   * Les téléphones iPhone 6+ sont détectés comme des tablettes par les lecteurs.

* Safari

   * Safari 6.1 ou version ultérieure : Les paramètres des plug-ins Internet peuvent empêcher la lecture vidéo Flash.
   * La &quot;recherche&quot; vidéo à l’aide de la diffusion en flux continu HLS sur Safari peut être incohérente.
   * Impossible de rechercher la fin de la vidéo sur Safari 6 à l’aide de la diffusion en flux continu HLS.

**Problèmes connus et restrictions**

* Les modificateurs de diffusion d’images de `iscommands` ne sont pas ajoutés à la `req=set` requête par conception. Les modificateurs qui affectent uniquement l’affichage des images fonctionnent correctement. Les modificateurs affectant la taille doivent être utilisés dans un fichier complexe. Par exemple,

   `https://s7d9.scene7.com/s7viewers/html5/BasicZoomViewer.html?asset= {Scene7SharedAssets/Backpack_B?extendn=0.5%252C0.5%252C0.5%252C0.5}`

* [L’application Flyout] IE9 reste parfois à l’écran après la désactivation de la souris.
* La mise à l’échelle du navigateur entraîne un redimensionnement incorrect.
* iPad 2 : Le fichier de catalogue électronique volumineux bloquera Safari sur iOS.
* Toutes les visionneuses

   * Les filigranes, l’obscurcissement et le verrouillage ne sont pas pris en charge.
   * Les paramètres d’image prédéfinis ne sont pas pris en charge.
   * L’ajout ou la suppression d’une visionneuse du DOM à l’aide de `display:none` CSS ou en la détachant dynamiquement du noeud parent n’est pas prise en charge pour le moment.

* HTML5 Toutes les visionneuses

   * L’incorporation de la visionneuse dans le tableau peut entraîner un dimensionnement incorrect ou un placement incorrect de la visionneuse en mode plein écran non natif. Suggérez plutôt d’utiliser des balises DIV.
   * Les paramètres avec des noms d’instance explicites dans le code nécessitent également que les noms d’instance dans l’URL soient remplacés (par exemple, `zoomView.iconfeffect=0`).
   * Le recadrage de la commande Diffusion d’images n’est pas pris en charge pour le moment.
   * Le bouton Fermer fonctionne uniquement si la visionneuse est ouverte dans la fenêtre enfant.
   * Le `iscommands` modificateur ne prend pas en charge les modificateurs de diffusion d’images qui affectent la taille de l’image.

* Catalogue électronique HTML5

   * Si vous naviguez jusqu’à une autre page HTML et revenez parfois, le lecteur se réinitialise à la première page.
   * La mise en page s’affiche parfois incorrectement après la rotation du périphérique iOS. Le zoom dans la page corrige la disposition.
   * Liens internes uniquement à la page la plus à gauche dans les planches de plusieurs pages. Affecte les périphériques mobiles en mode portrait.
   * InitalFrame lie uniquement la page la plus à gauche dans les planches de plusieurs pages. Affecte les périphériques mobiles en mode portrait.
   * En raison des limitations du navigateur, la fonction d’impression n’est pas disponible dans IE9.

* HTML5 MixedMedia

   * La lecture de la bande son n’est actuellement pas prise en charge.

* HTML5 Social

   * Pour que les vignettes soient correctement rendues dans le courrier électronique sortant, le `serverurl` modificateur doit avoir une URL absolue.

* Vidéo HTML5

   * L’image d’affiche peut rencontrer l’erreur &quot;taille maximale&quot;.  peut devoir augmenter le paramètre de limite pour la publication Image Serving.
   * Les légendes vidéo nécessitent un jeu de règles  si l’hébergement de la page HTML est diffusé à partir d’un serveur externe (et non d’un serveur Scene7). Contactez l’assistance d’Adobe pour obtenir de l’aide.
   * Le suivi Analytics peut signaler un pourcentage de lecture incorrect en raison de la mise en mémoire tampon
   * Le cadre noir au lieu de l’image d’affiche peut s’afficher sur les périphériques iPad ou Android.
   * L’image noire peut clignoter à l’écran pendant le chargement du lecteur sur les périphériques iPad ou Android.
   * Les bordures noires s’affichent du côté du composant VideoPlayer lorsque l’arrière-plan est défini sur blanc/transparent sur les périphériques iPad.
   * La dernière image de la vidéo peut être déformée sur iPad à l’aide d’iOS 7.
   * Des macroblocages peuvent survenir lors de la recherche vidéo en mode de diffusion HLS dans les navigateurs Chrome, Firefox et Internet Explorer.
   * L’image d’affiche peut ne pas s’afficher dans le navigateur Microsoft Edge pour la première fois dans le.
   * L’image d’affiche peut se masquer après le chargement de la vidéo dans Internet Explorer 9 lorsque la lecture progressive est utilisée.

## Scene7 HTML5 Viewer SDK 3.0.2 {#section-30e2392859c442d1aab2766d0f1d1580}

Le Guide de l’utilisateur se trouve dans le dossier Adobe HTML5 Viewer SDK de l’installation du client. La documentation de l’API de composant se trouve dans le sous-dossier docs de l’installation du client.

**Correctifs pour la version 3.0.2**

* Lecteur vidéo - La lecture de la vidéo a échoué dans Internet Explorer 11 sous Windows 7
* Table des matières - `initialframe` n’a pas affecté le mode portrait sur les périphériques mobiles pour la visionneuse de catalogue électronique HTML5.

**Nouvelles fonctionnalités, améliorations et correctifs pour la version 3.0.1**

* Généraux

   * Ajout de la lecture vidéo en flux continu HLS en tant que méthode de vidéo par défaut pour la majorité des systèmes de bureau. La diffusion vidéo en flux continu HDS Flash reste disponible en tant qu’option de lecture alternative.
   * Ajout des composants SearchManager, SearchPanel, SearchEffect et SearchButton pour prendre en charge la nouvelle fonctionnalité de recherche dans les visionneuses de catalogue électronique.
   * Ajout de la prise en charge des périphériques avec la souris et l’entrée tactile s’exécutant sur le navigateur Chrome.
   * Amélioration de la détection des versions Android pour prendre en charge les versions futures du système d’exploitation
   * Ajouter la prise en charge de l’orientation de droite à gauche dans les composants SDK propres au catalogue électronique.

* ControlBar

   * Ajout d’un défilement facultatif pour le contenu ControlBar au cas où il ne correspondrait pas à la largeur disponible.

* FlyoutzoomView

   * Correction d’un cas `tip=0,-1,0` d’erreur hors plage.

**Notes de compatibilité**

* Android 4.x

   * Pour désactiver la valeur par défaut, la règle CSS suivante doit être mise en surbrillance en bleu pour le composant :

      `-webkit-tap-highlight-color: rgba(0,0,0,0);`

* Blackberry

   * La lecture vidéo peut cesser lors de la modification des flux de débit binaire dans les visionneuses AVS.

* Chrome

   * Tout appel d’API qui force la reconstruction des composants peut être ignoré en raison de la mise en cache interne de Chrome.

* Galaxy SIII

   * Le lecteur ne parvient parfois pas à se charger en plein écran.
   * Pageview souffre actuellement d&#39;une fuite de mémoire sur le périphérique.
   * Le mouvement de  de la touche permet de zoomer sur la visionneuse et la page lorsque la mise à l’échelle côté navigateur est active.

* Galaxy Nexus

   * Artefacts qui s’affichent sur certains composants .
   * Le mouvement de  de la touche permet de zoomer sur la visionneuse et la page lorsque la mise à l’échelle côté navigateur est active.

* iPad 3

   * L’iPad 3 a une résolution native de 2 048 x 1 536 pixels. Cela peut entraîner des problèmes d’affichage si le  de publication IS du est défini, la taille limite de l’image est inférieure à cette valeur.

* iPhone4

   * L’icône de relecture de l’effet d’icône est remplacée par l’icône de lecture après le défilement de la page.

* Internet Explorer

   * Dans IE 10 et les versions plus anciennes, le mode plein écran n’occupe pas tout l’écran, mais redimensionne simplement l’application à la taille de la fenêtre du navigateur.
   * Le mode de rendu Quirks n’est pas pris en charge.
   * Internet Explorer sur mobile n’est pas pris en charge pour le moment.
   * Le chargement du fichier Util.js peut échouer s’il est inclus de manière asynchrone.
   * L’icône IconEffect bloque les  de clic sur les composants SpinView et ZoomView.

* Lecteurs vidéo natifs

   * La mise en forme des composants de l’interface utilisateur sur VideoPlayer n’est pas prise en charge lorsque VideoPlayer est utilisé pour appeler le lecteur natif du périphérique.
   * La lecture vidéo en mode natif est incohérente dans Safari 6.
   * La lecture native remplace l’icône de lecture par l’icône de lecture après le défilement de la page.

* Périphériques tactiles

   * Le mode plein écran n’occupe pas l’intégralité de l’écran du périphérique, mais redimensionne simplement l’application à la taille de la fenêtre du navigateur.
   * Les curseurs personnalisés ne fonctionnent pas sur les périphériques tactiles.
   * La mise à l’échelle des pages sur les périphériques tactiles n’est pas prise en charge pour le moment. L’incorporation de visionneuses HTML5 requiert la balise meta de fenêtre d’affichage avec les paramètres appropriés.

* Xoom

   * Le mouvement de  de la touche permet de zoomer sur la visionneuse et la page lorsque la mise à l’échelle côté navigateur est active.

**Problèmes connus et restrictions**

* Tous les composants

   * Dans les versions 2.7.2 et antérieures, certains composants ont été ajoutés au DOM à l’aide de `insertBefore()` l’API. Par conséquent, ces composants se placent au bas de l’ordre d’empilement, quelle que soit la date de création de l’instance de composant par rapport aux autres composants. Avec la version 2.8.1, tous les composants utilisent maintenant `appendChild()` l’API, ce qui signifie que l’ordre d’empilement des composants correspondrait à l’ordre de création de l’instance.

   * L’utilisation du `iscommand` modificateur pour définir le format de alpha de l’image n’est pas prise en charge. Utilisez plutôt le `FMT` paramètre de composant.
   * Pour le moment, la propriété de transformation CSS n’est pas prise en charge.

* Périphériques tactiles

   * Le mouvement de pincement sur les périphériques tactiles ne génère pas de de zoom 

* Conteneur

   * Les bordures, le remplissage et les marges sur le  du ne sont pas pris en charge. Adobe suggère d’ajouter des éléments de style à la balise DIV parente.
   * Vous devez définir explicitement la taille de  du ou les composants peuvent être correctement dimensionnés.

* Imprimer le composant

   * En raison des limitations du navigateur, dans Internet Explorer 9, le composant d’impression peut ne pas mettre à l’échelle correctement le contenu sur le papier.

* Composant IconEffect

   * IconEffect génère une erreur de script sur Internet Explorer si `autohide` est désactivé (défini sur `0`).

* Composant ImageMapEffect

   * Retarder avec l’icône de repositionnement lors du panoramique de l’image sur le composant .

* Composant MediaSet

   * Les fichiers insérés demandent le même codage que sur l’URL.

* Composant NavigationView

   * Actuellement, le composant ne prend pas en charge le redimensionnement.

* Composant PageScrubber

   * Sur iPhone 5, lorsque la bulle de défilement des pages est définie sur du texte, elle affiche des artefacts lors du glissement du bouton le long de la piste. L’utilisation `-webkit-background-clip: content;` dans le style s’articule autour du problème.

* Composant SpinView

   * La vue à 360° semble parfois se figer après le mouvement de glissement et la rotation du périphérique pendant que l’image tourne.

* Composant Nuancier

   * Lors de la sélection d’une nuance hors limites, deux mises en surbrillance s’affichent.
   * Défilement automatique avec `selectSwatch()` la méthode ne fonctionnant pas correctement.

* VideoPlayer

   * L’image vidéo n’est pas mise à jour si la recherche est définie sur 100 % et que la valeur de secours est définie sur auto.
   * Des blocages occasionnels de macros peuvent survenir lors de la recherche vidéo en mode de diffusion HLS dans les navigateurs Chrome, Firefox et Internet Explorer.
   * L’image d’affiche peut ne pas s’afficher dans le navigateur Microsoft Edge pour la première fois dans le.
   * L’image d’affiche peut se masquer après le chargement de la vidéo dans Internet Explorer 9 lorsque la lecture progressive est utilisée.

## Scene7 Image Serving 6.3.2 and Image Rendering 6.3.2 {#section-19a3e96f52c74757bcdea0f8a11001f2}

* Utilitaire IC - `downsample2x2` l&#39;indicateur n&#39;est plus pris en charge. Cet indicateur était un sous-échantillonneur 2x2 de mauvaise qualité qui n&#39;est plus utilisé par IPS.
* En-tête CORS : l’en-tête CORS est actuellement configuré pour les `/is/content/` requêtes.

