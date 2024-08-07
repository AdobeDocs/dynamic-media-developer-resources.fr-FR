---
title: Configuration requise et conditions préalables
description: Avant d’utiliser Dynamic Media Image Serving, assurez-vous que votre système est conforme à la configuration requise.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: ea2dfec9-0a42-4ccb-8442-6f7c4a39eda1
source-git-commit: 163ac6a6f44193f1b66ae24059630521d7247eae
workflow-type: tm+mt
source-wordcount: '382'
ht-degree: 0%

---

# Configuration requise et conditions préalables{#system-requirements-and-prerequisites}

Avant d’utiliser Dynamic Media Image Serving, assurez-vous que votre système est conforme à la configuration requise.

## Matériel du serveur {#section-f3c14a7bc1b745118602659628df779f}

Votre serveur doit répondre aux exigences matérielles suivantes.

>[!NOTE]
>
>Les systèmes avec processeurs AMD64 et Intel® EM64T sont généralement configurés en tant que plateformes NUMA (Non Uniform Memory Architecture). Cela signifie que le noyau construit plusieurs noeuds de mémoire au moment du démarrage plutôt que de construire un seul noeud de mémoire. La construction de plusieurs noeuds peut entraîner un épuisement de la mémoire sur un ou plusieurs noeuds avant que d’autres noeuds ne s’épuisent. Lorsque l’épuisement de la mémoire se produit, le noyau peut décider d’interrompre les processus (par exemple, le serveur d’images ou [!DNL Platform Server]) même si de la mémoire est disponible. Par conséquent, Adobe recommande de désactiver NUMA si vous exécutez un tel système. Utilisez l’option de démarrage `numa=off` pour éviter que le noyau arrête ces processus.

**Windows**

* Processeur Intel Xeon® ou AMD® Opteron avec au moins quatre coeurs.
* 1 Go de RAM au minimum.
* L’espace de permutation est égal à au moins deux fois la quantité de mémoire physique (RAM).
* 2 Go d’espace disque disponible pour l’installation et le fonctionnement de base ; un espace disque supplémentaire est nécessaire pour les images sources, les journaux, les caches de données et les fichiers de manifeste.
* Carte d’interface réseau Ethernet rapide.

**Linux®**

* Processeur Intel Xeon® ou AMD® Opteron avec au moins quatre coeurs.
* 16 Go de RAM au minimum.
* Permutation désactivée (recommandé).
* 2 Go d’espace disque disponible pour l’installation et le fonctionnement de base ; un espace disque supplémentaire est nécessaire pour les images sources, les journaux, les caches de données et les fichiers de manifeste.
* Carte d’interface réseau Ethernet rapide.

**Remarque (Linux®) :** La diffusion d’images ne fonctionne pas avec SELinux activé. Cette option est activée par défaut. Pour désactiver SELinux, modifiez le fichier [!DNL /etc/selinux/config] et modifiez la valeur SELinux de :

`SELINUX=enforcing`

À

`SELINUX=disabled`

**Remarque (Linux®) :** Assurez-vous que le nom d’hôte du serveur peut être résolu sur une adresse IP. Si cela n’est pas possible, ajoutez le nom d’hôte complet et l’adresse IP à [!DNL /etc/hosts] comme dans l’exemple suivant.

`<ip address> <fully qualified hostname>`

## Logiciels du serveur {#section-5c9aad2e6b8a4bca989e17a2c8476fc4}

La diffusion d’images Dynamic Media requiert le logiciel serveur suivant.

**Windows**

* Microsoft® Windows Server 2008.
* Système d’exploitation 64 bits.

**Linux®**

* Red Hat® Enterprise 5 ou CentOS 5.5 et versions ultérieures, avec les derniers correctifs.
* Système d’exploitation 64 bits.

**Remarque :** Pour utiliser le service d’images sous Windows, vous devez installer Microsoft® Visual Studio 2010.
