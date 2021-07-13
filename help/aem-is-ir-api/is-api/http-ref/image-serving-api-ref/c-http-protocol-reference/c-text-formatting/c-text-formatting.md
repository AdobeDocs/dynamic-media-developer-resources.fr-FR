---
description: La diffusion d’images offre plusieurs alternatives au rendu du texte, accessibles par les commandes text= et textPs=.
solution: Experience Manager
title: Formatage de texte
feature: Dynamic Media Classic, SDK/API
role: Developer,User
exl-id: 2c120ed1-b556-4caf-a30e-63ae48cc2104
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '562'
ht-degree: 7%

---

# Formatage de texte{#text-formatting}

La diffusion d’images offre plusieurs alternatives au rendu du texte, accessibles par les commandes text= et textPs=.

`textPs=` offre un niveau élevé de similitude avec le texte rendu avec Adobe Photoshop et Illustrator. `text=` est raisonnablement compatible avec le texte rendu avec Windows Wordpad.

>[!NOTE]
>
>Outre les différences répertoriées ailleurs, `text=` produit des différences subtiles dans le texte rendu par rapport à `textPs=`. Par exemple, les soulignements n’ont pas la même épaisseur et la même position et les italiques synthétisés sont rendus à un angle légèrement différent. Si le texte ne correspond pas à l’espace disponible, `text=` peut recadrer partiellement la dernière ligne, tandis que `textPs=` effectue uniquement le rendu des lignes complètes.

Toutes les commandes de texte acceptent du texte formaté en fonction d’un sous-ensemble de la spécification RTF (Rich Text Format). Chaque calque de texte peut spécifier une commande de texte différente.

Le tableau suivant répertorie les fonctions clés disponibles pour chaque commande de texte :

<table id="table_9C41CBDA94C24805B538E5049B0137C6"> 
 <thead> 
  <tr> 
   <th class="entry"> <b> Fonctionnalité</b> </th> 
   <th class="entry"> <b> texte=</b> </th> 
   <th class="entry"> <b> textPs=</b> </th> 
   <th class="entry"> <b> Voir aussi</b> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td> <p> Compatible avec Adobe Photoshop </p> </td> 
   <td> <p> non </p> </td> 
   <td> <p> limité </p> </td> 
   <td> <p> </p> </td> 
  </tr> 
  <tr> 
   <td> <p>Transformer le texte en formes arbitraires </p> </td> 
   <td> <p>non </p> </td> 
   <td> <p>oui </p> </td> 
   <td> <p>textFlowPath=, textFlowXPath= </p> </td> 
  </tr> 
  <tr> 
   <td> <p>Flux de texte le long de chemins arbitraires </p> </td> 
   <td> <p>non </p> </td> 
   <td> <p>oui </p> </td> 
   <td> <p>textPath= </p> </td> 
  </tr> 
  <tr> 
   <td> <p>Correspondance </p> </td> 
   <td> <p>non </p> </td> 
   <td> <p>oui </p> </td> 
   <td> Copie-ajustement <p>, <pre>\copyfit</pre>, <pre>\copyfitlines</pre>, <pre>\copyfitmaxlines</pre> </p> </td> 
  </tr> 
  <tr> 
   <td> <p>Marges des zones de texte </p> </td> 
   <td> <p>non </p> </td> 
   <td> <p>oui </p> </td> 
   <td> <p><pre>\rate</pre>, <pre>\rate</pre>, <pre>\rate</pre>, <pre>\margin</pre> </p> </td> 
  </tr> 
  <tr> 
   <td> <p>Justification complète du paragraphe </p> </td> 
   <td> <p>non </p> </td> 
   <td> <p>oui </p> </td> 
   <td> <p><pre>\qj</pre> </p> </td> 
  </tr> 
  <tr> 
   <td> <p>justification de la dernière ligne </p> </td> 
   <td> <p>non </p> </td> 
   <td> <p>oui </p> </td> 
   <td> <p>\lastql, \lastqr, \lastqc, \lastqj </p> </td> 
  </tr> 
  <tr> 
   <td> <p>Retrait de paragraphe </p> </td> 
   <td> <p>non </p> </td> 
   <td> <p>oui </p> </td> 
   <td> <p>\fi, \li, \ri </p> </td> 
  </tr> 
  <tr> 
   <td> <p>Majuscules et texte en majuscules </p> </td> 
   <td> <p>non </p> </td> 
   <td> <p>oui </p> </td> 
   <td> <p>\caps, \scaps </p> </td> 
  </tr> 
  <tr> 
   <td> <p>Couleurs de diffusion d’images </p> </td> 
   <td> <p>non </p> </td> 
   <td> <p>oui </p> </td> 
   <td> <p>\*\iscolortbl </p> </td> 
  </tr> 
  <tr> 
   <td> <p>Plusieurs modes de lissage </p> </td> 
   <td> <p>non </p> </td> 
   <td> <p>oui </p> </td> 
   <td> <p>textAttr= </p> </td> 
  </tr> 
  <tr> 
   <td> <p>flux de texte supérieur/inférieur/droit-gauche </p> </td> 
   <td> <p>non </p> </td> 
   <td> <p>oui </p> </td> 
   <td> <p>\stextFlow </p> </td> 
  </tr> 
  <tr> 
   <td> <p>Prise en charge de Photofont® </p> </td> 
   <td> <p>non </p> </td> 
   <td> <p>oui </p> </td> 
   <td> Gestion des polices </td> 
  </tr> 
  <tr> 
   <td> <p>Calque de taille automatique adapté au texte </p> </td> 
   <td> <p>oui </p> </td> 
   <td> <p>oui </p> </td> 
   <td> <p>text=, textId=, size= </p> </td> 
  </tr> 
  <tr> 
   <td> <p>Prise en charge CMJN </p> </td> 
   <td> <p>oui </p> </td> 
   <td> <p>oui </p> </td> 
   <td> <p>\cmykcolortbl, \*\iscolortbl </p> </td> 
  </tr> 
  <tr> 
   <td> <p>Flux de caractères de droite à gauche </p> </td> 
   <td> <p>oui </p> </td> 
   <td> <p>non </p> </td> 
   <td> <p>\rtlch </p> </td> 
  </tr> 
  <tr> 
   <td> <p>Désactiver le retour automatique à la ligne </p> </td> 
   <td> <p>oui </p> </td> 
   <td> <p>non </p> </td> 
   <td> <p>textAttr= </p> </td> 
  </tr> 
  <tr> 
   <td> <p>Mise à l’échelle automatique du texte en fonction de la taille du calque (avec une résolution variable) </p> </td> 
   <td> <p>oui </p> </td> 
   <td> <p>non </p> </td> 
   <td> <p>textAttr= </p> </td> 
  </tr> 
 </tbody> 
</table>

Les chaînes compatibles RTF peuvent être assemblées manuellement ou en formatant le texte souhaité dans un éditeur de texte ou un traitement de texte capable d’enregistrer des fichiers RTF. Le fichier RTF peut alors être ouvert dans un éditeur de texte brut et le contenu RTF brut approprié du fichier copié dans l’URL de requête.

Certains traitements de texte génèrent des fichiers plutôt volumineux, qui incluent des préambules substantiels qui ne sont pas utilisés par Dynamic Media Image Serving. Il est recommandé de supprimer les éléments RTF inutilisés de la chaîne avant de transmettre la chaîne aux commandes de texte.

L’encodage de langue basé sur les normes UTF-8 et ISO est pris en charge dans les chaînes RTF en tant qu’alternative aux mécanismes d’encodage de caractères RTF standard. Cela permet aux applications d’envoyer du texte non anglais au serveur sans connaissance du codage RTF.

Tous les caractères non compatibles HTTP doivent être correctement échappés si la chaîne doit être transmise via http. Seuls &quot;=&quot;, &quot;&amp;&quot; et &quot;%&quot; doivent être précédés d’une séquence d’échappement si la chaîne est incorporée dans le champ `catalog::Modifiers` d’un enregistrement de catalogue d’images. Les caractères de contrôle, y compris `<CR>`, `<LF>` et `<TAB>`, doivent toujours être supprimés.

Les moteurs de texte du serveur d’images interprètent un sous-ensemble de commandes définies par la spécification RTF (Rich Text Format), version 1.6. Ce sous-ensemble est axé sur le formatage des polices/caractères, le formatage simple des paragraphes, ainsi que sur la prise en charge des polices internationales et des jeux de caractères. Les éléments de mise en forme plus avancés, tels que les feuilles de style et les tableaux, ne sont pas pris en charge pour le moment.

Une connaissance de la spécification RTF (Rich Text Format), telle que publiée par Microsoft, est requise lorsque vous tentez de construire manuellement des chaînes de texte codées en RTF.

* [Gestion des polices](r-font-handling.md)
* [Gestion des couleurs](r-color-handling.md)
* [Correspondance](r-copy-fitting.md)
* [Calques de texte](r-text-layers.md)
* [Position du texte](r-text-positioning.md)
* [Caractères réservés](r-reserved-characters.md)
* [Commandes RTF et mots-clés pris en charge](c-supported-rtf-commands-and-keywords/c-supported-rtf-commands-and-keywords.md)
* [Exemples de codage RTF](r-rtf-encoding-examples.md)
