---
description: Décrit les paramètres d’opération courants gérés par l’API du service Web IPS.
solution: Experience Manager
title: Méthodes d’opérations
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 020c8e63-ad4e-4c0d-8da6-b51efb2b89a5
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '704'
ht-degree: 0%

---

# Méthodes d’opérations{#operations-methods}

Cette section décrit les paramètres d’opération courants gérés par l’API de service Web IPS.

Pour une description complète de chaque paramètre d’opération, consultez [Paramètres](/help/aem-ips-api/operations/c-operations-intro/c-methods/c-methods.md) d’opération.

## Poignées : À propos {#section-094ce1afa6244fa5b2c762f44ffdca1c}

Gère les objets IPS de référence renvoyés par certaines opérations de l’API. Vous pouvez également transmettre des descripteurs sous forme de paramètres aux appels d’opération suivants. Les descripteurs sont des chaînes de type données ( `xsd:string`).

Les poignées sont destinées à être utilisées pendant une seule session d’application. De plus, vous devez rendre les poignées persistantes car leur format peut changer entre les versions IPS. Lorsque vous écrivez des applications interactives, vous implémentez des délais d’expiration de session et ignorez toutes les poignées entre les sessions, en particulier après une mise à niveau IPS. Lorsque vous écrivez des applications non interactives, appelez les opérations appropriées pour récupérer les poignées chaque fois que l’application est exécutée. Les exemples de code Java/Axis2 suivants montrent une exécution de code incorrecte et correcte :

**Manipulation incorrecte Code**

Cet exemple de code est incorrect car il contient une valeur codée en dur (555) pour le pseudo de société.

```
SearchAssetsParam searchParam = new SearchAssetsParam(); searchParam.setCompanyHandle("555");// INCORRECT 
searchParam.setFolder("myFolder"); 
SearchAssetsReturn retVal = ipsApi.searchAssets(searchParam, authHeader);
```

**Gérer correctement les Code**

Cet exemple de code est correct car il appelle `getCompanyInfo` à renvoyer un handle valide. Elle ne repose pas sur une valeur codée en dur. Utilisez cette méthode (ou un autre équivalent d’API IPS) pour renvoyer le handle requis.

```
GetCompanyInfoParam companyInfoParam = new GetCompanyInfoParam(); 
companyInfoParam.setCompanyName("My Company"); GetCompanyInfoReturn companyInfoReturn = ipsApi.getCompanyInfo(companyInfoParam, authHeader); 
String companyHandle = companyInfoReturn.getCompanyInfo().getCompanyHandle(); 
SearchAssetsParam searchParam = new SearchAssetsParam(); searchParam.setCompanyHandle(companyHandle); //CORRECT 
searchParam.setFolder("myFolder"); 
SearchAssetsReturn retVal = ipsApi.searchAssets(searchParam, authHeader);
```

## Types de handle courants {#section-e683ac8283284f9688e63f51a494f7a0}

**CompanyHandle**

La plupart des opérations nécessitent de définir un contexte d’entreprise en transmettant un `companyHandle` paramètre. Le handle de société est un pointeur renvoyé par certaines opérations telles que `getCompanyInfo`, `addCompany`et `getCompanyMembership`.

**Poignée utilisateur**

Le `userHandle` paramètre est facultatif pour les opérations qui ciblent un utilisateur spécifique. Par défaut, ces opérations ciblent l’utilisateur appelant (l’utilisateur dont les informations d’identification sont transmises pour authentification). Toutefois, les utilisateurs administrateurs disposant des autorisations appropriées peuvent spécifier un autre utilisateur. Par exemple, l’opération `setPassword` définit normalement le mot de passe de l’utilisateur authentifié, mais un administrateur peut utiliser le `userHandle` paramètre pour définir le mot de passe d’un autre utilisateur.

Pour les opérations qui nécessitent un contexte d’entreprise (à l’aide du `companyHandle` paramètre), les utilisateurs authentifiés et cibles doivent être membres de la société spécifiée. Pour les opérations qui ne nécessitent pas de contexte d’entreprise, les utilisateurs authentifiés et cibles doivent tous deux être membres d’au moins une société commune.

Les opérations suivantes peuvent récupérer les pseudos utilisateur :

* `getUsers`
* `getAllUsers`
* `getUserInfo`
* `getCompanyMembers`
* `getGroupMembers`
* `addUser`

**accessUserHandle et accessGroupHandle**

Par défaut, les opérations qui nécessitent des autorisations d’accès (lecture, écriture, suppression) fonctionnent dans le contexte d’autorisation de l’utilisateur appelant. Certaines opérations permettent de modifier ce contexte avec le `accessUserHandle` paramètre ou `accessGroupHandle` . Le `accessUserHandle` paramètre permet à un administrateur d’emprunter l’identité d’un autre utilisateur. Le `accessGroupHandle` paramètre permet à l’appelant d’opérer dans le contexte d’un groupe d’utilisateurs spécifique.

**responseFieldArray et excludeFieldArray**

Certaines opérations permettent à l’appelant de limiter les champs inclus dans la réponse. La limitation des champs peut aider à réduire le temps et la mémoire requis pour traiter la demande et à réduire la taille des données de réponse. L’appelant peut demander une liste spécifique de champs en passant un `responseFieldArray` paramètre ou en énumérant une liste de champs exclus par le `excludeFieldArray` paramètre.

Les deux `responseFieldArray` et `excludeFieldArray` spécifiez des champs en utilisant un chemin de nœud séparé par `/`. Par exemple, pour spécifier que `searchAssets` renvoie uniquement le nom, la date de dernière modification et les métadonnées pour chaque ressource, reportez-vous aux sections suivantes :

```
<responseFieldArray> 
   <items>assetArray/items/name</items> 
   <items>assetArray/items/lastModified</items> 
   <items>assetArray/items/metadataArray</items> 
</responseFieldArray>
```

De même, pour renvoyer tous les champs (à l’exception des permissions) :

```
<excludeFieldArray> 
   <items>assetArray/items/permissions</items> 
</excludeFieldArray>
```

Notez que les chemins d’accès au nœud sont relatifs à la racine du nœud de retour. Si vous spécifiez un champ de type complexe sans aucun de ses sous-éléments (par exemple, `assetArray/items/imageInfo`), tous ses sous-éléments sont inclus. Si vous spécifiez un ou plusieurs sous-éléments dans un champ de type complexe (par exemple, `assetArray/items/imageInfo/originalPath`), seuls ces sous-éléments sont inclus.

Si vous n’incluez `responseFieldArray` pas ou `excludeFieldArray` dans une requête, tous les champs sont renvoyés.

**Paramètres régionaux**

Depuis IPS 4.0, l’API IPS prend en charge la définition du contexte régional d’une opération en transmettant le `authHeader` paramètre locale. Si le paramètre locale n’est pas présent, l’en-tête `Accept-Language` HTTP est utilisé. Si cet en-tête n’est pas non plus présent, le paramètre régional par défaut du serveur IPS est utilisé.

Certaines opérations prennent également des paramètres régionaux explicites, qui peuvent être différents du contexte de paramètres régionaux de l’opération. Par exemple, l’opération prend un `submitJob` paramètre qui définit les paramètres régionaux utilisés pour la journalisation des travaux et la `locale` notification par courrier électronique.

Les paramètres régionaux utilisent le format `<language_code>[-<country_code>]`

Lorsque le code de langue est un code à deux lettres minuscule spécifié par ISO-639 et que le code de pays facultatif est un code majuscule à deux lettres spécifié par ISO-3266. Par exemple, la chaîne du paramètre régional pour l’anglais américain est `en-US`.
