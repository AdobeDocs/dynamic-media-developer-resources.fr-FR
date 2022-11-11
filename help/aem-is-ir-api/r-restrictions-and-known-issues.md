---
description: Certaines restrictions et problèmes connus doivent être pris en compte lors de l’utilisation du service d’images Dynamic Media.
solution: Experience Manager
title: Restrictions et problèmes connus
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: fd32456b-9d99-4e82-a61c-2fc4d7030630
source-git-commit: bf31e5226cbb763e2fb82391772b64e5d5c89fae
workflow-type: tm+mt
source-wordcount: '1222'
ht-degree: 0%

---

# Restrictions et problèmes connus{#restrictions-and-known-issues}

Certaines restrictions et problèmes connus doivent être pris en compte lors de l’utilisation du service d’images Dynamic Media.

## errata de la documentation {#section-b1579410b11e41e488c7de9ecc7e8d5c}

* Le nombre de lignes ne dépassera pas le maximum de la valeur `\copyfitmaxlines` et le nombre de lignes explicites dans la saisie de texte.
* Les accolades et parenthèses correspondantes sont requises dans les visionneuses d’images. Si les accolades et les parenthèses ne correspondent pas, elles doivent être codées au format URL.
* L’alerte de temps de réponse globale côté serveur inclut les réponses d’erreur.
* Le `id=` est actuellement requise lors de l’utilisation de la fonction `rect=` avec une demande d’image ou de masque.

## Différences connues textPs= par rapport à text= {#section-16ede4c13a7648feb0d2fc93341fd4aa}

* L’italique synthétique est rendu moins incliné que lors de l’utilisation de `text=`.
* Le soulignement est un peu plus bas et plus fin que lors de l’utilisation de `text=`.
* `\expnd` et `\expndtw` si elles sont utilisées avec des valeurs négatives élevées, les caractères sont placés les uns devant les autres lors de l’utilisation de `text=`.

* `\charscaley` se met à l’échelle différemment que lors de l’utilisation de `text=` mais n’affecte pas la hauteur de la ligne.

* Si la dernière ligne de texte ne tient pas, la ligne entière est supprimée au lieu d’apparaître comme coupure.
* `\slmult` et `\sl` se comportent différemment de MS Word et de `text=`, elles prennent simplement effet pour les paragraphes actuels et suivants.

* `\sb` s’applique au premier paragraphe pour MS Word et `text=`, Adobe InDesign et [!DNL Photoshop] ne faites pas cela.

* `\sa` s’applique au dernier paragraphe pour MS Word et `text=`, Adobe InDesign et [!DNL Photoshop] ne faites pas cela.

## Compatibilité descendante {#section-a76842f751944f4fb664af296d064122}

* Échappement du caractère de soulignement ( `\_`) dans une chaîne RTF ne fonctionne pas avec toutes les polices utilisant `textPs=`

* Prise en charge de la gestion des macros non sensibles à la casse.
* Le cache du catalogue a été réduit de 60 secondes à 10 secondes.
* La fonction de redirection d’erreur ne redirige désormais que les demandes référençant des images, polices, profils de couleurs et images corrompues publiées dans un catalogue, mais introuvables sur le disque.
* `posN=`, `anchor=`, `anchorN=`, `origin=`, et `originN=` renvoie maintenant une erreur d’analyse si l’une des valeurs de modificateur est supérieure à 2147483648.

* Le codage des requêtes imbriquées n’est pas pris en charge. Transition vers le nouveau comportement et décodage des valeurs de requête imbriquées trouvées dans les requêtes d’URL de votre site et dans les catalogues de votre entreprise.
* DefaultImage applique désormais les attributs de miniature lors de l’utilisation de `req=tmb`.
* Dans les versions précédentes utilisant `flip=`, l’image n’a jamais été repositionnée, quel que soit le point d’ancrage.

## Restrictions applicables aux bibliothèques tierces {#section-79768b96bf634e44ab672c5b893f343d}

La bibliothèque Digimarc refuse d’appliquer un filigrane Digimarc à une image si celle-ci est déjà détectée. Si suffisamment de modifications sont effectuées sur une image Principale, la bibliothèque Digimarc peut toujours être en mesure de reconnaître que le filigrane a été appliqué. Cependant, il se peut qu’il ne puisse pas lire ces informations. Cela donne une nouvelle image où les informations Digimarc d’origine qui ont été appliquées à l’image d’origine ne peuvent pas être obtenues. La diffusion d’images peut désormais appliquer le filigrane Digimarc défini dans le catalogue de l’entreprise.

## Restrictions applicables à la diffusion d’images et au rendu d’images {#section-f836cb40ae2d4f32a9cf7ebda4d91bae}

* La diffusion d’images et le rendu d’images peuvent ne pas profiter pleinement de tous les processeurs lorsque plus de 4 processeurs sont disponibles. Simulez votre trafic sur ces machines pour voir à quel point il est avantageux avec plus de 4 processeurs.
* Les URL distantes renvoyant une redirection (états HTTP 301, 302 ou 303) sont rejetées.
* Lors de la configuration `errorRedirect.rootUrl` l’adresse IP définie dans cette propriété doit être incluse dans l’ensemble de règles. `<addressfilter>` valeur de balise sur ce serveur.

   *Exemple*:

   Le serveur A a été défini `errorRedirect.rootUrl=10.10.10.10` .

   Le serveur B, dont l’adresse IP est 10.10.10.10, définit la variable `<addressfilter>` dans le fichier ruleSet afin d’inclure son adresse IP (10.10.10.10).

* Le texte et le chemin du texte du point avec le positionnement peuvent présenter un écrêtage.
* `text=` s&#39;applique uniquement `\sa` et `\sb` au bloc de texte entier et non par paragraphe.

* Lors de l’utilisation d’une société définie dans l’URL et d’une autre société définie pour la variable `src=` ou `mask=` modifier, vous devez préfixer une barre oblique vers l’entreprise définie pour `src=` ou `mask=` pour que cette forme de demande fonctionne.

   *Exemple*:

   `/is/image/MyCompany?src=/YourCompany/MyImage` .

   Au lieu de : `/is/image/MyCompany?src=YourCompany/MyImage` .

* Les demandes de vignette ou de tiff non pyramidales génèrent un message d’erreur similaire à

   *&quot;Image `C:\Program Files\Scene7\ImageRendering\resources\MyVignette.vnt` ne dispose pas d’un DSF valide, et la taille de 2,25 MPixel dépasse la taille maximale de 2 MPixel.&quot;* .

   La bonne pratique consiste à utiliser des tiff et des vignettes pyramisées. Si vous devez utiliser des vignettes ou des vignettes non pyramisées, suivez les instructions ci-dessous pour augmenter la taille limite.

   *Solution*:

   Pour les vignettes non pyramidales de rendu d’image, augmentez la valeur de propriété de IrMaxNonPyrVignetteSize dans la variable [!DNL install_root/ImageServing/bin/ImageServerRegistry.xml] fichier de configuration.

   Pour les TIFFs non pyramidaux de diffusion d’images, augmentez la valeur de propriété pour `MaxNonDsfSize` dans le [!DNL install_root/ImageServing/bin/ImageServerRegistry.xml] fichier de configuration.

* Adobe [!DNL Photoshop] CS3 n’enregistre pas par défaut les fichiers de PSD superposés d’une image composite.

   *Symptômes*:

   L&#39;Adobe [!DNL Photoshop] Le fichier de PSD en couches CS3 s’affiche en noir avec le texte indiquant : &quot;Cette couche [!DNL Photoshop] n’a pas été enregistré avec une image composite.&quot; pour l’image de réponse du serveur d’images ou dans IPS.

   *Solution* :

   Enregistrer l’Adobe [!DNL Photoshop] Fichier CS3 avec une compatibilité maximale activée.

* L’affectation d’un profil ICC à une image de réponse CMJN/JPEG entraîne l’inversion des couleurs dans certains navigateurs.*Solution*:

   Modifier le format d’image de réponse à l’aide de `fmt=`

* La taille de la compression des données d’image de réponse HTTP, y compris l’en-tête de fichier, est limitée à 16 Mo.
* &quot;..&quot; n’est autorisé dans aucun élément de chemin d’accès dans les requêtes HTTP.
* La désinstallation peut supprimer le fichier créé par l’utilisateur ou modifié de *[!DNL install_root]* ou tout sous-dossier. Copiez ces fichiers à un autre emplacement avant de les désinstaller.

## Restrictions applicables uniquement à la diffusion d’images {#section-b08ad535e4454265b8157dec244c4faf}

* Couleurs de premier plan dans le RTF ( `\cf`) ne sont pas prises en charge pour le texte PhotoFont.
* La synthèse du gras, de l’italique et du gras/italique est rejetée comme erreur pour le texte PhotoFont.
* Le flux de texte vertical n’est pas pris en charge pour le texte PhotoFont.
* Les images PNG 16 bpc ne sont pas prises en charge pour le texte PhotoFont.
* Les corrections de couleurs pour les images PNG avec profils de couleurs incorporés utilisent des options codées en dur. L’intention de rendu est colorimétrique relatif et la compensation du point noir est activée pour le texte PhotoFont.
* La recherche basée sur des fichiers n’est pas prise en charge lorsque la traduction des paramètres régionaux est activée dans l’entreprise. [!DNL ini] fichier .
* Le serveur d’images n’écrit pas non fermé [!DNL Photoshop] chemins d’accès correctement.
* Le service d’images ne prend actuellement pas en charge le traitement des fichiers de TIFF exportés à l’aide de Adobe Media Encoder 4.0.1 ou version antérieure. Adobe Media Encoder est fourni avec Premiere Pro CS4, After Effects CS4 et Creative Suite 4 Production Premium.
* Utilisation `text=` avec les calques auto-dimensionnés ne prend pas en charge les chaînes RTF qui utilisent plusieurs paramètres pour la justification de ligne.

   *Exemple*

   La chaîne RTF ne peut pas utiliser de justification de ligne gauche et de ligne droite pour un calque de texte auto-dimensionné.

* SVG possède sa propre propriété pour le chemin de recherche des polices référencées qui ne sont pas incorporées dans le fichier du SVG.

   *Symptômes*

   Les images de SVG générées qui contiennent des définitions de police utilisent une police incorrecte.

   *Solution*

   Définir la propriété `svgProvider.fontRoot=` in [!DNL install_root/ImageServing/conf/PlatformServer.conf] .

* Le recadrage utilise actuellement `bgColor=` au lieu de `color=` pour remplir toute zone nouvellement étendue.

* La conversion des couleurs peut ne pas être correcte lorsque `bgColor=` ne correspond pas à l’espace colorimétrique de base impliquant des profils de couleurs.
* Les effets de couche externe ne sont pas rendus si le calque ne comporte pas de masque ou de données alpha.

## Restrictions applicables uniquement au rendu d’image {#section-4c6949e797174607a3d1ab4d3d4a725a}

* Les décorations et les matériaux mural ne peuvent pas être supprimés.
* La taille des textures est limitée par rapport à la taille de la vignette. Dans de rares cas, la limite par défaut de 425 % de la taille d’affichage peut interférer avec une application en utilisant des textures non répétables très grandes. S’il n’est pas possible de modifier l’application ou le contenu pour qu’il fonctionne dans les limites prédéfinies, le pourcentage peut être augmenté comme suit. À l’aide d’un éditeur de texte, ouvrez [!DNL install_root/ImageServing/conf/ImageServerRegistry.xml], localisez `IrMaxTextureSizeFactor` et saisissez une nouvelle valeur de pourcentage. La modification prend effet immédiatement sans redémarrer le serveur d’images.

* Les moteurs JavaScript dans les données de réponse du cache Netscape et Opera même si l’en-tête nocache est défini. Cela interfère avec le bon fonctionnement des requêtes avec état.

   *Solution*

   Ajoutez un horodatage ou un autre identifiant unique à la chaîne de requête, tel que `"&.ts=currentTime`.

## Restrictions applicables uniquement aux utilitaires {#section-906a6b2378154b3da122b2332983f7a5}

`ImageConvert`se bloque parfois avec un problème de segmentation lorsqu’il est arrêté avec un `control-c`.
