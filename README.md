# Data-Science-and-Big-Data-Analytics
For the project, we give you access to a database we actively use for our research on open source software development. The database contains information collected from the version control system, the issue tracker, and the mailing lists of the projects. You can find a documentation of the available data online.

Your task
The database contains data for many Apache Projects. For your group projects, only the following 39 projects are relevant:

ant-ivy, archiva, calcite, cayenne, commons-bcel, commons-beanutils, commons-codec, commons-collections, commons-compress, commons-configuration, commons-dbcp, commons-digester, commons-io, commons-jcs, commons-jexl, commons-lang, commons-math, commons-net, commons-rdf, commons-scxml, commons-validator, commons-vfs, deltaspike, eagle, giraph, gora, jspwiki, kylin, lens, mahout, manifoldcf, nutch, opennlp, parquet-mr, santuario-java, systemml, tika, wss4j
Your task is to develop an automated model for clustering project popularity over time. The model should be designed so that it can be used on GitHub, for example, to showcase trending or popular projects for a specific period of time. How many labels are useful for clustering depends on your decision.

You have to frame these questions into an analytic problem. Then, you have to create models that can be used to answer the questions. You have to choose appropriate features from the available data for this and decide which kind of analytic approach to use. Finally, you have to evaluate how well your approach performs.

Group registrations
You have to work in groups of three people on this task. One member of each group must register the whole group via an email to Benjamin Ledel (benjamin.ledel@cs.uni-goettingen.de) until Friday, May 21th. If you are fewer than three people, you register the same way and we will assign you additional group members from other groups with less than three people on May 24th. This registration, as well as the successful participation of your group is a mandatory requirement for the participation in the exam!

Presentation and voting
All results must be presented in the final lecture on Jul 13th, which will already start at 10:00 o'clock. Each group must give four minute presentation. Within this presentation, you should briefly describe which data you analyzed, how you treated it, which models you used, and your key findings. The time available for the presentation depends on the number of groups and may be increased. This will be announced in July.

Afterwards, everybody in attendance will vote to determine the best project. Each group votes for the best project (3 points), second best (2 points), and third best (1 point). The one with the most points wins a price.

Submission of the presentation
In order to allow the presentation session to run smoothly, each group must submit their presentation beforehand. Send the presentation latest on Jul 9th, 10:00 o'clock to Benjamin Ledel via Email (benjamin.ledel@cs.uni-goettingen.de). The presentations must be PDF format. Other formats are not allowed.

Success criteria
The following criteria must be fulfilled by a project, such that the group members can participate in the exam:

A model for automated clustering of the project popularity.
An evaluation of the quality of the clustering model.
A recommendation on how the model could be used, including key benefits and risks.
The model must be applied to at least 30 projects from the database, which must all be considered for the evaluation.
A presentation of the results is given in the final lecture on Jul 13th.
Getting started
The cell below shows how to access the data with Python. Please note that the database is behind a firewall and can only be accessed from within the Goenet. If you cannot reach the database, just establish a connection to the VPN of the GWDG and it should be reachable.

WARNING: Because we also actively use the MongoDB in our research, there can sometimes be heavy load on the database. The database currently contains 3.3 Terabytes of data. Do not just randomly query the database, but fetch only the data you need. Otherwise you might easily try to download several Gigabytes of data. For example, if you want to fetch all information that is stored in the commit collection, you will download 127 Gigabytes of data.

Accessing the database with Python
You can use the pycoSHARK library for accessing the MongoDB. The pycoSHARK provides an ORM layer based on the mongoengine library. Alternatively, you can also access the database with native MongoDB queries using the pymongo API.

The code below shows how to use the database with the pycoSHARK.
