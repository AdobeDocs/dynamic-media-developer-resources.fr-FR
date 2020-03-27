---
description: La personnalisation visuelle et la personnalisation du comportement la plus fréquente pour la visionneuse de zoom de base se font en créant une page CSS personnalisée.
keywords: responsive
seo-description: La personnalisation visuelle et la personnalisation du comportement la plus fréquente pour la visionneuse de zoom de base se font en créant une page CSS personnalisée.
seo-title: Personnalisation de la visionneuse de zoom de base
solution: Experience Manager
title: Personnalisation de la visionneuse de zoom de base
topic: Dynamic media
uuid: 9f3c203e-ff6f-4bf1-a1dc-26495412af45
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# Personnalisation de la visionneuse de zoom de base{#customizing-basic-zoom-viewer}

La personnalisation visuelle et la personnalisation du comportement la plus fréquente pour la visionneuse de zoom de base se font en créant une page CSS personnalisée.

Le flux de travail suggéré consiste à extraire le fichier CSS par défaut pour la visionneuse appropriée, à le copier vers un autre emplacement, à le personnaliser et à spécifier l’emplacement du fichier personnalisé dans la `style=` commande.

Les fichiers CSS par défaut se trouvent à l’emplacement suivant :

`<s7_viewers_root>/html5/BasicZoomViewer_light.css`

Le lecteur est fourni avec deux fichiers CSS prêts à l’emploi, pour les modèles de couleurs &quot;clair&quot; et &quot;foncé&quot;. La version &quot;light&quot; est utilisée par défaut, mais vous pouvez passer à la version &quot;dark&quot; à l’aide de la page CSS standard suivante :

`<s7_viewers_root>/html5/BasicZoomViewer_dark.css`

Le fichier CSS personnalisé doit contenir les mêmes déclarations de classe que les déclarations par défaut. Si une déclaration de classe est omise, le lecteur ne fonctionne pas correctement car il ne fournit pas de styles par défaut intégrés pour les éléments de l’interface utilisateur.

Vous pouvez également fournir des règles CSS personnalisées en utilisant des styles incorporés directement sur la page Web ou dans l’une des règles CSS externes liées.

Lors de la création d’une page CSS personnalisée, gardez à l’esprit que le lecteur affecte `.s7basiczoomviewer` une classe à son élément DOM . Si vous utilisez un fichier CSS externe transmis avec `style=` la commande, utilisez `.s7basiczoomviewer` class comme classe parent dans le sélecteur descendant pour vos règles CSS. Si vous créez des styles intégrés sur la page Web, qualifiez en outre ce sélecteur avec l’ID de l’élément DOM  comme suit :

`#<containerId>.s7basiczoomviewer`

## Création de CSS de conception réactive {#section-0bb49aca42d242d9b01879d5ba59d33b}

Il est possible d’de différents périphériques et de différentes tailles d’incorporation dans une page CSS afin que votre contenu s’affiche différemment selon le périphérique d’un utilisateur ou une disposition de page Web particulière. Cela inclut, entre autres, les différentes mises en page, la taille des éléments de l’interface utilisateur et la résolution des illustrations.

Le lecteur prend en charge deux mécanismes de création d’une page CSS adaptée : Marqueurs CSS et de médias CSS standard. Vous pouvez les utiliser indépendamment ou ensemble.

**Marqueurs CSS**

Pour faciliter la création de pages CSS adaptées, le lecteur prend en charge les marqueurs CSS. Il s’agit de classes CSS spéciales qui sont attribuées dynamiquement à l’élément de de la visionneuse de niveau supérieur en fonction de la taille du lecteur d’exécution et du type d’entrée utilisé sur le périphérique actuel.

Le premier groupe de marqueurs CSS comprend `.s7size_large`, `.s7size_medium`et `.s7size_small` des classes. Elles sont appliquées en fonction de la zone d’exécution du  du lecteur de contenu. Si la zone de visualisation est égale ou supérieure à la taille d’un moniteur de bureau commun, `.s7size_large` est utilisée ; si la zone est proche d’une tablette commune, `.s7size_medium` elle est affectée. Pour les zones similaires aux écrans de téléphone mobile, `.s7size_small` est alors définie. L’objectif principal de ces marqueurs CSS est de créer différentes mises en page d’interface utilisateur pour différents écrans et tailles de visionneuse.

Le deuxième groupe de marqueurs CSS contient `.s7mouseinput` et `.s7touchinput`. `.s7touchinput` est définie si le périphérique actif dispose de fonctionnalités d’entrée tactile ; dans le cas contraire, `.s7mouseinput` est utilisée. Ces marqueurs sont principalement destinés à créer des éléments d’entrée de l’interface utilisateur avec des tailles d’écran différentes pour différents types d’entrée, car l’entrée tactile requiert normalement des éléments plus volumineux. Si le périphérique dispose de fonctionnalités tactiles et d’entrée de souris, `.s7touchinput` est défini et le lecteur effectue le rendu d’une interface utilisateur tactile.

L’exemple CSS suivant définit la taille du bouton de zoom sur 28 x 28 pixels sur les systèmes avec saisie de la souris et sur 56 x 56 pixels sur les périphériques tactiles. En outre, il masque complètement le bouton si la taille du lecteur devient très petite :

```
.s7basiczoomviewer.s7mouseinput .s7zoominbutton { 
    width:28px; 
    height:28px; 
} 
.s7basiczoomviewer.s7touchinput .s7zoominbutton { 
    width:56px; 
    height:56px; 
} 
.s7basiczoomviewer.s7size_small .s7zoominbutton { 
    visibility:hidden; 
}
```

Pour des périphériques avec une densité de pixels différente, vous devez utiliser le de médias CSS. Le bloc de multimédia suivant contiendra des feuilles CSS spécifiques aux écrans haute densité :

```
@media screen and (-webkit-min-device-pixel-ratio: 1.5) 
{ 
}
```

L’utilisation de marqueurs CSS est la méthode la plus souple de création de feuilles de style CSS pour une conception adaptée, car elle vous permet de  non seulement la taille de l’écran du périphérique, mais aussi la taille réelle de la visionneuse, ce qui est utile pour les mises en page adaptées.

Vous pouvez utiliser le fichier CSS de visionneuse par défaut comme exemple d’approche des marqueurs CSS.

**de médias CSS**

Vous pouvez également effectuer des détections de périphériques à l’aide d’un  CSS Media pur. Tout ce qui est contenu dans un bloc de de médias donné est appliqué uniquement lorsqu&#39;il est exécuté sur un périphérique correspondant.

Lorsqu’elles sont appliquées aux visionneuses mobiles, elles utilisent quatre  de médias CSS, définis dans votre page CSS, dans l’ordre indiqué ci-dessous :

1. Contient uniquement des règles spécifiques à tous les périphériques tactiles.

   ```
   @media only screen and (max-device-width:13.5in) and (max-device- 
   height:13.5in) and (max-device-width:799px),  
   only screen and (max-device-width:13.5in) and (max-device-height:13.5in)  
   and (max-device-height:799px) 
   { 
   }
   ```

1. Contient uniquement des règles spécifiques aux tablettes avec des écrans haute résolution.

   ```
   @media only screen and (max-device-width:13.5in) and (max-device-height:13.5in) and (max-device-width:799px) and (-webkit-min-device-pixel-ratio:1.5), 
   only screen and (max-device-width:13.5in) and (max-device-height:13.5in) and (max-device-height:799px) and (-webkit-min-device-pixel-ratio:1.5)  
   { 
   }
   ```

1. Contient uniquement des règles spécifiques à tous les téléphones mobiles.

   ```
   @media only screen and (max-device-width:9in) and (max-device-height:9in) 
   { 
   }
   ```

1. Contient uniquement des règles spécifiques aux téléphones mobiles avec écrans haute résolution.

   ```
   @media only screen and (max-device-width:9in) and (max-device-height:9in) and (-webkit-min-device-pixel-ratio: 1.5), 
     only screen and (device-width:720px) and (device-height:1280px) and (-webkit-device-pixel-ratio: 2), 
     only screen and (device-width:1280px) and (device-height:720px) and (-webkit-device-pixel-ratio: 2) 
   { 
   }
   ```

À l’aide d’une approche  média, vous devez organiser les feuilles de style CSS avec la détection de périphérique comme suit :

* Tout d’abord, la section spécifique au bureau définit toutes les propriétés propres au bureau ou communes à tous les écrans.
* Ensuite, les quatre de médias suivent l’ordre défini ci-dessus et fournissent des règles CSS spécifiques au type de périphérique correspondant.

Il n’est pas nécessaire d’ l’intégralité du fichier CSS du lecteur dans chaque  de média. Seules les propriétés spécifiques à des périphériques donnés sont redéfinies dans un multimédia.

## Sprites CSS {#section-9b6d8d601cb441d08214dada7bb4eddc}

De nombreux éléments de l’interface utilisateur du lecteur sont mis en forme à l’aide d’illustrations bitmap et présentent plusieurs états visuels distincts. Un bon exemple est un bouton qui a normalement 3 états différents : &quot;up&quot;, &quot;over&quot; et &quot;down&quot;. Chaque état requiert l’attribution de sa propre illustration bitmap.

Avec une approche classique de la mise en forme, le fichier CSS aurait une référence distincte au fichier image individuel sur le serveur pour chaque état de l’élément d’interface utilisateur. Vous trouverez ci-dessous un exemple de page CSS pour la mise en forme du bouton Zoom avant :

```
.s7basiczoomviewer.s7mouseinput .s7zoominbutton[state='up'] {  
background-image:url(images/v2/ZoomInButton_dark_up.png);  
} 
.s7basiczoomviewer.s7mouseinput .s7zoominbutton[state='over'] {  
background-image:url(images/v2/ZoomInButton_dark_over.png);  
} 
.s7basiczoomviewer.s7mouseinput .s7zoominbutton[state='down'] {  
background-image:url(images/v2/ZoomInButton_dark_down.png);  
} 
.s7basiczoomviewer.s7mouseinput .s7zoominbutton[state='disabled'] {  
background-image:url(images/v2/ZoomInButton_dark_disabled.png);  
}
```

L’inconvénient de cette approche est que l’utilisateur final subit un scintillement ou une réponse différée de l’interface utilisateur lors de la première interaction de l’élément. Cette action se produit car l’illustration de l’image pour le nouvel état de l’élément n’est pas encore téléchargée. De plus, cette approche peut avoir un léger impact négatif sur les performances en raison d’une augmentation du nombre d’appels HTTP au serveur.

Les images-objets CSS sont une approche différente, où les illustrations d’image pour tous les états d’élément sont combinées dans un fichier PNG unique appelé &quot;image-objet&quot;. Un tel &quot;sprite&quot; a tous les états visuels pour l’élément donné positionné l’un après l’autre. Lors de la mise en forme d’un élément d’interface utilisateur avec des images-objets, la même image-objet est référencée pour tous les états différents du CSS. En outre, la `background-position` propriété est utilisée pour chaque état pour spécifier la partie de l’image &quot;sprite&quot; utilisée. Vous pouvez structurer une image &quot;sprite&quot; de n’importe quelle manière appropriée. Les lecteurs disposent normalement d’un empilement vertical. Vous trouverez ci-dessous un exemple de style basé sur des &quot;images-objets&quot; du même bouton de zoom avant :

```
.s7basiczoomviewer .s7zoominbutton[state]  { 
    background-image: url(images/v2/ZoomInButton_dark_sprite.png); 
} 
.s7basiczoomviewer.s7mouseinput .s7zoominbutton[state='up'] {  
background-position: -84px -560px;  
} 
.s7basiczoomviewer.s7mouseinput .s7zoominbutton[state='over'] {  
background-position: -56px -560px;  
} 
.s7basiczoomviewer.s7mouseinput .s7zoominbutton[state='down'] {  
background-position: -28px -560px;  
} 
.s7basiczoomviewer.s7mouseinput .s7zoominbutton[state='disabled'] { 
background-position: -0px -560px;  
}
```

## Notes et conseils de mise en forme générale {#section-95855dccbbc444e79970f1aaa3260b7b}

* Lors de la personnalisation de l’interface utilisateur du lecteur avec CSS, l’utilisation de la `!IMPORTANT` règle n’est pas prise en charge pour mettre en forme les éléments du lecteur. En particulier, `!IMPORTANT` la règle ne doit pas être utilisée pour remplacer le style par défaut ou d’exécution fourni par le lecteur ou le kit de développement de visionneuse. La raison en est qu&#39;elle peut affecter le comportement des composants appropriés. Utilisez plutôt des sélecteurs CSS avec la spécificité appropriée pour définir les propriétés CSS documentées dans ce guide de référence.
* Tous les chemins d’accès aux ressources externes dans CSS sont résolus par rapport à l’emplacement CSS et non par rapport à l’emplacement de la page HTML de la visionneuse. Tenez compte de cette règle lorsque vous copiez le fichier CSS par défaut vers un autre emplacement. Copiez également les ressources par défaut ou mettez à jour les chemins d’accès dans le fichier CSS personnalisé.
* Le format préféré pour les illustrations bitmap est le format PNG.
* Les illustrations bitmap sont affectées aux éléments de l’interface utilisateur à l’aide de la `background-image` propriété.
* Les propriétés `width` et `height` les propriétés d’un élément d’interface utilisateur définissent sa taille logique. La taille du bitmap transmis à `background-image` n’affecte pas la taille logique.
* Pour utiliser la haute densité de pixels des écrans haute résolution comme Retina, spécifiez une illustration bitmap deux fois plus grande que la taille d’élément logique de l’interface utilisateur. Ensuite, appliquez la `-webkit-background-size:contain` propriété pour réduire l’arrière-plan à la taille de l’élément logique de l’interface utilisateur.
* Pour supprimer un bouton de l’interface utilisateur, ajoutez `display:none` à sa classe CSS.
* Vous pouvez utiliser divers formats pour la valeur de couleur prise en charge par CSS. Si vous avez besoin de transparence, utilisez le format `rgba(R,G,B,A)`. Sinon, vous pouvez utiliser le format `#RRGGBB`.

## Éléments communs de l’interface utilisateur {#section-d6330c9be8c444aa9b2a07886e3dbc2a}

Voici la documentation de référence sur les éléments de l’interface utilisateur qui s’applique à la visionneuse de zoom de base :
