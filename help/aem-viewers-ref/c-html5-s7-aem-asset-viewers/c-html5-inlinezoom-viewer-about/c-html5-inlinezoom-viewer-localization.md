---
description: Le contenu affiché par la visionneuse déroulante est sujet à localisation. Ce contenu comprend des info-bulles d’éléments d’interface utilisateur et des messages d’information qui s’affichent par la vue de zoom déroulant au chargement.
solution: Experience Manager
title: Localisation des éléments de l’interface utilisateur
feature: Dynamic Media Classic, Visionneuses, SDK/API, Zoom intégré
role: Développeur, Professionnel
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '348'
ht-degree: 0%

---


# Localisation des éléments de l’interface utilisateur{#localization-of-user-interface-elements}

Le contenu affiché par la visionneuse déroulante est sujet à localisation. Ce contenu comprend des info-bulles d’éléments d’interface utilisateur et des messages d’information qui s’affichent par la vue de zoom déroulant au chargement.

Chaque contenu textuel de la visionneuse qui peut être localisé est représenté par l’identifiant spécial du kit de développement de visionneuse appelé SYMBOL. Tout SYMBOL est associé par défaut à une valeur de texte pour un paramètre régional anglais ( `"en"`) fournie avec le lecteur prêt à l’emploi et peut également avoir des valeurs définies par l’utilisateur pour autant de paramètres régionaux que nécessaire.

Lorsque le lecteur de contenu début, il vérifie les paramètres régionaux actuels pour déterminer s’il existe une valeur définie par l’utilisateur pour chaque SYMBOL pris en charge pour ces paramètres régionaux. Si tel est le cas, elle utilise la valeur définie par l’utilisateur ; sinon, il revient au texte par défaut prêt à l’emploi.

Les données de localisation définies par l’utilisateur peuvent être transmises au lecteur sous la forme d’un objet JSON de localisation. Cet objet contient la liste des paramètres régionaux pris en charge, les valeurs de texte SYMBOL pour chaque paramètre régional et les paramètres régionaux par défaut.

Voici un exemple d’objet de localisation :

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

Dans l’exemple ci-dessus, l’objet localisation définit deux paramètres régionaux ( `"en"` et `"fr"`) et fournit la localisation de deux éléments d’interface utilisateur dans chaque paramètre régional.

Le code de la page Web doit transmettre cet objet de localisation au constructeur de la visionneuse, en tant que valeur du champ `localizedTexts` de l’objet de configuration. Une autre option consiste à transmettre l&#39;objet de localisation en appelant la méthode `setLocalizedTexts(localizationInfo)`.

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
   <td colname="col1"> <p> <span class="codeph"> Conteneur.LABEL  </span> </p> </td> 
   <td colname="col2"> <p>Libellé ARIA pour l’élément de lecteur de niveau supérieur. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> FlyoutZoomView.ROLE_DESCRIPTION  </span> </p> </td> 
   <td colname="col2"> <p>Description du rôle ARIA pour le composant principal de la vue. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> FlyoutZoomView.USAGE_HINT  </span> </p> </td> 
   <td colname="col2"> <p>Conseils d’utilisation ARIA pour les utilisateurs du clavier. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> FlyoutZoomView.TIP_BUBBLE_OVER  </span> </p> </td> 
   <td colname="col2"> <p>Message d’information pour les systèmes de bureau. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> FlyoutZoomView.TIP_BUBBLE_TAP  </span> </p> </td> 
   <td colname="col2"> <p>Message d’information pour les périphériques tactiles. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> ScrollLeftButton.TOOLTIP  </span> </p> </td> 
   <td colname="col2"> <p>Info-bulle du bouton de défilement vers la gauche. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> ScrollRightButton.TOOLTIP  </span> </p> </td> 
   <td colname="col2"> <p>Info-bulle du bouton de défilement vers la droite. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> ScrollUpButton.TOOLTIP  </span> </p> </td> 
   <td colname="col2"> <p>Info-bulle pour le bouton de défilement vers le haut. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> ScrollDownButton.TOOLTIP  </span> </p> </td> 
   <td colname="col2"> <p>Info-bulle du bouton de défilement vers le bas. </p> </td> 
  </tr> 
 </tbody> 
</table>

