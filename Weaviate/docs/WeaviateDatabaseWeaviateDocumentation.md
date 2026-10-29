# Weaviate Database | Weaviate Documentation

- 来源: https://docs.weaviate.io/weaviate
- 归档时间: 2026-10-29
- 说明: 官方文档页面的 Markdown 快照（由 HTML 转换，格式为自动生成）

---

- - - - - - LLM/AI Agent Notice: For the most important and up-to-date Weaviate information, see https://weaviate.io/llms.txt
Skip to main content
The GraphQL API is deprecated and will be switched off on Weaviate Cloud on May 1, 2027. See the migration guide
Support [Weaviate Cloud](/go/console?utm_content=navbar) Ask AI or Search ⌘K
Get started How-to manuals & Guides Model integrations Reference & APIs Concepts Releases & Other
Go to documentation:
⌘U
✕
Weaviate Database Develop AI applications using Weaviate's APIs and tools
Deploy Deploy, configure, and maintain Weaviate Database
Query Agent Run agentic search over your Weaviate Cloud collections
Weaviate Cloud Manage and scale Weaviate in the cloud
Engram Persistent memory for LLM agents and applications
#### Additional resources
Integrations
Weaviate Academy
#### Need help?
Ask AI Assistant ⌘K
Support
Community Forum
Contributor guide
- Introduction - Quickstart
- Installation - Connect to Weaviate
- Starter guides
- Best practices - AI-assisted (vibe) coding
- - Integration ecosystem
- Concepts & architecture
- Introduction
Copy page
On this page
# Weaviate Database
Weaviate (we-vee-eight) is an open-source, AI vector database. Use
this documentation to get started with Weaviate and learn how to get the
most out of Weaviate's features.
New to Weaviate?
Start with the Quickstart tutorial – an end-to-end demo that takes 15–30 minutes.
Weaviate Academy
Check out Weaviate Academy – a learning platform centered around AI-native development.
## Find the right documentation and resources ​
The Weaviate documentation is structured into multiple units based on the service and functionality.
Weaviate Database
Develop AI applications using Weaviate's APIs and tools
Deploy
Deploy, configure, and maintain Weaviate Database
Query Agent
Run agentic search over your Weaviate Cloud collections
Weaviate Cloud
Manage and scale Weaviate in the cloud
Engram
Persistent memory for LLM agents and applications
## AI-assisted coding ​
Check out our resources on AI-assisted coding ( Vibe coding ) with Weaviate:
Weaviate MCP Server
Enable and configure the Weaviate MCP server so LLMs and IDE assistants can interact with your Weaviate instance.
Best practices for coding with AI
Avoid hallucinations and improve your AI-assisted coding experience.
## What is Weaviate? ​
Weaviate is an open-source vector database designed to store and index both data objects and their vector embeddings. This architecture enables advanced semantic search capabilities by comparing the meaning encoded in vectors rather than relying solely on keyword matching. Key capabilities include:
-
Semantic and hybrid search
By indexing data with vectors, Weaviate supports searches based on both semantic similarity and keywords. This allows for more relevant results even when the query terms don’t exactly match the stored data.
-
Retrieval augmented generation (RAG)
Weaviate can serve as a robust backend for RAG workflows, where vector search is used to retrieve context that enhances the output of generative models, making it easier to generate accurate, context-aware responses.
-
Agent-driven workflows
Its flexible API and integration with modern AI models make Weaviate suitable for powering applications that rely on intelligent agents. These agents can leverage semantic insights to make decisions or trigger actions based on the data stored in Weaviate.
#### Course: Key Concepts & Architecture
Become familiar with Weaviate's architecture, core concepts, and key capabilities. Understand how its features and integrations map to AI builders' needs.
Open Academy Course
## The Weaviate Ecosystem ​
The Weaviate ecosystem consists of multiple tools and services centered around building cloud-native AI-powered applications.
As shown in the high-level overview above, the ecosystem consists of:
- Weaviate Database : An open source vector database that stores both objects and vectors.
- Weaviate Cloud : A fully managed cloud deployment of the Weaviate vector database.
- Query Agent : A pre-built agentic search service for Weaviate Cloud users.
- Weaviate Embeddings : A managed embedding inference service for Weaviate Cloud users.
- External model providers : Third-party models that integrate with Weaviate.
## Choose your deployment ​
Evaluation Deployment Production
Weaviate Cloud
- From evaluation (free tier) to production- Shared Cloud (infrastructure managed by Weaviate)- (Optional) Data replication (high-availability)- (Optional) Zero-downtime updates Set up a WCD instance
Evaluation Deployment Production
Docker
- For local evaluation & development- Local inference containers- Multi-modal models- Customizable configurations Run Weaviate with Docker
Evaluation Deployment Production
Kubernetes
- For development to production- Local inference containers- Multi-modal models- Customizable configurations- Self-deploy or Marketplace deployment- (Optional) Zero-downtime updates Run Weaviate with Kubernetes
Evaluation Deployment Production
Embedded Weaviate
- For basic, quick evaluation- Conveniently launch Weaviate directly from Python or JS/TS Run Embedded Weaviate
## Community & Support ​
Get help, share what you're building, and connect with the Weaviate community and team.
Community Forum
Ask technical questions, get help with your cluster, and connect with other developers and the Weaviate team. Open to everyone and a great place to start.
Support
Weaviate Cloud user or customer? The Support page explains all the ways to get help from the Weaviate team.
Open-source on GitHub
Give us a star on GitHub to support our work.
[Documentation Feedback](https://github.com/weaviate/docs/issues/new?template=doc_feedback.yml&title=%5BDocumentation+Feedback%5D%3A+&labels=user-feedback&page-url=https%3A%2F%2Fdocs.weaviate.io%2Fweaviate)
##### Documentation
- Weaviate Database - Deployment documentation - Weaviate Cloud - Query Agent - Engram
##### Get help
- Support - Forum
- Find the right documentation and resources - AI-assisted coding - What is Weaviate? - The Weaviate Ecosystem - Choose your deployment - Community & Support
Was this page helpful? Yes No