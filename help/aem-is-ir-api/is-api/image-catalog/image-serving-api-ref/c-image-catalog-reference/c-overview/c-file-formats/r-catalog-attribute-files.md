---
description: Les fichiers d’attributs du catalogue peuvent porter n’importe quel nom, mais doivent comporter un suffixe de fichier .ini. Elles peuvent être facilement gérées à l’aide de n’importe quel éditeur de texte.
solution: Experience Manager
title: Fichiers d’attributs du catalogue
feature: Dynamic Media Classic, SDK/API
role: Developer,User
exl-id: 79d9439d-7749-4ae1-aa73-e88e01cf7555
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '202'
ht-degree: 0%

---

# Fichiers d’attributs du catalogue{#catalog-attribute-files}

Les fichiers d’attributs du catalogue peuvent porter n’importe quel nom, mais doivent comporter un suffixe de fichier .ini. Elles peuvent être facilement gérées à l’aide de n’importe quel éditeur de texte.

Les fichiers d’attributs du catalogue se composent d’un ensemble d’enregistrements texte, séparés par une seule balise `<CR>` (code ASCII `0xD`), une seule balise `<LF>` (code ASCII `0xA`) ou une paire `<CR><LF>`. Chaque enregistrement se compose d’un nom d’attribut et d’une ou de plusieurs valeurs d’attribut séparées par des virgules :

`*``*= *`namevalues`*{<CR>|<LF>|<CR><LF }`

<table id="simpletable_0F879121670046AE9414298725961303"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> valeurs</span> </p> </td> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> val</span>[,<span class="varname"> valeurs</span>]</span> </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> name</span> </p> </td> 
  <td class="stentry"> <p>Nom de l’attribut. Peut se composer d’une ou de plusieurs lettres, nombre, - et _. Non sensible à la casse. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> val</span> </p></td> 
  <td class="stentry"> <p>Valeur d’attribut. Ne doit pas inclure de caractères <span class="codeph"> &lt;CR&gt;</span> ou <span class="codeph"> &lt;LF&gt;</span>, sauf si une seule barre oblique inverse s’affiche juste avant le caractère de saut de page. </p></td> 
 </tr> 
</table>

L’espace entre les jetons est facultatif.

Les enregistrements avec des noms d’attribut inconnus sont ignorés par le serveur Platform.

Les noms d’attribut peuvent être composés de n’importe quelle combinaison de lettres ASCII, de nombres, ainsi que de &quot;-&quot;, &quot;_&quot; et &quot;.&quot;.

Si le même nom d’attribut apparaît plusieurs fois dans le même fichier d’attributs, c’est le dernier qui se produit qui prévaut.

Utilisez # comme premier caractère pour marquer un enregistrement comme commentaire, ce que l’analyseur ignore.
