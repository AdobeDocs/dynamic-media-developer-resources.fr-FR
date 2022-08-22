---
title: Fichiers d’attributs du catalogue
description: Les fichiers d’attributs du catalogue peuvent porter n’importe quel nom, mais doivent comporter un suffixe de fichier .ini. Elles peuvent être facilement gérées à l’aide de n’importe quel éditeur de texte.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 8b5afb99-3201-4e43-93e7-e8998354204f
source-git-commit: 8454991568374ecd1c4babdd3210250ea7988c4c
workflow-type: tm+mt
source-wordcount: '194'
ht-degree: 0%

---

# Fichiers d’attributs du catalogue{#catalog-attribute-files}

Les fichiers d’attributs du catalogue peuvent porter n’importe quel nom, mais doivent comporter une variable `.ini` suffixe du fichier. Elles peuvent être facilement gérées à l’aide de n’importe quel éditeur de texte.

Les fichiers d’attributs du catalogue se composent d’un ensemble d’enregistrements texte, séparés par une seule `<CR>` (code ASCII 0xD), une seule `<LF>` (code ASCII 0xA) ou un `<CR><LF>` paire . Chaque enregistrement se compose d’un nom d’attribut et d’une ou de plusieurs valeurs d’attribut séparées par des virgules :

`*`name`*= *`value`*&#42;[, *`value`*]{<CR>|<LF>|<CR><LF>}`

<table id="simpletable_8454AD549FDA421BA1469CDA44132773"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> name </span> </span> </p> </td> 
  <td class="stentry"> <p>Nom de l’attribut ; peut contenir une ou plusieurs lettres, le nombre, "-" et "_"; non sensible à la casse. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> value </span> </span> </p> </td> 
  <td class="stentry"> <p>Valeur d’attribut ; ne doit pas inclure <span class="codeph"> &lt;cr&gt; </span>ou <span class="codeph"> &lt;lf&gt; </span> , sauf si une seule barre oblique inverse s’affiche juste avant le caractère de saut de page. </p> </td> 
 </tr> 
</table>

* L’espace entre les jetons est facultatif.
* Les enregistrements avec des noms d’attribut inconnus sont ignorés par le serveur Platform.
* Les noms d’attribut peuvent être composés de n’importe quelle combinaison de lettres ASCII, de nombres et de &quot;-&quot;, &quot;_&quot; et &quot;.&quot;
* Si le même nom d’attribut apparaît plusieurs fois dans le même fichier d’attributs, c’est le dernier qui se produit qui prévaut.
* Utilisez &quot;#&quot; comme premier caractère pour marquer un enregistrement comme commentaire, ce que l’analyseur ignore.
