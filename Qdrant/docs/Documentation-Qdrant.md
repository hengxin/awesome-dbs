# Documentation - Qdrant

- 来源: https://qdrant.tech/documentation/
- 归档时间: 2026-10-29
- 说明: 官方文档页面的 Markdown 快照（由 HTML 转换，格式为自动生成）

---

- Develop
- Deploy
- Ecosystem
- Learn
- API Reference
Search
Log in
Start Free
Search
-
Develop
-
Deploy
-
Ecosystem
-
Learn
-
API Reference
### Getting Started
Overview - What is Qdrant?
- Understanding Vector Search in Qdrant
Local Quickstart
Cloud Quickstart
### User Manual
Manage Data - Points
- Vectors
- Payload
- Collections
- Storage
- Indexing
- Quantization
- Multitenancy
- Bulk Upload
Search - Search
- Filtering
- Hybrid Queries
- Explore
- Search Relevance
- Low-Latency Search
- Text Search - Text Filtering
- Full-Text Search
- Sparse Vector Search
- Hybrid Search
Inference - Inference API
- BM25
- Cloud Inference
- External Providers
- Matryoshka Models
Qdrant Edge - Edge vs. Qdrant Cluster
- Edge API - Shard Lifecycle
- Configuration
- Updating Data
- Reading Data
- Snapshots
- Quickstart
- On-Device Embeddings
- BM25
- Data Synchronization Patterns
- Synchronize with a Server
Qdrant Web UI
API & SDKs
### Qdrant Tools
Agentic Tools - Agent Skills
- Prompts in the Docs
FastEmbed - Quickstart
- FastEmbed & Qdrant
- Optimize Throughput
- Working with miniCOIL
- Working with SPLADE
- Working with ColBERT
- Reranking with FastEmbed
- Multi-Vector Postprocessing
Qdrant MCP Server
### Tutorials
Overview
Basics - Semantic Search 101
- FastEmbed: Qdrant's Efficient Python Library for Embedding Generation
- Multimodal Search
- Hybrid Search
- Hybrid Search with Reranking
Search Engineering - Multivectors and Late Interaction
- Relevance Feedback Retrieval in Qdrant
- Collaborative Filtering
- Multivector Document Retrieval
- Multimodal Food Search Demo
- Measuring ANN Recall
- Multi-Representation Search
- Branch-Aware Search
- Indexing Payloads of Random Shape
- Compressed Multivector Search
- Deterministic Collection Slicing
- Query Decomposition for Multi-Hop Questions
- Fine-Tuning Sparse Embeddings for E-Commerce Search | Part 1: Why Sparse Embeddings Beat BM25
- Fine-Tuning Sparse Embeddings for E-Commerce Search | Part 2: Training SPLADE on Modal
- Fine-Tuning Sparse Embeddings for E-Commerce Search | Part 3: Evaluation and Hard Negatives
- Fine-Tuning Sparse Embeddings for E-Commerce Search | Part 4: Specialization vs Generalization
- Fine-Tuning Sparse Embeddings for E-Commerce Search | Part 5: From Research to Product
Operations & Scale - Scaling and Monitoring Hybrid Cloud
- Snapshots
- Migrate to a New Embedding Model
- Incremental Embedding Updates
- Prevent Unoptimized Usage
- Blue-Green Cluster Deployment
- Time-Based Sharding
- Large-Scale Search
- Securing and Exposing a Hybrid Cloud Cluster
- GPU-Accelerated HNSW Indexing
- Secure a Self-Hosted Qdrant Instance
- Kafka Streaming into Qdrant
Develop & Implement - Async API
- Semantic Search for Code
- Build a Semantic Search API
- Serverless Semantic Search
- Build a Hybrid Search API
- Semantic Search As You Type
### Support
Release Notes
FAQ - Qdrant Fundamentals
- Database Optimization
### Getting Started
Overview - What is Qdrant?
- Understanding Vector Search in Qdrant
Local Quickstart
Cloud Quickstart
### User Manual
Manage Data - Points
- Vectors
- Payload
- Collections
- Storage
- Indexing
- Quantization
- Multitenancy
- Bulk Upload
Search - Search
- Filtering
- Hybrid Queries
- Explore
- Search Relevance
- Low-Latency Search
- Text Search - Text Filtering
- Full-Text Search
- Sparse Vector Search
- Hybrid Search
Inference - Inference API
- BM25
- Cloud Inference
- External Providers
- Matryoshka Models
Qdrant Edge - Edge vs. Qdrant Cluster
- Edge API - Shard Lifecycle
- Configuration
- Updating Data
- Reading Data
- Snapshots
- Quickstart
- On-Device Embeddings
- BM25
- Data Synchronization Patterns
- Synchronize with a Server
Qdrant Web UI
API & SDKs
### Qdrant Tools
Agentic Tools - Agent Skills
- Prompts in the Docs
FastEmbed - Quickstart
- FastEmbed & Qdrant
- Optimize Throughput
- Working with miniCOIL
- Working with SPLADE
- Working with ColBERT
- Reranking with FastEmbed
- Multi-Vector Postprocessing
Qdrant MCP Server
### Tutorials
Overview
Basics - Semantic Search 101
- FastEmbed: Qdrant's Efficient Python Library for Embedding Generation
- Multimodal Search
- Hybrid Search
- Hybrid Search with Reranking
Search Engineering - Multivectors and Late Interaction
- Relevance Feedback Retrieval in Qdrant
- Collaborative Filtering
- Multivector Document Retrieval
- Multimodal Food Search Demo
- Measuring ANN Recall
- Multi-Representation Search
- Branch-Aware Search
- Indexing Payloads of Random Shape
- Compressed Multivector Search
- Deterministic Collection Slicing
- Query Decomposition for Multi-Hop Questions
- Fine-Tuning Sparse Embeddings for E-Commerce Search | Part 1: Why Sparse Embeddings Beat BM25
- Fine-Tuning Sparse Embeddings for E-Commerce Search | Part 2: Training SPLADE on Modal
- Fine-Tuning Sparse Embeddings for E-Commerce Search | Part 3: Evaluation and Hard Negatives
- Fine-Tuning Sparse Embeddings for E-Commerce Search | Part 4: Specialization vs Generalization
- Fine-Tuning Sparse Embeddings for E-Commerce Search | Part 5: From Research to Product
Operations & Scale - Scaling and Monitoring Hybrid Cloud
- Snapshots
- Migrate to a New Embedding Model
- Incremental Embedding Updates
- Prevent Unoptimized Usage
- Blue-Green Cluster Deployment
- Time-Based Sharding
- Large-Scale Search
- Securing and Exposing a Hybrid Cloud Cluster
- GPU-Accelerated HNSW Indexing
- Secure a Self-Hosted Qdrant Instance
- Kafka Streaming into Qdrant
Develop & Implement - Async API
- Semantic Search for Code
- Build a Semantic Search API
- Serverless Semantic Search
- Build a Hybrid Search API
- Semantic Search As You Type
### Support
Release Notes
FAQ - Qdrant Fundamentals
- Database Optimization
# Qdrant Documentation
Qdrant is an AI-native vector search and a semantic search engine. You can use it to extract meaningful information from unstructured data.
Clone this repo now and build a search engine in five minutes.
Cloud Quickstart
Local Quickstart
## Introducing Qdrant Edge
Qdrant Edge is a lightweight, embedded vector search engine for in-process retrieval — no background services, minimal memory footprint, and no network required. Built for robots, kiosks, mobile devices, and any environment requiring offline-capable AI search.
### Run vector search anywhere, even offline
Get Started
## Qdrant User Manual
Learn how to manage your data, run powerful searches, and leverage inference to build AI-native applications.
### Manage Data
Create collections, manage vectors, payloads, and storage. Learn about indexing, quantization, and multitenancy.
Read More
### Search
Learn about similarity search, filtering, hybrid queries, and advanced retrieval techniques.
Read More
### Inference
Configure dense, sparse, and multi-vector embeddings. Use cloud-hosted embedding models directly with Qdrant.
Read More
## Free tier includes everything you need.
Get Started
-
Cloud Inference
-
Free embedding models
-
No token limits
-
No payment method required
## Support
Get help from the Qdrant community or contact our support team.
### Community Support
Join 6,000+ active members to learn, collaborate, and participate in Qdrant's latest activities.
Join our Discord
### Qdrant Cloud Support
Paying customers have access to our Support team. Links to the support portal are available in the Qdrant Cloud Console.
Join Qdrant
#### Ready to get started with Qdrant?
Start Free
© 2026 Qdrant. Terms
Privacy Policy
Impressum
Recruitment Privacy Policy
Cookie Consent