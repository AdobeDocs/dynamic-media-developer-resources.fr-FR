---
description: Le service Web IPS est pris en charge par un ensemble de WSDL (Web Services Description Language) accessibles à partir de toute installation IPS sur laquelle le composant Service Web IPS est installé. Chaque version de l’API IPS comprend un nouveau fichier WSDL qui référence un avec version  XML  . Les versions précédentes de  WSDL  sont également prises en charge pour permettre une compatibilité descendante avec les applications existantes.
seo-description: Le service Web IPS est pris en charge par un ensemble de WSDL (Web Services Description Language) accessibles à partir de toute installation IPS sur laquelle le composant Service Web IPS est installé. Chaque version de l’API IPS comprend un nouveau fichier WSDL qui référence un avec version  XML  . Les versions précédentes de  WSDL  sont également prises en charge pour permettre une compatibilité descendante avec les applications existantes.
seo-title: Versions WSDL du service Web IPS
solution: Experience Manager
title: Versions WSDL du service Web IPS
topic: Scene7 Image Production System API
uuid: 3443bb91-1663-4686-b20a-94c372f0026e
translation-type: tm+mt
source-git-commit: aa095022d43db4bf815aece9bc2b087c53a64e1b

---


# Versions WSDL du service Web IPS{#ips-web-service-wsdl-versions}

Le service Web IPS est pris en charge par un ensemble de WSDL (Web Services Description Language) accessibles à partir de toute installation IPS sur laquelle le composant Service Web IPS est installé. Chaque version de l’API IPS comprend un nouveau fichier WSDL qui référence un avec version  XML  . Les versions précédentes de  WSDL  sont également prises en charge pour permettre une compatibilité descendante avec les applications existantes.

## Accès WSDL {#section-62e69fa2c87f4dc9bca72f10ba028f6c}

Accédez aux fichiers WSDL Scene7 comme illustré ci-dessous.

```
https://<IPS_hostname:<IPS_port>/<IPS_webapp>/ 
webservice/IpsApi[-<API_version>].wsdl 
```

La valeur par défaut de `<IPS_webapp>` est `scene7`.

**Emplacement du service**

L&#39;URL du service est spécifiée dans la section de service du WSDL du service Web IPS. L’URL du service se présente généralement sous la forme suivante :

```
https://<IPS_hostname>:<IPS_port>/<IPS_webapp>/ 
services/IpsApiService 
```

**Accès aux URL pour les régions Scene7**

<table id="table_45BB314ABCDA49F38DF7BECF95CC984A"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>Emplacement géographique </p> </th> 
   <th colname="col2" class="entry"> <p>URL de production </p> </th> 
   <th colname="col3" class="entry"> <p>URL d’évaluation (à utiliser pour le développement et le test de pré-production) </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>Amérique du Nord </p> </td> 
   <td colname="col2"> <p> https://s7sps1apissl.scene7.com/scene7/ </p> </td> 
   <td colname="col3"> <p> https://s7sps1apissl-staging.scene7.com/scene7/ </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Europe, Moyen-Orient, Asie </p> </td> 
   <td colname="col2"> <p> https://s7sps3apissl.scene7.com/scene7/ </p> </td> 
   <td colname="col3"> <p> https://s7sps3apissl-staging.scene7.com/scene7/ </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Japon/Asie-Pacifique </p> </td> 
   <td colname="col2"> <p> https://s7sps5apissl.scene7.com/scene7/ </p> </td> 
   <td colname="col3"> <p> https://s7sps5apissl-staging.scene7.com/scene7/ </p> </td> 
  </tr> 
 </tbody> 
</table>

## WSDL pris en charge {#section-ebbba69880f94e9c823f1147974eb404}

N&#39;oubliez pas que vous devrez peut-être modifier votre code si vous souhaitez utiliser les fonctionnalités de la dernière version de l&#39;API IPS. L’API IPS prend en charge les fichiers WSDL pour les versions suivantes :

<table id="table_6FABCC4E7786448CB56C343E3C0B36CA"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>Version de la version API </p> </th> 
   <th colname="col2" class="entry"> <p>WSDL </p> </th> 
   <th colname="col3" class="entry"> <p> API  </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>6.8/2014R1 </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> IpsApi-2014-04-03.wsdl </span> </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> http://www.scene7.com/IpsApi/xsd/2014-04-03 </span> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>6.6/2013R1 </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> IpsApi-2013-02-15.wsdl </span> </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> http://www.scene7.com/IpsApi/xsd/2013-02-15 </span> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>6.0/2012R1 </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> IpsApi-2012-02-14.wsdl </span> </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> http://www.scene7.com/IpsApi/xsd/2012-02-14 </span> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>4.5 </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> IpsApi-2010-01-31.wsdl </span> </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> http://www.scene7.com/IpsApi/xsd/2010-01-31 </span> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>4.4 </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> IpsApi-2009-07-31.wsdl </span> </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> http://www.scene7.com/IpsApi/xsd/2009-07-31 </span> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>4.2 </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> IpsApi-2008-09-10.wsdl </span> </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> http://www.scene7.com/IpsApi/xsd/2008-09-10 </span> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>4.0 </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> IpsApi-2008-01-15.wsdl </span> </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> http://www.scene7.com/IpsApi/xsd/2008-01-15 </span> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Pre-4.0 </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> IpsApi.wsdl </span> </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> http://www.scene7.com/IpsApi/xsd </span> </p> </td> 
  </tr> 
 </tbody> 
</table>

Les applications existantes qui doivent être modifiées pour utiliser de nouvelles fonctionnalités doivent effectuer la mise à niveau vers la dernière version de l’API et modifier le code existant. Consultez le journal des modifications pour en savoir plus.

## SOAP {#section-51e7ecbd1d7f451b9e4f6bf7e1579cae}

**Liaisons**

Le service Web API IPS prend uniquement en charge une liaison SOAP.

**Transports pris en charge**

La liaison SOAP API IPS prend uniquement en charge le transport HTTP. Effectuez toutes les requêtes SOAP à l’aide de la méthode HTTPS POST.

**En-tête d’action SOAP**

Pour traiter une requête, définissez l’en-tête HTTP SOAPAction sur le nom de l’opération demandée. L’attribut du nom de l’opération dans la section de liaison WSDL spécifie le nom.

**Format du message**

Le style /littéral est utilisé pour tous les messages d’entrée et de sortie avec des types basés sur le langage de définition de XML ( [http://www.w3.org/TR/xmlschema-0/](http://www.w3.org/TR/xmlschema-0/)) et spécifiés dans le fichier WSDL. Tous les types nécessitent des noms qualifiés à l’aide de la   valeur de  spécifiée dans le fichier WSDL.

**Demande d’authentification**

La méthode recommandée pour transmettre des informations d’identification d’authentification dans les demandes d’API consiste à utiliser l’ `authHeader` élément tel que défini dans le fichier WSDL de l’API IPS.

```
<element name="authHeader"> 
    <complexType> 
       <sequence> 
            <element name="user" type="xsd:string"/> 
            <element name="password" type="xsd:string"/> 
            <element name="locale" type="xsd:string" minOccurs="0"/> 
            <element name="appName" type="xsd:string" minOccurs="0"/> 
            <element name="appVersion" type="xsd:string" minOccurs="0"/> 
            <element name="gzipResponse" type="xsd:boolean" minOccurs="0"/> 
            <element name="faultHttpStatusCode" type="xsd:int" minOccurs="0"/> 
       </sequence> 
    </complexType> 
 </element>
```

**Champs**

<table id="table_B295FEB0EA584C2BA4122FC084AEF18D"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>Nom </p> </th> 
   <th colname="col2" class="entry"> <p>Description </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> utilisateur </span> </p> </td> 
   <td colname="col2"> <p> Adresse électronique utilisateur IPS valide. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> mot de passe </span> </p> </td> 
   <td colname="col2"> <p>Mot de passe du compte utilisateur. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> locale </span> </p> </td> 
   <td colname="col2"> <p> Paramètres régionaux facultatifs pour la requête. See <b>Locale</b> for details. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> appName </span> </p> </td> 
   <td colname="col2"> <p> Appel du nom de l’application. Ce paramètre est facultatif, mais il est recommandé de l’inclure dans toutes les requêtes. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> appVersion </span> </p> </td> 
   <td colname="col2"> <p> Appel de la version de l’application. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> gzipResponse </span> </p> </td> 
   <td colname="col2"> <p> Indicateur facultatif pour activer ou désactiver la compression gzip du code XML de réponse. Par défaut, les réponses sont compressées au format gzip si l’en-tête HTTP Accept-Encoding indique la prise en charge de gzip. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> faulHttpStatusCode </span> </p> </td> 
   <td colname="col2"> <p> Paramètre facultatif permettant de remplacer le code d’état HTTP pour les réponses d’erreur. Par défaut, les réponses d’erreur renvoient le code d’état HTTP 500 (Erreur interne du serveur). Certaines plateformes clientes, notamment Adobe Flash, ne peuvent pas lire le corps de la réponse, sauf si un code d’état de 200 (OK) est renvoyé. </p> </td> 
  </tr> 
 </tbody> 
</table>

L’ `authHeader` élément est toujours défini dans le  du  `http://www.scene7.com/IpsApi/xsd`, quelle que soit la version de l’API.

Voici un exemple d’utilisation de l’ `authHeader` élément dans un en-tête SOAP de requête :

```
<soap:Header xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/"> 
   <authHeader xmlns="http://www.scene7.com/IpsApi/xsd"> 
      <user>user@scene7.com</user> 
      <password>mypassword</password> 
      <appName>MyApp</appName> 
      <appVersion>1.0</appVersion> 
   </authHeader> 
 </soap:Header>
```

**Autres méthodes d’authentification de requête**

Si, pour une raison quelconque, votre application cliente ne peut pas transmettre l’en-tête `authHeader` SOAP, les demandes d’API peuvent également spécifier des informations d’identification à l’aide de l’authentification HTTP de base (comme indiqué dans la RFC 2617).

Pour l’authentification HTTP de base, la section d’en-tête HTTP de chaque requête SOAP POST doit inclure un en-tête du formulaire :

`Authorization: Basic base64(<IPS_user_email>:<password>)`

Lorsque `base64()` applique le codage standard Base64, `<IPS_user_email>` correspond à l&#39;adresse électronique d&#39;un utilisateur IPS valide et `<password>` au mot de passe de l&#39;utilisateur.

Envoyez l’en-tête Autorisation de manière préventive avec la requête initiale. Si aucune information d’identification d’authentification n’est incluse dans la requête, `IpsApiService` ne répond pas avec un code d’état de `401 (Unauthorized)`. Au lieu de cela, un code d’état de `500 (Internal Server Error)` est renvoyé avec un corps d’erreur SOAP indiquant que la requête n’a pas pu être authentifiée.

Avant IPS 3.8, l&#39;authentification via l&#39;en-tête SOAP était implémentée à l&#39;aide des éléments `AuthUser` et `AuthPassword` dans le  de  `http://www.scene7.com/IpsApi`. Par exemple :

```
<soap:Header xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/"> 
   <AuthUser xmlns="http://www.scene7.com/IpsApi">user@scene7.com</AuthUser> 
   <AuthPassword xmlns="http://www.scene7.com/IpsApi">mypassword</AuthPassword> 
</soap:Header>
```

Ce style est toujours pris en charge pour la compatibilité descendante, mais a été abandonné au profit de l’ `authHeader` élément.

**Demande d’autorisation**

Une fois les informations d’identification de l’appelant authentifiées, la requête est vérifiée pour vérifier que l’appelant est autorisé à effectuer l’opération demandée. L’autorisation est basée sur le rôle utilisateur de l’appelant et peut également nécessiter la vérification du , de l’utilisateurde l’application et d’autres paramètres d’opération. En outre, les utilisateurs du portail d’images doivent appartenir à un groupe disposant des autorisations requises pour effectuer certaines opérations sur les dossiers et les fichiers. La section de référence Opérations décrit en détail les exigences d’autorisation pour chaque opération.

**Exemple de requête et de réponse SOAP**

L’exemple suivant illustre une `addCompany` opération complète, y compris les en-têtes HTTP :

```
POST /scene7/services/IpsApiService HTTP/1.1 
User-Agent: Axis/2.0 
SOAPAction: addCompany 
Content-Type: text/xml; charset=UTF-8 
 
<?xml version='1.0' encoding='UTF-8'?> 
<soapenv:Envelope xmlns:soapenv="http://schemas.xmlsoap.org/soap/envelope/"> 
    <soapenv:Header> 
      <authHeader xmlns="http://www.scene7.com/IpsApi/xsd"> 
        <user>user@scene7.com</user> 
        <password>mypassword</password> 
        <appName>MyApp</appName> 
        <appVersion>1.0</appVersion> 
      </authHeader> 
    </soapenv:Header> 
    <soapenv:Body> 
    <ns1:addCompanyParam xmlns:ns1="http://www.scene7.com/IpsApi/xsd/2008-01-15"> 
      <ns1:companyName>Sample Company</ns1:companyName> 
      <ns1:expires>2008-07-31T12:00:00-06:00</ns1:expires> 
    </ns1:addCompanyParam> 
    </soapenv:Body> 
 </soapenv:Envelope>
```

Et la réponse correspondante :

```
HTTP/1.1 200 OK 
Server: Apache-Coyote/1.1 
Content-Type: text/xml;charset=UTF-8 
Transfer-Encoding: chunked 
Date: Fri, 21 Jul 2006 20:47:55 GMT 
 
<?xml version='1.0' encoding='utf-8'?><soapenv:Envelope 
xmlns:soapenv="http://schemas.xmlsoap.org/soap/envelope/"> 
   <soapenv:Header /> 
   <soapenv:Body> 
     <ns1:addCompanyReturn xmlns:ns1="http://www.scene7.com/IpsApi/xsd/2008-01-15"> 
       <ns1:companyInfo> 
          <ns1:companyHandle>2</ns1:companyHandle> 
          <ns1:name>Sample Company</ns1:name> 
          <ns1:rootPath>SampleCompany/</ns1:rootPath> 
          <ns1:expires>2008-07-31T18:00:00.000Z</ns1:expires> 
       </ns1:companyInfo> 
     </ns1:addCompanyReturn> 
   </soapenv:Body> 
</soapenv:Envelope>
```

**Valeurs par défaut SOAP**

Lorsqu’une opération rencontre une condition d’exception, une erreur SOAP est renvoyée en tant que corps du message SOAP à la place de la réponse normale. Par exemple, si un utilisateur non-administrateur tente d’envoyer la `addCompany` requête précédente, la réponse suivante est renvoyée :

```
HTTP/1.1 500 Internal Server Error 
Server: Apache-Coyote/1.1 
Content-Type: text/xml;charset=UTF-8 
Transfer-Encoding: chunked 
Date: Fri, 21 Jul 2006 16:36:20 GMT 
Connection: close 
 
<?xml version='1.0' encoding='utf-8'?> 
<soapenv:Envelope xmlns:soapenv="http://schemas.xmlsoap.org/soap/envelope/"> 
   <soapenv:Header /> 
   <soapenv:Body> 
      <soapenv:Fault> 
         <faultcode>soapenv:Client</faultcode> 
         <faultstring>AuthorizationException</faultstring> 
         <detail> 
           <ns1:authorizationFault xmlns:ns1="http://www.scene7.com/IpsApi/xsd"> 
               <code xmlns="http://www.scene7.com/IpsApi/xsd">20003</code> 
             <reason xmlns="http://www.scene7.com/IpsApi/xsd">User does not  
             have permission to access operation 'addCompany'</reason> 
           </ns1:authorizationFault> 
         </detail> 
      </soapenv:Fault> 
   </soapenv:Body> 
</soapenv:Envelope>
```

