---
description: Avant d’utiliser Dynamic Media Image Serving, assurez-vous que votre système est conforme à la configuration requise.
solution: Experience Manager
title: Configuration requise et configuration requise
feature: Dynamic Media Classic,SDK/API
role: Developer,Business Practitioner
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '405'
ht-degree: 0%

---


# Configuration système requise et configuration requise{#system-requirements-and-prerequisites}

Avant d’utiliser Dynamic Media Image Serving, assurez-vous que votre système est conforme à la configuration requise.

## Matériel serveur {#section-f3c14a7bc1b745118602659628df779f}

Votre serveur doit répondre aux exigences matérielles suivantes.

>[!NOTE]
>
>Les systèmes dotés de processeurs AMD64 et Intel® EM64T sont généralement configurés en tant que plates-formes NUMA (Non-Uniform Memory Architecture). Cela signifie que le noyau construit plusieurs noeuds de mémoire au démarrage plutôt que de construire un seul noeud de mémoire. La construction de plusieurs noeuds peut entraîner une épuisement de la mémoire sur un ou plusieurs noeuds avant que les autres noeuds ne s’épuisent. Lorsque la mémoire est épuisée, le noyau peut décider de tuer les processus (par exemple, Image Server ou Platform Server) même s&#39;il y a de la mémoire disponible. Par conséquent, Adobe Systems recommande que si vous exécutez un tel système, vous éteigniez NUMA. Utilisez l&#39;option de début `numa=off` pour éviter que le noyau arrête ces processus.

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

**Remarque (Linux) :** Image Serving ne fonctionne pas avec SELinux activé. Cette option est activée par défaut. Pour désactiver SELinux, modifiez le fichier [!DNL /etc/selinux/config] et modifiez la valeur SELinux de :

`SELINUX=enforcing`

en

`SELINUX=disabled`

**Remarque (Linux) :** assurez-vous que le nom d’hôte du serveur peut être résolu sur une adresse IP. Si cela n’est pas possible, ajoutez le nom d’hôte complet et l’adresse IP à [!DNL /etc/hosts] comme dans l’exemple suivant.

`<ip address> <fully qualified hostname>`

## Logiciel serveur {#section-5c9aad2e6b8a4bca989e17a2c8476fc4}

Dynamic Media Image Serving nécessite le logiciel serveur suivant.

**Windows**

* Microsoft® Windows Server 2008.
* Système d’exploitation 64 bits.

**Linux**

* Red Hat® Enterprise 5 ou CentOS 5.5 et versions ultérieures, avec les derniers correctifs.
* Système d’exploitation 64 bits.

**Remarque :** Pour utiliser Image Serving sous Windows, vous devez installer le fichier redistribuable Microsoft Visual Studio 2010. La redistribuable est disponible à l’emplacement suivant :

[http://www.microsoft.com/en-us/download/details.aspx?id=13523](http://www.microsoft.com/en-us/download/details.aspx?id=13523)

