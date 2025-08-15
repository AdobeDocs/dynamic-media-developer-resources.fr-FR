---
description: Certaines restrictions et problèmes connus doivent être pris en compte lors de l’utilisation Dynamic Media serveur d’images.
solution: Experience Manager
title: Restrictions et problèmes connus
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: fd32456b-9d99-4e82-a61c-2fc4d7030630
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '1233'
ht-degree: 0%

---

# Restrictions et problèmes connus{#restrictions-and-known-issues}

Certaines restrictions et problèmes connus doivent être pris en compte lors de l’utilisation Dynamic Media serveur d’images.

## Errata de documentation {#section-b1579410b11e41e488c7de9ecc7e8d5c}

* Le nombre de lignes ne dépasse pas le maximum du `\copyfitmaxlines` paramètre et le nombre de lignes explicites dans la saisie de texte.
* Les accolades et les parenthèses correspondantes sont requises dans les visionneuses d’images. En l’absence de correspondance entre accolades et parenthèses, il convient de les coder dans l’URL.
* L’alerte de temps de réponse globale côté serveur inclut les réponses d’erreur.
* La `id=` commande est actuellement requise lors de l’utilisation de la commande avec une demande d’image `rect=` ou de masque.

## Différences connues textPs= vs text= {#section-16ede4c13a7648feb0d2fc93341fd4aa}

* Les italiques synthétiques sont rendus moins inclinés que lors de l’utilisation `text=`de .
* Le soulignement est un peu plus bas et plus fin que lors de l’utilisation `text=`de .
* `\expnd` et `\expndtw` utilisées avec des valeurs négatives élevées provoquent la place des caractères les uns devant les autres lors de l’utilisation `text=`de .

* `\charscaley` S’adapte différemment à l’utilisation `text=` de la ligne, sans toutefois l’affecter.

* Si la dernière ligne de texte ne convient pas, la ligne entière est supprimée au lieu d’apparaître comme coupée.
* `\slmult` et `\sl` se comportent différemment de MS Word et `text=`, ils prennent simplement effet pour les paragraphes actuels et suivants.

* `\sb` s’applique au premier paragraphe pour MS Word et `text=`, Adobe InDesign et [!DNL Photoshop] ne le faites pas.

* `\sa` s’applique au dernier paragraphe pour MS Word et `text=`, Adobe InDesign et [!DNL Photoshop] ne le faites pas.

## Rétrocompatibilité {#section-a76842f751944f4fb664af296d064122}

* L’échappement du caractère de soulignement ( `\_`) dans une chaîne RTF ne fonctionne pas avec toutes les polices utilisant `textPs=`

* Prise en charge de la gestion des macros non sensibles à la casse.
* Le cache du catalogue a été réduit de 60 secondes à 10 secondes.
* La fonctionnalité de redirection d’erreur redirige désormais uniquement les requêtes référençant des images, des polices, des profils de couleurs et des images corrompus qui sont publiés dans un catalogue, mais introuvables sur le disque.
* `posN=`, , `anchor=`, `anchorN=`et `origin=` `originN=` maintenant renvoyer une erreur d’analyse si l’une des valeurs du modificateur est supérieure à 2147483648.

* Le codage des demandes imbriquées n’est pas pris en charge. Passez au nouveau comportement et décodez toutes les valeurs de requête imbriquées trouvées dans les requêtes d’URL sur votre site et dans les catalogues de votre entreprise.
* DefaultImage applique maintenant des attributs de miniature lors de l’utilisation du `req=tmb`fichier .
* Dans les versions précédentes utilisant `flip=`, l’image n’était jamais repositionnée, quel que soit le point d’ancrage.

## Restrictions applicables aux bibliothèques tierces {#section-79768b96bf634e44ab672c5b893f343d}

La bibliothèque Digimarc refuse d’appliquer un filigrane Digimarc à une image si elle est déjà détectée. Si suffisamment d’édition est effectuée sur une image principale, la bibliothèque Digimarc peut toujours être en mesure de reconnaître que le filigrane a été appliqué. Cependant, il peut ne pas être en mesure de lire cette information. Il en résulte une nouvelle image où les informations Digimarc d’origine qui ont été appliquées à l’image d’origine ne peuvent pas être obtenues. Image Serving peut maintenant appliquer le filigrane Digimarc défini dans le catalogue de l’entreprise.

## Restrictions applicables à la fois au serveur d’images et au rendu d’images {#section-f836cb40ae2d4f32a9cf7ebda4d91bae}

* Image Serving et Image Rendering peuvent ne pas tirer pleinement parti de toutes les CPU lorsque plus de 4 CPU sont disponibles. Simulez votre trafic sur ces machines pour voir à quel point il est avantageux avec plus de 4 CPU.
* Les URL distantes renvoyant une redirection (statuts HTTP 301, 302 ou 303) sont rejetées.
* Lors de la configuration `errorRedirect.rootUrl` , l’adresse IP définie dans cette propriété doit être incluse dans la valeur de balise ruleSet `<addressfilter>` sur ce serveur.

  *Par exemple* :

  Le serveur A a défini `errorRedirect.rootUrl=10.10.10.10` .

  Le serveur B qui possède l’adresse IP de 10.10.10.10, définit la valeur de balise `<addressfilter>` dans le fichier d’ensemble de règles pour inclure son adresse IP (10.10.10.10).

* Le texte pointé et le chemin du texte avec positionnement peuvent présenter une écrêtage.
* `text=` s’applique `\sa` uniquement et `\sb` à l’ensemble du bloc de texte et non par paragraphe.

* Lorsque vous utilisez une société définie dans l’URL et une autre société définie pour le `src=` modificateur ou `mask=` , vous devez préfixer une barre oblique à la société définie pour `src=` ou `mask=` pour que cette forme de demande fonctionne.

  *Par exemple* :

  `/is/image/MyCompany?src=/YourCompany/MyImage` .

  Au lieu de : `/is/image/MyCompany?src=YourCompany/MyImage` .

* Les demandes de vignettes ou Tiff non pyramidées génèrent un message d’erreur similaire à celui de

  *« L’image `C:\Program Files\Scene7\ImageRendering\resources\MyVignette.vnt` n’a pas de DSF valide, et la zone de 2,25 MPixel dépasse le maximum de 2MPixel ».*

  Il est recommandé d’utiliser des Tiff pyramidés et des vignettes, Si vous devez utiliser des tiff ou des vignettes non pyramidés, suivez les instructions ci-dessous pour augmenter la limite de taille.

  *Solutions de contournement* :

  Pour les vignettes non pyramidées Image Rendering, augmentez la valeur de propriété pour IrMaxNonPyrVignetteSize dans le fichier de [!DNL install_root/ImageServing/bin/ImageServerRegistry.xml] configuration.

  Pour les fichiers TIFF non pyramidés diffusant des images, augmentez la valeur de propriété pour `MaxNonDsfSize` dans le fichier de [!DNL install_root/ImageServing/bin/ImageServerRegistry.xml] configuration.

* [!DNL Photoshop] Adobe CS3 n’enregistre pas les fichiers PSD calques par défaut en image composite.

  *Symptômes* :

  Le fichier PSD calqué CS3 Adobe [!DNL Photoshop] s’affiche en noir avec le texte indiquant « Ce fichier en [!DNL Photoshop] couches n’a pas été enregistré avec une image composite. » pour l’image de réponse Image Serving ou dans IPS.

  *Solution* :

  Enregistrez le fichier CS3 Adobe [!DNL Photoshop] avec l’optimisation de la compatibilité activée.

* L’affectation d’un profil ICC à une image de réponse CMJN/JPEG provoque l’inversion des couleurs dans certains navigateurs.*Solutions de contournement* :

  Modifier le format d’image de réponse à l’aide de `fmt=`

* La taille des données d’image de réponse HTTP (après compression, y compris l’en-tête du fichier) est limitée à 16 Mo.
* &quot; ..&quot; n’est pas autorisée dans les éléments de chemin des requêtes HTTP.
* La désinstallation peut supprimer le fichier créé ou modifié par l’utilisateur de ou de *[!DNL install_root]* tout sous-dossier. Copiez ces fichiers à un autre emplacement avant de les désinstaller.

## Restrictions applicables uniquement à la diffusion d’images {#section-b08ad535e4454265b8157dec244c4faf}

* Les couleurs de premier plan dans la commande RTF ( `\cf`) ne sont pas prises en charge pour le texte PhotoFont.
* La synthèse de gras, italique et gras/italique est rejetée en tant qu’erreur pour le texte PhotoFont.
* Le flux de texte vertical n’est pas pris en charge pour le texte PhotoFont.
* Les images PNG 16bpc ne sont pas prises en charge pour le texte PhotoFont.
* Les corrections des couleurs pour les images PNG avec profils de couleurs incorporés utilisent des options codées en dur. L’intention de rendu est colorimétrique relative et la compensation du point noir est activée pour le texte PhotoFont.
* La recherche basée sur un fichier n’est pas prise en charge lorsque la traduction des paramètres régionaux est activée dans le fichier de société [!DNL ini] .
* La diffusion d’images n’écrit pas correctement les chemins non fermés [!DNL Photoshop] .
* La diffusion d’images ne prend actuellement pas en charge le traitement des fichiers TIFF exportés à l’aide de Adobe Media Encoder 4.0.1 ou d’une version antérieure. Adobe Media Encoder est inclus dans les Premiere Pro CS4, After Effects CS4 et Creative Suite 4 Production Premium.
* L’utilisation `text=` avec des calques auto-dimensionnants ne prend pas en charge les chaînes RTF qui utilisent plusieurs paramètres pour justifier les lignes.

  *Exemple*

  La chaîne RTF ne peut pas utiliser à la fois la justification de ligne gauche et droite pour un calque de texte auto-dimensionnant.

* SVG a sa propre propriété pour le chemin de recherche de police des polices référencées qui ne sont pas incorporées dans le fichier SVG.

  *Symptômes*

  Les images SVG rendues contenant des définitions de police utilisent une police incorrecte.

  *Solution de contournement*

  Définissez la propriété `svgProvider.fontRoot=` dans [!DNL install_root/ImageServing/conf/PlatformServer.conf] .

* Recadrage est en cours d’utilisation `bgColor=` au lieu de `color=` remplir toute zone nouvellement étendue.

* La conversion des couleurs peut ne pas être correcte lorsqu’elle `bgColor=` ne correspond pas à l’espace colorimétrique de base impliquant des profils de couleurs.
* Les effets de calque externe ne sont pas rendus si le calque ne comporte pas de masque ou de données alpha.

## Restrictions applicables uniquement au rendu d’images {#section-4c6949e797174607a3d1ab4d3d4a725a}

* Les décalcomanies et les matériaux muraux ne sont pas amovibles.
* La taille des textures est limitée par rapport à la taille de la vue vignette. Dans de rares cas, la limite par défaut de 425 % de la taille d’affichage peut interférer avec une application utilisant de très grandes textures non reproductibles. S’il n’est pas possible de modifier l’application ou le contenu pour qu’il fonctionne dans les limites prédéfinies, le pourcentage peut être augmenté comme suit. A l’aide d’un éditeur de texte, ouvrez [!DNL install_root/ImageServing/conf/ImageServerRegistry.xml], recherchez `IrMaxTextureSizeFactor` et entrez une nouvelle valeur de pourcentage. La modification prend effet immédiatement, sans redémarrer le serveur d’images.

* Les moteurs JavaScript dans Netscape et Opera mettent en cache les données de réponse même si l’en-tête nocache est défini. Cela nuit au bon fonctionnement des demandes avec état.

  *Solution de contournement*

  Ajoutez un horodatage ou un autre identifiant unique à la chaîne de requête, tel que `"&.ts=currentTime`.

## Restrictions applicables uniquement aux services publics {#section-906a6b2378154b3da122b2332983f7a5}

`ImageConvert`Se bloque parfois avec une erreur de segmentation lorsqu’il est arrêté avec un `control-c`fichier .
