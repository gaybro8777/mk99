= A primer on network analysis for business
Clément Levallois <levallois@em-lyon.com>
2017-12-08

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


== 1. Definitions
//ST: 1. Definitions

//ST: !
A network is a dataset made of entities [underline]#and their relations#

Scientists use the term "graph" to discuss networks.

//ST: !
image::network-1.png[align="center", title="This is a network"]
{nbsp} +

//ST: !
=== a. Social networks

//ST: !
As users, we are very familiar with one type of networks - social networks:

image:facebook.png[width=150]
image:twitter.jpg[width=150]
image:weibo.png[width=150]
image:instagram.jpg[width=150]
image:snapchat.png[width=150]
image:wechat.jpg[width=150]
image:linkedin.png[width=150]

//ST: !
.A social network, visualized
[link=http://www.minanacheva.com/getting-visual-with-facebook-data/]
image::colored-network.png[align="center", title="source: http://www.minanacheva.com/getting-visual-with-facebook-data/"]
{nbsp} +


//ST: !
=== b. Other networks

//ST: !
It is important to realize that networks cover more than relations between humans:

//ST: !
For example, it is possible to imagine a network made out of cooking recipes.
2 ingredients are connected if they appear frequently in the same recipes.

Scanning all recipes and their ingredients from a website of cooking recipes, this gives:

//ST: !
[link=http://arxiv.org/abs/1111.3919]
image::ingredients-network.png[align="center", title="source: http://arxiv.org/abs/1111.3919"]
{nbsp} +

//ST: !
Semantic networks are another broad category of networks.
The method is the same: we need to find a way to "relate" wors in a text, then we get a network.

//ST: !
The general idea is the same as in cooking recipes: 2 terms of a text will be connected in the network if they frequently appeared in same paragraphs.

//ST: !
[link=http://www.nature.com/nature/journal/v463/n7278/full/463157a.html]
image::editorials.png[align="center", title="source: http://www.nature.com/nature/journal/v463/n7278/full/463157a.html"]
{nbsp} +

//ST: !
=== c. How big can networks be?

//ST: !
With a surge in computing power in the age of big data, and the adequate NOSQL databases (such as https://neo4j.com/[Neo4J] or http://orientdb.com/orientdb/[OrientDB]), we can deal with huge networks:

//ST: !
For example, https://www.facebook.com/notes/facebook-data-science/anatomy-of-facebook/10150388519243859/[“The Anatomy of the Facebook Social Graph” (2011)]

-> study of 721 million active Facebook users and the 69 billion (!) friendship links connecting them.

//ST: !
A limit is quickly reached in terms of visualization: it is hard to fit millions of nodes on a screen.
In the next visualization, we can see a network of 90,000 Swedish speakers and their relations on Twitter. The view is very cluttered.

(open the source for an interactive version)

//ST: !
[link=http://twittercensus.se/graph2015/]
image::swedish.png[align="center", title="source: http://twittercensus.se/graph2015/"]
{nbsp} +


//ST: !
=== d. How to discuss networks? Some vocabulary

//ST: !
image::Terminology.png[align="center",title="Terminology"]
{nbsp} +

== 2. Networks: what use for business?
//ST: 2. Networks: what use for business?

//ST: !
=== a. Segmentation
//ST: !

If a network is made of entities and their relations, then a segment is a subgroup of entities in the network, which has some cohesion or something in common.

This subgroup of nodes in the network is often called a "*community*".

//ST: !
Detecting communities in a network, also called "clustering", consists in finding nodes that have many connections in common.

//ST: !
This is a mathematical and algorithmic procedure, but it is very simple to understand visually:

//ST: !
image::segmentation-with-community-detection-in-networks.png[align="center", title="segmentation with community detection in networks"]
{nbsp} +

//ST: !
=== b. Finding key players
//ST: !

image::Key-players-visualized-by-resizing-nodes.png[align="center", title="Key players visualized by resizing nodes"]
{nbsp} +

//ST: !
=== c. Understanding how information spreads

//ST: !
A data science company created "Where does my tweet go", which traces how a given tweet spreads through retweets.

//ST: !
The service is now discontinued (Twitter data was too expensive to buy) but the mechanism can be explained:

//ST: !
[link=https://mfglabs.com/works/where-does-my-tweet-go/]
image::WDMTG-by-MFGLabs.png[align="center", title="WDMTG by MFGLabs"]
{nbsp} +


//ST: !
=== d. Identifying patterns - for fraud detection, control or intelligence.

//ST: !
In the following video, we see participants in the money market (short term loans between banks) in Europe.

2 banks are connected if one lends to the other. The pattern of exchanges shifts through years - banks withdraw from the market.

//ST: !
video::YvauCrHGWYc[youtube]

//ST: !
(the full study is available here: https://www.dnb.nl/en/binaries/Working%20Paper%20418_tcm47-305800.pdf)


//ST: !
Another example: connecting seemingly unrelated measures of business performance with https://www.oracle.com/solutions/business-analytics/business-intelligence/index.html[Oracle BI] and https://linkurio.us/[Linkurious]:

//ST: !
video::KBIZoUikfwo[youtube]


== 3. To go further
//ST: To go further

//ST: !
(if viewing from a screen you can click on the covers to get to the Amazon page)

//ST: !
image:golbeck.jpg[width=150,link=https://www.amazon.com/Analyzing-Social-Web-Jennifer-Golbeck/dp/0124055311]
image:nodexl.jpg[width=150,link=https://www.amazon.com/Analyzing-Social-Media-Networks-NodeXL/dp/0123822297]
image:newman.jpg[widtht=150,link=https://www.amazon.com/Networks-Introduction-Mark-Newman/dp/0199206651]
image:barabasi.jpg[width=150,link=https://www.amazon.com/Network-Science-Albert-L-e1szl-f3-Barab-e1si/dp/1107076269]


//ST: !
You can also visit my tutorials on Gephi, the leading software to visualize large graphs:

https://seinecle.github.io/gephi-tutorials/

== The end
//ST: The end
//ST: !

Find references for this lesson, and other lessons, https://seinecle.github.io/mk99/[here].

image:round_portrait_mini_150.png[align="center", role="right"]
This course is made by Clement Levallois.

Discover my other courses in data / tech for business: https://www.clementlevallois.net

Or get in touch via Twitter: https://www.twitter.com/seinecle[@seinecle]
