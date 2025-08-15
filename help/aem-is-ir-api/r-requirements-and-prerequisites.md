---
title: Configuration requise et conditions préalables
description: Avant d’utiliser Dynamic Media serveur d’images, assurez-vous que votre système répond à la configuration système requise.
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

Avant d’utiliser Dynamic Media serveur d’images, assurez-vous que votre système répond à la configuration système requise.

## Matériel du serveur {#section-f3c14a7bc1b745118602659628df779f}

Votre serveur doit répondre à la configuration matérielle requise suivante.

>[!NOTE]
>
>Les systèmes équipés de processeurs AMD64 et Intel® EM64T sont généralement configurés en tant que plates-formes NUMA (Non-Uniform Memory Architecture). Cela signifie que le noyau construit plusieurs nœuds de mémoire au démarrage plutôt que de construire un seul nœud de mémoire. La construction à plusieurs nœuds peut entraîner l’épuisement de la mémoire sur un ou plusieurs nœuds avant que les autres nœuds ne soient épuisés. Lorsque l’épuisement de la mémoire se produit, le noyau peut décider de tuer les processus (par exemple, le serveur d’images ou [!DNL Platform Server]) même s’il y a de la mémoire disponible. Par conséquent, Adobe recommande de désactiver NUMA si vous exécutez un tel système. Utilisez l’option de `numa=off` démarrage pour éviter que le noyau n’arrête ces processus.

**Windows**

* Processeur Intel Xeon® ou AMD® Opteron avec au moins quatre cœurs.
* 1 Go de mémoire vive (RAM) au minimum.
* L’espace d’échange est égal à au moins deux fois la quantité de mémoire physique (RAM).
* 2 Go d’espace disque disponible pour l’installation et l’opération de base, un espace disque supplémentaire est requis pour les images sources, les journaux, les caches de données et les fichiers manifeste.
* Carte d’interface réseau Fast Ethernet.

**Linux®**

* Processeur Intel Xeon® ou AMD® Opteron avec au moins quatre cœurs.
* 16 Go de mémoire vive (RAM) au minimum.
* Échange désactivé (recommandé).
* 2 Go d’espace disque disponible pour l’installation et l’opération de base, un espace disque supplémentaire est requis pour les images sources, les journaux, les caches de données et les fichiers manifeste.
* Carte d’interface réseau Fast Ethernet.

**Remarque (Linux®) :** la diffusion d’images ne fonctionne pas lorsque SELinux est activé. Cette option est activée par défaut. Pour désactiver SELinux, modifiez le [!DNL /etc/selinux/config] fichier et modifiez la valeur SELinux depuis :

`SELINUX=enforcing`

À

`SELINUX=disabled`

**Remarque (Linux®) :** Assurez-vous que le nom d’hôte du serveur peut être résolu en adresse IP. Si cela n’est pas possible, ajoutez le nom d’hôte complet et l’adresse IP comme dans l’exemple [!DNL /etc/hosts] suivant.

`<ip address> <fully qualified hostname>`

## Logiciel serveur {#section-5c9aad2e6b8a4bca989e17a2c8476fc4}

Dynamic Media diffusion d’images nécessite le logiciel serveur suivant.

**Windows**

* Microsoft® Windows Server 2008.
* Système d’exploitation 64 bits.

**Linux®**

* Red Hat® Enterprise 5 ou CentOS 5.5 et versions ultérieures, avec les derniers correctifs.
* Système d’exploitation 64 bits.

**Remarque :** pour utiliser la diffusion d’images sous Windows, vous devez installer Microsoft® Visual Studio 2010.
