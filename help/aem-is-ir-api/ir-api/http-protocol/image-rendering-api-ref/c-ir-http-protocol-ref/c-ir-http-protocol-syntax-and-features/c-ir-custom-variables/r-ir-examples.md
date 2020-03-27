---
description: Cet exemple utilise la fonction Image Serving (diffusion d’images) pour coloriser un objet et appliquer une étiquette contenant du texte personnalisé dans l’un des ensembles de vignettes.
seo-description: Cet exemple utilise la fonction Image Serving (diffusion d’images) pour coloriser un objet et appliquer une étiquette contenant du texte personnalisé dans l’un des ensembles de vignettes.
seo-title: Exemples
solution: Experience Manager
title: Exemples
topic: Scene7 Image Serving - Image Rendering API
uuid: 9f8e4346-6efe-4f21-982d-613328bd708d
translation-type: tm+mt
source-git-commit: b27327f940202b1883a654702aa386c7ae83c856

---


# Exemples{#examples}

Cet exemple utilise la fonction Image Serving (diffusion d’images) pour coloriser un objet et appliquer une étiquette contenant du texte personnalisé dans l’un des ensembles de vignettes.

Les variables IR permettent d’identifier la vignette, l’image du logo et le texte personnalisé.

Le `vignette::Modifier` champ de l’enregistrement appelé *modèle* dans la carte de vignette du catalogue de matières `myCat` contient les éléments suivants :

`$vig=defaultVignette&$text=text_goes_here&$color=220,220,220&vignette=myCat/$vig$&obj=group/object&color=$color$&decal&src=is{?size=300,100&text={\qc\fs36 $text$}}`

Toutes les vignettes qui seront utilisées sont répertoriées dans la carte de vignettes du catalogue de matériaux `myCat`.

Le client peut désormais effectuer la requête suivante pour récupérer l’image par défaut (en utilisant les variables définies au début du modèle) :

[!DNL `https://server/myCat/template`]

La requête suivante spécifie le contenu à rendre :

[!DNL `https://server/myCat/template?$vig=specialCup&$text=Happy%20Birthday!\line%20Pauline&$color=230,20,20`]

Pour plus d’informations sur la commande Image Serving `text=` , reportez-vous à la section Documentation du serveur d’images.
