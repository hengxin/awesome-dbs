# TDengine TSDB Reading Guide | TDengine TSDB Docs

- 来源: https://docs.tdengine.com
- 归档时间: 2026-10-29
- 说明: 官方文档页面的 Markdown 快照（由 HTML 转换，格式为自动生成）

---

- - - - - Skip to main content
IDMP Docs Contact Us Cloud Search
v3.4.3 (Latest) v3.4.2 Cloud v3.3.8 v3.3.6 (LTS) v3.2 v3.1 v3.0 v2.6 v2.4 v2.0 v1.6 Search
- Reading Guide - Introduction - Time-Series Data Basics - Quick Start
- TDengine SQL
- Data Subscription
- Stream Processing
- Data Ingest and Delivery
- AI and Advanced Analytics
- Developer's Guide
- Security Guide
- Operations and Tooling
- Ecosystem Integrations
- Best Practices
- Inside TDengine
- FAQ
- Release History
- Product Roadmap - TDengine IDMP
# TDengine TSDB Reading Guide
TDengine® TSDB (hereinafter TDengine) is an open-source , high-performance, cloud-native time-series database ( Time-Series Database , TSDB). It is purpose-built for IoT, connected vehicles, industrial internet, finance, IT operations, and similar scenarios. With built-in caching, stream processing, and data subscription, it greatly reduces system design complexity as well as development and operations cost—a streamlined platform for time-series data. This documentation is the user manual. It covers basic concepts, installation, usage, features, development interfaces, operations and maintenance, and kernel design, and is intended for architects, developers, and system administrators. If you are not yet familiar with the basics, value, and business meaning of time-series data, see Core Concepts . You can also get a quick overview from "What Is a Time-Series Database?" and other articles on our official website.
TDengine fully leverages the characteristics of time-series data. It introduced the “one table per data collection point”, “super table”, and “virtual table” models and designed an innovative storage engine that significantly improves write, query, and storage efficiency. To use TDengine correctly, regardless of your role, carefully read Basic Concepts .
Depending on your role and interests, you can read the following chapters as needed:
- If you are a developer, carefully read the Developer's Guide . It covers connecting to the database, data modeling, writing, querying, stream processing, caching, data subscription, user-defined functions, and more, with sample code in multiple languages. In most cases, you can copy the samples and adapt them slightly for your application. For the REST API and language connectors, see Connectors Reference .
- If you are a system administrator and need to understand installation, upgrades, fault tolerance and disaster recovery, cluster deployment and maintenance, data import and export, configuration parameters, health monitoring, and performance tuning, carefully read Operations and Maintenance . In the era of big data, vertical scaling alone cannot meet continuously growing business demand. Systems generally need horizontal scalability, and clustering has become essential for big data and database systems; the TDengine team not only built clustering but also open-sourced this core capability.
- If you are interested in database kernel design or the open-source implementation, carefully read Inside TDengine . It covers distributed architecture, the storage engine, the query engine, data subscription, and the stream processing engine. We recommend reading the source code on GitHub alongside the documentation, and we welcome contributions to the open-source community.
- If you would like to install TDengine and experience its features for yourself, see Get Started .
TDengine uses SQL as its query language to lower learning and migration cost, and extends SQL for time-series scenarios such as interpolation, downsampling, and time-weighted averages. The TDengine SQL chapter details the SQL syntax and lists supported commands and functions.
If you need visualization, event management, root-cause analysis, and AI insights in industrial scenarios, learn more about the platform’s other component TDengine IDMP , or visit the product page for a free trial .
TDengine TSDB, including this documentation, is an open-source project, and we welcome contributions from the community. If you find any errors or unclear descriptions, click Edit this page at the bottom of the page to submit your corrections. To view the source code, visit our GitHub repository .
Together, we make a difference!
Next
Introduction
## Support and Feedback
Thank you for being part of our community! Your feedback and bug reports for TDengine and its documentation are highly appreciated. Edit this page  |  Submit an issue  |  Contact us
TDengine® is an AI-powered data platform designed for industrial applications, combining the high-performance time-series database TDengine TSDB and the AI-native data management platform TDengine IDMP. With TDengine TSDB handling data ingestion, storage, and processing, and TDengine IDMP providing contextualization, standardization, and AI-powered analytics, TDengine enables industrial enterprises to unlock the true value of their time-series data. © 2022–2026 TDengine
Products
TDengine TSDB TDengine IDMP TDengine Cloud
Resources
TDengine TSDB Docs TDengine IDMP Docs Blog Webinars
Company
About Downloads Newsroom Security Legal Resellers Partners Contact Us
Social
GitHub Discord LinkedIn Twitter YouTube 中