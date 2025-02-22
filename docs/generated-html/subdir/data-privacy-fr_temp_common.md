= Notions essentielles sur la vie privée et la protection des données personnelles
Clément Levallois <levallois@em-lyon.com>
2018-06-20

last modified: {docdate}

:icons!:
:iconsfont:   font-awesome
:revnumber: 1.0
:example-caption!:
:sourcedir: ../../../main/java

:title-logo-image: EMLyon_logo_corp.png[align="center"]

image::EMLyon_logo_corp.png[align="center"]
{nbsp} +

//ST: 'Escape' or 'o' to see all sides, F11 for full screen, 's' for speaker notes


== 1. Confidentialité: un des aspects de la protection des données

// +
image::Plusieurs-définitions-possibles-à-la-protection-des-données.png[align ="center",title="Plusieurs définitions possibles à la protection des données",book=" keep"]
{nbsp} +

== 2. Quand les informations personnelles sont-elles considérées comme des "données"?

// +
Au niveau le plus basique, n'importe quoi pourrait compter comme "données" avec peut-être un caractère personnel, y compris les commentaires écrits sur quelqu'un dans un cahier personnel.

En pratique, les "données" commencent à être considérées comme telles lorsque:

// +
- C'est une information susceptible d'être traitée *automatiquement*
-> Par exemple : données sur les ordinateurs
// +
- Ou des *information structurées* qui peut être utilisée pour faciliter la récupération d'informations précises sur des individus spécifiques
-> Indice: documents papier, systèmes de classement, bases de données

== 3. Les données personnelles sont importantes en raison du droite à la vie privée

https://www.cnil.fr/fr/definition/donnee-personnelle[Définition des données personnelles]:

// +
[citation, CNIL (Autorité administrative indépendante française)]
____
Toute information identifiant directement ou indirectement une personne physique (ex. nom, no d’immatriculation, no de téléphone, photographie, date de naissance, commune de résidence, empreinte digitale...).
____

// +
Les données personnelles sont des données qu'une personne a le droit de garder privées. *Comment et pourquoi la vie privée est-elle une question importante*?
// +
La vie privée est mentionnée à l'article 12 de la http://www.un.org/fr/universal-declaration-human-rights/index.html[Déclaration universelle des droits de l'homme de 1948]:

// +
[citation, Déclaration universelle des droits de l'homme]
____
Nul ne peut être soumis à une ingérence arbitraire dans sa vie privée, sa famille, son domicile ou sa correspondance, ni à des atteintes à son honneur et à sa réputation. Toute personne a droit à la protection de la loi contre de telles ingérences ou attaques.
____

// +
Cet article de la Déclaration se retrouve sous des formes similaires dans la plupart des conventions sur les droits de l'homme dans le monde.
// +
Ce *droit à la vie privée* (((vie privée, droit à la))) permet aux individus de définir leur identité par rapport au monde, en donnant à chacun le pouvoir de contrôler ce qu'il préfère garder pour développer sa vie intérieure, et ce qu'il choisit de révéler le monde. Construire sa propre image, et l'image qu'on présente au monde : c'est construire son identité, et c'est qu'une vie privée contribue à maintenir.

// +
En 2005, un rapport sur https://books.google.fr/books?id=yeVRrrJw-zAC&pg=PA1&dq=right+to+privacy+tel+aviv&hl=en&ei=T0IhTaWhEI-msQOizMWZCg&sa=X&oi=book_result&ct=result&redir_esc=y#v=onepage&q=right%20to%20privacy%20tel%20aviv&f=false[Vie privée dans l'environnement numérique, par le Centre de droit et de technologie de Haïfa] :

// +
____
Le droit à la vie privée est notre droit de garder un domaine autour de nous, qui comprend toutes les choses qui font partie de nous, comme notre corps, notre maison, nos biens, nos pensées, nos sentiments, nos secrets et notre identité.
____

// +
____
Le droit à la vie privée nous donne la possibilité de choisir quelles parties de ce domaine peuvent être consultées par d'autres, et de contrôler l'étendue, la manière et le moment de l'utilisation des parties que nous choisissons de divulguer.
____

// +
En plus de façonner la sphère personnelle et l'identité d'un individu, la vie privée est également à la base du développement d'une relation entre l'individu et la société dont il fait partie:

// +
-> lorsque la vie privée d'une personne est protégée, elle n'a pas à craindre que ses opinions personnelles et ses activités (aussi simples que la lecture d'un journal) les mettent en danger en tant que citoyens.

-> ceci donne la liberté aux individus de développer des expressions politiques qui ne sont pas nécessairement conformes à la structure de pouvoir en place. Ce serait beaucoup plus difficile si les opinions politiques de tout le monde ne pouvaient pas rester privées.


== 4. Évolution de la vie privée

// +
La vie privée est une norme sociale qui se transforme à mesure que les sociétés évoluent. Depuis les années 2000, quelques tendances peuvent être identifiées:

// +
- il y a une augmentation du suivi des traces numériques laissées par les individus par les entreprises qui utilisent ces traces pour le ciblage publicitaire et la revente de données.
// +
- augmentation de la ((surveillance d'état)) par des moyens numériques, contre des menaces de sécurité et des buts non spécifiés.
// +
- acceptation croissante par le public de nouvelles formes de violation de la vie privée.

Par exemple, la https://fr.wikipedia.org/wiki/T%C3%A9l%C3%A9r%C3%A9alit%C3%A9[téléréalité, qui montre des participants filmés 24/24], et qui révèle leur intimité (réelle ou supposée), ne date que de la fin des années 1990.

[link = http: //www.imdb.com/title/tt0120382/]
image::truman.jpg[align = "center", title = "Le Truman SHow - film de 1998", livre = "book"]
{nbsp} +

== 5. Vie privée du consommateur et vie privée des citoyens: les relations entre les deux

Grâce aux lanceurs d'alerte comme https://en.wikipedia.org/wiki/Edward_Snowden[Edward Snowden], ((("Snowden, Edward"))) un ancien consultant pour la National Security Agency - NSA, l'ampleur des violations de la vie privée par les agences gouvernementales sont maintenant mieux connues.
// +
Ce trailer de "CitizenFour" donne une idée des dangers auxquels sont confrontés les lanceurs d'alerte lorsqu'ils révèlent comment les agences gouvernementales espionnent leurs citoyens :

video::xHuPkbP2NSo[youtube]

Des journalistes, des universitaires, des militants et des ONG tels que la https://www.eff.org/[Electronic Frontier Foundation] font valoir que:

- les consommateurs ne sont pas suffisamment conscients et sensibles à la quantité d'informations captées dans la conduite normale de leur vie, simplement en utilisant des téléphones mobiles et des applications, la navigation sur le Web et, de plus en plus, dans des lieux publics.
// +
- les citoyens sont insuffisamment conscients et sensibles à la violation de leur vie privée par les agences de sécurité de leur propre pays de résidence, et par d'autres pays.
// +
Beaucoup de citoyens considèrent que s'ils ne violent pas la loi, ils n'ont «rien à cacher».
// +
De même, les consommateurs pourraient trouver que négocier leurs données privées contre un service gratuit et certaines publicités ciblées, est une bonne affaire.
// +
La sociologue de la technologie http://technosociology.org/[Zeynep Tufekci] va plus loin:

// +
Selon elle, outre la surveillance et la perte de vie privée, des entreprises comme Google et Facebook développent un business model basé sur le ciblage publicitaire par l'analyse de données personnelles, et conçoivent une architecture de persuasion *utilisable / détournable* à des fins politiques.

// +
*Tufekci* ((("Tufekci, Zeynep"))) ne fait pas valoir que Google, Facebook ou les goûts ont intrinsèquement des fins antidémocratiques, mais que:

// +
- ils développent une architecture de l'information qui a le potentiel de façonner les opinions des foules,
- Ils le font sans transparence
// +
- quelques expériences passées sur le vote aux Etats-Unis, et les développements actuels sur la ((surveillance électronique)) en ((Chine)), montrent que la puissance de ces technologies a déjà des conséquences dans le monde réel:

// +
video::iFTWM7HV2UI[youtube]
// +

== 6. Conclusion: la protection des données dans les affaires, plus qu'une obligation réglementaire
La collecte et le traitement des données à caractère personnel par les entreprises ont une grande portée et ne doivent pas être considérés uniquement du point de vue juridique par les entreprises.
// +
Le sujet engage la https://en.wikipedia.org/wiki/Corporate_social_responsibility[Responsabilité sociale de l'entreprise].
// +
La nature du *business model* (((business model, basé sur le profilage du consommateur))) - elle-même, profilant les consommateurs de la manière la plus spécifique - a des conséquences profondes sur la société.

// +
Quelles seront les prochaines étapes? Plusieurs tendances peuvent être identifiées:

// +
1. Certaines voix s'interrogent sur le business model qui consiste à servir des publicités ciblées basées sur des données personnelles. Ce modèle est-il aussi efficace que la valorisation boursière de Facebook le suggère? https://digiday.com/media/ft-warns-advertisers-discovering-high-levels-of-domain-spoofing/[ L'étendue de la fraude dans les publicités numériques], est difficile à mesurer, comme le montre la vidéo ci-dessous:

video::oVfHeWTKjag[youtube]

// +
[début = 2]
2. Des situations contrastées en terme de cadre législatif visant à à protéger la vie privée, en particulier par le biais d'une obligation de transparence face à la collecte de plus de données personnelles. L'Europe renforce ce cadre avec la RGPD (voir https://www.pinterest.fr/seinecle/gdpr/en-fran%C3%A7ais/[une sélection d'articles sur le sujet de la RGPD]), la Chine met au contraire en place un système de surveillance des individus très puissant (voir https://www.pinterest.fr/seinecle/china-data-science-ai/en-fran%C3%A7ais/[une sélection d'articles sur la Chine])
// +
[début = 3]
3. Un approfondissement du modèle actuel avec plus de données personnelles collectées, dans les espaces privés (maisons) et le comportement dans les lieux publics (gestion des foules dans les rues, les stades, etc.). Ainsi, Echo d'Amazon, le HomePod d'Apple et Google Home ont fait une percée chez les consommateurs. Ces équipements renforcent la captation de données à caractère personnelle :

image::amazon-echo.jpg[align = "center", title = "Echo Alexa", livre = "book"]
{nbsp} +

== Pour aller plus loin
Retrouvez le site complet : https://seinecle.github.io/mk99/[here].

image:round_portrait_mini_150.png[align="center", role="right"]
Clement Levallois

Découvrez mes autres cours et projets : https://www.clementlevallois.net

Ou contactez-moi via Twitter: https://www.twitter.com/seinecle[@seinecle]
