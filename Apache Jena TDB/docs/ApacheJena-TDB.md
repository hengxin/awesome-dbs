# Apache Jena - TDB

- 来源: https://jena.apache.org/documentation/tdb/index.html
- 归档时间: 2026-10-29
- 说明: 官方文档页面的 Markdown 快照（由 HTML 转换，格式为自动生成）

---

[Apache Jena](/index.html)
- [Home](/index.html)
- [Download](/download/index.cgi)
-
[Docs](#)
- Tutorials
- [Overview](/tutorials/index.html)
- [Fuseki Triplestore](/documentation/fuseki2/index.html)
- [How-To's](/documentation/notes/index.html)
- [Manipulating SPARQL using ARQ](/documentation/query/manipulating_sparql_using_arq.html)
- [RDF core API tutorial](/tutorials/rdf_api.html)
- [SPARQL tutorial](/tutorials/sparql.html)
- [Using Jena with Eclipse](/tutorials/using_jena_with_eclipse.html)
-
- References
- [Overview](/documentation/index.html)
- [ARQ (SPARQL)](/documentation/query/index.html)
- [RDF I/O](/documentation/io/)
- [Assembler](/documentation/assembler/index.html)
- [Command-line tools](/documentation/tools/index.html)
- [Data with RDFS Inferencing](/documentation/rdfs/)
- [GeoSPARQL](/documentation/geosparql/index.html)
- [Inference API](/documentation/inference/index.html)
- [Ontology API](/documentation/ontology/)
- [Query Builder](/documentation/extras/querybuilder/index.html)
- [RDF API](/documentation/rdf/index.html)
- [RDF Connection - SPARQL API](/documentation/rdfconnection/)
- [RDF Patch](/documentation/rdf-patch/index.html)
- [SHACL](/documentation/shacl/index.html)
- [ShEx](/documentation/shex/index.html)
- [TDB2](/documentation/tdb2/index.html)
- [Text Search](/documentation/query/text-query.html)
-
[Javadoc](#)
- [All Javadoc](/documentation/javadoc.html)
- [ARQ](/documentation/javadoc/arq/)
- [Jena Core](/documentation/javadoc/jena/)
- [Jena OntAPI](/documentation/javadoc/ontapi/)
- [Fuseki](/documentation/javadoc/fuseki2/)
- [SHACL](/documentation/javadoc/shacl/)
- [ShEx](/documentation/javadoc/shex/)
- [TDB](/documentation/javadoc/tdb2/)
- [Text Search](/documentation/javadoc/text/)
- [Query Builder](/documentation/javadoc/extras/querybuilder/)
- [GeoSPARQL](/documentation/javadoc/geosparql/)
-
[Project](#)
- [Code](https://github.com/apache/jena)
- [Contributing](https://github.com/apache/jena/blob/main/CONTRIBUTING.md)
- [Security Policies](/security)
- [Security Advisories](/security/advisories.html)
- [Ask](/help_and_support/index.html)
-
[Get involved](#)
- [Contribute](/getting_involved/index.html)
- [Report a bug](/help_and_support/bugs_and_suggestions.html)
-
- Project
- [About Jena](/about_jena/about.html)
- [Citing](/about_jena/citing.html)
- [Project team](/about_jena/team.html)
- [Security](/security)
-
- ASF
- [Apache Software Foundation](https://www.apache.org/)
- [Become a Sponsor](https://www.apache.org/foundation/sponsorship.html)
- [License](https://www.apache.org/licenses/)
- [Thanks](https://www.apache.org/foundation/thanks.html)
- [Donate](https://www.apache.org/foundation/sponsorship.html)
- [Privacy](https://privacy.apache.org/policies/privacy-policy-public.html)
- [Edit this page](https://github.com/apache/jena-site/edit/main/source/documentation/tdb/__index.md)
- [DOCUMENTATION](/documentation)
- TDB
# TDB
## On this page
- [Documentation](#documentation)
TDB is a component of [Jena](https://jena.apache.org/) for RDF storage and
query. It supports the full range of Jena APIs. TDB can be used as a high
performance RDF store on a single machine. This documentation describes the
latest version, unless otherwise noted.
This is the documentation for the current standard version of TDB.
This is also called TDB1 to distinguish it from the next generation version
[TDB2](../tdb2/)
TDB1 and TDB2 databases are not compatible.
A TDB store can be accessed and managed with the provided command
line scripts and via the Jena API. When accessed using [transactions](tdb_transactions.html)
a TDB dataset is protected against corruption, unexpected process terminations and system crashes.
A TDB dataset should only be directly accessed from a single JVM at a time otherwise data corruption
may occur. From 1.1.0 onwards TDB includes automatic protection against multi-JVM usage which prevents this
under most circumstances.
If you wish to share a TDB dataset between multiple applications please use our
[Fuseki](../fuseki2/) component which provides a SPARQL server that
can use TDB for persistent storage and provides the SPARQL protocols
for query, update and REST update over HTTP.
## Documentation
- [Using TDB from Java through the API](java_api.html)
- [Command line utilities](commands.html)
- [Transactions](tdb_transactions.html)
- [Assemblers for Graphs and Datasets](assembler.html)
- [Datasets and Named Graphs](datasets.html)
- [Dynamic Datasets](dynamic_datasets.html): Query a subset of the named graphs
- [Quad filtering](quadfilter.html): Hide information in the dataset
- [The TDB Optimizer](optimizer.html)
- [TDB Configuration](configuration.html)
- [Value Canonicalization](value_canonicalization.html)
- [TDB Design](architecture.html)
- [Use on 64 bit or 32 bit Java systems](tdb_system.html)
- [FAQs](faqs.html)
## On this page
- [Documentation](#documentation)
Copyright © 2011–2026 The Apache Software Foundation, Licensed under the
[Apache License, Version 2.0](https://www.apache.org/licenses/LICENSE-2.0).
Apache Jena, Jena, the Apache Jena project logo, Apache and the Apache feather logos are trademarks of
The Apache Software Foundation.
[Apache Software Foundation Privacy Policy](https://privacy.apache.org/policies/privacy-policy-public.html).