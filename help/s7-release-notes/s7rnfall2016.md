---
description: '"Notes de mise à jour les plus récentes pour la version de l’automne 2016 d’Adobe Scene7, qui fait partie de la solution Adobe Experience Manager dans le Adobe Marketing Cloud."'
solution: Experience Manager
title: Version de l’automne 2016 de Scene7
feature: Dynamic Media Classic
role: Developer,Business Practitioner
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '2238'
ht-degree: 0%

---


# Version de l’automne 2016 de Scene7{#scene-fall-release}

Notes de mise à jour les plus récentes pour la version Adobe Scene7 de l’automne 2016 de la solution Adobe Experience Manager dans le Adobe Marketing Cloud.

## Version de l’automne 2016 de Scene7 {#topic-791cdf80f91e457fbb63bfedf79f5a94}

Notes de mise à jour les plus récentes pour la version de [!DNL Adobe Scene7] automne 2016 de la solution [!DNL Adobe Experience Manager] dans [!DNL Adobe Marketing Cloud].

* [Généraux](s7rnfall2016.md#section-52afeb72ecb34c1585ea67a5051825a2)
* [Scene7](s7rnfall2016.md#section-24487cb493444d808fb7193f0a00cdd4)
* [Visionneuses (Image Serving 5.5.3)](s7rnfall2016.md#section-1d59bcd5825d487b80b59a6d1a08ed30)
* [Visionneuses (Image Serving 5.5.2)](s7rnfall2016.md#section-9932c988cfee45749594af481dfc6476)
* [Visionneuses (Image Serving 5.5.1)](s7rnfall2016.md#section-833ab92c91c941d2bfdc27f233f582ad)
* [Kit de développement de visionneuse HTML5 3.0.1](s7rnfall2016.md#section-30e2392859c442d1aab2766d0f1d1580)
* [Dynamic Media Classic Image Serving 6.3.2 et Image Rendering 6.3.2](s7rnfall2016.md#section-19a3e96f52c74757bcdea0f8a11001f2)

## Généraux {#section-52afeb72ecb34c1585ea67a5051825a2}

L&#39;Adobe est heureux d&#39;annoncer la disponibilité de la diffusion de contenu HTTP/2 avec l&#39;avantage global d&#39;améliorer les performances.

Voir [Diffusion HTTP2 de la FAQ sur le contenu](https://experienceleague.adobe.com/docs/experience-manager-65/assets/dynamic/http2.html#dynamic).

## Scene7 Publishing System {#section-24487cb493444d808fb7193f0a00cdd4}

Pour obtenir une documentation complète, voir [https://experienceleague.adobe.com/docs/dynamic-media-classic/using/home.html](https://experienceleague.adobe.com/docs/dynamic-media-classic/using/home.html)

**Nouvelles fonctionnalités, améliorations et corrections de bogues**

* Suppression de la fonction de découpe vidéo de l’interface utilisateur [!DNL Adobe Scene7 Publishing System].
* Authentification Ajoutée à tous les servlets Scene7 si nécessaire et possible.
* Correction de bogues impliquant la Vue de Liste dans la corbeille.
* Suppression de **la fonction d’administrateur Dynamic Media Classic (Scene7)** de User Management en raison de problèmes de sécurité.
* FTP WebAdmin prend désormais en charge l’authentification OKTA.
* Suppression de la fonctionnalité du mot de passe par défaut qui a été créée pour les nouveaux utilisateurs du portail multimédia.
* Correction de bogues impliquant le mot de passe temporaire généré lors de l’ajout d’un nouvel utilisateur. Le mot de passe ne répondait pas aux exigences de mot de passe nécessaires.
* Résolution de problèmes de saturation du disque racine WebAdmin.
* Correction de bogues impliquant la désactivation d’un utilisateur qui n’est pas immédiatement répercuté dans l’interface utilisateur.
* Correction de bogues impliquant la suppression d’un utilisateur qui ne vous permettait pas de recréer l’utilisateur ultérieurement.
* Correction d’un bogue concernant le courrier électronique de bienvenue envoyé aux nouveaux utilisateurs de Scene7 qui n’incluait pas l’authentification pour contrôler certains paramètres.
* Correction d’un bogue en raison duquel la récupération d’une liste de dossiers FTP échouait si un dossier comportait des caractères spéciaux dans son nom.
* Configurez les prestataires OKTA pour les environnements Scene7.
* Prise en charge Ajoutée de l’ID d’organisation du Marketing Cloud pour Viewer Analytics.
* Mise en oeuvre du client Scene7 SAML.

## Visionneuses (Image Serving 5.5.3) {#section-1d59bcd5825d487b80b59a6d1a08ed30}

Pour obtenir une documentation complète, consultez le [Guide de référence des visionneuses](https://experienceleague.adobe.com/docs/dynamic-media-developer-resources/library/home.html).

**Correctifs pour Image Serving 5.5.3**

* Compatibilité avec les bibliothèques RequireJS et DOJO.

   Mise en cache JS du SDK consolidé pendant le déploiement de la visionneuse.

## Visionneuses (Image Serving 5.5.2) {#section-9932c988cfee45749594af481dfc6476}

Pour obtenir une documentation complète, consultez le [Guide de référence des visionneuses](https://experienceleague.adobe.com/docs/dynamic-media-developer-resources/library/home.html).

**Correctifs pour Image Serving 5.5.2**

* La lecture de la vidéo a échoué dans Internet Explorer 11 sous Windows 7.
* `initialframe` n’affectait pas le mode portrait sur les périphériques mobiles pour le catalogue électronique HTML5.

## Visionneuses (Image Serving 5.5.1) {#section-833ab92c91c941d2bfdc27f233f582ad}

Pour obtenir une documentation complète, consultez le [Guide de référence des visionneuses](https://experienceleague.adobe.com/docs/dynamic-media-developer-resources/library/home.html).

**Nouvelles fonctionnalités, améliorations et corrections de bogues pour Image Serving 5.5.1**

* Visionneuse de catalogue électronique HTML5 avec fonction de recherche.
* Ajouté la lecture vidéo en flux continu HLS comme méthode de diffusion vidéo par défaut pour la majorité des systèmes de bureau. La diffusion en flux continu de la vidéo HDS sur Flash est toujours disponible en tant qu’option de lecture alternative.
* Prise en charge Ajoutée des périphériques dotés de la souris et d’une entrée tactile exécutant le navigateur Chrome.
* Prise en charge Ajoutée de l’ID d’organisation de Marketing Cloud dans l’intégration d’Analytics.
* Mettez à jour la bibliothèque JavaScript AppMeasurement vers la version 1.6.1.
* Prise en charge Ajoutée de l’orientation de droite à gauche dans la visionneuse de catalogue électronique.
* Correction d’un problème en raison duquel `tip=0,-1,0` provoquait une erreur hors plage.

**Notes de compatibilité**

* Blackberry

   * Incompatibilité avec les anciens jeux AVS. Les clients peuvent avoir besoin de recharger les visionneuses AVS pour autoriser la lecture.

* Généraux

   * La mise à l’échelle côté navigateur peut rendre l’interface utilisateur et les images floues lorsque l’utilisateur effectue un zoom sur la page. La mise en forme de l’interface utilisateur peut également s’afficher incorrectement en fonction du zoom. Cette opération sera reportée en plein écran.
   * En raison de la limitation de taille sur les périphériques mobiles, la visionneuse de supports variés utilise le mouvement des diapositives pour permuter des images dans des visionneuses d’images incorporées au lieu d’appuyer sur le composant de nuances incorporées. Le composant est présent en tant qu’indicateur visuel.
   * Dans les navigateurs Internet Explorer et certains périphériques tactiles, le mode plein écran n’occupe pas l’intégralité de l’écran du périphérique. Il redimensionne l’application en fonction de la taille de la fenêtre du navigateur.
   * Le bouton Fermer ne fonctionne pas sous iOS 8.0 et 8.1, mais il n’apparaît plus sous iOS 8.2.

* Galaxy SIII

   * Fuite de mémoire visible avec les visionneuses HTML5 de zoom et de catalogue électronique. Une navigation répétée dans les cadres peut provoquer un blocage du navigateur.
   * Si vous appuyez sur le doublon sur la visionneuse, il se peut que la page entière fasse l’objet d’un zoom au lieu d’une seule visionneuse avec la mise à l’échelle côté navigateur activée.

* Galaxy S4

   * Périphérique détecté comme tablette en mode portrait avec le mode Plein écran coché dans les paramètres du navigateur.

* Galaxy Nexus

   * Si vous appuyez sur le doublon sur la visionneuse, il se peut que la page entière fasse l’objet d’un zoom au lieu d’une seule visionneuse avec la mise à l’échelle côté navigateur activée.

* Galaxy Nexus 10 et tablette Galaxy

   * Catalogue électronique présentant une planche incorrecte avec des orientations portrait et paysage.

* Périphériques mobiles HTC

   * Les périphériques mobiles HTC que nous avons découvert montrent que l&#39;incapacité à désactiver le zoom par pincement natif est une &quot;fonctionnalité&quot; de l&#39;enveloppe HTC UI wrapper (HTC Sense). Cela peut entraîner un zoom sur toute la page lors de l’utilisation du mouvement &quot;pincer pour zoomer&quot; sur la visionneuse. Suggérez plutôt d’utiliser doublon-appuyer.
   * Les icônes de zone cliquable peuvent se chevaucher si les zones cliquables sont petites et rapprochées les unes des autres.

* Vidéo HTML5

   * Internet Explorer 9 : les images d’affiche personnalisées ne s’affichent pas.
   * `IntialBitRate` est uniquement pris en charge avec la lecture HLS du logiciel et HDS du Flash. Il ne fonctionne pas lorsque la lecture utilise le lecteur natif.
   * Actuellement, la lecture progressive d’OGG et de WebM n’est pas prise en charge.
   * La mise à l’échelle du navigateur peut entraîner l’affichage d’une taille incorrecte du lecteur vidéo (inclut les paramètres d’affichage du panneau de configuration Windows)
   * La recherche de vidéos en flux continu HLS sur Safari peut être incohérente.

* Internet Explorer

   * Le mode Quirks n&#39;est pas pris en charge pour le moment.
   * Le mode de compatibilité n’est pas pris en charge pour le moment.
   * Internet Explorer sur mobile n’est pas pris en charge pour le moment.

* iOS

   * Les catalogues électroniques volumineux peuvent entraîner un blocage du navigateur sur l’iPad 2.
   * Les téléphones iPhone 6+ sont détectés comme tablettes par les lecteurs.

* Safari

   * Safari 6.1 ou version ultérieure : Les paramètres des modules externes Internet peuvent empêcher la lecture vidéo par Flash.
   * La &quot;recherche&quot; de vidéo à l’aide de la diffusion HLS en flux continu sur Safari peut être incohérente.
   * Impossible de rechercher la fin de la vidéo sur Safari 6 à l’aide de la diffusion en flux continu HLS.

**Problèmes et restrictions connus**

* Les modificateurs de diffusion d’images de `iscommands` ne sont pas ajoutés à la demande `req=set` par conception. Les modificateurs qui affectent uniquement l’affichage des images fonctionnent correctement. Les modificateurs affectant la taille doivent être utilisés dans une ressource complexe. Par exemple,

   `https://s7d9.scene7.com/s7viewers/html5/BasicZoomViewer.html?asset= {Scene7SharedAssets/Backpack_B?extendn=0.5%252C0.5%252C0.5%252C0.5}`

* [] FlyoutIE9 reste parfois à l’écran après désactivation de la souris.
* La mise à l’échelle du navigateur entraîne un mauvais redimensionnement.
* iPad 2 : La ressource de catalogue électronique volumineux bloquera Safari sur iOS.
* Toutes les visionneuses

   * Les filigranes, l’obscurcissement et le verrouillage ne sont pas pris en charge.
   * Les paramètres d’image prédéfinis ne sont pas pris en charge.
   * Pour le moment, il n’est pas possible d’Ajouter ou de supprimer la visionneuse du DOM à l’aide de `display:none` CSS ou en la détachant dynamiquement du noeud parent.

* HTML5 Toutes les visionneuses

   * L’incorporation de la visionneuse dans le tableau peut entraîner un dimensionnement incorrect ou un placement incorrect de la visionneuse en mode plein écran non natif. Suggérez plutôt d’utiliser des balises DIV.
   * Les paramètres dont les noms d&#39;instance sont explicites dans le code nécessitent également que les noms d&#39;instance de l&#39;URL soient remplacés (par exemple, `zoomView.iconfeffect=0`).
   * Pour le moment, le recadrage de la commande Diffusion d’images n’est pas pris en charge.
   * Le bouton Fermer fonctionne uniquement si la visionneuse est ouverte dans la fenêtre enfant.
   * Le modificateur `iscommands` ne prend pas en charge les modificateurs de diffusion d’images qui affectent la taille de l’image.

* Catalogue électronique HTML5

   * Si vous naviguez jusqu’à une autre page HTML et revenez parfois, la visionneuse se réinitialise à la première page.
   * La mise en page s’affiche parfois incorrectement après rotation du périphérique iOS. La fonction de zoom dans la page corrige la disposition.
   * Liens internes uniquement à la page la plus à gauche dans les planches de plusieurs pages. Affecte les périphériques mobiles en mode portrait.
   * Liens InitalFrame uniquement vers la page la plus à gauche dans les planches de plusieurs pages. Affecte les périphériques mobiles en mode portrait.
   * En raison des limitations du navigateur, la fonction d’impression n’est pas disponible dans IE9.

* HTML5 MixedMedia

   * Actuellement, la lecture de bande son n’est pas prise en charge.

* HTML5 Social

   * Pour afficher correctement les miniatures dans le courrier électronique sortant, le modificateur `serverurl` doit avoir une URL absolue.

* Vidéo HTML5

   * L’image d’affiche peut rencontrer l’erreur &quot;taille maximale&quot;. Il se peut que la société doive augmenter la limite définie pour la publication Image Serving.
   * Les légendes vidéo nécessitent un jeu de règles de société si l’hébergement de la page HTML est diffusé à partir d’un serveur externe (et non d’un serveur Scene7). Contactez l&#39;assistance Adobe pour obtenir de l&#39;aide.
   * Le suivi Analytics peut signaler un pourcentage de lecture incorrect en raison de la mise en mémoire tampon.
   * Un cadre noir peut s’afficher sur les appareils iPad ou Android à la place de l’image d’affiche.
   * L’image noire peut clignoter à l’écran pendant le chargement du lecteur sur les appareils iPad ou Android.
   * Les bordures noires s’affichent sur le côté du composant VideoPlayer lorsque l’arrière-plan est défini sur blanc/transparent sur les périphériques iPad.
   * La dernière image de la vidéo peut être déformée sur iPad sous iOS 7.
   * Des macroblocages occasionnels peuvent survenir lors de la recherche vidéo en mode de diffusion HLS dans les navigateurs Chrome, Firefox et Internet Explorer.
      * L&#39;image d&#39;affiche peut ne pas s&#39;afficher dans le navigateur Microsoft Edge pour la première fois du visiteur.
      * L’image d’affiche peut se masquer après le chargement de la vidéo dans Internet Explorer 9 lorsque la lecture progressive est utilisée.

## Kit de développement de visionneuse HTML5 Scene7 3.0.2 {#section-30e2392859c442d1aab2766d0f1d1580}

Le Guide de l’utilisateur se trouve dans le dossier SDK de la visionneuse HTML5 Adobe de l’installation du client. La documentation de l’API de composant se trouve dans le sous-dossier docs de l’installation du client.

**Correctifs pour la version 3.0.2**

* Lecteur vidéo - La lecture de la vidéo a échoué dans Internet Explorer 11 sous Windows 7
* Table des matières - `initialframe` n’a pas affecté le mode portrait sur les périphériques mobiles pour la visionneuse de catalogue électronique HTML5.

**Nouvelles fonctionnalités, améliorations et corrections de bogues pour la version 3.0.1**

* Généraux

   * Ajouté la lecture vidéo en flux continu HLS comme méthode de diffusion vidéo par défaut pour la majorité des systèmes de bureau. La diffusion en flux continu de la vidéo HDS sur Flash est toujours disponible en tant qu’option de lecture alternative.
   * Composants SearchManager, SearchPanel, SearchEffect et SearchButton Ajoutés pour prendre en charge la nouvelle fonctionnalité de recherche dans les visionneuses de catalogue électronique.
   * Prise en charge Ajoutée des périphériques dotés de la souris et d’une entrée tactile s’exécutant sur le navigateur Chrome.
   * Amélioration de la détection des versions d’Android pour la prise en charge des versions futures du système d’exploitation
   * Ajoutez la prise en charge de l’orientation de droite à gauche dans les composants SDK spécifiques au catalogue électronique.

* ControlBar

   * Défilement facultatif Ajouté pour le contenu ControlBar au cas où il ne correspondrait pas à la largeur disponible.

* Vue de zoomFenêtre déroulante

   * Correction de la casse en raison de laquelle `tip=0,-1,0` provoquait une erreur hors plage.

**Notes de compatibilité**

* Android 4.x

   * Pour désactiver la valeur par défaut, le bleu met en surbrillance la règle CSS suivante doit être ajoutée pour le composant :

      `-webkit-tap-highlight-color: rgba(0,0,0,0);`

* Blackberry

   * La lecture vidéo peut cesser lors de la modification des flux de débit binaire dans les visionneuses AVS.

* Chrome

   * Tout appel d’API qui force la reconstruction des composants peut être ignoré en raison de la mise en cache interne de Chrome.

* Galaxy SIII

   * Le chargement du lecteur échoue parfois en mode plein écran.
   * Pageview souffre actuellement d&#39;une fuite de mémoire sur le périphérique.
   * Le mouvement doublon de la touche permet de zoomer sur la visionneuse et la page lorsque la mise à l’échelle côté navigateur est principale.

* Galaxy Nexus

   * Artefacts s’affichant sur certains composants de vue.
   * Le mouvement doublon de la touche permet de zoomer sur la visionneuse et la page lorsque la mise à l’échelle côté navigateur est principale.

* iPad 3

   * L’iPad 3 a une résolution native de 2 048 x 1 536 pixels. Cela peut entraîner des problèmes d’affichage si la société EST publiée, la taille limite d’image définie est inférieure à cette valeur.

* iPhone4

   * L’icône de relecture de l’effet d’icône est remplacée par l’icône de lecture après le défilement de la page.

* Internet Explorer

   * Dans IE 10 et les versions plus anciennes du mode plein écran n’occupent pas tout l’écran, mais redimensionne simplement l’application à la taille de la fenêtre du navigateur.
   * Le mode de rendu des quirks n&#39;est pas pris en charge.
   * Internet Explorer sur mobile n’est pas pris en charge pour le moment.
   * Le chargement du fichier Util.js peut échouer s’il est inclus de manière asynchrone.
   * L’icône IconEffect bloque les événements de clic sur les composants SpinView et ZoomView.

* Lecteurs vidéo natifs

   * La mise en page des composants de l’interface utilisateur sur VideoPlayer n’est pas prise en charge lorsque VideoPlayer est utilisé pour appeler le lecteur natif du périphérique.
   * La lecture vidéo en mode natif est incohérente dans Safari 6.
   * La lecture native remplace l’icône de relecture par l’icône de lecture après le défilement de la page.

* Périphériques tactiles

   * Le mode plein écran n’occupe pas l’intégralité de l’écran du périphérique, mais redimensionne simplement l’application à la taille de la fenêtre du navigateur.
   * Les curseurs personnalisés ne fonctionnent pas sur les périphériques tactiles.
   * La mise à l’échelle des pages sur les périphériques tactiles n’est pas prise en charge pour le moment. L’incorporation de visionneuses HTML5 requiert la balise meta de fenêtre d’affichage avec les paramètres appropriés.

* Xoom

   * Le mouvement doublon de la touche permet de zoomer sur la visionneuse et la page lorsque la mise à l’échelle côté navigateur est principale.

**Problèmes et restrictions connus**

* Tous les composants

   * Dans les versions 2.7.2 et antérieures, certains composants ont été ajoutés au modèle DOM à l’aide de l’API `insertBefore()`. Par conséquent, ces composants se placeraient au bas de l’ordre d’empilement, peu importe quand l’instance de composant est créée par rapport aux autres composants. Avec la version 2.8.1, tous les composants utilisent maintenant l&#39;API `appendChild()`, ce qui signifie que l&#39;ordre d&#39;empilement des composants correspondrait à l&#39;ordre de création de l&#39;instance.

   * L’utilisation du modificateur `iscommand` pour définir le format de canal alpha de l’image n’est pas prise en charge. Utilisez plutôt le paramètre de composant `FMT`.
   * Pour le moment, la propriété de transformation CSS n’est pas prise en charge.

* Périphériques tactiles

   * Le mouvement de pincement sur les périphériques tactiles ne génère pas de événement de zoom

* Conteneur

   * La bordure, le remplissage et les marges sur le conteneur ne sont pas pris en charge. Adobe suggère d’ajouter des éléments de style à la balise DIV parente.
   * Vous devez définir explicitement la taille du conteneur ou les composants peuvent être correctement dimensionnés.

* Imprimer le composant

   * En raison des limitations du navigateur, dans Internet Explorer 9, le composant d’impression peut ne pas mettre à l’échelle correctement le contenu sur le papier.

* Composant IconEffect

   * IconEffect génère une erreur de script sur Internet Explorer si `autohide` est désactivé (défini sur `0`).

* Composant ImageMapEffect

   * Retard avec l’icône de repositionnement lors du panoramique de l’image sur le composant de vue.

* Composant MediaSet

   * Les ressources en ligne demandent le même codage que sur l’URL.

* Composant NavigationView

   * Actuellement, le composant ne prend pas en charge le redimensionnement.

* Composant PageScrubber

   * Sur iPhone 5, lorsque la bulle PageScrubber est définie sur texte, elle affiche des artefacts lors du glissement du bouton le long de la piste. L’utilisation de `-webkit-background-clip: content;` dans le style résout le problème.

* Composant SpinView

   * La vue à 360° semble parfois figée après le mouvement de glissement et la rotation du périphérique pendant que l’image tourne.

* Composant Nuancier

   * Lorsque vous sélectionnez une nuance hors limites, deux mises en surbrillance s’affichent.
   * Le défilement automatique avec la méthode `selectSwatch()` ne fonctionne pas correctement.

* VideoPlayer

   * L’image vidéo n’est pas mise à jour si la recherche est définie à 100 % et que la valeur de secours est définie sur auto.
   * Des blocages occasionnels de macros peuvent survenir lors de la recherche vidéo en mode de diffusion HLS dans les navigateurs Chrome, Firefox et Internet Explorer.
   * L&#39;image d&#39;affiche peut ne pas s&#39;afficher dans le navigateur Microsoft Edge pour la première fois du visiteur.
   * L’image d’affiche peut se masquer après le chargement de la vidéo dans Internet Explorer 9 lorsque la lecture progressive est utilisée.

## Dynamic Media Image Serving 6.3.2 et Image Rendering 6.3.2 {#section-19a3e96f52c74757bcdea0f8a11001f2}

* Utilitaire IC - L&#39;indicateur `downsample2x2` n&#39;est plus pris en charge. Cet indicateur était un sous-échantillonneur 2x2 de mauvaise qualité qui n&#39;est plus utilisé par IPS.
* En-tête CORS - Actuellement, l’en-tête CORS est configuré pour les demandes `/is/content/`.

