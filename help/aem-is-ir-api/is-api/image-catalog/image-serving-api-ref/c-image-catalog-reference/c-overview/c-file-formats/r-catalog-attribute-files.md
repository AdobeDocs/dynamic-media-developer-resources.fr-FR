---
description: Les fichiers d’attributs de catalogue peuvent porter n’importe quel nom, mais doivent comporter un suffixe de fichier .ini. Ils peuvent être facilement conservés à l’aide de n’importe quel éditeur de texte.
solution: Experience Manager
title: Fichiers d’attributs de catalogue
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 79d9439d-7749-4ae1-aa73-e88e01cf7555
TQID: 'https://experienceleague.adobe.com/RCxeXg3wb10jo37biAs1puqmEo8bAL-i-oZBwGHuloA'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 195
ht-degree: 0%

---

# Fichiers d’attributs de catalogue{#catalog-attribute-files}

Les fichiers d’attributs de catalogue peuvent porter n’importe quel nom, mais doivent comporter un suffixe de fichier .ini. Ils peuvent être facilement conservés à l’aide de n’importe quel éditeur de texte.

Les fichiers d’attributs de catalogue se composent d’un ensemble d’enregistrements texte, séparés par une seule `<CR>` (`0xD` de code ASCII), une seule `<LF>` (`0xA` de code ASCII) ou une paire de `<CR><LF>`. Chaque enregistrement se compose d’un nom d’attribut et d’une ou de plusieurs valeurs d’attribut séparées par des virgules :

`*`name`*= *`values`*{<CR>|<LF>|<CR><LF }`

<table id="simpletable_0F879121670046AE9414298725961303"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> valeurs </span> </p> </td> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> val</span>[,<span class="varname"> valeurs</span>]</span> </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> nom </span> </p> </td> 
  <td class="stentry"> <p>Nom de l’attribut. Se compose d’une ou de plusieurs lettres, chiffres, - et _. Non sensible à la casse. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> val</span> </p></td> 
  <td class="stentry"> <p>Valeur d’attribut. Ne doit pas inclure <span class="codeph"> &lt;CR&gt;</span> ou <span class="codeph"> &lt;LF&gt;</span> caractères, à moins qu’ils ne soient précédés d’une seule barre oblique inverse juste avant le caractère de nouvelle ligne. </p></td> 
 </tr> 
</table>

L’espace blanc entre les jetons est facultatif.

Les enregistrements dont les noms d&#39;attribut sont inconnus sont ignorés par le [!DNL Platform Server].

Les noms d’attribut peuvent être constitués de toute combinaison de lettres ASCII, de chiffres, ainsi que de « - », « _ » et « . ».

Si le même nom d’attribut apparaît plusieurs fois dans le même fichier d’attribut, le dernier événement rencontré prévaut.

Utilisez # comme premier caractère pour marquer un enregistrement comme commentaire, ce que l&#39;analyseur ignore.
