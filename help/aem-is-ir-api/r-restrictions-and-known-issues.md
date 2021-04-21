---
description: Certaines restrictions et problèmes connus doivent être pris en compte lors de l’utilisation de la diffusion d’images Dynamic Media.
solution: Experience Manager
title: Restrictions et problèmes connus
feature: Dynamic Media Classic,SDK/API
role: Developer,Business Practitioner
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '1238'
ht-degree: 0%

---


# Restrictions et problèmes connus{#restrictions-and-known-issues}

Certaines restrictions et problèmes connus doivent être pris en compte lors de l’utilisation de la diffusion d’images Dynamic Media.

## Erreur de documentation {#section-b1579410b11e41e488c7de9ecc7e8d5c}

* Le nombre de lignes ne doit pas dépasser le nombre maximal de lignes défini dans le paramètre `\copyfitmaxlines` et le nombre de lignes explicites dans la saisie de texte.
* Les accolades et parenthèses correspondantes sont requises dans les visionneuses d’images. Si les accolades et les parenthèses ne correspondent pas, elles doivent être codées en URL.
* L’alerte de temps de réponse globale côté serveur inclut les réponses d’erreur.
* La commande `id=` est actuellement requise lors de l&#39;utilisation de la commande `rect=` avec une demande d&#39;image ou de masque.

## Différences connues textPs= vs text= {#section-16ede4c13a7648feb0d2fc93341fd4aa}

* L&#39;italique synthétique est rendu moins incliné que lors de l&#39;utilisation de `text=`.
* Le soulignement est un peu plus bas et plus fin que lors de l&#39;utilisation de `text=`.
* `\expnd` et  `\expndtw` utilisés avec des valeurs négatives élevées provoquent la mise de caractères devant les autres lors de l’utilisation  `text=`de.

* `\charscaley` se met à l’échelle différemment que lors de l’utilisation  `text=` mais n’affecte pas la hauteur de ligne.

* Si la dernière ligne de texte ne tient pas, la ligne entière est laissée tomber au lieu d’être coupée.
* `\slmult` et  `\sl` se comportent différemment de MS Word et  `text=`ils prennent simplement effet pour les paragraphes actuels et suivants.

* `\sb` s&#39;applique au premier paragraphe pour MS Word et  `text=`Adobe InDesign et Photoshop ne le font pas.

* `\sa` s&#39;applique au dernier paragraphe pour MS Word et  `text=`Adobe InDesign et Photoshop ne le font pas.

## Compatibilité descendante {#section-a76842f751944f4fb664af296d064122}

* L’échappement du caractère de soulignement ( `\_`) dans une chaîne RTF ne fonctionne pas avec toutes les polices utilisant `textPs=`

* Prise en charge de la gestion des macros non sensibles à la casse.
* Le cache du catalogue a été réduit de 60 secondes à 10 secondes.
* La fonction de redirection d’erreur ne redirige désormais que les requêtes faisant référence à des images, polices, profils de couleur et images corrompus qui sont publiés dans un catalogue, mais qui ne sont pas détectées sur le disque.
* `posN=`,  `anchor=`,  `anchorN=`,  `origin=`et,  `originN=` maintenant, renvoient une erreur d’analyse si l’une des valeurs de modificateur est supérieure à 2147483648.

* Le codage des requêtes imbriquées n’est pas pris en charge. Transition au nouveau comportement et annulation du codage de toutes les valeurs de requête imbriquées figurant dans les requêtes d’URL de votre site et dans vos catalogues de sociétés.
* DefaultImage applique désormais les attributs de miniature lors de l’utilisation de `req=tmb`.
* Dans les versions précédentes utilisant `flip=`, l’image n’a jamais été repositionnée, quel que soit le point d’ancrage.

## Restrictions applicables aux bibliothèques tierces {#section-79768b96bf634e44ab672c5b893f343d}

La bibliothèque Digimarc refuse d’appliquer un filigrane Digimarc à une image si celle-ci est déjà détectée. Si une modification suffisante est apportée à une image Principale, la bibliothèque Digimarc peut tout de même reconnaître que le filigrane a été appliqué. Cependant, il se peut qu&#39;il ne puisse pas lire ces informations. Ceci génère une nouvelle image dans laquelle les informations Digimarc d’origine appliquées à l’image d’origine ne peuvent pas être obtenues. La diffusion d’images peut désormais appliquer le filigrane Digimarc défini dans le catalogue de sociétés.

## Restrictions applicables à la diffusion d’images et au rendu d’images {#section-f836cb40ae2d4f32a9cf7ebda4d91bae}

* La diffusion d’images et le rendu d’images peuvent ne pas tirer pleinement parti de toutes les UC lorsque plus de 4 UC sont disponibles. Simulez votre trafic sur ces machines pour voir à quel point il est avantageux avec plus de 4 CPU.
* Les URL distantes renvoyant une redirection (états HTTP 301, 302 ou 303) sont rejetées.
* Lors de la configuration de `errorRedirect.rootUrl` l&#39;adresse IP définie dans cette propriété doit être incluse dans la valeur de balise de l&#39;ensemble de règles `<addressfilter>` sur ce serveur.

   *Exemple*:

   Le serveur A a défini `errorRedirect.rootUrl=10.10.10.10`.

   Le serveur B, dont l’adresse IP est 10.10.10.10, définit la valeur de balise `<addressfilter>` dans le fichier d’ensemble de règles afin d’inclure son adresse IP (10.10.10.10).

* Le texte et le chemin de texte avec positionnement peuvent présenter un écrêtage.
* `text=` s&#39;applique uniquement  `\sa` et  `\sb` à l&#39;ensemble du bloc de texte et non à chaque paragraphe.

* Lors de l’utilisation d’une société définie dans l’URL et d’une autre société définie pour le modificateur `src=` ou `mask=`, vous devez préfixer une barre oblique à la société définie pour `src=` ou `mask=` pour cette forme de demande de travail.

   *Exemple*:

   `/is/image/MyCompany?src=/YourCompany/MyImage` .

   Au lieu de : `/is/image/MyCompany?src=YourCompany/MyImage` .

* Les requêtes de vignette ou de tiff non pyramidales génèrent un message d’erreur similaire à

   *&quot;L&#39;image  `C:\Program Files\Scene7\ImageRendering\resources\MyVignette.vnt` n&#39;a pas de DSF valide et la surface de 2,25 MPixel dépasse la taille maximale de 2MPixel&quot;* .

   Il est recommandé d’utiliser des vignettes et des vignettes pyramidales. Si vous devez utiliser des vignettes ou des vignettes non pyramidales, suivez les instructions ci-dessous pour augmenter la taille limite.

   *Contourner* :

   Pour les vignettes non pyramidales de rendu d’image, augmentez la valeur de propriété de IrMaxNonPyrVignetteSize dans le fichier de configuration [!DNL install_root/ImageServing/bin/ImageServerRegistry.xml].

   Pour les fichiers TIFF non pyramidaux de diffusion d’images, augmentez la valeur de propriété de `MaxNonDsfSize` dans le fichier de configuration [!DNL install_root/ImageServing/bin/ImageServerRegistry.xml].

* Adobe Photoshop CS3 n’enregistre pas les fichiers PSD superposés par défaut sur une image composite.

   *Symptômes* :

   Le fichier PSD superposé Adobe Photoshop CS3 s’affiche en noir avec le texte indiquant que &quot;ce fichier Photoshop superposé n’a pas été enregistré avec une image composite&quot;. pour l’image de réponse de diffusion d’images ou dans IPS.

   *Solution* :

   Enregistrez le fichier Adobe Photoshop CS3 avec la compatibilité maximale activée.

* L’affectation d’un Profil ICC à une image de réponse CMJN/JPEG entraîne l’inversion des couleurs dans certains navigateurs.*Contourner* :

   Modifiez le format d&#39;image de réponse en utilisant `fmt=`

* La taille des données d’image de réponse HTTP après compression, y compris l’en-tête de fichier, est limitée à 16 Mo.
* &quot;..&quot; n’est autorisée dans aucun élément de chemin dans les requêtes HTTP.
* La désinstallation peut supprimer un fichier créé par l&#39;utilisateur ou modifié de *[!DNL install_root]* ou de tout sous-dossier. Copiez ces fichiers à un autre emplacement avant de les désinstaller.

## Restrictions applicables uniquement à la diffusion d’images {#section-b08ad535e4454265b8157dec244c4faf}

* Les couleurs de premier plan dans la commande RTF ( `\cf`) ne sont pas prises en charge pour le texte PhotoFont.
* La synthèse des caractères gras, italique et gras/italique sera rejetée comme erreur pour le texte PhotoFont.
* Le flux de texte vertical n’est pas pris en charge pour le texte PhotoFont.
* Les images PNG 16 bpc ne sont pas prises en charge pour le texte PhotoFont.
* Les corrections de couleur pour les images PNG avec profils de couleur incorporés utilisent des options codées en dur. Le mode de rendu est colorimétrique relatif et la compensation de point noir est activée pour le texte PhotoFont.
* La recherche basée sur des fichiers n’est pas prise en charge lorsque la traduction des paramètres régionaux est activée dans le fichier de société [!DNL ini].
* La diffusion d’images n’écrit pas correctement les chemins Photoshop non fermés.
* La diffusion d’images ne prend actuellement pas en charge le traitement des fichiers TIFF exportés à l’aide de Adobe Media Encoder 4.0.1 ou version antérieure. Adobe Media Encoder est fourni avec Premiere Pro CS4, After Effects CS4 et Creative Suite 4 Production Premium.
* L’utilisation de `text=` avec des calques de redimensionnement automatique ne prend pas en charge les chaînes RTF qui utilisent plusieurs paramètres de justification de ligne.

   *Exemple*

   La chaîne RTF ne peut pas utiliser à la fois la justification de la ligne de gauche et de la ligne de droite pour un calque de texte auto-dimensionné.

* SVG possède sa propre propriété pour le chemin de recherche de polices des polices référencées qui ne sont pas incorporées dans le fichier SVG.

   *Symptômes*

   Les images SVG générées qui contiennent des définitions de police utilisent une police incorrecte.

   *Solution*

   Définissez la propriété `svgProvider.fontRoot=` dans [!DNL install_root/ImageServing/conf/PlatformServer.conf].

* Le recadrage utilise actuellement `bgColor=` au lieu de `color=` pour remplir toute zone nouvellement étendue.

* La conversion des couleurs peut ne pas être correcte si `bgColor=` ne correspond pas à l’espace colorimétrique de base qui implique des profils de couleur.
* Les effets de calque externe ne sont pas rendus si le calque ne comporte pas de masque ou de données alpha.

## Restrictions applicables uniquement au rendu d’image {#section-4c6949e797174607a3d1ab4d3d4a725a}

* Les décorations et les matériaux muraux ne sont pas amovibles.
* La taille des textures est limitée par rapport à la taille de la vue de vignettes. Dans de rares cas, la limite par défaut de 425 % de la taille de la vue peut interférer avec une application utilisant des textures non répétables très grandes. S&#39;il n&#39;est pas possible de modifier l&#39;application ou le contenu pour qu&#39;il fonctionne dans les limites prédéfinies, le pourcentage peut être augmenté comme suit. A l’aide d’un éditeur de texte, ouvrez [!DNL install_root/ImageServing/conf/ImageServerRegistry.xml], recherchez `IrMaxTextureSizeFactor` et entrez une nouvelle valeur de pourcentage. La modification prend effet immédiatement sans redémarrer le serveur Image Server.

* Les moteurs JavaScript dans les données de réponse du cache Netscape et Opera même si l’en-tête nocache est défini. Cela interfère avec le bon fonctionnement des demandes d&#39;état.

   *Solution*

   Ajoutez un horodatage ou un autre identifiant unique à la chaîne de requête, tel que `"&.ts=currentTime`.

## Restrictions applicables uniquement aux utilitaires {#section-906a6b2378154b3da122b2332983f7a5}

`ImageConvert`parfois se bloque avec une faille de segmentation lorsqu’elle est arrêtée avec un  `control-c`problème.
