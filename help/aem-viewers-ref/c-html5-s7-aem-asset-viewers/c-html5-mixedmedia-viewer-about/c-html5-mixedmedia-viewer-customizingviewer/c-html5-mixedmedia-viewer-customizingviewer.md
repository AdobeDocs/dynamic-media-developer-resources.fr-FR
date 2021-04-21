---
description: La personnalisation visuelle et la personnalisation comportementale la plus importante pour la visionneuse de supports variés s’effectuent en créant une page CSS personnalisée.
keywords: réactif
solution: Experience Manager
title: Personnalisation de la visionneuse de supports variés
feature: Dynamic Media Classic,Viewers,SDK/API,Mix Media Sets
role: Developer,Business Practitioner
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '1340'
ht-degree: 0%

---


# Personnalisation de la visionneuse de supports variés {#customizing-mixed-media-viewer}

La personnalisation visuelle et la personnalisation comportementale la plus importante pour la visionneuse de supports variés s’effectuent en créant une page CSS personnalisée.

Le processus suggéré consiste à extraire le fichier CSS par défaut pour la visionneuse appropriée, à le copier vers un autre emplacement, à le personnaliser et à spécifier l’emplacement du fichier personnalisé dans la commande `style=`.

Les fichiers CSS par défaut se trouvent à l’emplacement suivant :

`<s7_viewers_root>/html5/MixedMediaViewer_light.css`

Le lecteur est fourni avec deux fichiers CSS prêts à l’emploi, pour les modèles de couleurs &quot;clair&quot; et &quot;foncé&quot;. La version &quot;light&quot; est utilisée par défaut, mais vous pouvez passer à la version &quot;dark&quot; en utilisant la page CSS standard suivante :

`<s7_viewers_root>/html5/MixedMediaViewer_dark.css`

Le fichier CSS personnalisé doit contenir les mêmes déclarations de classe que celles par défaut. Si une déclaration de classe est omise, le lecteur ne fonctionne pas correctement car il ne fournit pas de styles par défaut intégrés pour les éléments de l’interface utilisateur.

Une autre façon de fournir des règles CSS personnalisées consiste à utiliser des styles incorporés directement sur la page Web ou dans l’une des règles CSS externes liées.

Lors de la création d’une page CSS personnalisée, gardez à l’esprit que le lecteur affecte une classe `.s7mixedmediaviewer` à son élément DOM conteneur. Si vous utilisez un fichier CSS externe transmis avec la commande `style=`, utilisez la classe `.s7mixedmediaviewer` en tant que classe parent dans le sélecteur descendant pour vos règles CSS. Si vous faites des styles incorporés sur la page Web, qualifiez en outre ce sélecteur avec l’identifiant de l’élément DOM du conteneur comme suit :

`#<containerId>.s7mixedmediaviewer`

## Création d&#39;une page CSS adaptée {#section-0bb49aca42d242d9b01879d5ba59d33b}

Il est possible de cible de différents périphériques et d’incorporer des tailles dans CSS pour que votre contenu s’affiche différemment, en fonction du périphérique d’un utilisateur ou d’une mise en page Web particulière. Cela comprend, entre autres, différentes mises en page de page Web, différentes tailles d’éléments de l’interface utilisateur et une résolution d’illustration.

Le lecteur de contenu prend en charge deux méthodes de création de pages CSS adaptées : Marqueurs CSS et requêtes multimédias CSS standard. Vous pouvez utiliser ces méthodes séparément ou ensemble.

**Marqueurs CSS**

Pour faciliter la création d’un fichier CSS adapté, le lecteur prend en charge les marqueurs CSS qui sont des classes CSS spéciales dynamiquement attribuées à l’élément de conteneur du lecteur de niveau supérieur en fonction de la taille du lecteur d’exécution et du type d’entrée utilisé sur le périphérique actuel.

Le premier groupe de marqueurs CSS comprend les classes `.s7size_large`, `.s7size_medium` et `.s7size_small`. Elles sont appliquées en fonction de la zone d’exécution du conteneur du lecteur de contenu. En d’autres termes, si la zone de visualisation est égale ou supérieure à la taille d’un moniteur de bureau commun `.s7size_large` est utilisée ; si la zone est proche de la taille d&#39;une tablette commune `.s7size_medium` est affectée. Pour les zones similaires aux écrans de téléphone mobile `.s7size_small` est défini. L’objectif Principal de ces marqueurs CSS est de créer différentes mises en page d’interface utilisateur pour différents écrans et tailles de visionneuse.

Le deuxième groupe de marqueurs CSS comprend `.s7mouseinput` et `.s7touchinput`. `.s7touchinput` est défini si le périphérique actuel possède des capacités d&#39;entrée tactile ; sinon,  `.s7mouseinput` est utilisé. Ces marqueurs sont destinés à créer des éléments d’entrée de l’interface utilisateur avec des tailles d’écran différentes pour différents types d’entrée, car en règle générale, la saisie tactile nécessite des éléments plus volumineux. Si le périphérique dispose à la fois de fonctions d’entrée de souris et de tactile, `.s7touchinput` est défini et le lecteur effectue le rendu d’une interface utilisateur tactile.

L’exemple de page CSS suivant définit la taille du bouton de zoom sur 28 x 28 pixels sur les systèmes avec saisie de la souris et 56 x 56 pixels sur les périphériques tactiles. En outre, il masque complètement le bouton si la taille de la visionneuse devient vraiment petite :

```
.s7mixedmediaviewer.s7mouseinput .s7zoominbutton { 
    width:28px; 
    height:28px; 
} 
.s7mixedmediaviewer.s7touchinput .s7zoominbutton { 
    width:56px; 
    height:56px; 
} 
.s7mixedmediaviewer.s7size_small .s7zoominbutton { 
    visibility:hidden; 
}
```

Pour cible des périphériques avec une densité de pixels différente, utilisez des requêtes multimédias CSS. Le bloc de requête de média suivant contient des fichiers CSS spécifiques aux écrans haute densité :

```
@media screen and (-webkit-min-device-pixel-ratio: 1.5) 
{ 
}
```

L’utilisation de marqueurs CSS est la méthode la plus souple de création de pages CSS adaptées, car elle vous permet de cible non seulement la taille de l’écran du périphérique, mais également la taille réelle de la visionneuse, ce qui peut s’avérer utile pour les mises en page adaptées.

Utilisez le fichier CSS de visionneuse par défaut comme exemple d’approche des marqueurs CSS.

**REQUÊTES de médias CSS**

La détection de périphérique peut également être effectuée à l’aide de requêtes multimédias CSS pures. Tout ce qui est inclus dans un bloc de requête de média donné est appliqué uniquement s&#39;il est exécuté sur un périphérique correspondant.

Lorsqu’elle est appliquée aux visionneuses mobiles, utilisez quatre requêtes multimédias CSS, définies dans votre page CSS dans l’ordre suivant :

1. Contient uniquement des règles spécifiques à tous les périphériques tactiles.

   ```
   @media only screen and (max-device-width:13.5in) and (max-device- 
   height:13.5in) and (max-device-width:799px),  
   only screen and (max-device-width:13.5in) and (max-device-height:13.5in)  
   and (max-device-height:799px) 
   { 
   }
   ```

1. Contient uniquement des règles spécifiques aux tablettes avec écrans haute résolution.

   ```
   @media only screen and (max-device-width:13.5in) and (max-device-height:13.5in) and (max-device-width:799px) and (-webkit-min-device-pixel-ratio:1.5), 
   only screen and (max-device-width:13.5in) and (max-device-height:13.5in) and (max-device-height:799px) and (-webkit-min-device-pixel-ratio:1.5)  
   { 
   }
   ```

1. Contient uniquement des règles spécifiques à tous les téléphones portables.

   ```
   @media only screen and (max-device-width:9in) and (max-device-height:9in) 
   { 
   }
   ```

1. Contient uniquement des règles spécifiques aux téléphones portables dotés d’écrans haute résolution.

   ```
   @media only screen and (max-device-width:9in) and (max-device-height:9in) and (-webkit-min-device-pixel-ratio: 1.5), 
     only screen and (device-width:720px) and (device-height:1280px) and (-webkit-device-pixel-ratio: 2), 
     only screen and (device-width:1280px) and (device-height:720px) and (-webkit-device-pixel-ratio: 2) 
   { 
   }
   ```

En utilisant une approche de requêtes multimédia, vous devez organiser les pages CSS avec la détection de périphérique comme suit :

* Tout d’abord, la section spécifique à l’ordinateur de bureau définit toutes les propriétés spécifiques à l’ordinateur de bureau ou communes à tous les écrans.
* Ensuite, les quatre requêtes de médias suivent l’ordre défini ci-dessus et fournissent des règles CSS spécifiques au type de périphérique correspondant.

Il n’est pas nécessaire de duplicata de l’intégralité du fichier CSS du lecteur de contenu dans chaque requête multimédia. Seules les propriétés spécifiques à des périphériques donnés sont redéfinies dans une requête multimédia.

## CSS Sprites {#section-209a43dfbddf4fc589e79cddaf233f50}

De nombreux éléments de l’interface utilisateur de la visionneuse sont mis en forme à l’aide d’illustrations bitmap et présentent plusieurs états visuels distincts. Un bon exemple est un bouton qui a normalement au moins trois états différents : &quot;up&quot;, &quot;over&quot; et &quot;down&quot;. Chaque état requiert l’attribution de sa propre illustration bitmap.

Avec une approche classique de la mise en forme, le fichier CSS aurait une référence distincte au fichier image individuel sur le serveur pour chaque état de l’élément d’interface utilisateur. Voici un exemple de page CSS pour la mise en forme d’un bouton de zoom avant :

```
.s7mixedmediaviewer.s7mouseinput .s7zoominbutton[state='up'] {  
background-image:url(images/v2/ZoomInButton_dark_up.png);  
} 
.s7mixedmediaviewer.s7mouseinput .s7zoominbutton[state='over'] {  
background-image:url(images/v2/ZoomInButton_dark_over.png);  
} 
.s7mixedmediaviewer.s7mouseinput .s7zoominbutton[state='down'] {  
background-image:url(images/v2/ZoomInButton_dark_down.png);  
} 
.s7mixedmediaviewer.s7mouseinput .s7zoominbutton[state='disabled'] {  
background-image:url(images/v2/ZoomInButton_dark_disabled.png);  
}
```

L’inconvénient de cette approche est que l’utilisateur final subit un scintillement ou une réponse différée de l’interface utilisateur lorsque l’élément est interagi pour la première fois. Cette action se produit car l’illustration de l’image pour le nouvel état d’élément n’est pas encore téléchargée. En outre, cette approche peut avoir un léger impact négatif sur les performances en raison d’une augmentation du nombre d’appels HTTP au serveur.

Les sprites CSS sont une approche différente selon laquelle les illustrations d’image pour tous les états d’élément sont combinées dans un fichier PNG unique appelé &quot;sprite&quot;. Un tel &quot;sprite&quot; a tous les états visuels pour l’élément donné positionné l’un après l’autre. Lors de la mise en forme d’un élément d’interface utilisateur avec des images-objets, la même image-objet est référencée pour tous les états différents du CSS. En outre, la propriété `background-position` est utilisée pour chaque état pour spécifier la partie de l’image &quot;sprite&quot; utilisée. Vous pouvez structurer une image &quot;sprite&quot; de n’importe quelle manière appropriée. Normalement, les visionneuses sont empilées verticalement. Vous trouverez ci-dessous un exemple de mise en forme du même bouton de zoom avant basé sur une &quot;image-objet&quot; :

```
.s7mixedmediaviewer .s7zoominbutton[state]  { 
    background-image: url(images/v2/ZoomInButton_dark_sprite.png); 
} 
.s7mixedmediaviewer.s7mouseinput .s7zoominbutton[state='up'] {  
background-position: -84px -560px;  
} 
.s7mixedmediaviewer.s7mouseinput .s7zoominbutton[state='over'] {  
background-position: -56px -560px;  
} 
.s7mixedmediaviewer.s7mouseinput .s7zoominbutton[state='down'] {  
background-position: -28px -560px;  
} 
.s7mixedmediaviewer.s7mouseinput .s7zoominbutton[state='disabled'] { 
background-position: -0px -560px;  
}
```

## Notes et conseils généraux sur le style {#section-95855dccbbc444e79970f1aaa3260b7b}

* Tous les chemins d’accès aux ressources externes dans CSS sont résolus par rapport à l’emplacement CSS, et non par rapport à l’emplacement de la page HTML de la visionneuse. Soyez conscient de cette règle lorsque vous copiez le fichier CSS par défaut vers un autre emplacement. Copiez également les ressources par défaut ou mettez à jour les chemins d’accès dans le fichier CSS personnalisé.
* Le format d’illustration bitmap préféré est le format PNG.
* L’illustration bitmap est affectée aux éléments de l’interface utilisateur à l’aide de la propriété `background-image`.
* Les propriétés `width` et `height` d&#39;un élément d&#39;interface utilisateur définissent sa taille logique. La taille du bitmap transmis à `background-image` n’affecte pas la taille logique.

* Pour utiliser la haute densité de pixels des écrans haute résolution comme Retina, spécifiez une illustration bitmap deux fois plus grande que la taille de l’élément d’interface utilisateur logique. Ensuite, appliquez la propriété `-webkit-background-size:contain` pour mettre à l’échelle l’arrière-plan en fonction de la taille de l’élément logique de l’interface utilisateur.
* Pour supprimer un bouton de l’interface utilisateur, ajoutez `display:none` à sa classe CSS.
* Vous pouvez utiliser divers formats pour la valeur de couleur prise en charge par CSS. Si vous avez besoin de transparence, utilisez le format `rgba(R,G,B,A)`. Sinon, vous pouvez utiliser le format `#RRGGBB`.

* Lors de la personnalisation de l’interface utilisateur du lecteur avec CSS, l’utilisation de la règle `!IMPORTANT` n’est pas prise en charge pour mettre en forme les éléments de la visionneuse. En particulier, la règle `!IMPORTANT` ne doit pas être utilisée pour remplacer le style par défaut ou d’exécution fourni par le lecteur ou le SDK du lecteur de contenu. La raison en est qu&#39;elle peut affecter le comportement des composants appropriés. Vous devez plutôt utiliser des sélecteurs CSS avec la spécificité appropriée pour définir les propriétés CSS documentées dans ce guide de référence.

## Éléments communs de l&#39;interface utilisateur {#section-d6330c9be8c444aa9b2a07886e3dbc2a}

Voici la documentation de référence sur les éléments de l’interface utilisateur qui s’applique à la visionneuse de supports variés :
