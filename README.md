# ![left 100%](https://raw.githubusercontent.com/thierry-laval/archives/master/images/logo-portfolio.png "Un bien beau logo !")

## Auteur

👤 &nbsp; **Thierry LAVAL** [🇫🇷 Contactez moi 🇬🇧](<contact@thierrylaval.dev>)

* Github: [@Thierry Laval](https://github.com/thierry-laval)
* LinkedIn: [@Thierry Laval](https://www.linkedin.com/in/thierry-laval)
* Visitez ==> 🏠 [Site Web](https://thierrylaval.dev)
* Visitez le projet ==> 🏠 [Site du projet](https://thierry-laval.github.io/01-FORK-HEAD/)

***

## 📎 Projet 01-FORK-HEAD - Un guide simple pour les éléments HTML `<head>`

_`Début du projet le 27/11/2023`_

### Table des matières

- [](#)
  - [Auteur](#auteur)
  - [📎 Projet 01-FORK-HEAD - Un guide simple pour les éléments HTML `<head>`](#-projet-01-fork-head---un-guide-simple-pour-les-éléments-html-head)
    - [Table des matières](#table-des-matières)
    - [Recommandation-minimale](#recommandation-minimale)
    - [Éléments](#éléments)
    - [Méta](#méta)
    - [Lien](#lien)
    - [Icônes](#icônes)
    - [Réseaux sociaux](#réseaux-sociaux)
      - [Facebook Open Graph](#facebook-open-graph)
        - [Twitter Card](#twitter-card)
        - [Confidentialité Twitter](#confidentialité-twitter)
        - [Schema.org](#schemaorg)
        - [Pinterest](#pinterest)
        - [Articles instantanés Facebook](#articles-instantanés-facebook)
        - [OEmbed](#oembed)
        - [QQ/Wechat](#qqwechat)
    - [Navigateurs / Plateformes](#navigateurs--plateformes)
      - [Apple iOS](#apple-ios)
      - [Google Android](#google-android)
      - [Google Chrome](#google-chrome)
      - [Microsoft Internet Explorer](#microsoft-internet-explorer)
      - [Navigateurs (chinois)](#navigateurs-chinois)
      - [Navigateur 360](#navigateur-360)
      - [Navigateur mobile QQ](#navigateur-mobile-qq)
      - [Navigateur mobile UC](#navigateur-mobile-uc)
      - [Liens d'application](#liens-dapplication)
    - [Autres ressources](#autres-ressources)
    - [Projets associés](#projets-associés)
  - [🌐 Traductions](#-traductions)
  - [🤝 Contribuer](#-contribuer)
  - [👤 Développeurs](#-développeurs)
  - [💛 Soutien](#-soutien)
  - [📝 Licence](#-licence)
  - [♥    Love Markdown](#love-markdown)

### Recommandation-minimale

Voici les éléments essentiels pour tout document Web (sites Web/applications) :

```html
<meta charset="utf-8">
<meta name="viewport" content="width=device-width, initial-scale=1">
<!--
Les 2 balises méta ci-dessus *doivent* apparaître en premier dans le <head>
pour garantir systématiquement un rendu correct du document.
Tout autre élément d'en-tête doit apparaître *après* ces balises.
-->
<title>Titre de la page</title>
```

`meta charset` - définit l'encodage du site Web, `utf-8` est la norme

`meta name="viewport"` - paramètres de la fenêtre d'affichage liés à la réactivité mobile

`width=device-width` - utilise la largeur physique de l'appareil (idéal pour les mobiles !)

`initial-scale=1` - le zoom initial, 1 signifie aucun zoom

**[⬆ retour en haut](#table-des-matières)**

### Éléments

Les éléments `<head>` valides incluent `meta`, `link`, `title`, `style`, `script`, `noscript` et `base`.

Ces éléments fournissent des informations sur la façon dont un document doit être perçu et rendu par les technologies Web. par exemple les navigateurs, les moteurs de recherche, les robots, etc.

```html
<!--
Définissez l'encodage des caractères pour ce document, de sorte que
tous les caractères dans l'espace UTF-8 (comme les emoji)
soient rendus correctement. -->
<meta charset="utf-8">

<!-- Définir le titre du document -->
<title>Titre de la page</title>

<!-- Définir l'URL de base pour toutes les URL relatives dans le document -->
<base href="https://example.com/page.html">

<!-- Lien vers un fichier CSS externe -->
<link rel="stylesheet" href="styles.css">

<!-- Utilisé pour ajouter du CSS dans le document -->
<style>
/* ... */
</style>

<!-- Balises JavaScript et sans JavaScript -->
<script src="script.js"></script>
<script>
// fonction(s) à placer ici
</script>
<noscript>
<!-- Aucune alternative JS -->
</noscript>
```

**[⬆ retour en haut](#table-des-matières)**

### Méta

```html
<!--
Les 2 éléments suivants Les balises méta *doivent* apparaître en premier dans le <head>
pour garantir un rendu correct du document.
Tout autre élément d'en-tête doit apparaître *après* ces balises.
-->
<meta charset="utf-8">
<meta name="viewport" content="width=device-width, initial-scale=1">

<!--
Permet de contrôler l'endroit d'où les ressources sont chargées.
Placez-la le plus tôt possible dans le <head>, car la balise
ne s'applique qu'aux ressources déclarées après elle.
-->
<meta http-equiv="Content-Security-Policy" content="default-src 'self'">

<!-- Nom de l'application Web (ne doit être utilisé que si le site Web est utilisé comme une application) -->
<meta name="application-name" content="Application Name">

<!-- Couleur du thème pour Chrome, Firefox OS et Opera -->
<meta name="theme-color" content="#4285f4">

<!-- Brève description du document (limite à 150 caractères) -->
<!-- Ce contenu *peut* être utilisé dans le cadre des résultats des moteurs de recherche. -->
<meta name="description" content="Une description de la page">

<!-- Contrôler le comportement de l'exploration et de l'indexation des moteurs de recherche -->
<meta name="robots" content="index,follow"><!-- Tous les moteurs de recherche -->
<meta name="googlebot" content="index,follow"><!-- Spécifique à Google -->

<!-- Indique à Google de ne pas afficher la zone de recherche des liens de site -->
<meta name="google" content="nositelinkssearchbox">

<!-- Indique à Google de ne pas fournir de traduction pour ce document -->
<meta name="google" content="notranslate">

<!-- Vérifier la propriété du site Web -->
<meta name="google-site-verification" content="verification_token"><!-- Google Search Console -->
<meta name="yandex-verification" content="verification_token"><!-- Yandex Webmasters -->
<meta name="msvalidate.01" content="verification_token"><!-- Centre pour les webmasters Bing -->
<meta name="alexaVerifyID" content="verification_token"><!-- Console Alexa -->
<meta name="p:domain_verify" content="code_from_pinterest"><!-- Console Pinterest-->
<meta name="norton-safeweb-site-verification" content="norton_code"><!-- Norton Safe Web -->

<!-- Identifiez le logiciel utilisé pour créer le document (c.-à-d. - WordPress, Dreamweaver) -->
<meta name="generator" content="program">

<!-- Brève description du sujet de votre document -->
<meta name="subject" content="your document's subject">

<!-- Donne une classification générale par âge en fonction du contenu du document -->
<meta name="rating" content="General">

<!-- Permet de contrôler la manière dont les informations de référence sont transmises -->
<meta name="referrer" content="no-referrer">

<!-- Désactive la détection et le formatage automatiques des numéros de téléphone possibles -->
<meta name="format-detection" content="telephone=no">

<!-- Désactive complètement la prélecture DNS en la définissant sur « off » -->
<meta http-equiv="x-dns-prefetch-control" content="off">

<!-- Spécifie le document à afficher dans un cadre spécifique -->
<meta http-equiv="Window-Target" content="_value">

<!-- Balises géographiques -->
<meta name="ICBM" content="latitude, longitude">
<meta name="geo.position" content="latitude;longitude">
<meta name="geo.region" content="country[-state]"><!-- Code de pays (ISO 3166-1) : obligatoire, code d'état (ISO 3166-2) : facultatif ; par ex. content="US" / content="US-NY" -->
<meta name="geo.placename" content="city/town"><!-- par ex. content="New York City" -->

<!-- Monétisation Web https://webmonetization.org/docs/getting-started -->
<meta name="monetization" content="$paymentpointer.example">
```

- 📖 [Balises méta que Google comprend](https://support.google.com/webmasters/answer/79812?hl=en)
- 📖 [WHATWG Wiki : MetaExtensions](https://wiki.whatwg.org/wiki/MetaExtensions)
- 📖 [ICBM sur Wikipédia](https://en.wikipedia.org/wiki/ICBM_address#Modern_use)
- 📖 [Géolocalisation sur Wikipédia](https://en.wikipedia.org/wiki/Géolocalisation#HTML_pages)

**[⬆ retour en haut](#table-des-matières)**

### Lien

```html
<!-- Pointe vers une feuille de style externe -->
<link rel="stylesheet" href="https://example.com/styles.css">

<!-- Aide à éviter les problèmes de contenu dupliqué -->
<link rel="canonical" href="https://example.com/article/?page=2">

<!-- Lien vers une version HTML AMP du document actuel -->
<link rel="amphtml" href="https://example.com/path/to/amp-version.html">

<!-- Lien vers un fichier JSON qui spécifie les informations d'identification « d'installation » pour les applications Web -->
<link rel="manifest" href="manifest.json">

<!-- Lien vers des informations sur le ou les auteurs du document -->
<link rel="author" href="humans.txt">

<!-- Fait référence à une déclaration de droits d'auteur qui s'applique au contexte du lien -->
<link rel="license" href="copyright.html">

<!-- Donne une référence à un emplacement dans votre document qui peut être dans une autre langue -->
<link rel="alternate" href="https://es.example.com/" hreflang="es">

<!-- Fournit des informations sur un auteur ou une autre personne -->
<link rel="me" href="https://google.com/profiles/thenextweb" type="text/html">
<link rel="me" href="mailto:name@example.com">
<link rel="me" href="sms:+15035550125">

<!-- Liens vers un document qui décrit une collection d'enregistrements, de documents ou d'autres éléments d'intérêt historique -->
<link rel="archives" href="https://example.com/archives/">

<!-- Liens vers une ressource de niveau supérieur dans une structure hiérarchique -->
<link rel="index" href="https://example.com/article/">

<!-- Fournit une auto-référence - utile lorsque le document a plusieurs références possibles -->
<link rel="self" type="application/atom+xml" href="https://example.com/atom.xml">

<!-- Les premier, dernier, précédent et suivant documents d'une série de documents, respectivement -->
<link rel="first" href="https://example.com/article/">
<link rel="last" href="https://example.com/article/?page=42">
<link rel="prev" href="https://example.com/article/?page=1">
<link rel="next" href="https://example.com/article/?page=3">

<!-- Utilisé lorsqu'un service tiers est utilisé pour maintenir un blog -->
<link rel="EditURI" href="https://example.com/xmlrpc.php?rsd" type="application/rsd+xml" title="RSD">

<!-- Forme un commentaire automatisé lorsqu'un autre blog WordPress crée un lien vers votre blog ou votre article WordPress -->
<link rel="pingback" href="https://example.com/xmlrpc.php">

<!-- Notifie une URL lorsque vous créez un lien vers celle-ci sur votre document -->
<link rel="webmention" href="https://example.com/webmention">

<!-- Permet de publier sur votre propre domaine à l'aide d'un client Micropub -->
<link rel="micropub" href="https://example.com/micropub">

<!-- Ouvrir la recherche -->
<link rel="search" href="/open-search.xml" type="application/opensearchdescription+xml" title="Titre de la recherche">

<!-- Flux -->
<link rel="alternate" href="https://feeds.feedburner.com/example" type="application/rss+xml" title="RSS">
<link rel="alternate" href="https://example.com/feed.atom" type="application/atom+xml" title="Atom 0.3">

<!-- Prélecture, préchargement, prénavigation -->
<!-- Plus d'infos : https://css-tricks.com/prefetching-preloading-prebrowsing/ -->
<link rel="dns-prefetch" href="//example.com/">
<link rel="preconnect" href="https://www.example.com/">
<link rel="prefetch" href="https://www.example.com/">
<link rel="prerender" href="https://example.com/">
<link rel="preload" href="image.png" as="image">
```

- 📖 [Relations de liens](https://www.iana.org/assignments/link-relations/link-relations.xhtml)

**[⬆ retour en haut](#table-des-matières)**

### Icônes

```html
<!-- Pour IE 10 et inférieur -->
<!-- Placez favicon.ico dans le répertoire racine - aucune balise n'est nécessaire -->

<!-- Icône dans la résolution la plus élevée dont nous avons besoin -->
<link rel="icon" sizes="192x192" href="/path/to/icon.png">

<!-- Icône Apple Touch (réutilisation de l'icône 192px.png) -->
<link rel="apple-touch-icon" href="/path/to/apple-touch-icon.png">

<!-- Icône d'onglet épinglé Safari -->
<link rel="mask-icon" href="/path/to/icon.svg" color="blue">
```

- 📖 [Tout sur les favicons (et les icônes tactiles)](https://bitsofco.de/all-about-favicons-and-touch-icons/)
- 📖 [Création d'icônes d'onglets épinglés](https://developer.apple.com/library/content/documentation/AppleApplications/Reference/SafariWebContent/pinnedTabs/pinnedTabs.html)
- 📖 [Aide-mémoire sur les favicons](https://github.com/audreyr/favicon-cheat-sheet)
- 📖 [Icônes et couleurs du navigateur](https://developers.google.com/web/fundamentals/design-and-ux/browser-customization/)

**[⬆ retour en haut](#table-des-matières)**

### Réseaux sociaux

#### Facebook Open Graph

La plupart du contenu est partagé sur Facebook en tant qu'URL, il est donc important de marquer votre site Web avec des balises Open Graph pour contrôler la façon dont votre contenu apparaît sur Facebook. [En savoir plus sur le balisage Open Graph de Facebook](https://developers.facebook.com/docs/sharing/webmasters#markup)

```html
<meta property="fb:app_id" content="123456789">
<meta property="og:url" content="https://example.com/page.html">
<meta property="og:type" content="website">
<meta property="og:title" content="Titre du contenu">
<meta property="og:image" content="https://example.com/image.jpg">
<meta property="og:image:alt" content="Une description du contenu de l'image (pas une légende)">
<meta property="og:description" content="Description ici">
<meta property="og:site_name" content="Nom du site">
<meta property="og:locale" content="en_US">
<meta property="article:author" content="">
```

- 📖 [Protocole Open Graph](http://ogp.me/)
- 🛠 Testez votre page avec le [Facebook Sharing Debugger](https://developers.facebook.com/tools/debug/)

##### Twitter Card
> Avec Twitter Cards, vous pouvez joindre des photos, des vidéos et des expériences multimédias riches aux Tweets, contribuant ainsi à générer du trafic vers votre site Web. [En savoir plus sur les cartes Twitter](https://developer.twitter.com/en/docs/tweets/optimize-with-cards/overview/abouts-cards)

```html
<meta name="twitter:card" content="summary">
<meta name="twitter:site" content="@site_account">
<meta name="twitter:creator" content="@individual_account">
<meta name="twitter:url" content="https://example.com/page.html">
<meta name="twitter:title" content="Titre du contenu">
<meta name="twitter:description" content="Description du contenu inférieure à 200 caractères">
<meta name="twitter:image" content="https://example.com/image.jpg">
<meta name="twitter:image:alt" content="Une description textuelle de l'image transmettant la nature essentielle d'une image aux utilisateurs malvoyants. Maximum 420 caractères.">
```

- 📖 [Démarrage avec les cartes — Développeurs Twitter](https://dev.twitter.com/cards/getting-started)
- 🛠 Testez votre page avec le [Twitter Card Validator](https://cards-dev.twitter.com/validator)

##### Confidentialité Twitter
Si vous intégrez des tweets sur votre site Web, Twitter peut utiliser les informations de votre site pour adapter le contenu et les suggestions aux utilisateurs de Twitter. [En savoir plus sur les options de confidentialité de Twitter](https://dev.twitter.com/web/overview/privacy#what-privacy-options-do-website-publishers-have).
```html
<!-- interdire à Twitter d'utiliser les informations de votre site à des fins de personnalisation -->
<meta name="twitter:dnt" content="on">
```

##### Schema.org

```html
<html lang="" itemscope itemtype="https://schema.org/Article">
<head>
<link rel="author" href="">
<link rel="publisher" href="">
<meta itemprop="name" content="Content Title">
<meta itemprop="description" content="Content description less than 200 characters">
<meta itemprop="image" content="https://example.com/image.jpg">
```

**Remarque :** ces balises méta nécessitent que les attributs `itemscope` et `itemtype` soient ajoutés à la balise `<html>`.

- 📖 [Mise en route - schema.org](https://schema.org/docs/gs.html)
- 🛠 Testez votre page avec le [Test des résultats enrichis](https://search.google.com/test/rich-results)

##### Pinterest

Pinterest vous permet d'empêcher les gens d'enregistrer des éléments de votre site Web, selon [leur centre d'aide](https://help.pinterest.com/en/business/article/prevent-saves-to-pinterest-from-your-site). La `description` est facultative.

```html
<meta name="pinterest" content="nopin" description="Désolé, vous ne pouvez pas enregistrer depuis mon site Web !">
```

##### Articles instantanés Facebook

```html
<meta charset="utf-8">
<meta property="op:markup_version" content="v1.0">

<!-- L'URL de la version Web de votre article -->
<link rel="canonical" href="https://example.com/article.html">

<!-- Le style à utiliser pour cet article -->
<meta property="fb:article_style" content="myarticlestyle">
```

- 📖 [Création d'articles - Articles instantanés](https://developers.facebook.com/docs/instant-articles/guides/articlecreate)
- 📖 [Exemples de code - Articles instantanés](https://developers.facebook.com/docs/instant-articles/reference)

##### OEmbed

```html
<link rel="alternate" type="application/json+oembed"
href="https://example.com/services/oembed?url=http%3A%2F%2Fexample.com%2Ffoo%2F&amp;format=json"
title="Profil oEmbed : JSON">
<link rel="alternate" type="text/xml+oembed"
href="https://example.com/services/oembed?url=http%3A%2F%2Fexample.com%2Ffoo%2F&amp;format=xml"
title="Profil oEmbed : XML">
```

- 📖 [Format oEmbed](https://oembed.com/)

##### QQ/Wechat

Les utilisateurs qui partagent des pages Web avec qq wechat auront un message formaté

```html
<meta itemprop="name" content="share title">
<meta itemprop="image" content="http://imgcache.qq.com/qqshow/ac/v4/global/logo.png">
<meta name="description" itemprop="description" content="share content">
```
- 📖 [Documents sur le format du code](http://open.mobile.qq.com/api/mqq/index#api:setShareInfo)

**[⬆ retour en haut](#table-des-matières)**

### Navigateurs / Plateformes

#### Apple iOS

```html
<!-- Bannière d'application intelligente -->
<meta name="apple-itunes-app" content="app-id=APP_ID,affiliate-data=AFFILIATE_ID,app-argument=SOME_TEXT">

<!-- Désactiver la détection et le formatage automatiques des numéros de téléphone possibles -->
<meta name="format-detection" content="telephone=no">

<!-- Icône de lancement (180x180px ou plus) -->
<link rel="apple-touch-icon" href="/path/to/apple-touch-icon.png">

<!-- Image de l'écran de lancement -->
<link rel="apple-touch-startup-image" href="/path/to/launch.png">

<!-- Titre de l'icône de lancement -->
<meta name="apple-mobile-web-app-title" content="Titre de l'application">

<!-- Activer le mode autonome (plein écran) -->
<meta name="apple-mobile-web-app-capable" content="yes">

<!-- Apparence de la barre d'état (n'a aucun effet sauf si le mode autonome est activé) -->
<meta name="apple-mobile-web-app-status-bar-style" content="black">

<!-- Lien profond vers l'application iOS -->
<meta name="apple-itunes-app" content="app-id=APP-ID, app-argument=http/url-sample.com">
<link rel="alternate" href="ios-app://APP-ID/http/url-sample.com">
```

- 📖 [Configuration des applications Web](https://developer.apple.com/library/content/documentation/AppleApplications/Reference/SafariWebContent/ConfiguringWebApplications/ConfiguringWebApplications.html)

#### Google Android

```html
<meta name="theme-color" content="#E64545">

<!-- Ajouter à l'écran d'accueil -->
<meta name="mobile-web-app-capable" content="yes">
<!-- Plus d'informations : https://developer.chrome.com/multidevice/android/installtohomescreen -->

<!-- Lien profond vers l'application Android -->
<meta name="google-play-app" content="app-id=package-name">
<link rel="alternate" href="android-app://package-name/http/url-sample.com">
```

#### Google Chrome

```html
<link rel="chrome-webstore-item" href="https://chrome.google.com/webstore/detail/APP_ID">

<!-- Désactiver l'invite de traduction -->
<meta name="google" content="notranslate">
```

#### Microsoft Internet Explorer

```html
<!-- Forcer IE 8/9/10 à utiliser son dernier moteur de rendu -->
<meta http-equiv="x-ua-compatible" content="ie=edge">

<!-- Désactiver la détection et le formatage automatiques des numéros de téléphone possibles par l'extension de navigateur Skype Toolbar -->
<meta name="skype_toolbar" content="skype_toolbar_parser_compatible">

<!-- Windows Tiles -->
<meta name="msapplication-config" content="/browserconfig.xml">
```

Balisage XML minimal requis pour `browserconfig.xml` :

```xml
<?xml version="1.0" encoding="utf-8"?>
<browserconfig>
<msapplication>
<tile>
<square70x70logo src="small.png"/>
<square150x150logo src="medium.png"/>
<wide310x150logo src="wide.png"/>
<square310x310logo src="large.png"/>
</tile>
</msapplication>
</browserconfig>
```

- 📖 [Schéma de configuration du navigateur [référence](https://msdn.microsoft.com/en-us/library/dn320426.aspx)

**[⬆ retour en haut](#table-des-matiÃ¨res)**

#### Navigateurs (chinois)

#### Navigateur 360

```html
<!-- Sélectionner l'ordre du moteur de rendu -->
<meta name="renderer" content="webkit|ie-comp|ie-stand">
```

#### Navigateur mobile QQ

```html
<!-- Verrouille l'écran dans l'orientation spécifiée -->
<meta name="x5-orientation" content="paysage/portrait">

<!-- Afficher ce document en plein écran -->
<meta name="x5-fullscreen" content="true">

<!-- Le document s'affichera en « mode application » (plein écran, etc.) -->
<meta name="x5-page-mode" content="app">
```

#### Navigateur mobile UC

```html
<!-- Verrouille l'écran dans l'orientation spécifiée -->
<meta name="screen-orientation" content="landscape/portrait">

<!-- Afficher ce document en plein écran -->
<meta name="full-screen" content="yes">

<!-- Le navigateur UC affichera les images même en "mode texte" -->
<meta name="imagemode" content="force">

<!-- Le document s'affichera en "mode application" (plein écran, interdiction des gestes, etc.) -->
<meta name="browsermode" content="application">

<!-- Désactiver le "mode nuit" du navigateur UC pour ce document -->
<meta name="nightmode" content="disable">

<!-- Simplifier le document pour réduire le transfert de données -->
<meta name="layoutmode" content="fitscreen">

<!-- Désactiver la fonction du navigateur UC de "mise à l'échelle de la police lorsqu'il y a beaucoup de mots dans ce document" -->
<meta name="wap-font-scale" content="no">
```

- 📖 [Documents du navigateur UC](https://www.uc.cn/download/UCBrowser_U3_API.doc)

**[⬆ retour en haut](#table-des-matières)**

#### Liens d'application

```html
<!-- iOS -->
<meta property="al:ios:url" content="applinks://docs">
<meta property="al:ios:app_store_id" content="12345">
<meta property="al:ios:app_name" content="Liens d'application">

<!-- Android -->
<meta property="al:android:url" content="applinks://docs">
<meta property="al:android:app_name" content="Liens d'application">
<meta property="al:android:package" content="org.applinks">

<!-- Web fall back -->
<meta property="al:web:url" content="https://applinks.org/documentation">
```

- 📖 [Liens d'application](https://developers.facebook.com/docs/applinks)

**[⬆ retour en haut](#table-des-matieres)**

### Autres ressources

- 📖 [Documents HTML5 Boilerplate : Le HTML](https://github.com/h5bp/html5-boilerplate/blob/master/dist/doc/html.md)
- 📖 [Documents HTML5 Boilerplate : Étendre et personnaliser](https://github.com/h5bp/html5-boilerplate/blob/master/dist/doc/extend.md)

### Projets associés

- [Atom HTML Head Snippets](https://github.com/joshbuchea/atom-html-head-snippets) - Paquet Atom pour les extraits `HEAD`
- [Sublime Text HTML Head Snippets](https://github.com/marcobiedermann/sublime-head-snippets) - Paquet Sublime Text pour les extraits `HEAD`
- [head-it](https://github.com/hemanth/head-it) - Interface CLI pour les extraits `HEAD`
- [vue-head](https://github.com/ktquez/vue-head) - Manipulation des méta-informations de la balise `HEAD` pour Vue.js

## 🌐 Traductions

- 🇫🇷 [Français](https://github.com/thierry-laval/01-FORK-HEAD)
- 🇮🇩 [Bahasa](https://github.com/rijdz/HEAD)
- 🇧🇷 [Portugais brésilien](https://github.com/Webschool-io/HEAD)
- 🇨🇳 [Chinois (simplifié)](https://github.com/Amery2010/HEAD)
- 🇩🇪 [Allemand](https://github.com/Shidigital/HEAD)
- 🇮🇹 [Italien](https://github.com/Fakkio/HEAD)
- 🇯🇵 [Japonais](https://coliss.com/articles/build-websites/operation/work/collection-of-html-head-elements.html)
- 🇰🇷 [Coréen](https://github.com/Lutece/HEAD)
- 🇷🇺 [Russe/Русский](https://github.com/Konfuze/HEAD)
- 🇪🇸 [Espagnol](https://github.com/alvaroadlf/HEAD)
- 🇹🇷 [Turc/Türkçe](https://github.com/mkg0/HEAD)

**[⬆ retour en haut](#table-des-matières)**

## 🤝 Contribuer

**Ouvrez un ticket ou une demande d'extraction pour suggérer des modifications ou des ajouts.**

## 👤 Développeurs

* GitHub : [@joshbuchea](https://github.com/joshbuchea)
* GitHub : [@thierry-laval](https://github.com/thierry-laval)

## 💛 Soutien

Si ce projet vous a été utile, à vous ou à votre organisation, pensez à soutenir mon travail directement :

- 💛 [Parrainez-moi sur GitHub](https://github.com/sponsors/thierry-laval)

Si vous appréciez ce projet, vous pouvez me soutenir :

<a href="https://paypal.me/thierrylaval01?country.x=FR&locale.x=fr_FR" target="_blank"><img src="https://www.paypalobjects.com/digitalassets/c/website/logo/full-text/pp_fc_hl.svg" alt="Soutiens-moi !" height="35" width="150"></a>

Tout m'aide, merci ! 🙏

[Voir mon travail](https://github.com/thierry-laval)

[Créer un bon template](https://github.com/thierry-laval/P22-template-pour-un-readme)

## 📝 Licence

[![CC0](https://i.creativecommons.org/p/zero/1.0/88x31.png)](https://creativecommons.org/publicdomain/zero/1.0/)

"Dans la mesure permise par la législation, [Josh Buchea](http://joshbuchea.com) renonce à tous les droits d'auteur et droits connexes ou relatifs à ce travail."

Copyright © 2024 [Thierry Laval](https://thierrylaval.dev)

## &hearts;&nbsp;&nbsp;&nbsp;&nbsp;Love Markdown

Donnez une ⭐️ &nbsp;si ce projet vous plaît !

<span style="font-family:Papyrus; font-size:4em;">FAN DE GITHUB !</span>

<!-- [This is an image](https://myoctocat.com/assets/images/base-octocat.svg) -->

<a href="url"><img src="https://github.com/thierry-laval/P00-mes-archives/blob/master/images/octocat-oley.png" height="300"></a>

**[⬆ Retour en haut](#auteur)** <br>
