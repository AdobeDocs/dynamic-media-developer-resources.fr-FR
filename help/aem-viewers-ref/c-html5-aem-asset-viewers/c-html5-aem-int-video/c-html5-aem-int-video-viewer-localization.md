---
description: Le contenu affiché par la visionneuse de vidéos interactive est sujet à localisation. Cela inclut des info-bulles sur les éléments de l’interface utilisateur et un message d’erreur qui s’affiche lorsque la lecture de la vidéo est impossible.
solution: Experience Manager
title: Localisation des éléments de l’interface utilisateur
feature: Dynamic Media Classic, Visionneuses, SDK/API, Vidéos interactives
role: Développeur, Professionnel
exl-id: d293c385-d355-4d9e-9fe9-8ef35fef60bf
translation-type: tm+mt
source-git-commit: b4344397f82eb7d2d61020909f4acc7fddea210b
workflow-type: tm+mt
source-wordcount: '467'
ht-degree: 0%

---

# Localisation des éléments de l’interface utilisateur{#localization-of-user-interface-elements}

Le contenu affiché par la visionneuse de vidéos interactive est sujet à localisation. Cela inclut des info-bulles sur les éléments de l’interface utilisateur et un message d’erreur qui s’affiche lorsque la lecture de la vidéo est impossible.

Chaque contenu textuel de la visionneuse qui peut être localisé est représenté par l’identifiant spécial du kit de développement de visionneuse appelé SYMBOL. Tout SYMBOL est associé par défaut à une valeur de texte pour un paramètre régional anglais ( `"en"`) fournie avec le lecteur prêt à l’emploi et peut également avoir des valeurs définies par l’utilisateur pour autant de paramètres régionaux que nécessaire.

Lorsque le lecteur de contenu début, il vérifie les paramètres régionaux actuels pour déterminer s’il existe une valeur définie par l’utilisateur pour chaque SYMBOL pris en charge pour ces paramètres régionaux. Si tel est le cas, elle utilise la valeur définie par l’utilisateur ; sinon, il revient au texte par défaut prêt à l’emploi.

Les données de localisation définies par l’utilisateur peuvent être transmises au lecteur sous la forme d’un objet JSON de localisation. Cet objet contient la liste des paramètres régionaux pris en charge, les valeurs de texte SYMBOL pour chaque paramètre régional et les paramètres régionaux par défaut.

Voici un exemple d’objet de localisation :

```
{ 
"en":{ 
"VideoPlayer.ERROR":"Your Browser does not support HTML5 Video tag or the video cannot be played.", 
"PlayPauseButton.TOOLTIP_SELECTED":"Play" 
 }, 
 "fr":{ 
"VideoPlayer.ERROR":"Votre navigateur ne prend pas en charge la vidéo HTML5 tag ou la vidéo ne peuvent pas être lus.", 
"PlayPauseButton.TOOLTIP_SELECTED":"Jouer" 
}, 
defaultLocale:"en" 
}
```

Dans l’exemple ci-dessus, l’objet localisation définit deux paramètres régionaux ( `"en"` et `"fr"`) et fournit la localisation de deux éléments d’interface utilisateur dans chaque paramètre régional.

Le code de la page Web doit transmettre l’objet de localisation au constructeur de la visionneuse, sous la forme d’un champ `localizedTexts` de l’objet de configuration. Une autre option consiste à transmettre l’objet de localisation en appelant la méthode `setLocalizedTexts(localizationInfo)`.

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
   <td colname="col1"> <p> <span class="codeph"> Conteneur.LABEL  </span> </p> </td> 
   <td colname="col2"> <p>Libellé ARIA pour l’élément de lecteur de niveau supérieur. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> PlayPauseButton.TOOLTIP_SELECTED  </span> </p> </td> 
   <td colname="col2"> <p> Etat du bouton Lecture pause sélectionné. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> PlayPauseButton.TOOLTIP_UNSELECTED  </span> </p> </td> 
   <td colname="col2"> <p>Désélectionnez l’état du bouton Lecture pause. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> PlayPauseButton.TOOLTIP_REPLAY  </span> </p> </td> 
   <td colname="col2"> <p> Réexécuter l’état du bouton Pause de lecture. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> VideoScrubber.TOOLTIP  </span> </p> </td> 
   <td colname="col2"> <p>Défilement vidéo. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> VideoTime.TOOLTIP  </span> </p> </td> 
   <td colname="col2"> <p>Durée de la vidéo sur la barre de contrôle. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> MutableVolume.TOOLTIP_SELECTED  </span> </p> </td> 
   <td colname="col2"> <p> Volume mutable sélectionné. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> MutableVolume.TOOLTIP_UNSELECTED  </span> </p> </td> 
   <td colname="col2"> <p>Volume mutable désélectionné. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> MutableVolume.TOOLTIP_VOLUME  </span> </p> </td> 
   <td colname="col2"> <p> Étiquette du bouton de glissière de volume exposée au moyen de l'attribut ARIA <span class="codeph"> aria-valuetext </span>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> FullScreenButton.TOOLTIP_SELECTED  </span> </p> </td> 
   <td colname="col2"> <p>Bouton plein écran en état normal. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> FullScreenButton.TOOLTIP_UNSELECTED  </span> </p> </td> 
   <td colname="col2"> <p>Bouton plein écran en mode plein écran. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> ClosedCaptionButton.TOOLTIP_SELECTED  </span> </p> </td> 
   <td colname="col2"> <p> Etat du bouton de sous-titrage sélectionné. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> ClosedCaptionButton.TOOLTIP_UNSELECTED  </span> </p> </td> 
   <td colname="col2"> <p> Etat du bouton de sous-titrage non sélectionné. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> InteractiveSwatches.BANNER  </span> </p> </td> 
   <td colname="col2"> <p>Légende de la bannière. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> ScrollUpButton.TOOLTIP  </span> </p> </td> 
   <td colname="col2"> <p>Bouton de défilement vers le haut. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> ScrollDownButton.TOOLTIP  </span> </p> </td> 
   <td colname="col2"> <p>Bouton de défilement vers le bas. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> SocialShare.TOOLTIP  </span> </p> </td> 
   <td colname="col2"> <p>Outil de partage sur les réseaux sociaux. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> LinkShare.TOOLTIP  </span> </p> </td> 
   <td colname="col2"> <p>Bouton de partage de lien. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> LinkShare.HEADER  </span> </p> </td> 
   <td colname="col2"> <p>En-tête de la boîte de dialogue Lien. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> LinkShare.TOOLTIP_HEADER_CLOSE  </span> </p> </td> 
   <td colname="col2"> <p>Bouton de fermeture supérieur droit de la boîte de dialogue Lien. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> LinkShare.DESCRIPTION  </span> </p> </td> 
   <td colname="col2"> <p>Description du lien de partage. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> LinkShare.CANCEL  </span> </p> </td> 
   <td colname="col2"> <p>Légende du bouton Annuler. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> LinkShare.TOOLTIP_CANCEL  </span> </p> </td> 
   <td colname="col2"> <p>Bouton Annuler. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> LinkShare.ACTION  </span> </p> </td> 
   <td colname="col2"> <p>Légende du bouton Sélectionner tout. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> LinkShare.TOOLTIP_ACTION  </span> </p> </td> 
   <td colname="col2"> <p> Cliquez sur le bouton Tout. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> FacebookShare.TOOLTIP  </span> </p> </td> 
   <td colname="col2"> <p>bouton de partage Facebook. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> TwitterShare.TOOLTIP  </span> </p> </td> 
   <td colname="col2"> <p>Bouton de partage Twitter. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> CloseButton.TOOLTIP  </span> </p> </td> 
   <td colname="col2"> <p>Bouton Fermer du panneau d’appel à l’action. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> VideoPlayer.ERROR  </span> </p> </td> 
   <td colname="col2"> <p>Message d’erreur qui s’affiche lorsqu’aucune lecture vidéo n’est possible. </p> </td> 
  </tr> 
 </tbody> 
</table>
