= Le cloud
Clément Levallois <levallois@em-lyon.com>
2018-06-18

last modified: {docdate}

:icons!:
:iconsfont:   font-awesome
:revnumber: 1.0
:example-caption!:
:sourcedir: ../../../main/java

:title-logo-image: EMLyon_logo_corp.png[width="242" align="center"]

image::EMLyon_logo_corp.png[width="242" align="center"]
{nbsp} +

//ST: 'Escape' or 'o' to see all sides, F11 for full screen, 's' for speaker notes

== 1. Note sur la terminologie: qu'est-ce qu'un serveur?

Pour comprendre le ((cloud)) précisément, nous devons d'abord avoir une vision claire de ce qu'est un ((serveur)). Un serveur est tout simplement un ordinateur dépourvu de tout ce qui n'est pas essentiel (écran, souris, carte graphique, carte son, clavier) ...
// +
Pour illustrer ceci: lorsque Google calcule quels sont les meilleurs résultats pour votre recherche "restaurant bon marché et délicieux à Lyon", ce calcul doit être fait sur un ordinateur, n'est-ce pas?
// +
Le type d'ordinateur utilisé pour faire ce calcul n'est *pas* celui-ci:

image::desktop.jpg[pdfwidth = "40%", align = "center", title = "Un ordinateur de bureau", book = "keep"]
{nbsp} +

En effet, pour faire cette recherche Google n'a pas besoin d'un écran, une souris, un bureau, et même pas de la grande boîte contenant l'ordinateur lui-même.
Ils prennent trop de place, consomment de l'énergie et ils sont juste inutiles dans ce cas.
Donc quand toutes les parties inutiles sont enlevées, l'ordinateur ressemble à ceci, et s'appelle un "serveur":

image::server.jpg[pdfwidth = "40%", align = "center", book = "keep", title = "Un serveur"]
{nbsp} +

Jetons un oeil à la forme : rectangulaire et très mince.
Cela facilite l'empilement des serveurs les uns sur les autres.
Parce que Google et d'autres entreprises ont besoin de beaucoup de serveurs pour gérer leurs données, gagner de l'espace est un véritable problème.
// +
Lorsque de nombreux serveurs sont empilés ensemble et mis dans une grande armoire, cela s'appelle un *rack*(((serveur, rack de))) de serveurs, et ressemble à ceci :

image::rack.jpg[pdfwidth = "40%", align = "center", title = "Un rack de serveurs", book = "keep"]
{nbsp} +

Lorsque tous les racks de serveurs sont placés dans la même pièce, cela s'appelle un *data center*(((serveur, data center))) et ressemble à ceci:

image::datacenter.jpg[pdfwidth = "40%", align = "center", title = "Un centre de données", book = "keep"]
{nbsp} +

Pour avoir une idée de la façon dont "le cloud" est réellement un espace physique, regardez cette vidéo montrant une visite d'un centre de données chez Google :

video::XZmGGAbHqa0[youtube]
{nbsp} +

Habituellement, jusqu'en 2005 à peu près, les entreprises avaient deux options:

- acheter leurs propres serveurs et les utiliser dans leurs locaux (sur leur site).
- payer les services de sociétés spécialisées dans la gestion de centres de données.

Ensuite, le "cloud" a changé cela.

== 2. Le cloud
Le terme * cloud *(((cloud, définition))) a été rendu populaire par ((Amazon)) avec leur service "Amazon Elastic Compute Cloud" : *Amazon EC2*(((Amazon, EC2))) lancé en 2006. Ce service était nouveau à bien des égards :

// +
- on ne loue plus un serveur en particulier, mais on achète à Amazon du "temps d'utilisation de serveur, doté d'une certaine puissance". En pratique, pour  livrer ce service, Amazon pourra mettre en route 1 gros serveur, ou 2 petits, ou attribuer juste la moitié d'un énorme serveur partagé avec un autre client : cela est géré de façon transparente pour le client. Cette façon de découpler le service rendu à l'utilisateur des ressources sous-jacentes s'appelle la *virtualisation*. *Ce n'est donc plus la location de tel ou tel serveur qui est facturée mais le temps d'utilisation d'un service correspondant à telle rapidité de calcul, telle capacité de stockage, etc.*
- on met l'accent sur la facilité d'utilisation : pas besoin de connaître les détails techniques de ces serveurs (comment ils sont branchés, comment ils sont configurés ...)
// +
- besoin d'un simple identifiant +  mot de passe pour commencer à utiliser ces serveurs.
- c'est "élastique": si le besoin du client évolue et qu'un serveur plus puissant devient nécessaire, ou plus d'espace de stockage, cela est pris en compte sur la facturation sans que les aspects techniques de ces changements ne soient venus ralentir la fourniture du service. Pas besoin de signer un nouveau contrat ou d'évaluer si Amazon bien des serveurs ou disques durs disponibles à la location ... le service est dimensionné pour que le changement soit possible et instantané.
// +
Comparons une situation avec ou sans ((cloud)) :

// +
[width = "100%"]
|=====
| *Sans le cloud* | *Avec le cloud*
| Vous faites une étude de marché pour quel serveur acheter

Obtenez l'approbation de votre service financier pour l'acheter (c'est un actif fixe!)

Attendez que le serveur soit expédié

Installez-le et configurez-le

Maintenez-le (sécurité, etc.)

|Sur le site https://aws.amazon.com/ec2/?nc1=h_ls[Amazon 'EC2], vous cliquez pour choisir un type de serveur parmi ceux proposés : c'est *sur demande*

Vous exécutez votre travail dessus.
Les coûts sont mesurés avec précision.

Pas de maintenance, pas de sécurité à gérer: tout cela est effectuté par le cloud provider.
|=====


// +
[width = "100%"]
|=====
| *Sans le cloud* | *Avec le cloud*
Quand le travail est terminé: que faites-vous avec votre serveur? C'est un coût irrécupérable.

Si le travail nécessite plus de capacité de calcul que votre serveur ne l'offre: vous êtes coincé avec votre trop petit serveur!

|Lorsque votre travail est terminé, vous arrêtez le serveur avec un clic et payez la facture.

Si le travail nécessite plus de capacité de calcul, vous passez à un serveur plus grand en un seul clic, ou vous pouvez le faire automatiquement: c'est *elastic*.
| C'est un capex | C'est un opex
|=====

// +
Le cloud peut s'intégrer dans le budget en tant que dépense opérationnelle au lieu d'une dépense en capital.
Les Opex ne sont pas intrinsèquement une option meilleure ou moins chère qu'un Capex, mais ils sont plus faciles à intégrer pour une équipe de projet ou une unité d'affaires dans leur budget.
Voir cet article sur http://gevaperry.typepad.com/main/2009/01/accounting-for-clouds-stop-saying-capex-vs-opex.html[opex et capex dans le contexte du cloud], en particulier les commentaires critiques en réponse, pour continuer cette discussion.

== 3. Le cloud : à quoi cela sert-il? IaaS, PaaS, SaaS
A quoi sert le cloud pour une entreprise? Les entreprises peuvent externaliser leurs opérations sur le cloud plutôt que de les exécuter chez elles, en utilisant leurs propres ressources.

// +
Quels types d'opérations peuvent être externalisés vers le cloud?

Les entreprises peuvent ne déléguer que l'infrastructure informatique de base ou les opérations informatiques les plusau coeur de leurs activités.
Ces différents degrés peuvent être décrits avec le *"modèle de pizza"*  (source: https://www.linkedin.com/pulse/20140730172610-9679881-pizza-as-a-service/[source]):

image::pizza-as-a-service.jpg[align = "center", title = "Pizza as a service", book="keep"]
{nbsp} +

Ce schéma montre qu'en tant qu'entreprise, vous pouvez soit exécuter toutes les opérations vous-même ("made at home"), soit tout déléguer ("diner au restaurant").
Chacun de ces degrés d'externalisation a un nom:

// +
*Infrastructure en tant que service* (Infrastucture as a Service, IaaS)

Ici, le cloud est utilisé pour remplacer les besoins en infrastructure informatique locale de l'entreprise. Par exemple, au lieu de stocker ses données dans une base de donnée sur place, on loue un service de stockage de données sur le cloud, qui sera facturé précisément au temps d'utilisation, à la taille de données stockées, et au volume de données écrites ou transférées (comme il s'agit d'un service de base de données, ce type de IaaS peut être appelé un DBaaS: database as a service).(((DBaaS: database as a service)))

// +
*Plate-forme en tant que service* (Platform as as Service, PaaS)

Le cloud est utilisé pour exécuter les blocs de construction d'un service: pour gérer un système de messagerie, pour héberger des applications, ...

// +
*Logiciel en tant que service* (Software as a Service, SaaS)

Le cloud est utilisé pour héberger un logiciel complet accessible "à la demande" via le navigateur.

Des exemples populaires sont Google Drive, https://www.d2l.com/products/learning-environment/[Brightspace] ou https://www.salesforce.com/fr/?ir=1[((SalesForce))].

== 4. Cloud privé ou public? cloud hybride?
- Amazon EC2(((Amazon, EC2))) est un exemple de *cloud public*(((cloud, cloud public))): il est accessible publiquement à tout client. Bien sûr, cela ne signifie pas que chaque client peut voir ce que les autres font sur le cloud! Chaque client a ses espaces privés sur le cloud.

- De nombreuses entreprises ont des exigences de sécurité qui les empêchent d'accéder aux clouds publics.
Ils ont besoin de leurs serveurs sur place.
// +
Dans ce cas, ils peuvent construire leur propre *cloud privé*:(((cloud, cloud privé))) c'est un cloud comme Amazon EC2, sauf qu'il est détenu, géré et utilisé par l'entreprise exclusivement - il n'est pas accessible à des tiers.
// +
Mais même privé, le cloud conserve les caractéristiques de base d'un cloud: à la demande et élastique notamment.

- *Les cloud ​​hybrides*(((cloud, cloud hybride))) sont une variété de clouds ​​privés: c'est un cloud privé où certaines formes d'opérations peuvent être déléguées à un cloud public.

// +
Par exemple, les opérations qui ne représentent pas un risque de sécurité et qui nécessitent une capacité de calcul supérieure à ce que le cloud privé de l'entreprise peut fournir.

== Pour aller plus loin
Retrouvez le site complet : https://seinecle.github.io/mk99/index-fr.html[ici].

image:round_portrait_mini_150.png[align="center", role="right"]

Clement Levallois

Découvrez mes autres cours et projets : https://www.clementlevallois.net

Ou contactez-moi via Twitter: https://www.twitter.com/seinecle[@seinecle]
einecle]
