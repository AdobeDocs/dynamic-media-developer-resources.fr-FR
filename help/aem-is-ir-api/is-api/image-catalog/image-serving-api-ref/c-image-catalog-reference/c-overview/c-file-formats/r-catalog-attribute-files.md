---
description: Les fichiers d’attributs du catalogue peuvent porter n’importe quel nom, mais doivent comporter un suffixe de fichier .ini. Elles peuvent être facilement gérées à l’aide de n’importe quel éditeur de texte.
solution: Experience Manager
title: Fichiers d’attributs du catalogue
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 79d9439d-7749-4ae1-aa73-e88e01cf7555
source-git-commit: bf31e5226cbb763e2fb82391772b64e5d5c89fae
workflow-type: tm+mt
source-wordcount: '195'
ht-degree: 1%

---

# Fichiers d’attributs du catalogue{#catalog-attribute-files}

Les fichiers d’attributs du catalogue peuvent porter n’importe quel nom, mais doivent comporter un suffixe de fichier .ini. Elles peuvent être facilement gérées à l’aide de n’importe quel éditeur de texte.

Les fichiers d’attributs du catalogue se composent d’un ensemble d’enregistrements texte, séparés par une seule `<CR>` (code ASCII) `0xD`), un seul `<LF>` (code ASCII) `0xA`), ou un `<CR><LF>` paire . Chaque enregistrement se compose d’un nom d’attribut et d’une ou de plusieurs valeurs d’attribut séparées par des virgules :

`*`name`*= *`values`*{<CR>|<LF>|<CR><LF }`

<table id="simpletable_0F879121670046AE9414298725961303"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> valeurs</span> </p> </td> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> val</span>[,<span class="varname"> values</span>]</span> </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> name</span> </p> </td> 
  <td class="stentry"> <p>Nom de l’attribut. Peut se composer d’une ou de plusieurs lettres, nombre, - et _. Non sensible à la casse. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> val</span> </p></td> 
  <td class="stentry"> <p>Valeur d’attribut. Ne doit pas inclure <span class="codeph"> &lt;cr&gt;</span> ou <span class="codeph"> &lt;lf&gt;</span> , sauf si une seule barre oblique inverse s’affiche juste avant le caractère de saut de page. </p></td> 
 </tr> 
</table>

L’espace entre les jetons est facultatif.

Les enregistrements dont les noms d’attribut sont inconnus sont ignorés par [!DNL Platform Server].

Les noms d’attribut peuvent être composés de n’importe quelle combinaison de lettres ASCII, de nombres, ainsi que de &quot;-&quot;, &quot;_&quot; et &quot;.&quot;.

Si le même nom d’attribut apparaît plusieurs fois dans le même fichier d’attributs, c’est le dernier qui se produit qui prévaut.

Utilisez # comme premier caractère pour marquer un enregistrement comme commentaire, ce que l’analyseur ignore.
