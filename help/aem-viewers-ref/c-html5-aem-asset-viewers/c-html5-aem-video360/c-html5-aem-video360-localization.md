---
description: Certains contenus affichés par le lecteur de contenu sont sujets aux  de. Cela inclut les info-bulles des éléments de l’interface utilisateur et un message d’erreur s’affiche lorsque la vidéo ne peut pas être lue.
seo-description: Certains contenus affichés par le lecteur de contenu sont sujets aux  de. Cela inclut les info-bulles des éléments de l’interface utilisateur et un message d’erreur s’affiche lorsque la vidéo ne peut pas être lue.
seo-title: ' des éléments de l’interface utilisateur'
solution: Experience Manager
title: ' des éléments de l’interface utilisateur'
topic: Dynamic media
uuid: d5e75af0-03d6-4357-a540-4094313ed026
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


#  des éléments de l’interface utilisateur{#localization-of-user-interface-elements}

Certains contenus affichés par le lecteur de contenu sont sujets aux  de. Cela inclut les info-bulles des éléments de l’interface utilisateur et un message d’erreur s’affiche lorsque la vidéo ne peut pas être lue.

Chaque contenu textuel dans le lecteur qui peut être localisé est représenté par un identifiant SDK de lecteur spécial appelé SYMBOL. Tout SYMBOL est associé par défaut à une valeur de texte pour le paramètre régional Anglais ( `"en"`) fourni avec le lecteur prêt à l’emploi. Des valeurs définies par l’utilisateur peuvent également être définies pour autant de paramètres régionaux que nécessaire.

Lorsque le du lecteur , il vérifie les paramètres régionaux actuels pour voir s’il existe une valeur définie par l’utilisateur pour chaque SYMBOL pris en charge pour les paramètres régionaux. Dans le cas contraire, elle utilise la valeur définie par l’utilisateur ; dans le cas contraire, il revient au texte par défaut prêt à l’emploi.

Les données de  définies par l’utilisateur peuvent être transmises au lecteur sous la forme d’un objet JSON de . Cet objet contient le  des paramètres régionaux pris en charge, les valeurs de texte SYMBOL pour chaque paramètre régional et les paramètres régionaux par défaut.

Voici un exemple de cet objet  :

```
{ 
"en":{ 
"Video360Player.ERROR":"Your Browser does not support HTML5 Video tag or the video cannot be played.", 
"PlayPauseButton.TOOLTIP_SELECTED":"Play" 
 }, 
 "fr":{ 
"Video360Player.ERROR":"Votre navigateur ne prend pas en charge la vidéo HTML5 tag ou la vidéo ne peuvent pas être lus.", 
"PlayPauseButton.TOOLTIP_SELECTED":"Jouer" 
}, 
defaultLocale:"en" 
}
```

Dans l’exemple ci-dessus, l’objet  de définit deux paramètres régionaux ( `"en"` et `"fr"`) et fournit un  pour deux éléments d’interface utilisateur dans chaque paramètre régional.

Le code de la page Web doit transmettre l’objet  du au constructeur de la visionneuse en tant que valeur du `localizedTexts` champ de l’objet de configuration. Une autre option consiste à transmettre l’objet  en appelant la `setLocalizedTexts(localizationInfo)` méthode.

Les SYMBOLES suivants sont pris en charge :

<table id="table_58C40353B7244335872350C98DF2CFB3"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>SYMBOLE </p> </th> 
   <th colname="col2" class="entry"> <p>Info-bulle pour... </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> .ÉTIQUETTE </span> </p> </td> 
   <td colname="col2"> <p>Libellé ARIA pour l’élément de lecteur de niveau supérieur. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> PlayPauseButton.TOOLTIP_SELECTED </span> </p> </td> 
   <td colname="col2"> <p>Etat du bouton Lecture en pause sélectionné. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> PlayPauseButton.TOOLTIP_UNSELECTED </span> </p> </td> 
   <td colname="col2"> <p>Désélectionnez l’état du bouton Lecture en pause. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> PlayPauseButton.TOOLTIP_REPLAY </span> </p> </td> 
   <td colname="col2"> <p>Lecture de l’état du bouton Pause. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> VideoScrubber.TOOLTIP </span> </p> </td> 
   <td colname="col2"> <p>Nettoyage vidéo. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> VideoTime.TOOLTIP </span> </p> </td> 
   <td colname="col2"> <p>Temps passé sur la barre de contrôle. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> MutableVolume.TOOLTIP_SELECTED </span> </p> </td> 
   <td colname="col2"> <p>Etat du volume mutable sélectionné. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> MutableVolume.TOOLTIP_UNSELECTED </span> </p> </td> 
   <td colname="col2"> <p>Volume muable désélectionné. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> MutableVolume.TOOLTIP_VOLUME </span> </p> </td> 
   <td colname="col2"> <p>Étiquette du bouton du curseur de volume exposée au moyen de l'attribut ARIA <span class="codeph"> aria-valuetext </span> . </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> FullScreenButton.TOOLTIP_SELECTED </span> </p> </td> 
   <td colname="col2"> <p>Bouton plein écran en état normal. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> FullScreenButton.TOOLTIP_UNSELECTED </span> </p> </td> 
   <td colname="col2"> <p>Bouton plein écran en mode plein écran. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> SocialShare.TOOLTIP </span> </p> </td> 
   <td colname="col2"> <p>Outil de partage sur les réseaux sociaux. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> EmbedShare.TOOLTIP </span> </p> </td> 
   <td colname="col2"> <p>Bouton d’intégration du partage. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> EmbedShare.HEADER </span> </p> </td> 
   <td colname="col2"> <p>En-tête de la boîte de dialogue d’intégration. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> EmbedShare.TOOLTIP_HEADER_CLOSE </span> </p> </td> 
   <td colname="col2"> <p>Bouton de fermeture supérieur droit de la boîte de dialogue d’intégration. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> EmbedShare.DESCRIPTION </span> </p> </td> 
   <td colname="col2"> <p>Texte du code incorporé. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> EmbedShare.EMBED_SIZE </span> </p> </td> 
   <td colname="col2"> <p>Zone de liste déroulante Taille d’incorporation. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> EmbedShare.CANCEL </span> </p> </td> 
   <td colname="col2"> <p>Le bouton "Annuler". </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> EmbedShare.TOOLTIP_CANCEL </span> </p> </td> 
   <td colname="col2"> <p>Le bouton "Annuler". </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> EmbedShare.ACTION </span> </p> </td> 
   <td colname="col2"> <p>Le bouton "Sélectionner tout". </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> ACTION EmbedShare.TOOLTIP </span> </p> </td> 
   <td colname="col2"> <p>Le bouton "Sélectionner tout". </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> EmbedShare.CUSTOM_SIZE </span> </p> </td> 
   <td colname="col2"> <p>Dernière entrée "taille personnalisée" dans la zone combinée Taille d’intégration. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> LinkShare.TOOLTIP </span> </p> </td> 
   <td colname="col2"> <p>Bouton de partage de lien. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> LinkShare.HEADER </span> </p> </td> 
   <td colname="col2"> <p>En-tête de la boîte de dialogue de lien. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> LinkShare.TOOLTIP_HEADER_CLOSE </span> </p> </td> 
   <td colname="col2"> <p>Bouton de fermeture supérieur droit de la boîte de dialogue de lien. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> LinkShare.DESCRIPTION </span> </p> </td> 
   <td colname="col2"> <p>Lien de partage. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> LinkShare.CANCEL </span> </p> </td> 
   <td colname="col2"> <p>Le bouton "Annuler". </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> LinkShare.TOOLTIP_CANCEL </span> </p> </td> 
   <td colname="col2"> <p>Le bouton "Annuler". </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> LinkShare.ACTION </span> </p> </td> 
   <td colname="col2"> <p>Le bouton "Sélectionner tout". </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> ACTION LinkShare.TOOLTIP </span> </p> </td> 
   <td colname="col2"> <p>Le bouton "Sélectionner tout". </p> </td> 
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
   <td colname="col1"> <p> <span class="codeph"> Video360Player.ERROR </span> </p> </td> 
   <td colname="col2"> <p>Message d’erreur qui s’affiche lorsqu’aucune lecture vidéo n’est possible. </p> </td> 
  </tr> 
 </tbody> 
</table>

