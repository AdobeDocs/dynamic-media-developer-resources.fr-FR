---
description: Certaines restrictions et problèmes connus doivent être pris en compte lors de l’utilisation de la diffusion d’images Dynamic Media.
solution: Experience Manager
title: Restrictions et problèmes connus
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: fd32456b-9d99-4e82-a61c-2fc4d7030630
TQID: 'https://experienceleague.adobe.com/TCVO43J9ABVIbKSBwPE6jSfMR8I-2sc-7Nj-gGDEyPM'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 1250
ht-degree: 0%

---

# Restrictions et problèmes connus{#restrictions-and-known-issues}

Certaines restrictions et problèmes connus doivent être pris en compte lors de l’utilisation de la diffusion d’images Dynamic Media.

## Erreurs de documentation {#section-b1579410b11e41e488c7de9ecc7e8d5c}

* Le nombre de lignes ne dépasse pas le nombre maximal du paramètre `\copyfitmaxlines` et le nombre de lignes explicites dans la saisie de texte.
* Les accolades et les parenthèses correspondantes sont requises dans les visionneuses d’images. Si les accolades et les parenthèses ne correspondent pas, elles doivent être encodées en URL.
* L’alerte du temps de réponse global côté serveur comprend des réponses d’erreur.
* La commande `id=` est actuellement requise lors de l’utilisation de la commande `rect=` avec une demande d’image ou de masque.

## Différences connues textPs= et text= {#section-16ede4c13a7648feb0d2fc93341fd4aa}

* Les italiques synthétiques sont moins inclinés que lors de l’utilisation de `text=`.
* Le soulignement est un peu plus faible et plus fin que lors de l’utilisation de `text=`.
* `\expnd` et `\expndtw` utilisés avec des valeurs négatives élevées entraînent le placement des caractères l’un devant l’autre lors de l’utilisation de `text=`.

* `\charscaley` se met à l’échelle différemment que lors de l’utilisation de `text=`, mais n’affecte pas la hauteur de ligne.

* Si la dernière ligne de texte n’est pas adaptée, la ligne entière est déposée au lieu d’apparaître comme coupure.
* `\slmult` et `\sl` se comportent différemment de MS Word et `text=` ; ils prennent simplement effet pour les paragraphes actifs et suivants.

* `\sb` s’applique au premier paragraphe pour MS Word et `text=`, Adobe InDesign et [!DNL Photoshop] ne le font pas.

* `\sa` s’applique au dernier paragraphe pour MS Word et `text=`, Adobe InDesign et [!DNL Photoshop] ne le font pas.

## Compatibilité descendante {#section-a76842f751944f4fb664af296d064122}

* L’échappement du caractère de soulignement ( `\_`) dans une chaîne RTF ne fonctionne pas avec toutes les polices utilisant `textPs=`

* Prise en charge de la gestion des macros non sensible à la casse.
* Le cache du catalogue a été réduit de 60 secondes à 10 secondes.
* La fonction de redirection d’erreur redirige désormais uniquement les requêtes faisant référence à des images, des polices, des profils de couleurs et des images corrompus qui sont publiés dans un catalogue, mais qui ne sont pas trouvés sur le disque.
* `posN=`, `anchor=`, `anchorN=`, `origin=` et `originN=` renvoient désormais une erreur d&#39;analyse si l&#39;une des valeurs des modificateurs est supérieure à 2147483648.

* Le codage des requêtes imbriquées n’est pas pris en charge. Passez au nouveau comportement et décodez toutes les valeurs de requête imbriquées trouvées dans les requêtes d’URL sur votre site et dans les catalogues de votre entreprise.
* DefaultImage applique désormais les attributs de miniature lors de l’utilisation de `req=tmb`.
* Dans les versions précédentes utilisant `flip=`, l’image n’était jamais repositionnée, quel que soit le point d’ancrage.

## Restrictions applicables aux bibliothèques tierces {#section-79768b96bf634e44ab672c5b893f343d}

La bibliothèque Digimarc refuse d&#39;appliquer un filigrane Digimarc à une image si celle-ci est déjà détectée. Si une modification suffisante est apportée à une image principale, la bibliothèque Digimarc peut toujours reconnaître que le filigrane a été appliqué. Cependant, il ne sera peut-être pas en mesure de lire cette information. Il en résulte une nouvelle image dans laquelle les informations Digimarc d’origine qui ont été appliquées à l’image d’origine ne peuvent pas être obtenues. La diffusion d’images peut désormais appliquer le filigrane Digimarc défini dans le catalogue d’entreprises.

## Restrictions applicables à la diffusion et au rendu d’images {#section-f836cb40ae2d4f32a9cf7ebda4d91bae}

* La diffusion d’images et le rendu d’images peuvent ne pas tirer pleinement parti de tous les processeurs lorsque plus de 4 processeurs sont disponibles. Simulez votre trafic sur ces machines pour voir à quel point il est avantageux de disposer de plus de 4 processeurs.
* Les URL distantes renvoyant une redirection (états HTTP 301, 302 ou 303) sont rejetées.
* Lors de la configuration de `errorRedirect.rootUrl`, l’adresse IP définie dans cette propriété doit être incluse dans la valeur de balise `<addressfilter>` de l’ensemble de règles sur ce serveur.

  *Exemple* :

  Le serveur A a défini `errorRedirect.rootUrl=10.10.10.10` .

  Le serveur B qui possède l’adresse IP 10.10.10.10 définit la valeur de la balise `<addressfilter>` dans le fichier d’ensemble de règles pour inclure son adresse IP (10.10.10.10).

* Le texte du point et le chemin du texte avec positionnement peuvent présenter un écrêtage.
* `text=` s’applique uniquement aux `\sa` et `\sb` à l’ensemble du bloc de texte et non à chaque paragraphe.

* Lors de l’utilisation d’une société définie dans l’URL et d’une autre définie pour le modificateur `src=` ou `mask=`, vous devez ajouter une barre oblique à la société définie pour `src=` ou `mask=` pour que ce formulaire de demande fonctionne.

  *Exemple* :

  `/is/image/MyCompany?src=/YourCompany/MyImage` .

  Au lieu de : `/is/image/MyCompany?src=YourCompany/MyImage` .

* Les requêtes Tiff ou vignette non pyramidales génèrent un message d’erreur similaire à .

  *« Le `C:\Program Files\Scene7\ImageRendering\resources\MyVignette.vnt` d’image n’a pas de DSF valide et la zone de 2,25 MPixel dépasse le maximum de 2 MPixel »* .

  La bonne pratique consiste à utiliser des vignettes et des Tiff pyramidaux. Si vous devez utiliser des vignettes ou des tiff non pyramidaux, suivez les instructions ci-dessous pour augmenter la limite de taille.

  *Solution de contournement* :

  Pour les vignettes de rendu d’image non pyramidales, augmentez la valeur de la propriété pour IrMaxNonPyrVignetteSize dans le fichier de configuration de [!DNL install_root/ImageServing/bin/ImageServerRegistry.xml].

  Pour les fichiers TIFF non pyramidaux de diffusion d’images, augmentez la valeur de la propriété pour `MaxNonDsfSize` dans le fichier de configuration [!DNL install_root/ImageServing/bin/ImageServerRegistry.xml].

* Adobe [!DNL Photoshop] CS3 n’enregistre pas les fichiers PSD superposés par défaut en tant qu’image composite.

  *Symptômes* :

  Le fichier PSD superposé Adobe [!DNL Photoshop] CS3 s’affiche en noir avec le texte suivant : « Ce fichier [!DNL Photoshop] superposé n’a pas été enregistré avec une image composite. » pour l’image de réponse du service d’images ou dans IPS.

  *Solution* :

  Enregistrez le fichier Adobe [!DNL Photoshop] CS3 en activant l’option d’optimisation de la compatibilité.

* L’affectation d’un profil ICC à une image de réponse CMJN/JPEG entraîne l’inversion des couleurs dans certains navigateurs.*Solution de contournement* :

  Modifier le format de l’image de réponse à l’aide de `fmt=`

* La taille des données d’image de réponse HTTP après compression, y compris l’en-tête du fichier, est limitée à 16 Mo.
* &quot; ..&quot; n’est autorisé dans aucun élément de chemin d’accès dans les requêtes HTTP.
* Uninstall peut supprimer le fichier créé ou modifié par l&#39;utilisateur de *[!DNL install_root]* ou de tout sous-dossier. Copiez ces fichiers vers un autre emplacement avant de désinstaller.

## Restrictions applicables uniquement à la diffusion d’images {#section-b08ad535e4454265b8157dec244c4faf}

* Les couleurs de premier plan de la commande RTF ( `\cf`) ne sont pas prises en charge pour le texte PhotoFont.
* La synthèse des caractères gras, italique et gras/italique est rejetée comme une erreur pour le texte PhotoFont.
* Le flux de texte vertical n’est pas pris en charge pour le texte PhotoFont.
* Les images PNG 16 bpc ne sont pas prises en charge pour le texte PhotoFont.
* Les corrections de couleurs pour les images PNG avec des profils de couleurs incorporés utilisent des options codées en dur. L’intention de rendu est une colorimétrie relative et la compensation du point de noir est activée pour le texte PhotoFont.
* La recherche basée sur des fichiers n’est pas prise en charge lorsque la traduction des paramètres régionaux est activée dans le fichier de [!DNL ini] d’entreprise.
* Le service d’images n’écrit pas correctement les chemins d’accès [!DNL Photoshop] non fermés.
* Le traitement des images ne prend actuellement pas en charge le traitement des fichiers TIFF exportés à l’aide de Adobe Media Encoder 4.0.1 ou d’une version antérieure. Adobe Media Encoder est inclus dans Premiere Pro CS4, After Effects CS4 et Creative Suite 4 Production Premium.
* L’utilisation de `text=` avec des calques de redimensionnement automatique ne prend pas en charge les chaînes RTF qui utilisent plusieurs paramètres pour la justification des lignes.

  *Exemple*

  La chaîne RTF ne peut pas utiliser à la fois la justification des lignes gauche et droite pour un calque de texte à auto-dimensionnement.

* SVG possède sa propre propriété pour le chemin de recherche des polices référencées qui ne sont pas incorporées dans le fichier SVG.

  *Symptômes*

  Les images SVG rendues contenant des définitions de police utilisent une police incorrecte.

  *Solution*

  Définissez la propriété `svgProvider.fontRoot=` dans [!DNL install_root/ImageServing/conf/PlatformServer.conf] .

* Le recadrage utilise actuellement `bgColor=` au lieu de `color=` pour remplir toute zone nouvellement étendue.

* La conversion des couleurs peut ne pas être correcte lorsque `bgColor=` ne correspond pas à l’espace colorimétrique de base impliquant des profils de couleurs.
* Les effets de calque externe ne sont pas rendus si le calque ne comporte pas de masque ou de données alpha.

## Restrictions applicables uniquement au rendu des images {#section-4c6949e797174607a3d1ab4d3d4a725a}

* Les autocollants et les matériaux de mur ne sont pas amovibles.
* La taille des textures est limitée par rapport à la taille de la vue de la vignette. Dans de rares cas, la limite par défaut de 425 % de la taille de la vue peut interférer avec une application utilisant des textures non répétables très volumineuses. S’il n’est pas possible de modifier l’application ou le contenu pour qu’ils fonctionnent dans les limites prédéfinies, le pourcentage peut être augmenté comme suit. À l’aide d’un éditeur de texte, ouvrez [!DNL install_root/ImageServing/conf/ImageServerRegistry.xml], localisez `IrMaxTextureSizeFactor` et saisissez une nouvelle valeur de pourcentage. La modification prend effet immédiatement sans redémarrer le serveur d’images.

* Les moteurs JavaScript dans Netscape et Opera mettent en cache les données de réponse même si l&#39;en-tête nocache est défini. Cela interfère avec le bon fonctionnement des requêtes avec état.

  *Solution*

  Ajoutez un horodatage ou un autre identifiant unique à la chaîne de requête, tel que `"&.ts=currentTime`.

## Restrictions applicables uniquement aux services publics {#section-906a6b2378154b3da122b2332983f7a5}

`ImageConvert`se bloque parfois avec une erreur de segmentation lorsqu’il est arrêté avec une `control-c`.
