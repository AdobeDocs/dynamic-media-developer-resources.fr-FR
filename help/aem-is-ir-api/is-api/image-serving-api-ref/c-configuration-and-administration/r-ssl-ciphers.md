---
description: La balise Connector du fichier server.xml prend en charge un attribut de chiffrement afin de limiter les chiffrement pouvant être sélectionnés pour une connexion SSL.
solution: Experience Manager
title: Définition de chiffrement SSL
feature: Dynamic Media Classic,SDK/API
role: Developer,Administrator,Business Practitioner
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '123'
ht-degree: 0%

---


# Définition de chiffrement SSL{#defining-ssl-ciphers}

La balise Connector du fichier server.xml prend en charge un attribut de chiffrement afin de limiter les chiffrement pouvant être sélectionnés pour une connexion SSL.

Par défaut, tous les chiffrement sont disponibles. La liste est séparée par des virgules et peut contenir l’une des valeurs suivantes :

`SSL_DHE_DSS_EXPORT_WITH_DES40_CBC_SHA`

`SSL_DHE_DSS_WITH_3DES_EDE_CBC_SHA`

`SSL_DHE_DSS_WITH_DES_CBC_SHA`

`SSL_DHE_RSA_EXPORT_WITH_DES40_CBC_SHA`

`SSL_DHE_RSA_WITH_3DES_EDE_CBC_SHA`

`SSL_DHE_RSA_WITH_DES_CBC_SHA`

`SSL_RSA_EXPORT_WITH_DES40_CBC_SHA`

`SSL_RSA_EXPORT_WITH_RC4_40_MD5`

`SSL_RSA_WITH_3DES_EDE_CBC_SHA`

`SSL_RSA_WITH_DES_CBC_SHA`

`SSL_RSA_WITH_RC4_128_MD5`

`SSL_RSA_WITH_RC4_128_SHA`

`TLS_DHE_DSS_WITH_AES_128_CBC_SHA`

`TLS_DHE_RSA_WITH_AES_128_CBC_SHA`

`TLS_RSA_WITH_AES_128_CBC_SHA`

Si l&#39;une des valeurs est incorrecte, Tomcat activera chaque chiffre. Il est donc essentiel de vérifier avec un outil externe après la configuration pour savoir quels chiffriers sont réellement activés.

A titre d’exemple, la configuration suivante n’activera que les suites de chiffrement &quot;128 bits&quot; et plus :

`ciphers="SSL_DHE_DSS_WITH_3DES_EDE_CBC_SHA,SSL_DHE_DSS_WITH_DES_CBC_SHA,SSL_DHE_RSA_WITH_3DES_EDE_CBC_SHA,SSL_RSA_WITH_3DES_EDE_CBC_SHA,TLS_DHE_DSS_WITH_AES_128_CBC_SHA,TLS_DHE_RSA_WITH_AES_128_CBC_SHA,TLS_RSA_WITH_AES_128_CBC_SHA"`
