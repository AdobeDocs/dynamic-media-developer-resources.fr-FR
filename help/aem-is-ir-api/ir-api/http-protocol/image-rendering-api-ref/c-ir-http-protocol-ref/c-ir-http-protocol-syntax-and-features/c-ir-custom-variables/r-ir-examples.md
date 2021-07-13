---
description: Cet exemple utilise le service d’images pour colorer un objet et appliquer une balise contenant du texte personnalisé dans l’une des vignettes.
solution: Experience Manager
title: Exemples
feature: Dynamic Media Classic, SDK/API
role: Developer,User
exl-id: 85f11642-e1ff-4bf0-bd21-d419805cff4a
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '146'
ht-degree: 1%

---

# Exemples{#examples}

Cet exemple utilise le service d’images pour colorer un objet et appliquer une balise contenant du texte personnalisé dans l’une des vignettes.

Les variables IR sont utilisées pour identifier la vignette, l’image du logo et le texte personnalisé.

Le champ `vignette::Modifier` de l&#39;enregistrement nommé *template* dans la vignette map du catalogue de matériaux `myCat` contient les éléments suivants :

`$vig=defaultVignette&$text=text_goes_here&$color=220,220,220&vignette=myCat/$vig$&obj=group/object&color=$color$&decal&src=is{?size=300,100&text={\qc\fs36 $text$}}`

Toutes les vignettes qui seront utilisées sont répertoriées dans la vignette du catalogue de matériaux `myCat`.

Le client peut maintenant effectuer la requête suivante pour récupérer l’image par défaut (elle utilise les variables définies au début du modèle) :

[!DNL `https://server/myCat/template`]

La requête suivante spécifie le contenu à rendre :

[!DNL `https://server/myCat/template?$vig=specialCup&$text=Happy%20Birthday!\line%20Pauline&$color=230,20,20`]

Pour plus d’informations sur la commande Image Serving `text=`, reportez-vous à la documentation sur le serveur d’images .
