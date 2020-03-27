---
description: Certains contenus affichés par la visionneuse Fenêtre déroulante sont soumis à des  de. Ce contenu comprend des info-bulles sur les éléments de l’interface utilisateur et des messages d’informations qui sont affichés par le de zoom déroulant  au chargement.
seo-description: Certains contenus affichés par la visionneuse Fenêtre déroulante sont soumis à des  de. Ce contenu comprend des info-bulles sur les éléments de l’interface utilisateur et des messages d’informations qui sont affichés par le de zoom déroulant  au chargement.
seo-title: ' des éléments de l’interface utilisateur'
solution: Experience Manager
title: ' des éléments de l’interface utilisateur'
topic: Dynamic media
uuid: d824c0c3-3606-4903-96f7-de26a61a8f65
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


#  des éléments de l’interface utilisateur{#localization-of-user-interface-elements}

Certains contenus affichés par la visionneuse Fenêtre déroulante sont soumis à des  de. Ce contenu comprend des info-bulles sur les éléments de l’interface utilisateur et des messages d’informations qui sont affichés par le de zoom déroulant  au chargement.

Chaque contenu textuel du lecteur pouvant être localisé est représenté par l’identifiant spécial du kit de développement de visionneuse appelé SYMBOL. Tout SYMBOL est associé par défaut à une valeur de texte pour un paramètre régional en anglais ( `"en"`) fourni avec le lecteur prêt à l’emploi et peut également avoir des valeurs définies par l’utilisateur pour autant de paramètres régionaux que nécessaire.

Lorsque le du lecteur , il vérifie les paramètres régionaux actuels pour voir s’il existe une valeur définie par l’utilisateur pour chaque SYMBOL pris en charge pour ces paramètres régionaux. Dans le cas contraire, elle utilise la valeur définie par l’utilisateur ; dans le cas contraire, il revient au texte par défaut prêt à l’emploi.

Les données de  définies par l’utilisateur peuvent être transmises au lecteur sous la forme d’un objet JSON de . Cet objet contient le  des paramètres régionaux pris en charge, les valeurs de texte SYMBOL pour chaque paramètre régional et les paramètres régionaux par défaut.

Voici un exemple de cet objet  :

```
{ 
"en":{ 
"FlyoutZoomView.TIP_BUBBLE_OVER":"Mouse over to zoom", 
"FlyoutZoomView.TIP_BUBBLE_TAP":"Tap and hold to zoom" 
 }, 
 "fr":{ 
"FlyoutZoomView.TIP_BUBBLE_OVER":"Passez la souris sur pour zoomer", 
"FlyoutZoomView.TIP_BUBBLE_TAP":"Appuyez et maintenez pour agrandir" 
}, 
defaultLocale:"en" 
}
```

Dans l’exemple ci-dessus, l’objet  de définit deux paramètres régionaux ( `"en"` et `"fr"`) et fournit un  pour deux éléments d’interface utilisateur dans chaque paramètre régional.

Le code de la page Web doit transmettre cet objet  au constructeur du lecteur de contenu, en tant que valeur du `localizedTexts` champ de l’objet de configuration. Une autre option consiste à transmettre l’objet  en appelant la `setLocalizedTexts(localizationInfo)` méthode.

Les SYMBOLES suivants sont pris en charge :

<table id="table_58C40353B7244335872350C98DF2CFB3"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>SYMBOLE </p> </th> 
   <th colname="col2" class="entry"> <p>Description </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> .ÉTIQUETTE </span> </p> </td> 
   <td colname="col2"> <p>Libellé ARIA pour l’élément de lecteur de niveau supérieur. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> FlyoutZoomView.ROLE_DESCRIPTION </span> </p> </td> 
   <td colname="col2"> <p>Description du rôle ARIA pour le composant  principal. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> FlyoutZoomView.USAGE_HINT </span> </p> </td> 
   <td colname="col2"> <p>Conseils d’utilisation ARIA pour les utilisateurs du clavier. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> FlyoutZoomView.TIP_BUBBLE_OVER </span> </p> </td> 
   <td colname="col2"> <p>Message d’information pour les systèmes de bureau. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> FlyoutZoomView.TIP_BUBBLE_TAP </span> </p> </td> 
   <td colname="col2"> <p>Message d’information pour les périphériques tactiles. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> ScrollLeftButton.TOOLTIP </span> </p> </td> 
   <td colname="col2"> <p>Info-bulle du bouton de défilement vers la gauche. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> ScrollRightButton.TOOLTIP </span> </p> </td> 
   <td colname="col2"> <p>Info-bulle du bouton de défilement vers la droite. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> ScrollUpButton.TOOLTIP </span> </p> </td> 
   <td colname="col2"> <p>Info-bulle du bouton de défilement vers le haut. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> ScrollDownButton.TOOLTIP </span> </p> </td> 
   <td colname="col2"> <p>Info-bulle du bouton de défilement vers le bas. </p> </td> 
  </tr> 
 </tbody> 
</table>

