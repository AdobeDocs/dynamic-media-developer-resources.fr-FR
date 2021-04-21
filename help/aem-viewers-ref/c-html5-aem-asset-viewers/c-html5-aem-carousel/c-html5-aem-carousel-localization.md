---
description: Le contenu affiché par la visionneuse de carrousel est sujet à localisation. Cela inclut les boutons de navigation dans les diapositives.
solution: Experience Manager
title: Localisation des éléments de l’interface utilisateur
feature: Dynamic Media Classic,Viewers,SDK/API,Carousel Banners
role: Developer,Business Practitioner
exl-id: 05f5abe0-1124-4114-864d-440699bcdc39
translation-type: tm+mt
source-git-commit: b4344397f82eb7d2d61020909f4acc7fddea210b
workflow-type: tm+mt
source-wordcount: '324'
ht-degree: 0%

---

# Localisation des éléments de l’interface utilisateur{#localization-of-user-interface-elements}

Le contenu affiché par la visionneuse de carrousel est sujet à localisation. Cela inclut les boutons de navigation dans les diapositives.

Chaque contenu textuel de la visionneuse qui peut être localisé est représenté par l’identifiant spécial du kit de développement de visionneuse appelé SYMBOL. Tout SYMBOL est associé par défaut à une valeur de texte pour un paramètre régional anglais ( `"en"`) fournie avec le lecteur prêt à l’emploi et peut également avoir des valeurs définies par l’utilisateur pour autant de paramètres régionaux que nécessaire.

Lorsque le lecteur de contenu début, il vérifie les paramètres régionaux actuels pour déterminer s’il existe une valeur définie par l’utilisateur pour chaque SYMBOL pris en charge pour ces paramètres régionaux. Si tel est le cas, elle utilise la valeur définie par l’utilisateur ; sinon, il revient au texte par défaut prêt à l’emploi.

Les données de localisation définies par l’utilisateur peuvent être transmises au lecteur sous la forme d’un objet JSON de localisation. Cet objet contient la liste des paramètres régionaux pris en charge, les valeurs de texte SYMBOL pour chaque paramètre régional et les paramètres régionaux par défaut.

Voici un exemple d’objet de localisation :

```
{ 
"en":{ 
"PanLeftButton.TOOLTIP":"Left", 
"PanRightButton.TOOLTIP":"Right" 
 }, 
 "fr":{ 
"PanLeftButton.TOOLTIP":"Gauchiste", 
"PanRightButton .TOOLTIP":"Droit" 
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
   <td colname="col1"> <p> <span class="codeph"> PlayPauseButton.TOOLTIP_SELECTED  </span> </p> </td> 
   <td colname="col2"> <p>Etat du bouton Lecture pause sélectionné. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> PlayPauseButton.TOOLTIP_UNSELECTED  </span> </p> </td> 
   <td colname="col2"> <p>Désélectionnez l’état du bouton Lecture pause. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> CAROUSELVIEWER_TOOLTIP_GOTO  </span> </p> </td> 
   <td colname="col2"> <p> Info-bulle et libellé ARIA pour les boutons de diapositives précédente et suivante. </p> <p>Accepte deux jetons de remplacement : <span class="codeph"> $CURRENT_FRAME$ </span> pour l'index de diapositives actuel et <span class="codeph"> $TOTAL_FRAMES$ </span> pour le nombre total de diapositives. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> Conteneur.LABEL  </span> </p> </td> 
   <td colname="col2"> <p> Libellé ARIA pour l’élément de lecteur de niveau supérieur. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> CarouselView.ROLE_DESCRIPTION  </span> </p> </td> 
   <td colname="col2"> <p> Description du rôle ARIA pour le composant principal de la vue. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> CarouselView.USAGE_HINT  </span> </p> </td> 
   <td colname="col2"> <p> Conseils d’utilisation ARIA pour les utilisateurs du clavier. </p> </td> 
  </tr> 
 </tbody> 
</table>
