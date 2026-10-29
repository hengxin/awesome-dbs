# Documentation

- 来源: https://infinispan.org/documentation/
- 归档时间: 2026-10-29
- 说明: 官方文档页面的 Markdown 快照（由 HTML 转换，格式为自动生成）

---

[Skip to main content](#main-content)
[](/)
-
[AI](/ai/)
-
Learn
- [Get Started](/get-started/)
- [Tutorials](/tutorials/)
- [Features](/features/)
- [Documentation](/documentation/)
- [Videos](/videos/)
-
[Use Cases](/use-cases/)
-
Community
- [Community](/community/)
- [Blog](/blog/)
- [References](/references/)
- [Roadmap](/roadmap/)
- [Contribute](/contribute/)
-
Download
- [Releases](/downloads/releases)
- [Clients](/hotrod-clients/)
- [Cache Stores](/downloads/cache-stores/)
-
# Documentation
Find guides, references, and tutorials for Infinispan 16.3
### Get Started
[#### Quick Start
Get Infinispan running in 4 easy steps.](/get-started/)
[#### Getting Started Guide
Comprehensive introduction to Infinispan concepts and features.](/docs/stable/titles/getting_started/getting_started.html)
[#### Tutorials
Hands-on code tutorials to learn by doing.](/tutorials/)
[#### Videos
Videos and presentation by the Infinispan team](/videos/)
### Clients & Protocols
[#### Embedded (Library)
Use Infinispan as an in-process Java library for maximum performance.](/docs/stable/titles/embedding/embedding.html)
[#### Java Hot Rod Client
High-performance binary protocol for remote Java clients.](/docs/stable/titles/hotrod_java/hotrod_java.html)
[#### REST API
HTTP/JSON interface — works with any language or tool.](/docs/stable/titles/rest/rest.html)
[#### Redis Protocol (RESP)
Drop-in replacement for Redis. Use any Redis client library.](/docs/stable/titles/resp/resp-endpoint.html)
[#### Memcached
Memcached-compatible text and binary protocol endpoint.](/docs/stable/titles/memcached/memcached.html)
[#### Go Hot Rod Client
High-performance binary protocol for remote Go clients.](/docs/hotrod-clients/go-client/latest/)
[#### JavaScript Hot Rod Client
High-performance binary protocol for remote JavaScript clients.](/docs/hotrod-clients/js-client/latest/)
[#### C#/.NET Hot Rod Client
High-performance binary protocol for remote C#/.NET clients.](/docs/hotrod-clients/dotnet-client/latest/)
[#### C++ Hot Rod Client
High-performance binary protocol for remote C++ clients.](/docs/hotrod-clients/cpp-client/latest/cpp_client.html)
### Framework Integrations
[#### Spring Boot
Spring Boot starter with auto-configuration for caching and sessions.](/docs/stable/titles/spring_boot/starter.html)
[#### Spring Framework
Spring Cache and Spring Session integration.](/docs/stable/titles/spring/spring.html)
[#### Hibernate / JPA
Second-level cache provider for Hibernate ORM.](/docs/stable/titles/hibernate/hibernate.html)
[#### JCache
JCache provider for embedded and Hot Rod deployments.](/docs/stable/titles/jcache/jcache.html)
[#### Quarkus
Quarkus extension for native, cloud-native applications.](https://quarkus.io/guides/infinispan-client)
[#### Vert.x Cluster Manager
Distributed cluster manager for Eclipse Vert.x.](https://vertx.io/docs/vertx-infinispan/java/)
[#### Vert.x Web Sessions
Store web sessions in Infinispan with Vert.x.](https://how-to.vertx.io/web-session-infinispan-howto/)
[#### Keycloak
Infinispan powers Keycloak's distributed caches and sessions.](https://www.keycloak.org/server/caching)
[#### Apache Camel
Camel component for reading and writing to Infinispan caches.](https://camel.apache.org/components/latest/infinispan-component.html)
[#### WildFly
Infinispan provides clustering and caching for WildFly / JBoss EAP.](https://www.wildfly.org/)
### Operations & Deployment
[#### Server Guide
Install, configure, and run Infinispan Server.](/docs/stable/titles/server/server.html)
[#### Kubernetes Operator
Deploy and manage Infinispan clusters on Kubernetes and OpenShift.](/docs/infinispan-operator/main/operator.html)
[#### Helm Chart
Deploy Infinispan using Helm charts on Kubernetes.](/docs/helm-chart/main/helm-chart.html)
[#### Ansible Collection
Automate Infinispan provisioning with Ansible. Community](https://github.com/ansible-middleware/infinispan)
[#### CLI Reference
Command-line tool for managing and interacting with Infinispan.](/docs/stable/titles/cli/cli.html)
[#### Cross-Site Replication
Replicate data across geographically distributed data centers.](/docs/stable/titles/xsite/xsite.html)
[#### Planning & Tuning
Capacity planning, performance tuning, and optimization.](/docs/stable/titles/tuning/tuning.html)
[#### Upgrade Guide
Upgrade Infinispan deployments, migrate cachestore data, version compatibility.](/docs/stable/titles/upgrading/upgrading.html)
[#### Container Images
Official container images for Infinispan Server.](https://github.com/infinispan/infinispan-images/tree/main)
### AI & Vector Search
[#### Vector Search & Querying
Distributed vector indexes, kNN search, and Ickle query language.](/docs/stable/titles/query/query.html)
[#### MCP Server
Model Context Protocol server for AI/LLM tool integration.](https://infinispan.org/docs/stable/titles/mcp_server/mcp_server.html)
[#### Spring AI
Infinispan as a vector store for Spring AI applications.](https://infinispan.org/docs/spring-ai/stable/spring-ai.html)
[#### LangChain4j
Embedding store integration for LangChain4j (Java).](https://docs.langchain4j.dev/integrations/embedding-stores/infinispan)
[#### Quarkus LangChain4j
Quarkus extension for LangChain4j with Infinispan embedding store.](https://docs.quarkiverse.io/quarkus-langchain4j/dev/infinispan-store.html)
[#### LangChain (Python)
Python vector store integration for LangChain.](https://infinispan.org/docs/langchain/stable/langchain.html)
[#### AI Skills
Skills for Infinispan to help AI coding assistants.](https://github.com/infinispan/infinispan-ai-skills/)
### References
[#### Java API
Javadocs for the embedded and client API.](/docs/stable/apidocs/)
[#### Configuration Guide
All configuration options for caches, clusters, and server.](/docs/stable/titles/configuring/configuring.html)
[#### Encoding & Serialization
Data encoding, media types, and serialization formats.](/docs/stable/titles/encoding/encoding.html)
[#### Querying & Indexing
Ickle queries, full-text search, and indexing configuration.](/docs/stable/titles/query/query.html)
[#### Security
Authentication, authorization, TLS/SSL, and RBAC.](/docs/stable/titles/security/security.html)
[#### Configuration Schema
Configuration schema reference](/docs/stable/configuration-schema/index.html)
[#### Logging Reference
Log categories, levels, and troubleshooting.](/docs/stable/logging/logs.html)
[#### Metrics
Metrics exposed via JMX or OpenMetrics / Prometheus](/docs/stable/titles/metrics/metrics.html)
[#### Architecture
Infinispan architecture: design, implementation, components, diagrams, flows.](/docs/dev/titles/architecture/architecture.html)
Other versions:
[Stable (16.3)](/docs/stable/index.html)
[Archive](/documentation-archive)
No docs match your search.
Try a different keyword or [clear the filter](#).
#### Got an improvement to the source code or want to write some docs?
[Review the Guide and submit a PR](https://infinispan.org/docs/dev/titles/contributing/contributing.html)
#### Chat with us, report issues, suggest changes, or ask questions.
[Join the Community](/community)
[](/)
Infinispan is released under the [Apache 2.0](https://www.apache.org/licenses/LICENSE-2.0) open source license. The source code is available on [GitHub](https://github.com/infinispan).
Thanks to
[](https://zulip.com)
[](https://weblate.org)
Navigation
- [Home](/)
- [Get Started](/get-started)
- [Features](/features)
- [AI](/ai)
- [Documentation](/documentation)
- [Tutorials](/tutorials)
- [Use Cases](/use-cases)
- [Releases](/downloads/releases)
- [Clients](/hotrod-clients)
- [Cache Stores](/downloads/cache-stores)
Get Help
- [Documentation](/documentation)
- [Guides](/tutorials)
- [Stack Overflow](https://stackoverflow.com/questions/tagged/infinispan)
- [GitHub Discussions](https://github.com/infinispan/infinispan/discussions)
- [Zulip Chat](https://infinispan.zulipchat.com)
Contribute
- [Source Code](https://github.com/infinispan/infinispan)
- [Submit a Bug](https://github.com/infinispan/infinispan/issues)
- [Website Source](https://github.com/infinispan/infinispan.github.io)
Follow Us
- [Blog](/blog)
- [X / Twitter](https://twitter.com/infinispan)
- [Facebook](https://www.facebook.com/infinispan/)
- [YouTube](https://www.youtube.com/@InfinispanProject)
- [GitHub](https://github.com/infinispan)
[](https://www.commonhaus.org/)
Copyright © Infinispan. All rights reserved. For details on trademarks, please visit the [Trademark Policy](https://www.commonhaus.org/policies/trademark-policy/) and [Trademark List](https://www.commonhaus.org/trademarks/). Trademarks of third parties are owned by their respective holders and their mention here does not suggest any endorsement or association.