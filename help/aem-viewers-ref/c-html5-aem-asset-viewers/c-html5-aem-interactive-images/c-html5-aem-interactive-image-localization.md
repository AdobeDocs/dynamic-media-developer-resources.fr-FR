---
title: Localisation des éléments de l’interface utilisateur
description: Certains contenus affichés par la visionneuse d’images interactives sont sujets à la localisation. Ce contenu comprend des info-bulles d’éléments d’interface utilisateur et un message d’information affiché par la vue déroulante de zoom au moment du chargement.
feature: Dynamic Media Classic,Viewers,SDK/API,Interactive Images
role: Developer,User
exl-id: 19749c74-5c31-4dcf-ab07-0e7f10176a86
autotag-review: '2026-05-13T22:17:15.458Z'
TQID: 'https://experienceleague.adobe.com/XYvxUsA4fiBhf5gT35bxHZTo9Tn6QvT5ld89zNnHiOo'
product_v2:
  - id: beaff0dd-a904-4c6b-8290-b527cd877d75
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: e76d4c499daf8c8a7a0be31e56d84f917c643095
workflow-type: tm+mt
source-wordcount: 308
ht-degree: 0%

---

# Localisation des éléments de l’interface utilisateur{#localization-of-user-interface-elements}

Certains contenus affichés par la visionneuse d’images interactives sont sujets à la localisation. Ce contenu comprend des info-bulles d’éléments d’interface utilisateur et un message d’information affiché par la vue déroulante de zoom au moment du chargement.

Chaque contenu textuel de la visionneuse qui peut être localisé est représenté par l’identifiant SDK de visionneuse spécial appelé SYMBOL. Tout SYMBOLE possède une valeur de texte associée par défaut pour un paramètre régional d’anglais ( `"en"`) fourni avec la visionneuse prête à l’emploi, et peut avoir des valeurs définies par l’utilisateur définies pour autant de paramètres régionaux que nécessaire.

Lorsque la visionneuse démarre, elle vérifie le paramètre régional en cours pour voir s’il existe une valeur définie par l’utilisateur pour chaque SYMBOLE pris en charge pour ce paramètre régional. Si tel est le cas, il utilise la valeur définie par l’utilisateur ou l’utilisatrice ; dans le cas contraire, il revient au texte par défaut prêt à l’emploi.

Les données de localisation définies par l’utilisateur peuvent être transmises à la visionneuse en tant qu’objet JSON de localisation. Cet objet contient la liste des paramètres régionaux pris en charge, les valeurs de texte SYMBOL pour chaque paramètre régional et le paramètre régional par défaut.

Voici un exemple d’un tel objet de localisation :

```
{ 
"en":{ 
"Container.LABEL":"Interactive Image Viewer" 
 }, 
 "fr":{ 
"Container.LABEL":"Visionneuse d'images interactive" 
}, 
defaultLocale:"en" 
}
```

Dans l’exemple ci-dessus, l’objet de localisation définit deux paramètres régionaux ( `"en"` et `"fr"`) et fournit la localisation de deux éléments de l’interface utilisateur dans chaque paramètre régional.

Le code de la page web doit transmettre l’objet de localisation au constructeur de la visionneuse, en tant que valeur `localizedTexts` champ de l’objet de configuration. Une autre option consiste à transmettre l’objet de localisation en appelant `setLocalizedTexts(localizationInfo)` méthode .

Les symboles suivants sont pris en charge :

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
   <td colname="col2"> <p>Description du rôle ARIA pour le composant de vue principal. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> ZoomView.USAGE_HINT </span> </p> </td> 
   <td colname="col2"> <p>Conseils d’utilisation ARIA pour les utilisateurs et utilisatrices de clavier. </p> </td> 
  </tr> 
 </tbody> 
</table>
