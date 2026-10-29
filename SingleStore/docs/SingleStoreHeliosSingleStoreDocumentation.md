# SingleStore Helios · SingleStore Documentation

- 来源: https://docs.singlestore.com
- 归档时间: 2026-10-29
- 说明: 官方文档页面的 Markdown 快照（由 HTML 转换，格式为自动生成）

---

[](/)
Search
or
Ask SQrL
[Sign in](https://portal.singlestore.com/)[Try Free](https://www.singlestore.com/cloud-trial/)
- [Getting Started with SingleStore Helios](/cloud/getting-started-with-singlestore-helios/)
- [Connect to SingleStore](/cloud/connect-to-singlestore/)
- [Create a Database](/cloud/create-a-database/)
- [Load Data](/cloud/load-data/)
- [Query Data](/cloud/query-data/)
- [Manage Data](/cloud/manage-data/)
- [AI](/cloud/ai/)
- [Container Services](/cloud/container-services/)
- [Developer Resources](/cloud/developer-resources/)
- [User and Cluster Administration](/cloud/user-and-cluster-administration/)
- [Security](/cloud/security/)
- [Reference](/cloud/reference/)
- [Release Notes](/cloud/release-notes/)
- [Support](/cloud/support/)
- [Glossary](/cloud/glossary/)
AI agents/LLMs: Fetch /llms.txt first to access the documentation index. Remove the trailing slash and append .md to any URL to access lighter, easier-to-parse Markdown pages instead of HTML .
Important
Helios features are now enabled during weekly update windows and are no longer directly tied to SingleStore engine releases. Refer to the [release notes](/cloud/release-notes/) to view the latest features available in your Helios cluster.
# SingleStore Helios
SingleStore is a distributed SQL database built to power intelligent applications . It is both relational and multi-model, enabling developers to easily build and scale applications and workloads .
SingleStore is built around [Universal Storage](/cloud/create-a-database/choosing-a-table-storage-type/) which combines in-memory rowstore and on-disk columnstore data formats to deliver a single table type that is optimized to handle both transactional and analytical workloads .
Combined with superior query execution performance through [code generation](/cloud/query-data/advanced-query-topics/code-generation/), SingleStore delivers extremely low latency query responses under highly concurrent application workloads .
SingleStore is delivered as a SaaS data platform ( SingleStore Helios ) and is available in AWS, Azure, and GCP .
Deploy a database with SingleStore Helios to experience the performance and scalability of the SingleStore database engine in the cloud .
Ask SQrL, our AI assistant, trained on all things SingleStore
Ask SQrL
## New to SingleStore Helios ? Start here .
[](https://portal.singlestore.com/) Step 1
[Create an Account](https://portal.singlestore.com/)
[](/cloud/getting-started-with-singlestore-helios/compute-clusters/) Step 2
[Deploy SingleStore](/cloud/getting-started-with-singlestore-helios/compute-clusters/)
[](/cloud/connect-to-singlestore/) Step 3
[Connect to SingleStore](/cloud/connect-to-singlestore/)
[](/cloud/create-a-database/) Step 4
[Create a Database](/cloud/create-a-database/)
## [](#guides-2)Guides
## About SingleStore Helios
Learn more about what makes SingleStore Helios tick .
-
[About SingleStore Helios](/cloud/getting-started-with-singlestore-helios/about-singlestore-helios/)
-
[Editions](/cloud/getting-started-with-singlestore-helios/about-singlestore-helios/singlestore-helios-editions/)
-
[Glossary](/cloud/glossary/)
-
[FAQs](/cloud/getting-started-with-singlestore-helios/about-singlestore-helios/singlestore-helios-faqs/)
## Vector Data
Use SingleStore to efficiently store, index, and search your vector data .
-
[Working with Vector Data](/cloud/developer-resources/functional-extensions/working-with-vector-data/)
-
[Vector Type](/cloud/reference/sql-reference/data-types/vector-type/)
-
[Vector Indexing](/cloud/reference/sql-reference/vector-functions/vector-indexing/)
-
[Hybrid Search - Reranking Full-Text and Vector Search Results](/cloud/developer-resources/functional-extensions/hybrid-search-reranking-full-text-and-vector-search-results/)
## Connect
Connect to SingleStore Helios using a variety of SQL clients, drivers, programming languages, and frameworks .
-
[SQL Developer](/cloud/connect-to-singlestore/connect-with-sql-developer/)
-
[SingleStore JDBC Driver](/cloud/developer-resources/connect-with-application-development-tools/connect-with-java-jdbc/the-singlestore-jdbc-driver/)
-
[SingleStore Client](/cloud/connect-to-singlestore/connect-with-the-singlestore-client/)
-
[All SQL Clients & Drivers](/cloud/connect-to-singlestore/client-and-driver-downloads/)
-
[All Languages & Frameworks](/cloud/developer-resources/connect-with-application-development-tools/)
## Load Data
Load your data from a multitude of data sources .
-
[Amazon S3](/cloud/load-data/data-sources/load-data-from-amazon-web-services-aws-s-3/)
-
[Kafka](/cloud/load-data/data-sources/load-data-from-kafka/load-data-from-kafka-using-a-pipeline/)
-
[MongoDB®](/cloud/reference/singlestore-kai/)
-
[Spark](/cloud/load-data/integrate-with-singlestore-helios/load-data-from-spark/)
-
[All Data Sources](/cloud/load-data/)
## Code & Examples
Explore SingleStore’s code and examples .
-
[Code Repository](https://github.com/singlestore-labs)
-
[Sample Data-Intensive App](https://github.com/singlestore-labs/singlestore-workshop-data-intensive-app)
-
[Build a Full-Stack App](https://www.npmjs.com/package/create-singlestoredb-app)
-
[Basic Query Examples](/cloud/query-data/basic-query-examples/)
## More Ways to Learn
Explore other ways to learn and participate
-
[Engineering Blog](https://www.singlestore.com/blog/category/engineering/)
-
[Training](https://training.singlestore.com)
-
[Events and Meetups](https://www.singlestore.com/events/)
-
[Already an Expert?](https://www.singlestore.com/blog/introducing-singlestore-ambassador-program/)
## Get Help
Troubleshoot issues and get help from the community .
-
[Troubleshooting Reference](/cloud/reference/troubleshooting-reference/)
-
[Solve MySQL Out-of-Memory Error](https://www.singlestore.com/blog/mysql-error-out-of-memory/)
-
[SingleStore Forums](https://www.singlestore.com/forum)
-
[Support FAQ](/cloud/support/support-faq/)
This documentation is for SingleStore Helios . For on-premises deployments, visit the [SingleStore Self-Managed documentation](/db/v10/).
## Was this article helpful?
Product - [Product Overview](https://www.singlestore.com/product-overview/)
- [Request a Demo](https://www.singlestore.com/demo/)
- [Pricing](https://www.singlestore.com/pricing/)
- [Support](https://www.singlestore.com/support/)
- [Status](https://status.singlestore.com/)
Community - [Forums](https://www.singlestore.com/forum/)
- [Spaces](https://www.singlestore.com/spaces/)
- [Events](https://www.singlestore.com/events/)
- [Training](https://www.singlestore.com/training/)
Company - [Contact Us](https://www.singlestore.com/contact/)
- [Blog](https://www.singlestore.com/blog/)
- [Careers](https://www.singlestore.com/careers/)
- [Partners](https://www.singlestore.com/partners/)
This site is protected by reCAPTCHA and the Google [Privacy Policy](https://policies.google.com/privacy) and [Terms of Service](https://policies.google.com/terms) apply.
- © SingleStore
- |
- [Privacy Policy](https://www.singlestore.com/privacy-notice/)
- |
- [Terms of Service](https://www.singlestore.com/terms/)
- |
- [Legal Terms and Conditions](https://www.singlestore.com/legal/)
## Verification instructions
Note: You must install [cosign](https://docs.sigstore.dev/cosign/system_config/installation/) to verify the authenticity of the SingleStore file.
Use the following steps to verify the authenticity of singlestoredb-server , singlestoredb-toolbox , singlestoredb-studio , and singlestore-client SingleStore files that have been downloaded.
You may perform the following steps on any computer that can run cosign , such as the main deployment host of the cluster.
- (Optional) Run the following command to view the associated signature files.
Shell
Copy
curl undefined
- Download the signature file from the SingleStore release server.
- Option 1: Click the Download Signature button next to the SingleStore file.
- Option 2: Copy and paste the following URL into the address bar of your browser and save the signature file.
Copy
- Option 3: Run the following command to download the signature file.
Shell
Copy
curl -O undefined
- After the signature file has been downloaded, run the following command to verify the authenticity of the SingleStore file.
Shell
Copy
echo -n undefined |
cosign verify-blob --certificate-oidc-issuer https://oidc.eks.us-east-1.amazonaws.com/id/CCDCDBA1379A5596AB5B2E46DCA385BC \
--certificate-identity https://kubernetes.io/namespaces/freya-production/serviceaccounts/job-worker \
--bundle undefined \
--new-bundle-format -
Verified OK
Done
## Try Out This Notebook to See What’s Possible in SingleStore
Get access to other groundbreaking datasets and engage with our community for expert advice.
[Sign Up](https://portal.singlestore.com/intention/notebooks?notebookTemplate=null)[Log In](https://portal.singlestore.com/intention/notebooks-login?notebookTemplate=null)