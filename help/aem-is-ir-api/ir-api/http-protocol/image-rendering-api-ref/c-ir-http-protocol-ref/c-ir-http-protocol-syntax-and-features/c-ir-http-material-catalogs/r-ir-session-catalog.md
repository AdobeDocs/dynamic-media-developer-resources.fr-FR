---
title: Catalogue de sessions
description: Le catalogue de sessions est le catalogue de matériaux qui fournit des attributs de session pour la demande et une valeur catId par défaut pour toutes les commandes src=, vignette= et icc=.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 36e0571e-7451-423f-a1df-540680381902
source-git-commit: 790ce3aa4e9aadc019d17e663fc93d7c69772b23
workflow-type: tm+mt
source-wordcount: '233'
ht-degree: 0%

---

# Catalogue de sessions{#session-catalog}

Le catalogue de sessions est le catalogue de matériaux qui fournit des attributs de session pour la requête et une valeur catId par défaut pour toutes les `src=`commandes , `vignette=`et `icc=` .

Le catalogue de sessions est spécifié en tant que premier élément de chemin du chemin d’accès de la requête HTTP (immédiatement après le nom du serveur). Si le premier élément de chemin ne correspond pas à attribute ::RootId d’un catalogue, le catalogue par défaut est utilisé comme catalogue de session.

Le catalogue de sessions fournit les valeurs par défaut de session suivantes :

<table id="table_DB5E0DD8E9B440A4964A1326433597C8"> 
 <thead> 
  <tr> 
   <th class="entry"> <p>Attribut </p> </th> 
   <th class="entry"> <p>Remarques </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td> <p> <span class="codeph"> attribute ::RootPath</span> </p> </td> 
   <td> <p> Chemin racine pour les fichiers de données de matériaux </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> attribute ::VignettePath</span> </p> </td> 
   <td> <p> Chemin d’accès racine pour les fichiers de vignettes </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> attribut ::IccProfileRgb</span> </p> </td> 
   <td> <p> Espace colorimétrique de travail par défaut si une vignette n’intègre pas de profil ICC </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> attribut ::RootUrl</span> </p> </td> 
   <td> <p> URL racine pour les chemins relatifs aux fichiers HTTP dans les <span class="codeph"> commandes src=</span> </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> attribute ::ShowOverlapObjs</span> </p> </td> 
   <td> <p> État d’affichage/masquage initial des objets de chevauchement </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> attribute ::Expiration</span> </p> </td> 
   <td> <p> Valeur de durée d’activation de l’image de réponse pour les caches du serveur proxy et du navigateur </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> attribut ::MaxPix</span> </p> </td> 
   <td> <p> Largeur et hauteur maximales autorisées de l’image de réponse </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> attribut ::D efaultPix</span> </p> </td> 
   <td> <p> Valeurs par défaut pour <span class="codeph"> wid=</span> et <span class="codeph"> hei=</span> </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> attribut ::Format</span> </p> </td> 
   <td> <p> Valeur par défaut pour <span class="codeph"> fmt=</span> </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> attribut ::JpegQuality</span> </p> </td> 
   <td> <p> Valeur par défaut de <span class="codeph"> qlt=</span> </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> attribut ::TiffEncoding</span> </p> </td> 
   <td> <p> Type de compression pour la sortie d’image TIFF </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> attribut ::Accentuer</span> </p> </td> 
   <td> <p> Valeur par défaut pour <span class="codeph"> sharpen=</span> </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> attribut ::OnFailSel</span> </p> </td> 
   <td> <p> Spécifie le comportement en cas d’échec d’une <span class="codeph"> commande sel=</span> </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> attribut ::OnFailObj</span> </p> </td> 
   <td> <p> Spécifie le comportement lorsqu’une <span class="codeph"> commande obj=</span> échoue </p> </td> 
  </tr> 
 </tbody> 
</table>
