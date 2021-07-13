---
description: '"Notes de mise à jour les plus récentes pour la version de l’automne 2016 d’Adobe Scene7, qui fait partie de la solution Adobe Experience Manager dans Adobe Marketing Cloud."'
solution: Experience Manager
title: Version de Scene7 à l’automne 2016
feature: Dynamic Media Classic
role: Developer,User
exl-id: 23091ef7-750a-4ec2-9d03-1d713f436991
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '2235'
ht-degree: 0%

---

# Version de Scene7 à l’automne 2016{#scene-fall-release}

Notes de mise à jour les plus récentes pour la version d’Adobe Scene7 de l’automne 2016 de la solution Adobe Experience Manager dans Adobe Marketing Cloud.

## Version de Scene7 à l’automne 2016 {#topic-791cdf80f91e457fbb63bfedf79f5a94}

Notes de mise à jour les plus récentes pour la version [!DNL Adobe Scene7] de l’automne 2016 de la solution [!DNL Adobe Experience Manager] dans [!DNL Adobe Marketing Cloud].

* [Généraux](s7rnfall2016.md#section-52afeb72ecb34c1585ea67a5051825a2)
* [Scene7](s7rnfall2016.md#section-24487cb493444d808fb7193f0a00cdd4)
* [Visionneuses (Image Serving 5.5.3)](s7rnfall2016.md#section-1d59bcd5825d487b80b59a6d1a08ed30)
* [Visionneuses (Image Serving 5.5.2)](s7rnfall2016.md#section-9932c988cfee45749594af481dfc6476)
* [Visionneuses (Image Serving 5.5.1)](s7rnfall2016.md#section-833ab92c91c941d2bfdc27f233f582ad)
* [SDK de la visionneuse HTML5 3.0.1](s7rnfall2016.md#section-30e2392859c442d1aab2766d0f1d1580)
* [Dynamic Media Classic Image Serving 6.3.2 et Image Rendering 6.3.2](s7rnfall2016.md#section-19a3e96f52c74757bcdea0f8a11001f2)

## Généraux {#section-52afeb72ecb34c1585ea67a5051825a2}

Adobe est heureux d’annoncer la disponibilité de la diffusion de contenu HTTP/2 avec l’avantage global de l’amélioration des performances.

Voir [FAQ sur la diffusion de contenu HTTP2](https://experienceleague.adobe.com/docs/experience-manager-65/assets/dynamic/http2.html#dynamic).

## Scene7 Publishing System {#section-24487cb493444d808fb7193f0a00cdd4}

Pour obtenir une documentation complète, voir [https://experienceleague.adobe.com/docs/dynamic-media-classic/using/home.html](https://experienceleague.adobe.com/docs/dynamic-media-classic/using/home.html)

**Nouvelles fonctionnalités, améliorations et correctifs**

* Suppression de la fonction de découpe vidéo de l’interface utilisateur [!DNL Adobe Scene7 Publishing System].
* Ajout de l’authentification à tous les servlets Scene7 si nécessaire et possible.
* Correction de bogue concernant le mode Liste dans la corbeille.
* Suppression de la fonction **Créer un utilisateur Dynamic Media Classic (Scene7) Admin** de User Management en raison de problèmes de sécurité.
* FTP WebAdmin prend désormais en charge l’authentification OKTA.
* Suppression de la fonctionnalité du mot de passe par défaut qui a été créé pour les nouveaux utilisateurs du portail multimédia.
* Correction de bogue impliquant le mot de passe temporaire généré lors de l’ajout d’un nouvel utilisateur. Le mot de passe ne remplissait pas les exigences de mot de passe nécessaires.
* Résolution de problèmes de saturation du disque racine WebAdmin.
* Correction de bogues impliquant la désactivation d’un utilisateur qui n’est pas répercutée immédiatement dans l’interface utilisateur.
* Correction de bogues impliquant la suppression d’un utilisateur qui ne vous a pas permis de recréer l’utilisateur ultérieurement.
* Correction de bogue concernant le courrier électronique de bienvenue envoyé aux nouveaux utilisateurs de Scene7 qui n’incluaient pas l’authentification pour contrôler certains paramètres.
* Correction d’un bogue qui empêchait la récupération d’une liste de dossiers FTP si un dossier portait des caractères spéciaux dans son nom.
* Configurez les fournisseurs de services OKTA pour les environnements Scene7.
* Ajout de la prise en charge de l’ID d’organisation de Marketing Cloud pour Viewer Analytics.
* Mise en oeuvre du consommateur SAML Scene7.

## Visionneuses (Image Serving 5.5.3) {#section-1d59bcd5825d487b80b59a6d1a08ed30}

Pour obtenir une documentation complète, reportez-vous au [Guide de référence des visionneuses](https://experienceleague.adobe.com/docs/dynamic-media-developer-resources/library/home.html).

**Correctifs de bogues pour Image Serving 5.5.3**

* Compatibilité avec les bibliothèques RequireJS et DOJO.

   Mise en cache JS du SDK consolidé pendant le déploiement de la visionneuse.

## Visionneuses (Image Serving 5.5.2) {#section-9932c988cfee45749594af481dfc6476}

Pour obtenir une documentation complète, reportez-vous au [Guide de référence des visionneuses](https://experienceleague.adobe.com/docs/dynamic-media-developer-resources/library/home.html).

**Correctifs de bogues pour Image Serving 5.5.2**

* La lecture de la vidéo a échoué dans Internet Explorer 11 sous Windows 7.
* `initialframe` n’affectait pas le mode portrait sur les appareils mobiles pour le catalogue électronique HTML5.

## Visionneuses (Image Serving 5.5.1) {#section-833ab92c91c941d2bfdc27f233f582ad}

Pour obtenir une documentation complète, reportez-vous au [Guide de référence des visionneuses](https://experienceleague.adobe.com/docs/dynamic-media-developer-resources/library/home.html).

**Nouvelles fonctionnalités, améliorations et correctifs pour Image Serving 5.5.1**

* Visionneuse de catalogue électronique HTML5 avec fonctionnalité de recherche.
* Ajout de la lecture vidéo en continu HLS comme méthode de diffusion vidéo par défaut pour la majorité des systèmes de bureau. La diffusion vidéo HDS par Flash est toujours disponible en tant qu’option de lecture alternative.
* Ajout de la prise en charge des appareils dotés de la souris et d’une entrée tactile exécutant le navigateur Chrome.
* Ajout de la prise en charge de l’ID d’organisation de Marketing Cloud à l’intégration d’Analytics.
* Mise à jour de la bibliothèque JavaScript AppMeasurement vers la version 1.6.1.
* Ajout de la prise en charge de l’orientation de droite à gauche dans la visionneuse de catalogue électronique.
* Correction d’un problème en raison duquel `tip=0,-1,0` provoquait une erreur &quot;out-of-range&quot;.

**Remarques sur la compatibilité**

* Blackberry

   * Incompatibilité avec les anciens ensembles AVS. Les clients peuvent avoir besoin de charger à nouveau des visionneuses AVS pour permettre la lecture.

* Généraux

   * La mise à l’échelle côté navigateur peut rendre l’interface utilisateur et les images floues lorsque l’utilisateur effectue un zoom sur la page. La mise en forme de l’interface utilisateur peut également s’afficher incorrectement en fonction du zoom. Cette opération sera répercutée en plein écran.
   * En raison de la taille limitée sur les appareils mobiles, la visionneuse de supports variés utilise le mouvement des diapositives pour permuter des images dans des visionneuses d’images incorporées au lieu d’appuyer sur le composant des échantillons incorporés. Le composant est présent en tant qu’indicateur visuel.
   * Dans les navigateurs Internet Explorer et certains périphériques tactiles, le mode Plein écran n’occupe pas tout l’écran du périphérique. Il redimensionne l’application à la taille de la fenêtre du navigateur.
   * Le bouton Fermer ne fonctionne pas sous iOS 8.0 et 8.1, mais ne fonctionne plus sous iOS 8.2.

* Galaxy SIII

   * Fuite de mémoire vue avec les visionneuses HTML5 Zoom et eCatalog. Une navigation répétée dans les images peut entraîner le blocage du navigateur.
   * Si vous appuyez deux fois sur la visionneuse, il se peut que la page entière fasse l’objet d’un zoom au lieu de la seule visionneuse avec la mise à l’échelle côté navigateur activée.

* Galaxy S4

   * Appareil détecté comme tablette en mode portrait avec le plein écran coché dans les paramètres du navigateur.

* Galaxy Nexus

   * Si vous appuyez deux fois sur la visionneuse, il se peut que la page entière fasse l’objet d’un zoom au lieu de la seule visionneuse avec la mise à l’échelle côté navigateur activée.

* Galaxy Nexus 10 et tablette Galaxy

   * Catalogue électronique présentant une page incorrecte avec des orientations portrait et paysage.

* Périphériques mobiles HTC

   * Nos résultats sur les appareils mobiles HTC montrent que l’impossibilité de désactiver le zoom par pincement natif est une &quot;fonctionnalité&quot; de l’wrapper HTC UI (HTC Sense). Cela peut entraîner un zoom de la page entière lors de l’utilisation du mouvement &quot;Pincer pour zoomer&quot; sur la visionneuse. Suggérez d’utiliser plutôt le bouton double.
   * Les icônes de zone cliquable peuvent se chevaucher si les zones cliquables sont petites et rapprochées.

* Vidéo HTML5

   * Internet Explorer 9 : les images d’affiche personnalisées ne s’affichent pas.
   * `IntialBitRate` est uniquement pris en charge avec la lecture HLS du logiciel et HDS par Flash. Cela ne fonctionne pas lorsque la lecture utilise le lecteur natif.
   * La lecture progressive OGG et WebM n’est actuellement pas prise en charge.
   * La mise à l’échelle du navigateur peut entraîner l’affichage d’un lecteur vidéo à une taille incorrecte (inclut les paramètres d’affichage du panneau de configuration de Windows OS).
   * La recherche vidéo à l’aide de la diffusion HLS en continu sur Safari peut être incohérente.

* Internet Explorer

   * Le mode Quirks n’est actuellement pas pris en charge.
   * Pour l’instant, le mode de compatibilité n’est pas pris en charge.
   * Internet Explorer sur mobile n’est pas pris en charge pour l’instant.

* iOS

   * Les catalogues électroniques volumineux peuvent provoquer un blocage du navigateur sur iPad 2.
   * Les téléphones iPhone 6+ sont détectés en tant que tablettes par les utilisateurs.

* Safari

   * Safari 6.1 ou version ultérieure : Les paramètres des modules externes Internet peuvent empêcher la lecture vidéo par Flash.
   * La &quot;recherche&quot; vidéo à l’aide de la diffusion HLS en continu sur Safari peut être incohérente.
   * Impossible de rechercher la fin de la vidéo sur Safari 6 à l’aide de la diffusion HLS en continu.

**Problèmes connus et restrictions**

* Les modificateurs de diffusion d’images de `iscommands` ne sont pas ajoutés à la requête `req=set` par conception. Les modificateurs qui affectent uniquement l’affichage de l’image fonctionnent correctement. Les modificateurs affectant la taille doivent être utilisés dans une ressource complexe. Par exemple,

   `https://s7d9.scene7.com/s7viewers/html5/BasicZoomViewer.html?asset= {Scene7SharedAssets/Backpack_B?extendn=0.5%252C0.5%252C0.5%252C0.5}`

* [] FlyoutIE9 reste parfois à l’écran après la désactivation de la souris.
* La mise à l’échelle du navigateur entraîne un mauvais redimensionnement.
* iPad 2 : Une ressource de catalogue électronique volumineuse bloque Safari sur iOS.
* Toutes les visionneuses

   * Les filigranes, l’obscurcissement et le verrouillage ne sont pas pris en charge.
   * Les paramètres d’image prédéfinis ne sont pas pris en charge.
   * L’ajout ou la suppression de la visionneuse du DOM à l’aide d’une feuille CSS `display:none` ou en la désolidarisant dynamiquement du noeud parent n’est pas prise en charge pour l’instant.

* HTML5 Toutes les visionneuses

   * L’incorporation de la visionneuse dans le tableau peut entraîner un dimensionnement ou un placement incorrect de la visionneuse en mode plein écran non natif. Suggérez plutôt d’utiliser des DIV.
   * Les paramètres dont les noms d’instance sont explicites dans le code requièrent également le remplacement des noms d’instance dans l’URL (par exemple, `zoomView.iconfeffect=0`).
   * Pour l’instant, le recadrage de la commande de diffusion d’images n’est pas pris en charge.
   * Le bouton Fermer ne fonctionne que si la visionneuse est ouverte dans la fenêtre enfant.
   * Le modificateur `iscommands` ne prend pas en charge les modificateurs de diffusion d’images qui affectent la taille de l’image.

* Catalogue électronique HTML5

   * La navigation vers une autre page HTML et le renvoi entraînent parfois la réinitialisation de la visionneuse sur la première page.
   * La mise en page s’affiche parfois de manière incorrecte après la rotation de l’appareil iOS. Le zoom avant corrige la mise en page.
   * Liens internes uniquement vers la page la plus à gauche dans les planches de plusieurs pages. Affecte les appareils mobiles en mode portrait.
   * Liens InitalFrame uniquement vers la page la plus à gauche dans les planches de plusieurs pages. Affecte les appareils mobiles en mode portrait.
   * En raison des restrictions du navigateur, la fonction d’impression n’est pas disponible dans IE9.

* HTML5 MixedMedia

   * La lecture de la piste audio n’est actuellement pas prise en charge.

* Social HTML5

   * Pour effectuer correctement le rendu des miniatures dans un email sortant, le modificateur `serverurl` doit avoir une URL absolue.

* Vidéo HTML5

   * L’image d’affiche peut rencontrer une erreur &quot;taille maximale&quot;. Il se peut que l’entreprise doive augmenter le paramètre de limite pour la publication sur hébergeur d’images.
   * Les sous-titres vidéo nécessitent un jeu de règles de l’entreprise si l’hébergement de la page HTML est diffusé à partir d’un serveur externe (et non d’un serveur Scene7). Contactez l’assistance Adobe pour obtenir de l’aide.
   * Le suivi Analytics peut signaler un pourcentage de lecture incorrect en raison de la mise en mémoire tampon.
   * L’image noire peut s’afficher sur les appareils iPad ou Android au lieu de l’image d’affiche.
   * L’image noire peut clignoter à l’écran lors du chargement de la visionneuse sur des appareils iPad ou Android.
   * Les bordures noires s’affichent sur le côté du composant Lecteur vidéo lorsque l’arrière-plan est défini sur blanc/transparent sur les appareils iPad.
   * La dernière image de la vidéo peut être déformée sur iPad à l’aide d’iOS 7.
   * Des macroblocages peuvent parfois survenir lors de la recherche vidéo en mode de diffusion HLS dans les navigateurs Chrome, Firefox et Internet Explorer.
      * Il se peut que l’image d’affiche ne s’affiche pas dans le navigateur Microsoft Edge pour le premier visiteur.
      * L’image d’affiche peut se masquer après le chargement de la vidéo dans Internet Explorer 9 lorsque la lecture progressive est utilisée.

## SDK de la visionneuse HTML5 Scene7 3.0.2 {#section-30e2392859c442d1aab2766d0f1d1580}

Le Guide de l’utilisateur se trouve dans le dossier SDK de la visionneuse HTML5 Adobe de l’installation du client. La documentation de l’API de composant se trouve dans le sous-dossier docs de l’installation du client.

**Correctifs de bogues pour la version 3.0.2**

* Lecteur vidéo : la lecture de la vidéo a échoué dans Internet Explorer 11 sous Windows 7
* TableOfContents - `initialframe` n’a pas affecté le mode portrait sur les appareils mobiles pour la visionneuse de catalogue électronique HTML5.

**Nouvelles fonctionnalités, améliorations et correctifs pour la version 3.0.1**

* Généraux

   * Ajout de la lecture vidéo en continu HLS comme méthode de diffusion vidéo par défaut pour la majorité des systèmes de bureau. La diffusion vidéo HDS par Flash est toujours disponible en tant qu’option de lecture alternative.
   * Ajout des composants SearchManager, SearchPanel, SearchEffect et SearchButton pour la prise en charge de la nouvelle fonctionnalité de recherche dans les visionneuses de catalogue électronique.
   * Ajout de la prise en charge des appareils dotés d’entrées de souris et de touches s’exécutant sur le navigateur Chrome.
   * Refactorisation de la détection des versions d’Android pour la prise en charge des versions futures du système d’exploitation
   * Ajoutez la prise en charge de l’orientation de droite à gauche dans les composants de SDK spécifiques au catalogue électronique.

* ControlBar

   * Ajout d’un défilement facultatif pour le contenu ControlBar si celui-ci ne correspond pas à la largeur disponible.

* FlyoutzoomView

   * Correction du cas où `tip=0,-1,0` provoquait une erreur &quot;out-of-range&quot;.

**Remarques sur la compatibilité**

* Android 4.x

   * Pour désactiver la valeur par défaut, la règle CSS suivante doit être ajoutée en surbrillance bleue pour le composant :

      `-webkit-tap-highlight-color: rgba(0,0,0,0);`

* BlackBerry

   * La lecture vidéo peut cesser lors de la modification des flux de débit dans les visionneuses AVS.

* Chrome

   * Tout appel API qui force la reconstruction des composants peut être ignoré en raison de la mise en cache interne de Chrome.

* Galaxy SIII

   * Le chargement de la visionneuse échoue parfois en plein écran.
   * Pour l’instant, Pageview souffre d’une fuite de mémoire sur l’appareil.
   * Lorsque vous appuyez deux fois, le mouvement agrandit la visionneuse et la page lorsque la mise à l’échelle côté navigateur est principale.

* Galaxy Nexus

   * Artefacts s’affichant sur certains composants d’affichage.
   * Lorsque vous appuyez deux fois, le mouvement agrandit la visionneuse et la page lorsque la mise à l’échelle côté navigateur est principale.

* iPad 3

   * L’iPad 3 a une résolution native de 2 048 x 1 536. Cela peut entraîner des problèmes d’affichage si la limite de taille d’image définie par l’IS de l’entreprise est inférieure à cette limite.

* iPhone4

   * Icône de relecture incohérente remplacée par icône de lecture après la page de défilement.

* Internet Explorer

   * Dans IE 10, le mode Plein écran plus ancien n’occupe pas tout l’écran, mais redimensionne simplement l’application à la taille de la fenêtre du navigateur.
   * Le mode de rendu des quirks n’est pas pris en charge.
   * Internet Explorer sur mobile n’est pas pris en charge pour l’instant.
   * Util.js peut ne pas se charger s’il est inclus de manière asynchrone.
   * L’icône IconEffect bloque les événements de clic sur les composants SpinView et ZoomView.

* Lecteurs vidéo natifs

   * La mise en page des composants de l’interface utilisateur sur VideoPlayer n’est pas prise en charge lorsque VideoPlayer est utilisé pour appeler le lecteur natif de l’appareil.
   * La lecture vidéo en mode natif est incohérente sur Safari 6.
   * La lecture native remplace l’icône de relecture par l’icône de lecture après la page de défilement.

* Appareils tactiles

   * Le mode Plein écran n’occupe pas tout l’écran de l’appareil, mais redimensionne simplement l’application à la taille de la fenêtre du navigateur.
   * Les curseurs personnalisés ne fonctionnent pas sur les périphériques tactiles.
   * La mise à l’échelle des pages sur les périphériques tactiles n’est pas prise en charge pour le moment. L’incorporation de visionneuses HTML5 nécessite une balise meta viewport avec les paramètres appropriés.

* Xoom

   * Lorsque vous appuyez deux fois, le mouvement agrandit la visionneuse et la page lorsque la mise à l’échelle côté navigateur est principale.

**Problèmes connus et restrictions**

* Tous les composants

   * Dans les versions 2.7.2 et antérieures, certains composants ont été ajoutés au modèle DOM à l’aide de l’API `insertBefore()`. Par conséquent, ces composants se placent au bas de l’ordre d’empilement, peu importe quand l’instance de composant est créée par rapport aux autres composants. Avec la version 2.8.1, tous les composants utilisent désormais l’API `appendChild()`, ce qui signifie que l’ordre d’empilement des composants correspondrait à l’ordre de création de l’instance.

   * L’utilisation du modificateur `iscommand` pour définir le format du canal alpha de l’image n’est pas prise en charge. Utilisez plutôt le paramètre du composant `FMT` .
   * Pour le moment, la propriété de transformation CSS n’est pas prise en charge.

* Appareils tactiles

   * Le mouvement de pincement sur les périphériques tactiles ne génère pas d’événement de zoom.

* Conteneur

   * La bordure, le remplissage et les marges du conteneur ne sont pas pris en charge. Adobe suggère d’ajouter des éléments de style à la balise DIV parente.
   * Vous devez définir explicitement la taille du conteneur ou les composants peuvent être dimensionnés correctement.

* Composant d’impression

   * En raison des restrictions du navigateur, dans Internet Explorer 9, le composant d’impression peut ne pas mettre correctement à l’échelle le contenu sur le papier.

* Composant IconEffect

   * IconEffect génère une erreur de script sur Internet Explorer si `autohide` est désactivé (défini sur `0`).

* Composant ImageMapEffect

   * Retardez l’icône de repositionnement lors du panoramique de l’image sur le composant d’affichage.

* Composant MediaSet

   * Les ressources intégrées demandent le même codage que sur l’URL.

* Composant NavigationView

   * Actuellement, le composant ne prend pas en charge le redimensionnement.

* Composant PageScrubber

   * Sur l’iPhone 5, lorsque la bulle PageScrubber est définie sur text, elle affiche des artefacts lorsque vous faites glisser le bouton le long de la piste. L’utilisation de `-webkit-background-clip: content;` dans le style résout le problème.

* Composant SpinView

   * La vue à 360° semble parfois se figer après le mouvement de glissement et la rotation de l’appareil lorsque l’image tourne.

* Composant Nuancier

   * Lorsque vous sélectionnez un échantillon hors limites, deux mises en surbrillance s’affichent.
   * Le défilement automatique avec la méthode `selectSwatch()` ne fonctionne pas correctement.

* VideoPlayer

   * Image vidéo non mise à jour si la recherche est définie sur 100 % et que la version de secours est définie sur auto.
   * Un blocage des macros peut parfois survenir lors de la recherche vidéo en mode de diffusion HLS dans les navigateurs Chrome, Firefox et Internet Explorer.
   * Il se peut que l’image d’affiche ne s’affiche pas dans le navigateur Microsoft Edge pour le premier visiteur.
   * L’image d’affiche peut se masquer après le chargement de la vidéo dans Internet Explorer 9 lorsque la lecture progressive est utilisée.

## Dynamic Media Image Serving 6.3.2 et Image Rendering 6.3.2 {#section-19a3e96f52c74757bcdea0f8a11001f2}

* Utilitaire IC - L’indicateur `downsample2x2` n’est plus pris en charge. Cet indicateur était un sous-échantillonneur 2x2 de mauvaise qualité qui n’est plus utilisé par IPS.
* En-tête CORS : actuellement, l’en-tête CORS est configuré pour les requêtes `/is/content/`.
