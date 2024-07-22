---
title: Localisation des éléments de l’interface utilisateur
description: Certains contenus affichés par la visionneuse de zoom de base peuvent être localisés, notamment des boutons de zoom et un bouton plein écran.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Zoom
role: Developer,User
exl-id: 8c399b64-e278-41bc-a9eb-692812979fea
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '293'
ht-degree: 0%

---

# Localisation des éléments de l’interface utilisateur{#localization-of-user-interface-elements}

Certains contenus affichés par la visionneuse de zoom de base peuvent être localisés, notamment des boutons de zoom et un bouton plein écran.

Chaque contenu textuel de la visionneuse qui peut être localisé est représenté par un identifiant spécial du SDK de la visionneuse appelé SYMBOL. Tout SYMBOL est associé par défaut à une valeur de texte pour le paramètre régional anglais ( `"en"`) fournie avec la visionneuse prête à l’emploi et peut également avoir des valeurs définies par l’utilisateur pour autant de paramètres régionaux que nécessaire.

Lorsque la visionneuse démarre, elle vérifie les paramètres régionaux actuels afin de déterminer s’il existe une valeur définie par l’utilisateur pour chaque SYMBOL pris en charge dans les paramètres régionaux. Si tel est le cas, il utilise la valeur définie par l’utilisateur ; dans le cas contraire, il revient au texte par défaut d’usine.

Les données de localisation définies par l’utilisateur peuvent être transmises à la visionneuse en tant qu’objet JSON de localisation. Un tel objet contient la liste des paramètres régionaux pris en charge, les valeurs de texte SYMBOL pour chaque paramètre régional et les paramètres régionaux par défaut.

Exemple d’objet de localisation :

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

Dans l’exemple ci-dessus, l’objet de localisation définit deux paramètres régionaux ( `"en"` et `"fr"`) et fournit la localisation de deux éléments de l’interface utilisateur dans chaque paramètre régional.

Le code de page web doit transmettre cet objet de localisation au constructeur de la visionneuse en tant que champ de valeur `localizedTexts` de l’objet de configuration. Une autre option consiste à transmettre l’objet de localisation en appelant la méthode `setLocalizedTexts(localizationInfo)`.

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
   <td colname="col1"> <p> <span class="codeph"> Container.LABEL </span> </p> </td> 
   <td colname="col2"> <p>Libellé ARIA pour l’élément de visionneuse de niveau supérieur. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> ZoomView.ROLE_DESCRIPTION </span> </p> </td> 
   <td colname="col2"> <p>Description du rôle ARIA pour le composant d’affichage principal. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> ZoomView.USAGE_HINT </span> </p> </td> 
   <td colname="col2"> <p>Conseils d’utilisation ARIA pour les utilisateurs de clavier. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> CloseButton.TOOLTIP </span> </p> </td> 
   <td colname="col2"> <p>Bouton Fermer . </p> </td> 
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
   <td colname="col2"> <p>Bouton Réinitialiser le zoom . </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> FullScreenButton.TOOLTIP_SELECTED </span> </p> </td> 
   <td colname="col2"> <p>bouton plein écran en état normal. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> FullScreenButton.TOOLTIP_UNSELECTED </span> </p> </td> 
   <td colname="col2"> <p>bouton plein écran en mode plein écran. </p> </td> 
  </tr> 
 </tbody> 
</table>
