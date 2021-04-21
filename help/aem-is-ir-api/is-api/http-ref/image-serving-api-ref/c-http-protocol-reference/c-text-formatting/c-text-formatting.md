---
description: La diffusion d’images offre plusieurs alternatives au rendu du texte, accessibles avec les commandes text= et textPs=.
solution: Experience Manager
title: Formatage du texte
feature: Dynamic Media Classic,SDK/API
role: Developer,Business Practitioner
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '565'
ht-degree: 7%

---


# Formatage du texte{#text-formatting}

La diffusion d’images offre plusieurs alternatives au rendu du texte, accessibles avec les commandes text= et textPs=.

`textPs=` offre un niveau élevé de similitude avec le texte rendu avec Adobe Photoshop et Illustrator. `text=` est raisonnablement compatible avec le texte rendu avec Windows Wordpad.

>[!NOTE]
>
>Outre les différences répertoriées ailleurs, `text=` produit des différences subtiles dans le texte rendu par rapport à `textPs=`. Par exemple, les soulignements n’ont pas la même épaisseur et la même position et les italiques synthétisés sont rendus à un angle légèrement différent. Si le texte ne tient pas dans l’espace disponible, `text=` peut recadrer partiellement la dernière ligne, tandis que `textPs=` ne rendra que les lignes complètes.

Toutes les commandes de texte acceptent du texte formaté en fonction d’un sous-ensemble de la spécification RTF (Rich Text Format). Chaque calque de texte peut spécifier une commande de texte différente.

Le tableau suivant liste les principales fonctionnalités disponibles pour chaque commande de texte :

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
   <td> <p> compatible Adobe Photoshop </p> </td> 
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
   <td> <p>Ajustement de copie </p> </td> 
   <td> <p>non </p> </td> 
   <td> <p>oui </p> </td> 
   <td> Copier-ajuster <p>, <pre>\copyfit</pre>, <pre>\copyfitlines</pre>, <pre>\copyfitmaxlines</pre> </p> </td> 
  </tr> 
  <tr> 
   <td> <p>Marges de zone de texte </p> </td> 
   <td> <p>non </p> </td> 
   <td> <p>oui </p> </td> 
   <td> <p><pre>\margl</pre>, <pre>\margr</pre>, <pre>\margt</pre>, <pre>\margb</pre> </p> </td> 
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
   <td> <p>Retrait du paragraphe </p> </td> 
   <td> <p>non </p> </td> 
   <td> <p>oui </p> </td> 
   <td> <p>\fi, \li, \ri </p> </td> 
  </tr> 
  <tr> 
   <td> <p>Texte en majuscules et en petites capitales </p> </td> 
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
   <td> <p>enchaînement de texte de haut en bas/de droite à gauche </p> </td> 
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
   <td> <p>Ajuster automatiquement le calque au texte </p> </td> 
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
   <td> <p>Désactiver le retour à la ligne </p> </td> 
   <td> <p>oui </p> </td> 
   <td> <p>non </p> </td> 
   <td> <p>textAttr= </p> </td> 
  </tr> 
  <tr> 
   <td> <p>Mise à l’échelle automatique du texte en fonction de la taille du calque (selon une résolution variable) </p> </td> 
   <td> <p>oui </p> </td> 
   <td> <p>non </p> </td> 
   <td> <p>textAttr= </p> </td> 
  </tr> 
 </tbody> 
</table>

Les chaînes compatibles RTF peuvent être assemblées manuellement ou en formatant le texte de votre choix dans un éditeur de texte ou un traitement de texte capable d’enregistrer des fichiers RTF. Le fichier RTF peut alors être ouvert dans un éditeur de texte brut et le contenu RTF brut approprié du fichier copié dans l’URL de demande.

Certains traitements de texte génèrent des fichiers plutôt volumineux, qui incluent des préambules substantiels qui ne sont pas utilisés par Dynamic Media Image Serving. Il est recommandé de supprimer les éléments RTF inutilisés de la chaîne avant de transmettre la chaîne aux commandes de texte.

Le codage de langue basé sur les normes UTF-8 et ISO est pris en charge dans les chaînes RTF en tant qu’alternative aux mécanismes de codage de caractères RTF standard. Cela permet aux applications d&#39;envoyer du texte non anglais au serveur sans connaissance du codage RTF.

Tous les caractères non conformes au protocole HTTP doivent être correctement protégés par une séquence d’échappement si la chaîne doit être transmise via http. Seuls &quot;=&quot;, &quot;&amp;&quot; et &quot;%&quot; doivent être placés en séquence d’échappement si la chaîne est incorporée dans le champ `catalog::Modifiers` d’un enregistrement de catalogue d’images. Les caractères de contrôle, y compris `<CR>`, `<LF>` et `<TAB>`, doivent toujours être supprimés.

Les moteurs de texte Image Serving interprètent un sous-ensemble de commandes définies par la spécification RTF (Rich Text Format), version 1.6. Ce sous-ensemble est axé sur le formatage des polices/caractères, le formatage des paragraphes simple et la prise en charge des polices et des jeux de caractères internationaux. Pour le moment, les éléments de formatage plus avancés, tels que les feuilles de style et les tableaux, ne sont pas pris en charge.

La familiarité avec la spécification RTF (Rich Text Format), telle que publiée par Microsoft, est requise lors de la tentative de construction manuelle de chaînes de texte codées RTF.

* [Gestion des polices](r-font-handling.md)
* [Traitement des couleurs](r-color-handling.md)
* [Ajustement de copie](r-copy-fitting.md)
* [calques de texte](r-text-layers.md)
* [Positionnement du texte](r-text-positioning.md)
* [Caractères réservés](r-reserved-characters.md)
* [Commandes et mots-clés RTF pris en charge](c-supported-rtf-commands-and-keywords/c-supported-rtf-commands-and-keywords.md)
* [Exemples de codage RTF](r-rtf-encoding-examples.md)
