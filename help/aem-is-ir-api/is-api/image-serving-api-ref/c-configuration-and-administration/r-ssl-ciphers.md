---
description: La balise Connector du fichier server.xml prend en charge un attribut ciphers afin de limiter le choix des chiffrement pour une connexion SSL.
seo-description: La balise Connector du fichier server.xml prend en charge un attribut ciphers afin de limiter le choix des chiffrement pour une connexion SSL.
seo-title: Définition des chiffrement SSL
solution: Experience Manager
title: Définition des chiffrement SSL
topic: Scene7 Image Serving - Image Rendering API
uuid: 9490fb9a-5abb-4f5e-b660-b7af0a5e4b4d
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# Définition des chiffrement SSL{#defining-ssl-ciphers}

La balise Connector du fichier server.xml prend en charge un attribut ciphers afin de limiter le choix des chiffrement pour une connexion SSL.

Par défaut, tous les algorithmes de chiffrement sont disponibles. Le est séparé par des virgules et peut contenir l’une des valeurs suivantes :

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

Si l’une des valeurs est erronée, Tomcat activera chaque chiffre. Il est donc essentiel de vérifier avec un outil externe après la configuration pour voir quels chiffriers sont réellement activés.

Par exemple, la configuration suivante n’activera que les suites de chiffrement &quot;128 bits&quot; et ultérieures :

`ciphers="SSL_DHE_DSS_WITH_3DES_EDE_CBC_SHA,SSL_DHE_DSS_WITH_DES_CBC_SHA,SSL_DHE_RSA_WITH_3DES_EDE_CBC_SHA,SSL_RSA_WITH_3DES_EDE_CBC_SHA,TLS_DHE_DSS_WITH_AES_128_CBC_SHA,TLS_DHE_RSA_WITH_AES_128_CBC_SHA,TLS_RSA_WITH_AES_128_CBC_SHA"`
