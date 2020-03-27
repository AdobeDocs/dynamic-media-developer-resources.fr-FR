---
description: Certains contenus affichés par la visionneuse vidéo sont soumis à des  de, notamment des boutons de zoom et un bouton plein écran.
seo-description: Certains contenus affichés par la visionneuse vidéo sont soumis à des  de, notamment des boutons de zoom et un bouton plein écran.
seo-title: ' des éléments de l’interface utilisateur'
solution: Experience Manager
title: ' des éléments de l’interface utilisateur'
topic: Dynamic media
uuid: 00df92c5-3a10-4973-904d-de5a6b3b9258
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


#  des éléments de l’interface utilisateur{#localization-of-user-interface-elements}

Certains contenus affichés par la visionneuse vidéo sont soumis à des  de, notamment des boutons de zoom et un bouton plein écran.

Chaque contenu textuel dans le lecteur qui peut être localisé est représenté par un identifiant SDK de lecteur spécial appelé SYMBOL. Tout SYMBOL est associé par défaut à une valeur de texte pour le paramètre régional Anglais ( `"en"`) fourni avec le lecteur prêt à l’emploi. Des valeurs définies par l’utilisateur peuvent également être définies pour autant de paramètres régionaux que nécessaire.

Lorsque le du lecteur , il vérifie les paramètres régionaux actuels pour voir s’il existe une valeur définie par l’utilisateur pour chaque SYMBOL pris en charge pour les paramètres régionaux. Dans le cas contraire, elle utilise la valeur définie par l’utilisateur ; dans le cas contraire, il revient au texte par défaut prêt à l’emploi.

Les données de  définies par l’utilisateur peuvent être transmises au lecteur sous la forme d’un objet JSON de . Cet objet contient le  des paramètres régionaux pris en charge, les valeurs de texte SYMBOL pour chaque paramètre régional et les paramètres régionaux par défaut.

Voici un exemple de cet objet  :

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

Dans l’exemple ci-dessus, l’objet  de définit deux paramètres régionaux ( `"en"` et `"fr"`) et fournit un  pour deux éléments d’interface utilisateur dans chaque paramètre régional.

Le code de page Web doit transmettre cet objet  au constructeur du lecteur de contenu sous la forme d’une valeur de `localizedTexts` champ de l’objet de configuration. Une autre option consiste à transmettre l’objet  en appelant la `setLocalizedTexts(localizationInfo)` méthode.

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
   <td colname="col1"> <p> <span class="codeph"> ZoomView.ROLE_DESCRIPTION </span> </p> </td> 
   <td colname="col2"> <p>Description du rôle ARIA pour le composant  principal. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> ZoomView.USAGE_HINT </span> </p> </td> 
   <td colname="col2"> <p>Conseils d’utilisation ARIA pour les utilisateurs du clavier. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> CloseButton.TOOLTIP </span> </p> </td> 
   <td colname="col2"> <p>Bouton Fermer. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> ZoomInButton.TOOLTIP </span> </p> </td> 
   <td colname="col2"> <p>Zoom avant. </p> </td> 
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
   <td colname="col2"> <p>Bouton plein écran en état normal. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> FullScreenButton.TOOLTIP_UNSELECTED </span> </p> </td> 
   <td colname="col2"> <p>Bouton plein écran en mode plein écran. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> ScrollLeftButton.TOOLTIP </span> </p> </td> 
   <td colname="col2"> <p>Faites défiler vers la gauche. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> ScrollRightButton.TOOLTIP </span> </p> </td> 
   <td colname="col2"> <p>Faites défiler vers la droite. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> ScrollUpButton.TOOLTIP </span> </p> </td> 
   <td colname="col2"> <p>Bouton de défilement vers le haut. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> ScrollDownButton.TOOLTIP </span> </p> </td> 
   <td colname="col2"> <p>Bouton de défilement vers le bas. </p> </td> 
  </tr> 
 </tbody> 
</table>

