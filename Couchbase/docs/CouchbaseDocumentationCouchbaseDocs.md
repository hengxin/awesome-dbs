# Couchbase Documentation | Couchbase Docs

- 来源: https://docs.couchbase.com/
- 归档时间: 2026-10-29
- 说明: 官方文档页面的 Markdown 快照（由 HTML 转换，格式为自动生成）

---

-
[](https://www.couchbase.com)
-
[](https://docs.couchbase.com/home/index.html)
-
[](https://docs.couchbase.com/home/index.html)
-
[Start Here](start-here.html)
-
[Server](server.html)
-
[Self-Managed Server](server.html)
-
[Kubernetes Operator](../operator/current/overview.html)
-
[Cloud Native Gateway](../cloud-native-gateway/current/intro/about-cng.html)
-
[Fleet Manager](../fleet-manager/current/introduction.html)
-
[Operational SDKs](sdk.html)
-
[Capella](cloud.html)
-
[Capella Operational](cloud.html)
-
[Operational SDKs](sdk.html)
-
[Mobile / Edge](mobile.html)
-
[Couchbase Lite](../couchbase-lite/current/index.html)
-
[Edge Server](../couchbase-edge-server/current/introduction/intro.html)
-
[Sync Gateway](../sync-gateway/current/introduction.html)
-
[App Services](../app-services/get-started/configuring-app-services.html)
-
[Operational Insights](operational-insights.html)
-
[Operational Insights Enterprise](../operational-insights/current/intro/intro.html)
-
[Operational Insights Capella](../operational-insights-cloud/intro/intro.html)
-
[Operational Insights SDKs](operational-insights-sdk.html)
-
[Analytics SDKs](analytics-sdk.html)
-
[Operational Insights Connectors](analytics-connectors.html)
-
[AI Data Plane](../ai/get-started/intro.html)
Filters
No exact results for this search.
The following are variant spellings that might be useful.
[Search](../home/search.html)
[Downloads](https://www.couchbase.com/downloads)
[Try Free](https://cloud.couchbase.com/sign-up)
# For AI agents:
A documentation index is available at [/llms.txt](https://docs.couchbase.com/llms.txt).
Markdown versions of all docs pages are available by replacing `.html` with `.md`.
# Couchbase Documentation
######
Couchbase is the modern database for enterprise applications.
Couchbase is a distributed document database with a powerful search engine and in-built operational and analytical capabilities.
It brings the power of NoSQL to the edge and provides fast, efficient bidirectional synchronization of data between the edge and the cloud.
Find the documentation, samples, and references to help you use Couchbase and build applications.
######
// List the schedule of flights from Boston
// to San Francisco on JETBLUE
SELECT DISTINCT airline.name, route.schedule
FROM `travel-sample`.inventory.route
JOIN `travel-sample`.inventory.airline
ON KEYS route.airlineid
WHERE route.sourceairport = "BOS"
AND route.destinationairport = "SFO"
AND airline.callsign = "JETBLUE";
######
## Get Started
######
Couchbase Capella (DBaaS)
Explore Couchbase Capella, our fully-managed database as a service offering.
Take the complexity out of deploying, managing, scaling, and securing Couchbase in the public cloud.
Store, query, and analyze any amount of data — and let us handle more of the administration — all in a few clicks.
[Couchbase Capella](cloud.html)
Operational Insights Capella (RT-OLAP)
Operational Insights Capella is a real-time analytical database (RT-OLAP) for real time apps and operational intelligence.
Operational Insights Capella is a standalone, cloud-only offering from Couchbase under the Capella family of products.
[Operational Insights Capella](../operational-insights-cloud/intro/intro.html)
######
Couchbase Server
Explore Couchbase Server, a modern, distributed document database with all the desired capabilities of a relational database and more. It exposes a scale-out, key-value store with managed cache for sub-millisecond data operations, purpose-built indexers for efficient queries, and a powerful query engine for executing SQL-like queries.
[Couchbase Server](server.html)
Operational Insights Enterprise (RT-OLAP)
Operational Insights Enterprise is a self-managed analytical database (RT-OLAP) for real time apps and operational intelligence.
[Operational Insights](../operational-insights/current/intro/intro.html)
######
Couchbase Mobile
Couchbase Mobile brings the power of NoSQL to the edge.
The combination of Sync Gateway and Couchbase Lite coupled with the power of Couchbase Server provides fast, efficient bidirectional synchronization of data between the edge and the cloud.
Enabling you to deploy your offline-first mobile and embedded applications with greater agility on premises or in any cloud.
[Couchbase Lite](../couchbase-lite/current/index.html) |
[Sync Gateway](../sync-gateway/current/introduction.html) |
[Couchbase Edge Server](../couchbase-edge-server/current/introduction/intro.html)
The Couchbase AI Data Plane
The Couchbase AI Data Plane is a fully managed set of tools that help you build, deploy, and scale your agentic and retrieval-augmented generation (RAG) AI applications.
These tools integrate seamlessly with the Couchbase Capella cloud platform, enabling you to develop your AI applications on the same platform as your data.
[The Couchbase AI Data Plane](../ai/get-started/intro.html)
######
## Developer Tools
######
SDK and Connectors
Couchbase SDKs allow applications to access a Couchbase cluster and the big data Connectors enable data exchange with other platforms.
[Developer Docs](developer.html) |
[Operational SDKs](sdk.html) |
[Operational Insights SDKs](operational-insights-sdk.html) |
[Analytics SDKs](analytics-sdk.html)
######
CLI and REST APIs
Use the command-line interface (CLI) tools and REST API to manage and monitor your Couchbase deployment.
[Couchbase CLI](../server/current/cli/cli-intro.html) | [REST API](../server/current/rest-api/rest-intro.html)
######
Couchbase Shell
A modern shell to interact with Couchbase Server and Capella, now available.
[Explore Couchbase Shell](https://couchbase.sh)
######
## More Developer Resources
######
Developer Portal
Explore a variety of resources - sample apps, videos, blogs, and more, to build applications using Couchbase.
[Developer Portal](https://developer.couchbase.com)
[Developer Tutorials](https://developer.couchbase.com/tutorials)
######
Academy
Explore extensive hands-on learning experiences through free, online courses or under the guidance of an in-person instructor.
[Academy](https://learn.couchbase.com/store)
######
Community
With open source roots, Couchbase has a rich history of collaboration and community. Connect with our developer community and get involved.
[Community](https://forums.couchbase.com/)
######
## Explore Products and Services
Cloud
Server
SDK and Connectors
Mobile
[Couchbase Capella](cloud.html)
[Operational Insights Capella](../operational-insights-cloud/intro/intro.html)
[Couchbase Server](server.html)
[Operational Insights Enterprise](../operational-insights/current/intro/intro.html)
[Couchbase Autonomous Operator](../operator/current/overview.html)
[Couchbase Service Broker](#service-broker::index.adoc)
[Couchbase Monitoring and Observability Stack](#cmos::index.adoc)
[Couchbase C SDK](../c-sdk/current/hello-world/overview.html)
[Couchbase C++ SDK](../cxx-sdk/current/hello-world/overview.html)
[Couchbase .NET SDK](../dotnet-sdk/current/hello-world/overview.html)
[Couchbase Go SDK](../go-sdk/current/hello-world/overview.html)
[Couchbase Java SDK](../java-sdk/current/hello-world/overview.html)
[Couchbase Kotlin SDK](../kotlin-sdk/current/hello-world/overview.html)
[Couchbase Node.js SDK](../nodejs-sdk/current/hello-world/overview.html)
[Couchbase PHP SDK](../php-sdk/current/hello-world/overview.html)
[Couchbase Python SDK](../python-sdk/current/hello-world/overview.html)
[Couchbase Ruby SDK](../ruby-sdk/current/hello-world/overview.html)
[Couchbase Rust SDK](../rust-sdk/current/hello-world/overview.html)
[Couchbase Scala SDK](../scala-sdk/current/hello-world/overview.html)
[Couchbase Elasticsearch Connector](../elasticsearch-connector/current/getting-started.html)
[Couchbase Kafka Connector](../kafka-connector/current/quickstart.html)
[Couchbase Spark Connector](../spark-connector/current/getting-started.html)
[.NET Operational Insights SDK](../dotnet-operational-insights-sdk/current/hello-world/overview.html)
[Go Operational Insights SDK](../go-operational-insights-sdk/current/hello-world/overview.html)
[Java Operational Insights SDK](../java-operational-insights-sdk/current/hello-world/overview.html)
[Node.js Operational Insights SDK](../nodejs-operational-insights-sdk/current/hello-world/overview.html)
[Python Operational Insights SDK](../python-operational-insights-sdk/current/hello-world/overview.html)
[.NET Analytics SDK](../dotnet-analytics-sdk/current/hello-world/overview.html)
[Go Analytics SDK](../go-analytics-sdk/current/hello-world/overview.html)
[Java Analytics SDK](../java-analytics-sdk/current/hello-world/overview.html)
[Node.js Analytics SDK](../nodejs-analytics-sdk/current/hello-world/overview.html)
[Python Analytics SDK](../python-analytics-sdk/current/hello-world/overview.html)
[Go Columnar SDK](../go-columnar-sdk/current/hello-world/overview.html)
[Java Columnar SDK](../java-columnar-sdk/current/hello-world/overview.html)
[Node.js Columnar SDK](../nodejs-columnar-sdk/current/hello-world/overview.html)
[Python Columnar SDK](../python-columnar-sdk/current/hello-world/overview.html)
[Couchbase Lite JavaScript](#couchbase-lite:javascript:quickstart.adoc)
[Couchbase Lite C#](../couchbase-lite/current/csharp/quickstart.html)
[Couchbase Lite Java](../couchbase-lite/current/java/quickstart.html)
[Couchbase Lite Java Android](../couchbase-lite/current/android/quickstart.html)
[Couchbase Lite Swift](../couchbase-lite/current/swift/quickstart.html)
[Couchbase Lite Objective-C](../couchbase-lite/current/objc/quickstart.html)
[Couchbase Sync Gateway](../sync-gateway/current/index.html)
######
## Feedback and Contributions
######
Provide Feedback
Provide feedback, and get help with any problem you may encounter.
[Provide Feedback](../server/current/introduction/contact-couchbase.html)
######
Contact Support
Couchbase Support provides online support for customers of Enterprise Edition who have a support contract.
[Contact Couchbase](../server/current/introduction/contact-couchbase.html)
######
Contribute
You can submit simple changes, such as typo fixes and minor clarifications directly on GitHub. Contributions are greatly encouraged.
[Contribute to the Documentation](contribute/index.html)
[](https://www.couchbase.com)
- [Documentation](https://docs.couchbase.com)
- [Forums](https://forums.couchbase.com)
- [Support](https://support.couchbase.com)
- [Developer Portal](https://developer.couchbase.com)
- [Blog](https://blog.couchbase.com)
- [Resources](https://www.couchbase.com/resources)
- [Get Started](https://www.couchbase.com/get-started-developing-nosql)
- [Downloads](https://www.couchbase.com/downloads)
- [Training](https://learn.couchbase.com/store?utf8=%E2%9C%93&ss=1&ct=78327&commit=Filter)
-
[Twitter](https://twitter.com/couchbase)
-
[Linkedin](https://www.linkedin.com/company/couchbase)
-
[Facebook](https://www.facebook.com/Couchbase)
© 2026
Couchbase and the Couchbase logo are registered trademarks of Couchbase, Inc.
All third party trademarks (including logos and icons) referenced by Couchbase, Inc. remain the property of their respective owners.
[Terms of Use](https://www.couchbase.com/terms-of-use)
[Privacy Policy](https://www.couchbase.com/privacy-policy)
[Cookie Policy](https://www.couchbase.com/cookie-policy)
[Support Policy](https://www.couchbase.com/support-policy)
[Marketing Preference Center](https://info.couchbase.com/unsubscribe-or-manage-preferences.html)
Output
Close