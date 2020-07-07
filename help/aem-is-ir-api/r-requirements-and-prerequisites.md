---
description: Avant d’utiliser Scene7 Image Serving, assurez-vous que votre système est conforme à la configuration requise.
seo-description: Avant d’utiliser Scene7 Image Serving, assurez-vous que votre système est conforme à la configuration requise.
seo-title: Configuration requise et configuration requise
solution: Experience Manager
title: Configuration requise et configuration requise
topic: Scene7 Image Serving - Image Rendering API
uuid: 80196574-f5a2-4298-880a-cc36f90b6e21
translation-type: tm+mt
source-git-commit: e8e5b07329bde3e23ee095d5022da62d67e9478c
workflow-type: tm+mt
source-wordcount: '411'
ht-degree: 0%

---


# Configuration requise et configuration requise{#system-requirements-and-prerequisites}

Avant d’utiliser Scene7 Image Serving, assurez-vous que votre système est conforme à la configuration requise.

## Matériel serveur {#section-f3c14a7bc1b745118602659628df779f}

Votre serveur doit répondre aux exigences matérielles suivantes.

>[!NOTE]
>
>Les systèmes dotés de processeurs AMD64 et Intel® EM64T sont généralement configurés en tant que plates-formes NUMA (Non-Uniform Memory Architecture). Cela signifie que le noyau construit plusieurs noeuds de mémoire au démarrage plutôt que de construire un seul noeud de mémoire. La construction de plusieurs noeuds peut entraîner une épuisement de la mémoire sur un ou plusieurs noeuds avant que les autres noeuds ne s’épuisent. Lorsque la mémoire est épuisée, le noyau peut décider de tuer les processus (par exemple, Image Server ou Platform Server) même s&#39;il y a de la mémoire disponible. Par conséquent, Adobe Systems recommande que si vous exécutez un tel système, vous éteigniez NUMA. Utilisez l&#39;option `numa=off` début pour éviter que le noyau ne bloque ces processus.

**Windows**

* Processeur Intel Xeon® ou AMD® Opteron avec au moins 4 coeurs.
* 16 Go de RAM minimum.
* Permuter l’espace au moins deux fois la quantité de mémoire physique (RAM).
* 2 Go d’espace disque disponible pour l’installation et le fonctionnement de base, de l’espace disque supplémentaire est nécessaire pour les images source, les journaux, les caches de données et les fichiers de manifeste.
* Carte d&#39;interface réseau Fast Ethernet.

**Linux**

* Processeur Intel Xeon® ou AMD® Opteron avec au moins 4 coeurs.
* 16 Go de RAM minimum.
* Permutation désactivée (recommandé).
* 2 Go d’espace disque disponible pour l’installation et le fonctionnement de base, de l’espace disque supplémentaire est nécessaire pour les images source, les journaux, les caches de données et les fichiers de manifeste.
* Carte d&#39;interface réseau Fast Ethernet.

**Remarque (Linux) :** La diffusion d’images ne fonctionne pas avec SELinux activé. Cette option est activée par défaut. Pour désactiver SELinux, modifiez le [!DNL /etc/selinux/config] fichier et modifiez la valeur SELinux de :

`SELINUX=enforcing`

en

`SELINUX=disabled`

**Remarque (Linux) :** Assurez-vous que le nom d’hôte du serveur peut être résolu sur une adresse IP. Si cela n’est pas possible, ajoutez le nom d’hôte complet et l’adresse IP à [!DNL /etc/hosts] la, comme dans l’exemple suivant.

`<ip address> <fully qualified hostname>`

## Logiciel serveur {#section-5c9aad2e6b8a4bca989e17a2c8476fc4}

Scene7 Image Serving requiert le logiciel serveur suivant.

**Windows**

* Microsoft® Windows Server 2008.
* Système d’exploitation 64 bits.

**Linux**

* Red Hat® Enterprise 5 ou CentOS 5.5 et versions ultérieures, avec les derniers correctifs.
* Système d’exploitation 64 bits.

**Remarque :** Pour utiliser Image Serving sous Windows, vous devez installer le fichier redistribuable Microsoft Visual Studio 2010. La redistribuable est disponible à l’emplacement suivant :

[http://www.microsoft.com/en-us/download/details.aspx?id=13523](http://www.microsoft.com/en-us/download/details.aspx?id=13523)

