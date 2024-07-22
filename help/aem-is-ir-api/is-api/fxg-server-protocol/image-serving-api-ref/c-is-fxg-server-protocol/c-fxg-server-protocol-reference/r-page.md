---
title: page
description: Récupérez la page . Récupère une page spécifique dans un fichier FXG multipage.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 7c72ceff-30d9-4e0b-8b4f-6cb0039d389e
source-git-commit: 38f3e425be0ce3e241fc18b477e3f68b7b763b51
workflow-type: tm+mt
source-wordcount: '50'
ht-degree: 6%

---

# page{#page}

Récupérez la page . Récupère une page spécifique dans un fichier FXG multipage.

`page= *`val`*`

<table id="simpletable_E92560F812B64A36A3D108CA7DEED5AC"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> val</span></span> </p> </td> 
  <td class="stentry"> <p>Numéro de page (la première page est 1). </p></td> 
 </tr> 
</table>

## Par défaut {#section-3fd7fcc525b947c7a95457e50414ac9e}

Si `page` n’est pas spécifié, la première page est renvoyée pour la sortie de pixellisation et toutes les pages pour la sortie de PDF.
