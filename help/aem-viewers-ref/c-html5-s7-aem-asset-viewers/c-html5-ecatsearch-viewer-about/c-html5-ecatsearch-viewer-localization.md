---
description: Certains contenus affichés par la visionneuse de catalogue électronique sont sujets à localisation, notamment les boutons de zoom, les boutons de modification de page, les boutons de miniature, les boutons plein écran, les boutons de fermeture et les boutons de barre de défilement.
solution: Experience Manager
title: Localisation des éléments de l’interface utilisateur
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog Search
role: Developer,User
exl-id: c44bfb38-a523-4399-8dbd-936830bb7cac
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '1057'
ht-degree: 0%

---

# Localisation des éléments de l’interface utilisateur{#localization-of-user-interface-elements}

Certains contenus affichés par la visionneuse de catalogue électronique sont sujets à localisation, notamment les boutons de zoom, les boutons de modification de page, les boutons de miniature, les boutons plein écran, les boutons de fermeture et les boutons de barre de défilement.

Chaque contenu textuel de la visionneuse qui peut être localisé est représenté par un identificateur spécial du SDK de la visionneuse appelé SYMBOL. Tout SYMBOLE possède une valeur de texte associée par défaut pour les paramètres régionaux anglais ( `"en"`) fournis avec la visionneuse prête à l’emploi, et peut également avoir des valeurs définies par l’utilisateur définies pour autant de paramètres régionaux que nécessaire.

Lorsque la visionneuse démarre, elle vérifie les paramètres régionaux actuels pour voir s’il existe une valeur définie par l’utilisateur pour chaque SYMBOL pris en charge dans la langue. Si c’est le cas, elle utilise la valeur définie par l’utilisateur ; Sinon, il revient au texte par défaut prêt à l’emploi.

Les données de localisation définies par l’utilisateur peuvent être transmises à la visionneuse en tant qu’objet JSON de localisation. Un tel objet contient la liste des paramètres régionaux pris en charge, les valeurs de texte SYMBOL pour chaque paramètre régional et les paramètres régionaux par défaut.

Exemple d’un tel objet de localisation :

```
{ 
"en":{ 
"CloseButton.TOOLTIP":"Close", 
"ZoomInButton.TOOLTIP":"Zoom In" 
 }, 
 "fr":{ 
"CloseButton.TOOLTIP":"Fermer", 
"ZoomInButton.TOOLTIP":"Agrandir" 
}, 
defaultLocale:"en" 
}
```

Dans l’exemple ci-dessus, l’objet de localisation définit deux paramètres régionaux ( `"en"` et `"fr"`) et fournit la localisation de deux éléments d’interface utilisateur dans chaque langue.

Le code de la page web doit transmettre cet objet de localisation au constructeur de la visionneuse en tant que valeur `localizedTexts` champ de l’objet de configuration. Une autre option consiste à transmettre l’objet de localisation en appelant `setLocalizedTexts(localizationInfo)` méthode .

Les symboles suivants sont pris en charge (en supposant que containerId soit l’ID du conteneur de la visionneuse) :

<table id="table_58C40353B7244335872350C98DF2CFB3"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>SYMBOLE </p> </th> 
   <th colname="col2" class="entry"> <p>Info-bulle pour... </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> Conteneur.ÉTIQUETTE </span> </p> </td> 
   <td colname="col2"> <p>Étiquette ARIA pour l’élément de visionneuse de niveau supérieur. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> PageView.ROLE_DESCRIPTION </span> </p> </td> 
   <td colname="col2"> <p>Description du rôle ARIA pour le composant Vue principale. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> PageView.USAGE_HINT </span> </p> </td> 
   <td colname="col2"> <p>Conseils d’utilisation ARIA pour les utilisateurs et utilisatrices de clavier. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> CloseButton.TOOLTIP </span> </p> </td> 
   <td colname="col2"> <p>Bouton Fermer. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> ZoomInButton.TOOLTIP </span> </p> </td> 
   <td colname="col2"> <p>Bouton Zoom avant. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> ZoomOutButton.TOOLTIP </span> </p> </td> 
   <td colname="col2"> <p>Bouton Zoom arrière. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> ZoomResetButton.TOOLTIP </span> </p> </td> 
   <td colname="col2"> <p>Bouton de réinitialisation du zoom. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> FullScreenButton.TOOLTIP_SELECTED </span> </p> </td> 
   <td colname="col2"> <p>Bouton plein écran à l’état normal. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> FullScreenButton.TOOLTIP_UNSELECTED </span> </p> </td> 
   <td colname="col2"> <p>Bouton plein écran à l’état plein écran. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> ScrollUpButton.TOOLTIP </span> </p> </td> 
   <td colname="col2"> <p>Bouton de défilement vers le haut. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> ScrollDownButton.TOOLTIP </span> </p> </td> 
   <td colname="col2"> <p>Bouton de défilement vers le bas. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> &lt;containerId&gt;_rightButton.PanRightButton.TOOLTIP </span> </p> </td> 
   <td colname="col2"> <p>Grand bouton de la page suivante. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> &lt;containerId&gt;_leftButton.PanLeftButton.TOOLTIP </span> </p> </td> 
   <td colname="col2"> <p>Grand bouton de la page précédente. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> &lt;containerId&gt;_lastPageButton.PanRightButton.TOOLTIP </span> </p> </td> 
   <td colname="col2"> <p>Bouton Dernière page. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">&lt;containerId&gt;_secondaryLastPageButton.PanRightButton.TOOLTIP </span>&lt;/containerId&gt; </p> </td> 
   <td colname="col2"> <p>Bouton Dernière page. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">&lt;containerId&gt;_firstPageButton.PanLeftButton.TOOLTIP </span>&lt;/containerId&gt; </p> </td> 
   <td colname="col2"> <p>Bouton Première page. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> &lt;containerId&gt;_secondaryFirstPageButton.PanLeftButton.TOOLTIP </span> </p> </td> 
   <td colname="col2"> <p>Bouton Première page. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">&lt;containerId&gt;_toolBarRightButton.PanRightButton.TOOLTIP </span>&lt;/containerId&gt; </p> </td> 
   <td colname="col2"> <p>Bouton Page suivante. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">&lt;containerId&gt;_toolBarLeftButton.PanLeftButton.TOOLTIP </span>&lt;/containerId&gt; </p> </td> 
   <td colname="col2"> <p>Bouton Page précédente. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> ThumbnailPageButton.TOOLTIP_SELECTED </span> </p> </td> 
   <td colname="col2"> <p>Bouton Miniatures en mode Miniatures. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> ThumbnailPageButton.TOOLTIP_UNSELECTED </span> </p> </td> 
   <td colname="col2"> <p>Bouton des miniatures en mode normal. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> CloseButton.TOOLTIP </span> </p> </td> 
   <td colname="col2"> <p>Bouton Fermer. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> InfoPanelPopup.TOOLTIP_CLOSE </span> </p> </td> 
   <td colname="col2"> <p>Bouton Fermer du panneau d’informations. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> SocialShare.TOOLTIP </span> </p> </td> 
   <td colname="col2"> <p>Social outil de partage. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> EmailShare.TOOLTIP </span> </p> </td> 
   <td colname="col2"> <p>Bouton de partage d’email. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> EmailShare.HEADER </span> </p> </td> 
   <td colname="col2"> <p>En-tête de boîte de dialogue de courrier électronique. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> EmailShare.TOOLTIP_HEADER_CLOSE </span> </p> </td> 
   <td colname="col2"> <p>Bouton de fermeture de la boîte de dialogue Email en haut à droite. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> EmailShare.INVALID_ADDRESS </span> </p> </td> 
   <td colname="col2"> <p>Message d’erreur affiché au cas où l’adresse électronique serait incorrecte. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> EmailShare.TO </span> </p> </td> 
   <td colname="col2"> <p>Libellé du champ de saisie « À ». </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> EmailShare.TOOLTIP_ADD </span> </p> </td> 
   <td colname="col2"> <p>Ajoutez un autre bouton d’adresse électronique. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> EmailShare.ADD </span> </p> </td> 
   <td colname="col2"> <p>Ajoutez un autre bouton d’adresse électronique. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> EmailShare.FROM </span> </p> </td> 
   <td colname="col2"> <p>Champ de saisie. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> EmailShare.MESSAGE </span> </p> </td> 
   <td colname="col2"> <p>Champ de saisie du message. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> EmailShare.TOOLTIP_REMOVE </span> </p> </td> 
   <td colname="col2"> <p>Bouton Supprimer l’adresse électronique. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> EmailShare.CANCEL </span> </p> </td> 
   <td colname="col2"> <p>Légende du bouton Annuler. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> EmailShare.TOOLTIP_CANCEL </span> </p> </td> 
   <td colname="col2"> <p>Bouton Annuler </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> EmbedShare.ACTION </span> </p> </td> 
   <td colname="col2"> <p>Légende du bouton Sélectionner tout. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> EmbedShare.TOOLTIP_ACTION </span> </p> </td> 
   <td colname="col2"> <p>Cliquez sur le bouton Tout. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> EmailShare.CLOSE </span> </p> </td> 
   <td colname="col2"> <p>Légende du bouton de fermeture affiché dans la partie inférieure de la boîte de dialogue après l’envoi du formulaire. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> EmailShare.TOOLTIP_CLOSE </span> </p> </td> 
   <td colname="col2"> <p>Bouton Fermer affiché au bas de la boîte de dialogue après l’envoi du formulaire. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> EmailShare.ACTION </span> </p> </td> 
   <td colname="col2"> <p>Légende pour le bouton d’envoi de formulaire. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> EmailShare.TOOLTIP_ACTION </span> </p> </td> 
   <td colname="col2"> <p>Bouton d’envoi de formulaire. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> EmailShare.SEND_SUCCESS </span> </p> </td> 
   <td colname="col2"> <p>Message de confirmation affiché lors de l’envoi de l’e-mail. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> EmailShare.SEND_FAILURE </span> </p> </td> 
   <td colname="col2"> <p>Message d’erreur affiché lorsque l’e-mail n’a pas été envoyé. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> EmbedShare.TOOLTIP </span> </p> </td> 
   <td colname="col2"> <p>Bouton de partage intégré. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> EmbedShare.HEADER </span> </p> </td> 
   <td colname="col2"> <p>En-tête de la boîte de dialogue Incorporer. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> EmbedShare.TOOLTIP_HEADER_CLOSE </span> </p> </td> 
   <td colname="col2"> <p>Bouton Fermer de la boîte de dialogue Incorporer en haut à droite. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> EmbedShare.DESCRIPTION </span> </p> </td> 
   <td colname="col2"> <p>Description du texte du code incorporé. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> EmbedShare.EMBED_SIZE </span> </p> </td> 
   <td colname="col2"> <p>Libellé de la zone de liste déroulante Taille intégrée. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> EmbedShare.CANCEL </span> </p> </td> 
   <td colname="col2"> <p>Légende du bouton Annuler. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> EmbedShare.TOOLTIP_CANCEL </span> </p> </td> 
   <td colname="col2"> <p>Bouton Annuler. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> EmbedShare.CUSTOM_SIZE </span> </p> </td> 
   <td colname="col2"> <p>Texte de la dernière entrée « Taille personnalisée » dans la zone de liste déroulante Taille intégrée. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> LinkShare.TOOLTIP </span> </p> </td> 
   <td colname="col2"> <p>Bouton de partage de lien. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> LinkShare.HEADER </span> </p> </td> 
   <td colname="col2"> <p>En-tête de la boîte de dialogue Lien. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> LinkShare.TOOLTIP_HEADER_CLOSE </span> </p> </td> 
   <td colname="col2"> <p>Bouton de fermeture de la boîte de dialogue Lien, en haut à droite. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> LinkShare.DESCRIPTION </span> </p> </td> 
   <td colname="col2"> <p>Description du lien de partage. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> LinkShare.CANCEL </span> </p> </td> 
   <td colname="col2"> <p>Légende du bouton Annuler. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> LinkShare.TOOLTIP_CANCEL </span> </p> </td> 
   <td colname="col2"> <p>Bouton Annuler. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> LinkShare.ACTION </span> </p> </td> 
   <td colname="col2"> <p>Légende pour le bouton Tout sélectionner . </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> LinkShare.TOOLTIP_ACTION </span> </p> </td> 
   <td colname="col2"> <p> Bouton Tout sélectionner. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> FacebookShare.TOOLTIP </span> </p> </td> 
   <td colname="col2"> <p>Bouton de partage Facebook. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> TwitterShare.TOOLTIP </span> </p> </td> 
   <td colname="col2"> <p>Bouton de partage Twitter. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> Print.TOOLTIP </span> </p> </td> 
   <td colname="col2"> <p>Bouton Imprimer. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> Print.HEADER </span> </p> </td> 
   <td colname="col2"> <p>En-tête de la boîte de dialogue d’impression. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> Print.TOOLTIP_HEADER_CLOSE </span> </p> </td> 
   <td colname="col2"> <p>Bouton Fermer en haut à droite de la boîte de dialogue Imprimer. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> Print.PRINT_RANGE </span> </p> </td> 
   <td colname="col2"> <p>Libellé de la section « Sélectionner des pages imprimées ». </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> Print.PRINT_RANGE_CURRENT </span> </p> </td> 
   <td colname="col2"> <p>Légende du bouton radio « Pages actives ». </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> Print.PRINT_RANGE_FROM </span> </p> </td> 
   <td colname="col2"> <p>Légende pour le bouton radio « Étendre la plage à partir de ». </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> Print.PRINT_RANGE_TO </span> </p> </td> 
   <td colname="col2"> <p>Légende pour le sélecteur numérique « à ». </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> Print.PRINT_RANGE_ALL </span> </p> </td> 
   <td colname="col2"> <p>Légende pour le bouton radio « Toutes les pages ». </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> Print.PAGE_HANDLING </span> </p> </td> 
   <td colname="col2"> <p>Libellé de la section « Gestion des pages ». </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> Print.PAGE_HANDLING_ONE </span> </p> </td> 
   <td colname="col2"> <p>Légende du bouton radio « 1 page par feuille ». </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> Print.PAGE_HANDLING_TWO </span> </p> </td> 
   <td colname="col2"> <p>Légende du bouton radio « 2 pages par feuille ». </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> Imprimer.ANNULER </span> </p> </td> 
   <td colname="col2"> <p>Légende du bouton Annuler. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> Print.TOOLTIP_CANCEL </span> </p> </td> 
   <td colname="col2"> <p> Bouton Annuler. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> Imprimer.ACTION </span> </p> </td> 
   <td colname="col2"> <p>Légende du bouton Envoyer pour impression </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> Print.TOOLTIP_ACTION </span> </p> </td> 
   <td colname="col2"> <p> Bouton Envoyer pour impression. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> FavoritesMenu.TOOLTIP </span> </p> </td> 
   <td colname="col2"> <p>Bouton de menu Favoris. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> AddFavoriteButton.TOOLTIP_SELECTED </span> </p> </td> 
   <td colname="col2"> <p>Bouton Ajouter un favori en mode d’édition des favoris. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> AddFavoriteButton.TOOLTIP_UNSELECTED </span> </p> </td> 
   <td colname="col2"> <p>Bouton « Ajouter un favori » en mode normal. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> RemoveFavoriteButton.TOOLTIP_SELECTED </span> </p> </td> 
   <td colname="col2"> <p>Bouton « Supprimer le favori » en mode d’édition des favoris. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> RemoveFavoriteButton.TOOLTIP_UNSELECTED </span> </p> </td> 
   <td colname="col2"> <p>Bouton « Supprimer favori » en mode normal. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> ViewAllFavoriteButton.TOOLTIP_SELECTED </span> </p> </td> 
   <td colname="col2"> <p>Bouton « Afficher tous les favoris » lorsque la vue Favoris est active. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> ViewAllFavoriteButton.TOOLTIP_UNSELECTED </span> </p> </td> 
   <td colname="col2"> <p>Bouton « Afficher tous les favoris » lorsque la vue Favoris est inactive. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> FavorisEffect.TOOLTIP </span> </p> </td> 
   <td colname="col2"> <p>Une seule icône favorite. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> MediaSet.LABEL_XX[_YY] </span> </p> </td> 
   <td colname="col2"> <p>Libellé de page généré par la visionneuse au moment du chargement. </p> <p>Le nom de ce symbole est un modèle, où <span class="codeph"> XX </span> est un index de planche à base zéro en orientation paysage, et YY <span class="codeph"> facultatif </span> est un index de page à base zéro à l’intérieur de la planche ciblée par <span class="codeph"> XX</span>. </p> <p>S’applique uniquement à la ressource chargée initialement ; ignoré si un élément est modifié à l’aide de l’appel d’API <span class="codeph"> setAsset(). </span> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> MediaSet.LABEL_DELIM </span> </p> </td> 
   <td colname="col2"> <p> Caractère utilisé comme délimiteur d’étiquettes de page dans le cas où des étiquettes sont définies pour des pages gauche et droite dans une planche. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> ScrollLeftRightButton.TOOLTIP_SELECTED </span> </p> </td> 
   <td colname="col2"> <p>Bouton de défilement vers la gauche de la barre de commande principale. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> ScrollLeftRightButton.TOOLTIP_UNSELECTED </span> </p> </td> 
   <td colname="col2"> <p>Bouton droit de défilement de la barre de commande principale. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> SearchPanel.PLACEHOLDER </span> </p> </td> 
   <td colname="col2"> <p>Invite localisée affichée dans la zone de saisie de recherche avant que l’utilisateur ne commence à saisir le texte de recherche. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> SearchPanel.INFO_PROMPT </span> </p> </td> 
   <td colname="col2"> <p>Message localisé affiché lorsque le panneau de recherche est ouvert pour la première fois, suggérant à l’utilisateur d’effectuer la recherche. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> SearchPanel.INFO_NO_RESULTS </span> </p> </td> 
   <td colname="col2"> <p>Message localisé affiché lorsque la recherche ne renvoyait aucun résultat. </p> <p>Ce symbole prend en charge le jeton de remplacement d’exécution suivant : <span class="codeph"> $SEARCH_TEXT$ </span>. Le composant le remplace par le texte de recherche saisi par l’utilisateur. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> SearchPanel.INFO_RESULTS </span> </p> </td> 
   <td colname="col2"> <p>Message localisé affiché lorsque la recherche est terminée avec succès et renvoie au moins un résultat. </p> <p>Ce symbole prend en charge les jetons de remplacement d’exécution suivants : </p> <p> 
     <ul id="ul_30B76EAB921848069BE843A5F91F697A"> 
      <li id="li_16AF3EFCC4BF4180B66DE5EA82CC77F4"> <span class="codeph"> $SEARCH_TEXT$ </span> - Texte de recherche saisi par l’utilisateur. </li> 
      <li id="li_A0FBF12344B04BF0B702A2B7473330A8"> <span class="codeph"> $HIT_COUNT$ </span> - Nombre total d’accès à la recherche trouvés. </li> 
      <li id="li_9EB7B41A989B455ABEC72E052284F117"> <span class="codeph"> $PAGE_COUNT$ </span> - Nombre de pages de catalogue contenant au moins un accès de recherche. </li> 
     </ul> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> SearchPanel.THUMBNAIL_LABEL </span> </p> </td> 
   <td colname="col2"> <p>Libellé localisé pour la miniature de résultats du panneau de recherche. </p> <p>Ce symbole prend en charge les jetons de remplacement d’exécution suivants : </p> <p> 
     <ul id="ul_7620C59FA56544CD9CE9E49B1871BCC1"> 
      <li id="li_FAF092734B4B4B55A309413690DA3FCC"> <span class="codeph"> $PAGE$ </span> - Numéro de page. </li> 
      <li id="li_3414176505BB4A768FB42341A315E96F"> <span class="codeph"> $PAGE_HIT_COUNT$ </span> - Nombre de résultats de recherche trouvés sur la page. </li> 
     </ul> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> SearchPanel.LABEL </span> </p> </td> 
   <td colname="col2"> <p>Définit une valeur de l’attribut ARIA <span class="codeph"> aria-label </span> pour l’ensemble du panneau de recherche. </p> </td> 
  </tr> 
 </tbody> 
</table>
