---
title: Version d’automne 2016 de Scene7
description: Dernières notes de mise à jour d’Adobe Scene7 (automne 2016), qui fait partie de la solution Adobe Experience Manager dans Adobe Experience Cloud.
solution: Experience Manager
feature: Dynamic Media Classic
role: Developer,User
exl-id: 23091ef7-750a-4ec2-9d03-1d713f436991
source-git-commit: baf8015dc93cfa6be0a841243a7e3524f06f1639
workflow-type: tm+mt
source-wordcount: '2234'
ht-degree: 0%

---

# Version d’automne 2016 de Scene7{#scene-fall-release}

Notes de mise à jour les plus récentes pour Adobe Scene7 - Version d’automne 2016 de la solution Adobe Experience Manager dans Adobe Experience Cloud.

## Version d’automne 2016 de Scene7 {#topic-791cdf80f91e457fbb63bfedf79f5a94}

Notes de mise à jour les plus récentes pour [!DNL Adobe Scene7] version de l’automne 2016 de la solution [!DNL Adobe Experience Manager] dans le [!DNL Adobe Experience Cloud] .

* [Généraux](s7rnfall2016.md#section-52afeb72ecb34c1585ea67a5051825a2)
* [Scene7](s7rnfall2016.md#section-24487cb493444d808fb7193f0a00cdd4)
* [Visionneuses (Diffusion D’Images 5.5.3)](s7rnfall2016.md#section-1d59bcd5825d487b80b59a6d1a08ed30)
* [Visionneuses (Diffusion D’Images 5.5.2)](s7rnfall2016.md#section-9932c988cfee45749594af481dfc6476)
* [Visionneuses (Diffusion D’Images 5.5.1)](s7rnfall2016.md#section-833ab92c91c941d2bfdc27f233f582ad)
* [Visionneuse HTML5 SDK 3.0.1](s7rnfall2016.md#section-30e2392859c442d1aab2766d0f1d1580)
* [Dynamic Media Classic Image Serving 6.3.2 et Image Rendering 6.3.2](s7rnfall2016.md#section-19a3e96f52c74757bcdea0f8a11001f2)

## Généraux {#section-52afeb72ecb34c1585ea67a5051825a2}

Adobe est heureux d’annoncer la disponibilité de la diffusion de contenu HTTP/2, avec l’avantage global d’améliorer les performances.

Voir la [HTTP2 FAQ sur la diffusion de contenu](https://experienceleague.adobe.com/docs/experience-manager-65/assets/dynamic/http2.html#dynamic).

## Scene7 Publishing System {#section-24487cb493444d808fb7193f0a00cdd4}

Pour consulter la documentation complète, voir [https://experienceleague.adobe.com/docs/dynamic-media-classic/using/home.html](https://experienceleague.adobe.com/docs/dynamic-media-classic/using/home.html)

**Nouvelles fonctionnalités, améliorations et correctifs de bugs**

* Suppression de la fonction de recut vidéo de [!DNL Adobe Scene7 Publishing System]’interface utilisateur d’.
* Ajout de l’authentification à toutes les servlets Scene7 lorsque cela est nécessaire et possible
* Correction de bugs impliquant la vue Liste dans la corbeille.
* Suppression de la fonctionnalité utilisateur **Créer un administrateur Dynamic Media Classic (Scene7)** de User Management pour des raisons de sécurité.
* FTP WebAdmin prend désormais en charge l’authentification OKTA.
* Suppression de la fonction du mot de passe par défaut qui a été créée pour les nouveaux utilisateurs du portail multimédia.
* Correction de bug impliquant le mot de passe temporaire qui était généré lorsqu’un nouvel utilisateur était ajouté. Le mot de passe ne répondait pas aux exigences de mot de passe requises.
* Résolution des problèmes de saturation du disque racine WebAdmin.
* Correction de bug entraînant la désactivation d’un utilisateur ou d’une utilisatrice qui n’était pas répercutée immédiatement dans l’interface utilisateur.
* Correction de bug impliquant la suppression d’un utilisateur ou d’une utilisatrice qui ne vous permettait pas de recréer l’utilisateur ou l’utilisatrice ultérieurement.
* Correction de bug impliquant l’e-mail de bienvenue envoyé aux nouveaux utilisateurs de Scene7 qui n’incluait pas d’authentification pour contrôler certains paramètres.
* Correction de bugs impliquant l’échec de la récupération d’une liste de dossiers FTP si le nom d’un dossier contenait des caractères spéciaux.
* Configurez les fournisseurs de services OKTA pour les environnements Scene7.
* Ajout de la prise en charge de l’ID d’organisation Experience Cloud pour la visionneuse Analytics.
* Client SAML Scene7 implémenté.

## Visionneuses (Diffusion D’Images 5.5.3) {#section-1d59bcd5825d487b80b59a6d1a08ed30}

Pour consulter la documentation complète, voir [&#x200B; Guide de référence des visionneuses &#x200B;](https://experienceleague.adobe.com/docs/dynamic-media-developer-resources/library/homeviewers.html?lang=en).

**Correctifs de bugs pour la diffusion d’images 5.5.3**

* Compatibilité avec les bibliothèques RequireJS et DOJO.

  Mise en cache JS de SDK consolidée pendant le déploiement de la visionneuse.

## Visionneuses (Diffusion D’Images 5.5.2) {#section-9932c988cfee45749594af481dfc6476}

Pour consulter la documentation complète, voir [&#x200B; Guide de référence des visionneuses &#x200B;](https://experienceleague.adobe.com/docs/dynamic-media-developer-resources/library/homeviewers.html?lang=en).

**Correctifs de bugs pour la diffusion d’images 5.5.2**

* La lecture de la vidéo a échoué dans Internet Explorer 11 sous Windows 7.
* `initialframe` n’affectait pas le mode portrait sur les appareils mobiles pour le catalogue électronique HTML5.

## Visionneuses (Diffusion D’Images 5.5.1) {#section-833ab92c91c941d2bfdc27f233f582ad}

Pour consulter la documentation complète, voir [&#x200B; Guide de référence des visionneuses &#x200B;](https://experienceleague.adobe.com/docs/dynamic-media-developer-resources/library/homeviewers.html?lang=en).

**Nouvelles fonctionnalités, améliorations et correctifs pour la diffusion d’images 5.5.1**

* Visionneuse de catalogue électronique HTML5 avec fonction de recherche.
* Ajout de la lecture vidéo en continu HLS en tant que méthode de diffusion vidéo par défaut pour la plupart des ordinateurs de bureau. La diffusion vidéo en continu HDS basée sur Flash est toujours disponible en tant qu’option de lecture alternative.
* Ajout de la prise en charge des appareils dotés d’entrées souris et tactiles exécutant le navigateur Chrome.
* Ajout de la prise en charge de l’ID d’organisation Experience Cloud à l’intégration Analytics.
* Mettez à jour la bibliothèque JavaScript d’AppMeasurement vers la version 1.6.1.
* Ajout de la prise en charge de l’orientation de droite à gauche dans la visionneuse de catalogue électronique.
* Correction d’un problème en raison duquel `tip=0,-1,0` provoquait une erreur hors plage.

**Notes de compatibilité**

* BlackBerry®

   * Incompatibilité avec les anciens ensembles AVS. Les clients doivent charger à nouveau les visionneuses AVS pour permettre la lecture.

* Généraux

   * La mise à l’échelle côté navigateur peut rendre l’interface utilisateur et les images floues lorsque l’utilisateur effectue un zoom avant sur la page. Le formatage de l’interface utilisateur peut également ne pas s’afficher correctement selon le zoom. Cet effet est propagé au plein écran.
   * En raison de la limitation de la taille sur les appareils mobiles, la visionneuse de médias mixtes utilise un mouvement de diapositive pour permuter les images dans les visionneuses d’images intégrées au lieu d’appuyer sur le composant d’échantillons intégrés. Le composant est présent comme indicateur visuel.
   * Dans les navigateurs Internet Explorer et certains appareils tactiles, le mode plein écran n’occupe pas l’écran entier de l’appareil. Au lieu de cela, il redimensionne l’application à la taille de la fenêtre du navigateur.
   * Le bouton Fermer ne fonctionne pas dans iOS 8.0 et 8.1 mais n’apparaît plus dans iOS 8.2

* Galaxy SIII

   * Fuite de mémoire vue avec les visionneuses Zoom et eCatalog HTML5. La navigation répétée à travers les cadres peut provoquer le blocage du navigateur.
   * Appuyez deux fois sur la visionneuse peut entraîner un zoom de toute la page au lieu d’une simple visionneuse avec la mise à l’échelle côté navigateur activée.

* Galaxy S4

   * Appareil détecté comme tablette en mode portrait avec plein écran activé dans les paramètres du navigateur.

* Galaxy Nexus

   * Appuyez deux fois sur la visionneuse peut entraîner un zoom de toute la page au lieu d’une simple visionneuse avec la mise à l’échelle côté navigateur activée.

* Galaxy Nexus 10 et Galaxy Tablet

   * Catalogue électronique affichant une page mal répartie avec des orientations portrait et paysage.

* Appareils mobiles HTC

   * Appareils mobiles HTC Les résultats d’Adobe montrent que l’impossibilité de désactiver le pincement-zoom natif est une « fonctionnalité » du wrapper de l’interface utilisateur HTC (HTC Sense). Ce problème peut entraîner un zoom de toute la page lors de l’utilisation du mouvement « pincer pour zoomer » sur la visionneuse. Suggérez d’utiliser le double-clic à la place.
   * Les icônes des zones cliquables peuvent se chevaucher si elles sont petites et proches.

* Vidéo HTML5

   * Internet Explorer 9 : les images d’affiche personnalisées ne s’affichent pas.
   * `IntialBitRate` modificateur n’est pris en charge qu’avec la lecture logicielle HLS et Flash HDS. Cela ne fonctionne pas lorsque la lecture utilise le lecteur natif.
   * La lecture progressive OGG et WebM n’est actuellement pas prise en charge.
   * La mise à l’échelle du navigateur peut entraîner l’affichage du lecteur vidéo à une taille incorrecte (y compris les paramètres d’affichage du panneau de contrôle du système d’exploitation Windows).
   * La recherche de vidéos à l’aide de la diffusion en continu HLS sur Safari peut être incohérente.

* Internet Explorer

   * Le mode Quirks n’est actuellement pas pris en charge.
   * Le mode de compatibilité n’est actuellement pas pris en charge.
   * Internet Explorer sur mobile n’est actuellement pas pris en charge.

* iOS

   * Les catalogues électroniques volumineux peuvent provoquer un blocage du navigateur sur iPad 2.
   * Les téléphones iPhone 6+ sont détectés comme des tablettes par les visionneuses.

* Safari

   * Safari 6.1 ou version ultérieure : les paramètres des plug-ins Internet peuvent empêcher la lecture de la vidéo Flash.
   * La « recherche » de vidéo à l’aide de la diffusion en continu HLS sur Safari peut être incohérente.
   * Impossible de rechercher la fin de la vidéo sur Safari 6 à l’aide de la diffusion en continu HLS.

**Problèmes connus et restrictions**

* Les modificateurs Diffusion d’images de `iscommands` ne sont pas ajoutés à la requête `req=set` par défaut. Les modificateurs qui affectent uniquement l’affichage des images fonctionnent correctement. Les modificateurs affectant la taille doivent être utilisés dans une ressource complexe.
* [Fenêtre déroulante] IE9 reste parfois à l’écran après l’arrêt de la souris.
* La mise à l’échelle du navigateur entraîne un redimensionnement incorrect.
* iPad 2 : une ressource de catalogue électronique volumineuse bloque Safari sur iOS.
* Toutes les visionneuses

   * Les filigranes, l’obfuscation et le verrouillage ne sont pas pris en charge.
   * Les paramètres d’image prédéfinis ne sont pas pris en charge.
   * L’ajout ou la suppression d’une visionneuse du DOM à l’aide d’`display:none` CSS ou en la détachant dynamiquement du nœud parent n’est actuellement pas pris en charge.

* HTML5 - Toutes les visionneuses

   * L’incorporation de la visionneuse dans un tableau peut entraîner un dimensionnement ou un placement incorrect de la visionneuse en mode plein écran non natif. Suggérez d’utiliser plutôt des DIV.
   * Les paramètres dont le nom d’instance est explicite dans le code nécessitent que les noms d’instance dans l’URL soient également remplacés (par exemple, `zoomView.iconfeffect=0`).
   * Le recadrage de commande de la diffusion d’images n’est actuellement pas pris en charge.
   * Le bouton Fermer fonctionne uniquement si la visionneuse est ouverte dans la fenêtre enfant.
   * Le modificateur `iscommands` ne prend pas en charge les modificateurs de diffusion d’images affectant la taille des images.

* Catalogue électronique HTML5

   * Lorsque vous accédez à une autre page HTML et revenez de temps en temps, la visionneuse revient à la première page.
   * La mise en page s’affiche parfois incorrectement après la rotation de l’appareil iOS. Le zoom sur la page corrige la disposition.
   * Liens internes uniquement vers la page la plus à gauche dans les planches à plusieurs pages. Affecte les appareils mobiles en mode portrait.
   * InitialFrame renvoie uniquement vers la page la plus à gauche dans les planches à plusieurs pages. Affecte les appareils mobiles en mode portrait.
   * En raison des limitations du navigateur, la fonction d’impression n’est pas disponible dans IE9.

* HTML5 MixedMedia

   * La lecture de la bande sonore n’est pas prise en charge.

* HTML5 Social

   * Pour effectuer correctement le rendu des miniatures dans l’e-mail sortant, le modificateur `serverurl` doit avoir une URL absolue.

* Vidéo HTML5

   * L’image d’affiche peut rencontrer une erreur de « taille maximale ». La société doit augmenter le paramètre de limite pour la publication du service d’image.
   * Les sous-titres vidéo nécessitent un ensemble de règles d’entreprise si la page HTML est hébergée sur un serveur externe (et non un serveur Scene7). Contactez l’assistance Adobe pour obtenir de l’aide.
   * Le suivi Analytics peut signaler un pourcentage de lecture incorrect en raison de la mise en mémoire tampon
   * Un cadre noir au lieu d’une image d’affiche peut s’afficher sur les appareils iPad ou Android™.
   * Un cadre noir peut clignoter à l’écran lors du chargement de la visionneuse sur les appareils iPad ou Android™.
   * Les bordures noires s’affichent sur le côté du composant VideoPlayer lorsque l’arrière-plan est défini sur blanc/transparent sur les appareils iPad.
   * La dernière image de la vidéo peut être déformée sur iPad à l’aide d’iOS 7.
   * Des macroblocages occasionnels peuvent se produire pendant la recherche de vidéos en mode de diffusion en continu HLS dans les navigateurs Chrome, Firefox et Internet Explorer.
      * L’image d’affichage peut ne pas s’afficher dans le navigateur Microsoft® Edge pour le premier visiteur.
      * L’image d’affichage peut se masquer après le chargement de la vidéo dans Internet Explorer 9 lorsque la lecture progressive est utilisée.

## SDK 3.0.2 de la visionneuse Scene7 HTML5 {#section-30e2392859c442d1aab2766d0f1d1580}

Le Guide de l’utilisateur se trouve dans le dossier SDK de la visionneuse Adobe HTML5 de l’installation du client. La documentation de l’API de composant se trouve dans le sous-dossier docs de l’installation du client.

**Correctifs de bugs pour 3.0.2**

* VideoPlayer - La lecture de la vidéo a échoué dans Internet Explorer 11 sous Windows 7.
* Table des matières - `initialframe` n’a pas affecté le mode portrait sur les appareils mobiles pour la visionneuse de catalogue électronique HTML5.

**Nouvelles fonctionnalités, améliorations et correctifs pour 3.0.1**

* Généraux

   * Ajout de la lecture vidéo en continu HLS en tant que méthode de diffusion vidéo par défaut pour la plupart des ordinateurs de bureau. La diffusion vidéo en continu HDS basée sur Flash est toujours disponible en tant qu’option de lecture alternative.
   * Ajout des composants SearchManager, SearchPanel, SearchEffect et SearchButton pour la prise en charge de la nouvelle fonctionnalité Search dans les visionneuses de catalogue électronique.
   * Ajout de la prise en charge des appareils dotés d’une entrée de souris et tactile s’exécutant sur le navigateur Chrome.
   * Refactorisation de la détection des versions d’Android™ pour prendre en charge les futures versions du système d’exploitation.
   * Ajoutez la prise en charge de l’orientation de droite à gauche dans les composants SDK spécifiques au catalogue électronique.

* ControlBar

   * Ajout d’un défilement facultatif pour le contenu ControlBar s’il ne tient pas dans la largeur disponible.

* FlyoutzoomView

   * Correction d’un cas où `tip=0,-1,0` provoquait une erreur hors plage.

**Notes de compatibilité**

* Android™ 4.x

   * Pour désactiver la valeur par défaut, mettez en surbrillance bleue la règle CSS suivante doit être ajoutée pour le composant :

     `-webkit-tap-highlight-color: rgba(0,0,0,0);`

* BlackBerry®

   * La lecture vidéo peut cesser lors de la modification des flux de débit dans les visionneuses AVS.

* Chrome

   * Tout appel d’API qui force la reconstruction du composant peut être ignoré en raison du cache interne de Chrome.

* Galaxy SIII

   * Le chargement de la visionneuse en plein écran échoue parfois.
   * La page vue souffre actuellement d’une fuite de mémoire sur l’appareil.
   * Appuyez deux fois pour zoomer sur la visionneuse et la page lorsque la mise à l’échelle côté navigateur est active.

* Galaxy Nexus

   * Les artefacts s’affichent sur certains composants de vue.
   * Appuyez deux fois pour zoomer sur la visionneuse et la page lorsque la mise à l’échelle côté navigateur est active.

* IPAD 3

   * IPad 3 a une résolution native de 2 048 x 1 536. Cette résolution peut entraîner des problèmes d’affichage si la limite de taille d’image de la publication IS de l’entreprise est définie sur une valeur inférieure.

* IPHONE4

   * Icône Icône de relecture remplacée par Icône de relecture après le défilement de la page.

* Internet Explorer

   * Sur IE 10 et les versions antérieures, le mode plein écran n’occupe pas tout l’écran, mais redimensionne simplement l’application à la taille de la fenêtre du navigateur.
   * Le mode de rendu des requêtes n’est pas pris en charge.
   * Internet Explorer sur mobile n’est actuellement pas pris en charge.
   * Le chargement d’Util.js peut échouer en cas d’inclusion asynchrone.
   * L’icône IconEffect bloque les événements de clic sur les composants SpinView et ZoomView.

* Lecteurs vidéo natifs de l’appareil

   * La superposition des composants de l’interface utilisateur sur VideoPlayer n’est pas prise en charge lorsque VideoPlayer est utilisé pour appeler le lecteur natif de l’appareil.
   * La lecture vidéo en mode natif est incohérente dans Safari 6.
   * La lecture native remplace l’icône de relecture par l’icône de lecture après le défilement de la page.

* Appareils tactiles

   * le mode plein écran n’occupe pas tout l’écran de l’appareil, il redimensionne simplement l’application à la taille de la fenêtre du navigateur.
   * Les curseurs personnalisés ne fonctionnent pas sur les appareils tactiles.
   * La mise à l’échelle de page sur les appareils tactiles n’est actuellement pas prise en charge. L’incorporation des visionneuses HTML5 nécessite une balise meta viewport avec les paramètres appropriés.

* Chambre

   * Appuyez deux fois pour zoomer sur la visionneuse et la page lorsque la mise à l’échelle côté navigateur est active.

**Problèmes connus et restrictions**

* Tous les composants

   * Dans les versions 2.7.2 et antérieures, certains composants étaient ajoutés au DOM à l’aide de l’API `insertBefore()`. Par conséquent, ces composants se placent au bas de l’ordre d’empilement, quel que soit le moment où l’instance du composant est créée par rapport aux autres composants. Avec la version 2.8.1, tous les composants utilisent désormais `appendChild()` API, ce qui signifie que l’ordre d’empilement des composants correspond à l’ordre de création des instances.

   * L’utilisation du modificateur `iscommand` pour définir le format de canal alpha de l’image n’est pas prise en charge. Utilisez plutôt le paramètre de `FMT` de composant .
   * La propriété de transformation CSS n’est actuellement pas prise en charge.

* Appareils tactiles

   * Le mouvement de pincement sur les appareils tactiles ne génère pas d’événement de zoom

* Conteneur

   * Les bordures, marges intérieures et marges du conteneur ne sont pas prises en charge. Adobe suggère d’ajouter des éléments de style au DIV parent.
   * Doit définir explicitement la taille du conteneur ou les composants peuvent être dimensionnés correctement.

* Composant d’impression

   * En raison des limitations du navigateur, dans Internet Explorer 9, le composant d’impression peut ne pas mettre correctement à l’échelle le contenu sur le papier.

* Composant IconEffect

   * IconEffect génère une erreur de script sur Internet Explorer si `autohide` est désactivé (défini sur `0`).

* Composant ImageMapEffect

   * Retard avec icône de repositionnement lors du panoramique sur le composant d’affichage.

* Composant MediaSet

   * Les ressources intégrées demandent le même codage que sur l’URL.

* Composant NavigationView

   * Actuellement, le composant ne prend pas en charge le redimensionnement.

* Composant PageScrubber

   * Sur iPhone 5, lorsque la bulle PageScrubber est définie sur texte, elle affiche des artefacts lors du glissement du bouton le long de la piste. L’utilisation de `-webkit-background-clip: content;` dans le style permet de contourner le problème.

* Composant SpinView

   * SpinView semble parfois se figer après un mouvement de balayage et une rotation de l’appareil pendant que l’image tourne.

* Composant Nuanciers

   * Lors de la sélection d’un échantillon hors limites, deux surbrillances s’affichent.
   * Le défilement automatique avec `selectSwatch()` méthode ne fonctionne pas correctement.

* VideoPlayer

   * L’image vidéo n’est pas mise à jour si la recherche est définie sur 100 % avec la version de secours définie sur auto.
   * Un blocage occasionnel des macros peut se produire pendant la recherche de vidéos dans le mode de diffusion en continu d’HLS dans les navigateurs Chrome, Firefox et Internet Explorer.
   * L’image d’affichage peut ne pas s’afficher dans le navigateur Microsoft® Edge pour le premier visiteur.
   * L’image d’affichage peut se masquer après le chargement de la vidéo dans Internet Explorer 9 lorsque la lecture progressive est utilisée.

## Dynamic Media Image Serving 6.3.2 et Image Rendering 6.3.2 {#section-19a3e96f52c74757bcdea0f8a11001f2}

* Utilitaire IC - `downsample2x2` indicateur n&#39;est plus pris en charge. Cet indicateur était un sous-échantillonneur 2x2 de mauvaise qualité qui n&#39;est plus utilisé par IPS.
* En-tête CORS : actuellement, l’en-tête CORS est configuré pour les requêtes `/is/content/`.
