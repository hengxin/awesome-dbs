# Resources - Apache Solr

- 来源: https://solr.apache.org/resources.html
- 归档时间: 2026-10-29
- 说明: 官方文档页面的 Markdown 快照（由 HTML 转换，格式为自动生成）

---

-
[](/)
- [Menu](#)
-
[Docs](https://solr.apache.org/guide/solr/latest/)
-
[Learn](/features.html)
- [Features](/features.html)
- [Resources](/resources.html)
-
[Security](/security.html)
-
[About](/community.html)
- [Community](/community.html)
- [Project](/whoweare.html)
- [News](/posts.html)
-
[Solr Operator](/operator/)
-
[Download](/downloads.html)
# Resources
Find everything you need about Solr ™ here.
[Tutorials](#tutorials)
[Docs](#documentation)
[Helm Charts](#helm-charts)
[Books](#solr-books)
[Presentations](#presentations)
[Videos](#videos)
## Tutorials[¶](#tutorials)
-
[Solr Quick Start](/guide/solr-tutorial.html)
-
[Solr on Docker](/guide/solr/latest/deployment-guide/solr-in-docker.html)
-
[Solr on Kubernetes](/operator/resources.html#tutorials)
Users who have completed the tutorial are encouraged to review the [other documentation available](#documentation).
## Documentation[¶](#documentation)
### The Apache Solr Reference Guide
-
[Solr Reference Guide](/guide)
-
[Visual Guide to Streaming Expressions and Math Expressions](http://bit.ly/32srTpA)
### Solr Javadocs
Solr generates JavaDocs for all included code in each release.
Copies of this documentation for every release can be found online:
- [Latest Release](/api/index.html)
### Additional Documentation
Additional documentation can be found on the [Solr Community Wiki](https://cwiki.apache.org/confluence/display/solr) or the various [books published about Solr](#solr-books).
## Helm Charts[¶](#helm-charts)
If you want to run Solr on Kubernetes, the easiest way to get started is via installing the Helm charts below.
- [Solr Operator](/operator) - A management layer that runs independently in Kubernetes. Only deploy 1 per Kubernetes cluster or namespace.
- Solr - A SolrCloud cluster. In order to deploy this Helm chart successfully, you must first install the Solr Operator and Solr CRDs. Follow the instructions on the ArtifactHub page below.
## Solr Books[¶](#solr-books)
If you have a Solr book that you would like to see listed here, please [edit this website and submit a Pull Request](/editing-website.html).
### How Large Language Models Can Help Your Search Project [2025]
[](https://link.springer.com/book/10.1007/978-3-032-01563-1) [Alessandro Benedetti](https://www.linkedin.com/in/alexbenedetti/) and [Sease](https://www.sease.io) are proud to introduce the book, "[How Large Language Models Can Help Your Search Project](https://link.springer.com/book/10.1007/978-3-032-01563-1)".
The primary scope of this book is to communicate the current state of the art of large language model applications in the domain of information retrieval and search with a pragmatic perspective on industrial adoption via open source software.
To this end, the book is organised in three parts: “Large Language Models” gives an introduction to artificial intelligence and large language models, including an overview of open source and commercial options. Next, “Large Language Models and Search” describes techniques and strategies to integrate large language models in search projects, including how to choose the right model for a specific use case and how to avoid the classic mistakes that can happen in the process. Eventually, “How to Use Open Source Software to Interact with Large Language Models” gives an overview of open source technologies to interact with large language models and gives a detailed survey of how the most popular open source search engines support them.
The book lays the foundations, deeply analyses the building blocks and shows examples how to implement the ideas described. It highlights both the positives, negatives and possible mitigations of the limitations. This way, it caters primarily software engineers, data scientists and practitioners in artificial intelligence or information retrieval who are curious to learn about the latest trends, research and industrial applications related to search and large language models.
The book has a chapter dedicated to Apache Solr, exploring the ways you can interact with Large Language Models related features, specifically:
- dense vector search, quantisation and nested vectors
- text vectorisation using LLM fine tuned for sentence similarity
- Intro to Future features such as Retrieval augmented generation, Semantic highlighting and LLM query parser
[Buy Here](https://link.springer.com/book/10.1007/978-3-032-01563-1)
### Inside Apache Solr and Lucene: Algorithms and Engineering Deep Dive [2025]
[](https://testmysearch.com/books/inside-solr.html)[Rauf Aliev](https://www.linkedin.com/in/raufaliev/) is proud to announce his book, "[Inside Apache Solr and Lucene: Algorithms and Engineering Deep Dive](https://testmysearch.com/books/inside-solr.html)". This book dives deep into the core of Apache Solr and Lucene, offering answers from a system engineer's perspective. It explores the architectural decisions, data structures, and algorithms that enable these world-class search platforms to deliver exceptional performance and scalability, providing a blueprint for designing high-performance systems.
What sets this book apart is its focus on the 'why' behind the 'how'. It follows an engineering-first approach, often starting with a core problem (like high memory usage or slow queries), examining naive solutions, and then detailing the specific data structures and underlying algorithms Solr and Lucene's developers implemented. This deep dive covers not just the inverted index, but the inner workings of Finite-State Transducers (FSTs), Pulsing Codecs, HNSW for vector search, Roaring Bitmaps, Delta Encoding, Skip Lists, PackedInts, LZ4 compression, Memory-Mapped I/O, and SIMD vectorization.
The insights in this book extend beyond the Solr and Lucene ecosystem. By using these platforms as a masterclass in pragmatic engineering, it offers valuable lessons for building any complex, data-intensive application. This book breaks down these complex systems, distilling years of development and thousands of lines of code into core principles and patterns. It's an opportunity to learn from the architectural choices of high-load systems, offering useful information for architects and engineers. Paperback and e-book versions are available. A preview of the first part of the book is also available for download.
[Look inside and buy here](https://testmysearch.com/books/inside-solr.html)
### Relevant Search [2016]
Doug Turnbull, John Berryman and Manning Publications are proud to announce Relevant Search .
This book demystifies relevance work and shows you that a search engine is a programmable relevance framework. You'll learn how to apply Elasticsearch or Solr to your business' unique ranking problems. The book demonstrates how to program relevance and how to incorporate secondary data sources, taxonomies, text analytics, and personalization. By the end, you’ll be able to achieve a virtuous cycle of provable, measurable relevance improvements over a search product’s lifetime.
[Buy here](https://www.manning.com/books/relevant-search) (Use code relsepc for 40% discount)
### Apache Solr Enterprise Search Server, 3rd Edition [2015]
[David Smiley](https://www.linkedin.com/in/davidwsmiley), [Eric Pugh](https://www.linkedin.com/in/epugh), [Kranti Parisa](https://www.linkedin.com/in/krantiparisa), and [Matt Mitchell](https://www.linkedin.com/in/mattmitchell4) are proud to finally announce the book “[Apache Solr Enterprise Search Server, Third Edition](http://www.solrenterprisesearchserver.com)” by [Packt Publishing](https://www.packtpub.com/). You can find links to buy it at Packt’s site & Amazon from our book’s official website: [solrenterprisesearchserver.com](http://www.solrenterprisesearchserver.com). You'll find a useful search parameter quick-reference sheet (the appendix) online there too.
[](http://www.solrenterprisesearchserver.com)
Apache Solr Enterprise Search Server, Third Edition is a comprehensive resource to almost everything Solr has to offer. It serves the reader right from initiation to development to deployment. It also comes with complete running examples to demonstrate its use and show how to integrate Solr with other languages and frameworks — even Hadoop.
By using a large set of metadata, including artists, releases, and tracks, courtesy of the MusicBrainz.org project, you will have a testing ground for Solr and will learn how to import this data in various ways. You will then learn how to search this data in different ways, including Solr's rich query syntax and boosting match scores based on record data. Finally, we'll cover various deployment considerations to include indexing strategies and performance-oriented configuration that will enable you to scale Solr to meet the needs of a high-volume site.
Solr 4 was Solr's biggest release ever. We updated the previous edition to cover Solr 4, and some of Solr 5 -- particularly the part of Solr 5 that needs to be covered most, the bin/solr script. Chapter 9, Integrating Solr, now covers Hadoop integration, and better covers SolrJ. Chapter 3, Text Analysis, introduces various approaches for implementing Multilingual Search in your applications. And we think you'll appreciate the enhanced coverage of the topic of query auto-suggesters (AKA query completion) in Chapter 8, Search Components -- a feature that is important to most search applications. This edition has two additional authors, Kranti & Matt, who add their perspectives based on their experience working with Solr for a long time.
[Buy here](http://www.solrenterprisesearchserver.com)
### Scaling Big Data with Hadoop and Solr - Second Edition [2015]
[Hrishikesh Karambelkar](https://www.linkedin.com/in/hrishik/) is proud to announce the book "[Scaling Big Data with Hadoop and Solr - Second Edition](https://www.packtpub.com/big-data-and-business-intelligence/scaling-big-data-hadoop-and-solr-second-edition)" by [Packt Publishing](https://www.packtpub.com/). This book will help the readers understand, design, build, and optimize their big data search engine with Hadoop and Apache Solr.
[](https://www.packtpub.com/big-data-and-business-intelligence/scaling-big-data-hadoop-and-solr-second-edition)
Scaling Big Data with Hadoop and Solr - Second Edition is aimed at developers, designers, and architects who would like to build big data enterprise search solutions for their customers or organizations. It explores the different approaches to making Solr work on big data ecosystems apart from Apache Hadoop.
A practical guide that covers interesting, real-life cases for big data search along with sample code targetted to help the readers to improve search performance while working with big data.
Click [here](https://www.packtpub.com/big-data-and-business-intelligence/scaling-big-data-hadoop-and-solr-second-edition) to read more about the Scaling Big Data with Hadoop and Solr - Second Edition
### Apache Solr Search Patterns [2015]
[Jayant Kumar](https://www.linkedin.com/in/jayantkumar) is proud to announce the book "[Apache Solr Search Patterns](http://bit.ly/1J2neZ9)" by [Packt Publishing](https://www.packtpub.com/). This book is for developers who have prior knowledge on Solr and are looking at procuring advanced strategies for improving their search using Solr. Also, if you work with analytics to generate graphs and reports using Solr and you are a search architect who is looking forward to scale your search using Solr, then this book is a perfect guide for you.
[](http://bit.ly/1J2neZ9)
Apache Solr Search Patterns begins with a brief introduction of analyzers and tokenizers to understand the challenges associated with implementing large-scale indexing and multilingual search functionality. It then moves on to working with custom queries and understanding how filters work internally. While doing so, it also helps the readers create their own query language or Solr plugin that does proximity searches.
Furthermore, the book discusses how Solr can be used for real-time analytics and tackle problems faced during its implementation in e-commerce search. It then dives into the spatial features such as indexing strategies and search/filtering strategies for a spatial search. And also do an in-depth analysis of problems faced in an ad serving platform and how Solr can be used to solve these problems.
Click [here](http://bit.ly/1J2neZ9) to read more about the Apache Solr Search Patterns
### Solr Cookbook - Third Edition [2015]
[Rafał Kuć](https://pl.linkedin.com/in/rafalkuc) is proud to finally announce the book "[Solr Cookbook - Third Edition](http://bit.ly/1Q2AGS8)" by [Packt Publishing](https://www.packtpub.com/). This edition will specifically appeal to developers who wish to quickly get to grips with the changes and new features of Apache Solr 5.
[](http://bit.ly/1Q2AGS8)
Solr Cookbook - Third Edition has over 100 easy to follow recipes to solve real-time problems related to Apache Solr 4.x and 5.0 effectively. Starting with vital information on setting up Solr, the developer will quickly progress to analyzing their text data through querying and performance improvement. Finally, they will explore real-life situations, where Solr can be used to simplify daily collection handling.
With numerous practical chapters centered on important Solr techniques and methods Solr Cookbook - Third Edition will guide intermediate Solr Developers who are willing to learn and implement Pro-level practices, techniques, and solutions.
Click [here](http://bit.ly/1Q2AGS8) to read more about the Solr Cookbook - Third Edition.
### Mastering Apache Solr [2014]
[Mathieu Nayrolles](https://www.linkedin.com/in/mathieun) and Inkstall Publications are proud to announce their latest book — [Mastering Apache Solr](http://www.amazon.com/Mastering-Apache-Solr-practical-guide/dp/8192784509). This book will empower you to provide a world-class search experience to your end users through the discovery of the powerful mechanisms presented in it.
[](http://www.amazon.com/Mastering-Apache-Solr-practical-guide/dp/8192784509)
Mastering Apache Solr is a short, focused, practical, hands-on guide containing crisp, relevant, systematically arranged, progressive chapters. These chapters contain a wealth of information presented in a direct and easy-to-understand manner. Highlighting Solr's supremacy over classical databases in full-text search, this book covers key technical concepts which will help you accelerate your progress in the Solr world.
Mastering Apache Solr starts with an introduction to Apache Solr, its underlying technologies, the main differences between the classical database engines, and gradually moves to more advance topics such as boosting performance. In this book, we will look under the hood of a large number of topics and discuss answers to pertinent questions such as why denormalize data, how to import classical databases' data inside Apache Solr, how to serve Solr through five different web servers, how to optimize them to serve Solr even faster. An important and major topic covered in this book is Solr's querying mechanism, which will prove to be a strong ally in our journey through this book. We then look at boosting performance and deploying Solr using several servlet servers. Finally, we cover how to communicate with Solr using different programming languages, before deploying it in a cloud-based environment.
Mastering Apache Solr is written lucidly and has a clear simple approach. From the first page to the last, the book remains practical and focuses on the most important topics used in the world of Apache Solr without neglecting important theoretical fundamentals that help you build a strong foundation.
[Buy here](http://www.amazon.com/Mastering-Apache-Solr-practical-guide/dp/8192784509)
### Solr in Action [2014]
Trey Grainger, Timothy Potter, and Manning Publications are proud to announce [Solr in Action](http://solrinaction.com), a comprehensive (638 pg.), example-driven guide covering through Solr 4.7.
[](http://solrinaction.com)
Solr in Action is an essential resource for implementing fast and scalable search using Apache Solr. It uses well-documented examples ranging from basic keyword searching to scaling a system for billions of documents and queries. With this book, you’ll gain a deep understanding of how to implement core Solr capabilities such as faceted navigation through search results, matched snippet highlighting, field collapsing and search results grouping, spell-checking, query autocomplete, querying by functions, and more. You’ll also see how to take Solr to the next level, with deep coverage of large-scale production use cases, sophisticated multilingual search, complex query operations, and advanced relevancy tuning strategies.
[Buy here](http://solrinaction.com)
### Einführung in Apache Solr [2014]
[](https://www.oreilly.com/library/view/einfuhrung-in-apache/9783955614249/)
Markus Klose, Daniel Wrigley and O’Reilly are proud to present the first book on Apache Solr in German.
[Einführung in Apache Solr](https://www.oreilly.com/library/view/einfuhrung-in-apache/9783955614249/) offers a substantiated and practice-oriented introduction into the search technology Apache Solr. The sample configurations, instructions, tips and pitfalls from the practice of the authors enable the reader to get a quick insight to this search technology. The book provides the necessary knowledge and tools to implement custom search solutions with Apache Solr, covering the following topics:
- Quick start guide : Start Apache Solr after download and execute your first search.
- Index configuration : Learn how to configure the schema.xml and the analysis process to improve search quality.
- Features out-of-the-box : Use all build-in features like faceting, auto suggest or spellcheck and integrate them into a search user interface.
- Scoring and relevance : Learn how to influence the scoring mechanism to bias the quantity and quality of your hitlist.
- Solr architectures : Read about the options scaling Apache Solr. Set up your own Solr Cluster as Master/Slave or SolrCloud architecture.
[Buy here](https://www.oreilly.com/library/view/einfuhrung-in-apache/9783955614249/)
### Instant Apache Solr for Indexing Data How-to [2013]
[](https://www.amazon.com/Instant-Apache-Solr-Indexing-Data/dp/1782164847)
Alexandre Rafalovitch and Packt Publishing are proud to announce [Instant Apache Solr for Indexing Data How-to](https://www.amazon.com/Instant-Apache-Solr-Indexing-Data/dp/1782164847) - an example-driven guide that will take you on a journey from the basic collection of data to a multi-lingual, multi-field, multi-type schema.
Content and data searching is a very important part of the modern user experience, and before something can be searched, it has to be indexed. Indexing is a hidden part of the process that has a surprisingly strong impact on the overall user experience. From speed, to faceting, to multilingual support, everything depends on correct indexing. Instant Apache Solr for Indexing Data How-to is a friendly, practical guide that will show you how to index your data with Solr 4.3.
[Buy here](https://www.amazon.com/Instant-Apache-Solr-Indexing-Data/dp/1782164847)
### Apache Solr 4 Cookbook [2013]
[](http://www.packtpub.com/apache-solr-4-cookbook/book)
Rafał Kuć and Packt Publishing are proud to announce the second edition of [Apache Solr 4 Cookbook](http://www.packtpub.com/apache-solr-4-cookbook/book). The Cookbook is newly updated and improved with new chapters on SolrCloud and every chapter updated to Solr 4.
Apache Solr 4 Cookbook features over 100 recipes to make Apache Solr faster, more reliable, and return better results. It will show you how to get the most out of your search engine. Full of practical recipes and examples, this book will show you how to set up Apache Solr, tune and benchmark performance as well as index and analyze your data to provide better, more precise, and useful search data.
The book will make your search better, more accurate and faster with practical recipes on essential topics such as SolrCloud, querying data, search faceting, text and data analysis, and cache configuration.
With numerous practical chapters centered on important Solr techniques and methods, Apache Solr 4 Cookbook is an essential resource for developers who wish to take their knowledge and skills further. Thoroughly updated and improved, this Cookbook also covers the changes in Apache Solr 4 including the awesome capabilities of SolrCloud.
[Buy here](http://www.packtpub.com/apache-solr-4-cookbook/book)
### Taming Text [2012]
[](http://www.manning.com/ingersoll/)
Taming Text is a hands-on, example-driven guide to working with unstructured text in the context of real-world applications. This book explores how to automatically organize text using approaches such as full-text search with Apache Solr (v3), proper name recognition,
clustering, tagging, information extraction, and summarization. The book guides you through examples illustrating each of these topics, as well as the foundations upon which they are built. Source code
is available on [Github](https://github.com/tamingtext/book).
[Buy here](http://www.manning.com/ingersoll/)
### Apache Solr 3.1 Cookbook [2011]
[](http://www.packtpub.com/solr-3-1-enterprise-search-server-cookbook/book)
Rafał Kuć is proud to introduce a new book on Solr, [Apache Solr 3.1 Cookbook](http://www.packtpub.com/solr-3-1-enterprise-search-server-cookbook/book) from Packt Publishing.
Apache Solr 3.1 Cookbook will make your everyday work easier by using real-life examples that show you how to deal with the most common problems that can arise while using the Apache Solr search engine.
This cookbook will show you how to get the most out of your search engine. Each chapter covers a different aspect of working with Solr from analyzing your text data through querying, performance improvement, and developing your own modules. The practical recipes will help you to quickly solve common problems with data analysis, show you how to use faceting to collect data and to speed up the performance of Solr. You will learn about functionalities that most newbies are unaware of, such as sorting results by a function value, highlighting matched words, and computing statistics to make your work with Solr easy and stress free.
[Buy here](http://www.packtpub.com/solr-3-1-enterprise-search-server-cookbook/book)
## Presentations[¶](#presentations)
If you have a Solr presentation that you would like to see listed here, please submit a [patch](https://github.com/apache/solr/blob/main/CONTRIBUTING.md) via a JIRA with the appropriate content.
### Slideshare
[Search Slideshare for Solr](http://www.slideshare.net/search/slideshow?&q=solr)
## Videos[¶](#videos)
If you have a Solr video that you would like to see listed here, please [edit this website and submit a Pull Request](/editing-website.html).
### Conferences with Solr talks
[Videos from Past ApacheCon events](https://www.youtube.com/c/TheApacheFoundation/search?query=lucene%20solr)
[Videos from Past Activate / Lucene/Solr revolution events](https://www.activate-conf.com/more-events)
[Videos from past Berlin Buzzwords events](https://www.youtube.com/c/PlainSchwarzUG/playlists?view=50&sort=dd&shelf_id=1)
[Videos from past Haystack events (search relevance)](https://www.youtube.com/channel/UCiuXt-f2Faan4Es37nADUdQ/playlists)
[Videos from Lucidwork's Lucene Eurocon](https://vimeo.com/search?q=lucene%20eurocon)
[Videos from past London Information Retrieval & AI Meetups](https://www.youtube.com/playlist?list=PL3MGdCOBPhsccrQRGrUjQlzRSdlWrcF9N)
### YouTube
[Search YouTube for Solr](https://www.youtube.com/results?search_query=solr)
### Vimeo
[Search Vimeo for Solr](http://vimeo.com/search?q=solr)
#### Features
- [Overview](/features.html)
- [Data Handling](/features.html#data-handling)
- [Querying](/features.html#query)
- [Faceting](/features.html#facets)
- [Discovery](/features.html#discovery)
- [Plugins and Extensions](/features.html#plugins)
- [Statistics and Aggregations](/features.html#stats)
- [Spatial](/features.html#spatial)
- [Rich Content](/features.html#rich-content)
- [Performance](/features.html#performance)
- [Scaling with SolrCloud](/features.html#solrcloud)
- [User Interface](/features.html#admin-ui)
#### Resources
- [Tutorial](/resources.html#tutorials)
- [Docs](https://solr.apache.org/guide/solr/latest/)
- [Books](/resources.html#solr-books)
- [Presentations](/resources.html#presentations)
- [Videos](/resources.html#videos)
- [Solr Logos and Assets](/logos-and-assets.html)
- [Editing this Website](/editing-website.html)
- [Apache Software Foundation](https://www.apache.org/)
- [Thanks](https://www.apache.org/foundation/thanks.html)
- [Sponsorship](https://www.apache.org/foundation/sponsorship.html)
- [Security](https://www.apache.org/security/)
- [License](https://www.apache.org/licenses/)
#### Get Started
- [Download](/downloads.html)
- [Run Through the Tutorial](/guide/solr-tutorial.html)
- [Level Up](/resources.html)
#### Community
- [Support](/community.html#support)
- [Mailing Lists](/community.html#mailing-lists-irc)
- [Issues (JIRA)](/community.html#issue-tracker)
- [Contribute](/community.html#how-to-contribute)
- [Version control (GIT)](/community.html#version-control)
#### Related Projects
- [Apache Lucene](http://lucene.apache.org/)
- [Apache Zookeeper](http://zookeeper.apache.org/)
- [Apache Tika](http://tika.apache.org/)
- [Apache ManifoldCF](http://manifoldcf.apache.org/)
- [Apache Spark](http://spark.apache.org/)
- [Apache Nutch](http://nutch.apache.org/)
- [Apache Zeppelin](http://zeppelin.apache.org/)
- [Apache OpenNLP](http://opennlp.apache.org/)
Copyright © 2026 The Apache Software Foundation, Licensed under the
[Apache License, Version 2.0](https://www.apache.org/licenses/LICENSE-2.0). [Privacy Policy](https://privacy.apache.org/policies/privacy-policy-public.html)
Apache and the Apache logo are trademarks of The Apache Software Foundation. Apache Lucene,
Apache Solr and their respective logos are trademarks of the Apache Software Foundation.
Please see the [Apache Trademark Policy](https://www.apache.org/foundation/marks/) for more information.
All non-Apache logos are the trademarks of their respective owners.