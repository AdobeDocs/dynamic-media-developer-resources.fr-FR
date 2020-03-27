---
description: Certaines restrictions et problèmes connus doivent être pris en compte lors de l’utilisation de Scene7 Image Serving.
seo-description: Certaines restrictions et problèmes connus doivent être pris en compte lors de l’utilisation de Scene7 Image Serving.
seo-title: Restrictions et problèmes connus
solution: Experience Manager
title: Restrictions et problèmes connus
topic: Scene7 Image Serving - Image Rendering API
uuid: 9f9fad41-4828-4fba-8f5f-2c33e7811c71
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# Restrictions et problèmes connus{#restrictions-and-known-issues}

Certaines restrictions et problèmes connus doivent être pris en compte lors de l’utilisation de Scene7 Image Serving.

## Erreur de documentation {#section-b1579410b11e41e488c7de9ecc7e8d5c}

* Le nombre de lignes ne dépassera pas le nombre maximal de `\copyfitmaxlines` paramètres et le nombre de lignes explicites dans la saisie de texte.
* Les accolades et les parenthèses correspondantes sont requises dans les visionneuses d’images. Si les accolades et les parenthèses ne correspondent pas, elles doivent être codées au format URL.
* L’alerte de temps de réponse globale côté serveur inclut les réponses d’erreur.
* La `id=` commande est actuellement requise lors de l’utilisation de la `rect=` commande avec une demande d’image ou de masque.

## Différences connues textPs= vs text= {#section-16ede4c13a7648feb0d2fc93341fd4aa}

* L’italique synthétique est rendu moins incliné que lors de l’utilisation `text=`.
* Le soulignement est un peu plus bas et plus fin que lors de l’utilisation `text=`.
* `\expnd` et `\expndtw` utilisée avec des valeurs négatives élevées provoquent le placement des caractères devant les autres lors de l’utilisation `text=`.

* `\charscaley` se met à l’échelle différemment que lors de l’utilisation `text=` , mais n’affecte pas la hauteur de ligne.

* Si la dernière ligne de texte ne tient pas, la ligne entière est ignorée au lieu d’apparaître comme coupure.
* `\slmult` et `\sl` se comportent différemment de MS Word et `text=`, ils prennent simplement effet pour les paragraphes actuels et suivants.

* `\sb` s’applique au premier paragraphe pour MS Word et `text=`, ce n’est pas le cas d’Adobe InDesign et de Photoshop.

* `\sa` s’applique au dernier paragraphe pour MS Word et `text=`, ce n’est pas le cas d’Adobe InDesign et de Photoshop.

## Compatibilité descendante {#section-a76842f751944f4fb664af296d064122}

* L’échappement du caractère de soulignement ( `\_`) dans une chaîne RTF ne fonctionne pas avec toutes les polices utilisant `textPs=`

* Prise en charge de la gestion des macros non sensibles à la casse.
* Le cache du catalogue a été réduit de 60 secondes à 10 secondes.
* La fonction de redirection d’erreur ne redirige désormais que les requêtes faisant référence à des images, polices, de couleurs et images corrompues publiées dans un catalogue, mais introuvables sur le disque.
* `posN=`, `anchor=`, `anchorN=`, `origin=``originN=` , et renvoie désormais une erreur d’analyse si l’une des valeurs de modificateur est supérieure à 2147483648.

* Le codage des requêtes imbriquées n’est pas pris en charge.  au nouveau comportement et décodez toutes les valeurs de requête imbriquée trouvées dans les requêtes d’URL de votre site et dans vos catalogues de .
* DefaultImage applique désormais les attributs de miniature lors de l’utilisation `req=tmb`.
* Dans les versions précédentes utilisant `flip=`, l’image n’a jamais été repositionnée, quel que soit le point d’ancrage.

## Restrictions applicables aux bibliothèques tierces {#section-79768b96bf634e44ab672c5b893f343d}

La bibliothèque Digimarc refuse d’appliquer un filigrane Digimarc à une image si celle-ci est déjà détectée. Si suffisamment de modifications sont effectuées sur une image originale, la bibliothèque Digimarc peut tout de même reconnaître que le filigrane a été appliqué. Toutefois, il se peut qu&#39;il ne puisse pas lire ces informations. Ceci génère une nouvelle image dans laquelle les informations Digimarc d’origine appliquées à l’image d’origine ne peuvent pas être obtenues. La diffusion d’images peut désormais appliquer le filigrane Digimarc défini dans le catalogue des  de.

## Restrictions applicables à la diffusion d’images et au rendu d’images {#section-f836cb40ae2d4f32a9cf7ebda4d91bae}

* La diffusion d’images et le rendu d’images peuvent ne pas tirer pleinement parti de tous les processeurs lorsque plus de 4 processeurs sont disponibles. Simulez votre trafic sur ces machines pour voir à quel point il est avantageux avec plus de 4 processeurs.
* Les URL distantes renvoyant une redirection (états HTTP 301, 302 ou 303) sont rejetées.
* Lors de la configuration `errorRedirect.rootUrl` de l’adresse IP définie dans cette propriété, vous devez être inclus dans la valeur de la `<addressfilter>` balise de l’ensemble de règles sur ce serveur.

   *Exemple*:

   Le serveur A a défini `errorRedirect.rootUrl=10.10.10.10` .

   Le serveur B, dont l’adresse IP est 10.10.10.10, définit la valeur de la `<addressfilter>` balise dans le fichier du jeu de règles afin d’inclure son adresse IP (10.10.10.10).

* Le texte de point et le chemin de texte avec positionnement peuvent présenter un écrêtage.
* `text=` s’applique uniquement `\sa` et `\sb` à l’ensemble du bloc de texte et non à chaque paragraphe.

* Lors de l’utilisation d’un  défini dans l’URL et d’un autre  défini pour le modificateur `src=` ou `mask=` , vous devez préfixer une barre oblique vers le défini pour `src=` ou `mask=` pour que cette forme de requête fonctionne.

   *Exemple*:

   `/is/image/MyCompany?src=/YourCompany/MyImage` .

   Au lieu de : `/is/image/MyCompany?src=YourCompany/MyImage` .

* Les requêtes Tiff ou vignette non pyramidales génèrent un message d’erreur similaire à

   *&quot;Image C:\Program Files\Scene7\ImageRendering\resources\MyVignette.vnt n&#39;a pas de DSF valide, et la surface de 2.25MPixel dépasse le maximum de 2MPixel&quot;* .

   Il est recommandé d’utiliser des vignettes pyramidales et des vignettes. Si vous devez utiliser des vignettes ou des vignettes non pyramidales, suivez les instructions ci-dessous pour augmenter la taille limite.

   *Contourner*:

   Pour les vignettes non pyramidales de rendu d’image, augmentez la valeur de propriété d’IrMaxNonPyrVignetteSize dans le fichier de configuration [!DNL *[!DNL install_root]*/ImageServing/bin/ ImageServerRegistry.xml].

   Pour les fichiers TIFF non pyramidaux de diffusion d’images, augmentez la valeur de propriété `MaxNonDsfSize` dans le fichier de configuration [!DNL *[!DNL install_root]* /ImageServing/bin/ ImageServerRegistry.xml].

* Adobe Photoshop CS3 n’enregistre pas les fichiers PSD superposés par défaut sur une image composite.

   *Symptômes*:

   Le fichier PSD superposé Adobe Photoshop CS3 s’affiche en noir avec le texte indiquant que le fichier Photoshop superposé n’a pas été enregistré avec une image composite. pour l’image de réponse du serveur d’images ou dans IPS.

   *Solution* :

   Enregistrez le fichier Adobe Photoshop CS3 avec l’option Optimisation de la compatibilité activée.

* L’affectation d’ ICC à une image de réponse CMJN/JPEG entraîne l’inversion des couleurs dans certains navigateurs.*Contourner*:

   Modifiez le format d’image de réponse en utilisant `fmt=`

* La taille de la compression des données d’image de réponse HTTP, y compris l’en-tête de fichier, est limitée à 16 Mo.
* &quot; ..&quot; n’est autorisée dans aucun élément de chemin d’accès dans les requêtes HTTP.
* La désinstallation peut supprimer un fichier créé par l’utilisateur ou modifié d’ *[!DNL install_root]* un sous-dossier ou d’un sous-dossier quelconque. Copiez ces fichiers à un autre emplacement avant de procéder à la désinstallation.

## Restrictions applicables uniquement à la diffusion d’images {#section-b08ad535e4454265b8157dec244c4faf}

* Les couleurs de premier plan dans la commande RTF ( `\cf`) ne sont pas prises en charge pour le texte PhotoFont.
* La syntaxe en gras, en italique et en gras/italique sera rejetée comme erreur pour le texte PhotoFont.
* L’enchaînement de texte vertical n’est pas pris en charge pour le texte PhotoFont.
* Les images PNG 16 bpc ne sont pas prises en charge pour le texte PhotoFont.
* Les corrections de couleurs pour les images PNG avec de couleurs incorporé  utilisent des options codées en dur. Le mode de rendu est colorimétrique relatif et la compensation du point noir est activée pour le texte PhotoFont.
* La recherche basée sur des fichiers n’est pas prise en charge lorsque la traduction des paramètres régionaux est activée dans le [!DNL ini] fichier .
* La diffusion d’images n’écrit pas correctement les chemins Photoshop non fermés.
* La diffusion d’images ne prend actuellement pas en charge le traitement des fichiers TIFF exportés à l’aide d’Adobe Media Encoder 4.0.1 ou version antérieure. Adobe Media Encoder est fourni avec Adobe Premiere Pro CS4, After Effects CS4 et Creative Suite 4 Production Premium.
* L’utilisation `text=` de calques de redimensionnement automatique ne prend pas en charge les chaînes RTF qui utilisent plusieurs paramètres pour la justification de ligne.

   *Exemple*

   La chaîne RTF ne peut pas utiliser à la fois la justification de ligne gauche et de ligne droite pour un calque de texte auto-dimensionné.

* SVG possède sa propre propriété pour le chemin de recherche des polices référencées qui ne sont pas incorporées dans le fichier SVG.

   *Symptômes*

   Les images SVG rendues qui contiennent des définitions de police utilisent une police incorrecte.

   *Solution*

   Définissez la propriété `svgProvider.fontRoot=` dans [!DNL *[!DNL install_root]* /ImageServing/conf/PlatformServer.conf] .

* Le recadrage est actuellement utilisé `bgColor=` au lieu `color=` de remplir toute nouvelle zone étendue.

* La conversion des couleurs peut ne pas être correcte si elle `bgColor=` ne correspond pas à l’espace colorimétrique de base impliquant des  de couleurs.
* Les effets de calque externe ne sont pas rendus si le calque ne comporte pas de masque ou de données alpha.

## Restrictions applicables uniquement au rendu d’image {#section-4c6949e797174607a3d1ab4d3d4a725a}

* Les poubelles et les matériaux muraux ne sont pas amovibles.
* La taille des textures est limitée par rapport à la taille du de vignettes. Dans de rares cas, la limite par défaut de 425 % de la taille du  peut interférer avec une application utilisant des textures non répétables très grandes. S’il n’est pas possible de modifier l’application ou le contenu pour qu’il fonctionne dans les limites prédéfinies, le pourcentage peut être augmenté comme suit. A l’aide d’un éditeur de texte, ouvrez [!DNL *[!DNL install_root]*/ImageServing/conf/ImageServerRegistry.xml], recherchez `IrMaxTextureSizeFactor` et entrez une nouvelle valeur de pourcentage. La modification prend effet immédiatement sans redémarrer le serveur Image Server.

* Les moteurs JavaScript dans les données de réponse du cache Netscape et Opera même si l&#39;en-tête nocache est défini. Cela nuit au bon fonctionnement des demandes d&#39;état.

   *Solution*

   Ajoutez un horodatage ou un autre identifiant unique à la chaîne de requête, tel que `"&.ts=currentTime`.

## Restrictions applicables uniquement aux services publics {#section-906a6b2378154b3da122b2332983f7a5}

`ImageConvert`se bloque parfois avec une erreur de segmentation lorsqu’elle est arrêtée avec une erreur `control-c`.
