# Overview of parallel reduce search processing - Splunk Documentation

- 来源: https://docs.splunk.com/Documentation/Splunk/8.0.0/DistSearch/Parallelreduceoverview
- 归档时间: 2026-10-29
- 说明: 官方技术白皮书 / 架构文档的 Markdown 快照（由 HTML 转换，格式为自动生成）

---

[logo](https://www.splunk.com)
-
[Support](#)
-
#####
[Support Portal](http://login.splunk.com/page/sso_redirect?type=portal)
Submit a case ticket
-
#####
[Splunk Answers](https://community.splunk.com/t5/Splunk-Answers/ct-p/en-us-splunk-answers)
Ask Splunk experts questions
-
#####
[Support Programs](https://www.splunk.com/en_us/customer-success/support-programs.html)
Find support service offerings
-
#####
[System Status](https://www.splunk.com/en_us/products/system-status.html)
-
#####
[Contact Us](https://www.splunk.com/en_us/about-splunk/contact-us.html#customer-support)
Contact our customer support
-
#####
[Product Security Updates](https://www.splunk.com/en_us/product-security.html)
Keep your data secure
-
#####
[System Status](https://www.splunk.com/en_us/products/system-status.html)
-
[Click User Account](#)
- [Login](http://docs.splunk.com/Documentation?saml=true&redirecturl=https://docs.splunk.com%2FDocumentation%2FSplunk%2F8.0.0%2FDistSearch%2FParallelreduceoverview)
- [Sign Up](http://idp.login.splunk.com/signin/register?redirecturl=https://docs.splunk.com/Documentation/Splunk/8.0.0/DistSearch/Parallelreduceoverview)
[logo](https://www.splunk.com)
-
[Products](#)
[Product Overview](https://www.splunk.com/en_us/products.html)
A data platform built for expansive data access, powerful analytics and automation
[Learn more](https://www.splunk.com/en_us/products.html)
MORE FROM SPLUNK
-
#####
[Pricing](https://www.splunk.com/en_us/products/pricing.html)
-
#####
[Free Trials & Downloads](https://www.splunk.com/en_us/download.html)
[Platform](https://www.splunk.com/en_us/products/platform.html)
-
#####
[Splunk Cloud Platform](https://www.splunk.com/en_us/products/splunk-cloud-platform.html)
Cloud-powered insights for petabyte-scale data analytics across the hybrid cloud
-
#####
[Splunk Enterprise](https://www.splunk.com/en_us/products/splunk-enterprise.html)
Search, analysis and visualization for actionable insights from all of your data
[Security](https://www.splunk.com/en_us/products/cyber-security.html)
-
#####
[Splunk Enterprise Security](https://www.splunk.com/en_us/products/enterprise-security.html)
Analytics-driven SIEM to quickly detect and respond to threats
-
#####
[Splunk SOAR](https://www.splunk.com/en_us/products/splunk-security-orchestration-and-automation.html)
Security orchestration, automation and response to supercharge your SOC
[Observability](https://www.splunk.com/en_us/products/observability.html)
-
#####
[Splunk Infrastructure Monitoring](https://www.splunk.com/en_us/products/infrastructure-monitoring.html)
Instant visibility and accurate alerts for improved hybrid cloud performance
-
#####
[Splunk Application Performance Monitoring](https://www.splunk.com/en_us/products/apm-application-performance-monitoring.html)
Full-fidelity tracing and always-on profiling to enhance app performance
-
#####
[Splunk IT Service Intelligence](https://www.splunk.com/en_us/products/it-service-intelligence.html)
AIOps, incident intelligence and full visibility to ensure service performance
[View all products](https://www.splunk.com/en_us/products.html)
-
[Solutions](#)
KEY INItiatives
-
#####
[Cloud Transformation](https://www.splunk.com/en_us/solutions/cloud-transformation.html)
Transform your business in the cloud with Splunk
-
#####
[Business Resilience](https://www.splunk.com/en_us/solutions/business-resilience.html)
Build resilience to meet today’s unpredictable business challenges
-
#####
[Digital Customer Experience](https://www.splunk.com/en_us/solutions/digital-customer-experience.html)
Deliver the innovative and seamless experiences your customers expect
by Use Case
-
#####
[Advanced Threat Detection](https://www.splunk.com/en_us/solutions/advanced-threat-detection.html)
-
#####
[Application Modernization](https://www.splunk.com/en_us/solutions/application-modernization.html)
-
#####
[Cloud Migration](https://www.splunk.com/en_us/solutions/cloud-migration.html)
-
#####
[Incident Investigation & Forensics](https://www.splunk.com/en_us/solutions/incident-investigation-and-forensics.html)
-
#####
[IT Modernization](https://www.splunk.com/en_us/solutions/it-modernization.html)
-
#####
[SOC Automation & Orchestration](https://www.splunk.com/en_us/solutions/automate-and-orchestrate-the-soc.html)
BY TECHNOLOGY
-
#####
[AWS](https://www.splunk.com/en_us/solutions/aws-monitoring.html)
-
#####
[Azure](https://www.splunk.com/en_us/solutions/microsoft-azure-monitoring.html)
-
#####
[GCP](https://www.splunk.com/en_us/solutions/gcp-monitoring.html)
-
#####
[Kubernetes](https://www.splunk.com/en_us/solutions/kubernetes-monitoring.html)
-
#####
[OpenTelemetry](https://www.splunk.com/en_us/solutions/opentelemetry.html)
-
#####
[SAP](https://www.splunk.com/en_us/solutions/sap-monitoring.html)
BY INDUSTRY
-
#####
[Aerospace & Defense](https://www.splunk.com/en_us/solutions/industries/aerospace-defense.html)
-
#####
[Energy & Utilities](https://www.splunk.com/en_us/solutions/industries/energy-and-utilities.html)
-
#####
[Financial Services](https://www.splunk.com/en_us/solutions/industries/financial-services.html)
-
#####
[Healthcare](https://www.splunk.com/en_us/solutions/industries/healthcare.html)
-
#####
[Higher Education](https://www.splunk.com/en_us/solutions/industries/higher-education.html)
-
#####
[Public Sector](https://www.splunk.com/en_us/solutions/industries/public-sector.html)
[View All Solutions](https://www.splunk.com/en_us/solutions.html)
-
[Why Splunk?](#)
[Why Splunk?](https://www.splunk.com/en_us/about-us/why-splunk.html)
Bring data to every question, decision and action across your organization.
[Learn More](https://www.splunk.com/en_us/about-us/why-splunk.html)
-
#####
[Customer Stories](https://www.splunk.com/en_us/customers.html)
See why organizations around the world trust Splunk.
-
#####
[Partners](https://www.splunk.com/en_us/partners.html)
Accelerate value with our powerful partner ecosystem.
-
#####
[Diversity, Equity & Inclusion](/en_us/careers/diversity.html)
Learn how we support change for customers and communities.
-
[Resources](#)
MORE FROM SPLUNK
[Resources](https://www.splunk.com/en_us/resources.html)
Explore e-books, white papers and more.
[Events](https://www.splunk.com/en_us/about-us/events.html)
Join us at an event near you.
[Blogs](https://www.splunk.com/en_us/blog)
See what Splunk is doing.
GET STARTED
-
#####
[Splunk Lantern](https://lantern.splunk.com/)
Splunk experts provide clear and actionable guidance.
-
#####
[Customer Success](https://www.splunk.com/en_us/customer-success.html)
Customer success starts with data success.
-
#####
[Get Started With Splunk](https://www.splunk.com/en_us/get-started.html)
Learn how to use Splunk.
-
#####
[Data Insider](https://www.splunk.com/en_us/data-insider.html)
Read focused primers on disruptive technology topics.
become an expert
-
#####
[Splunk Training & Certification](https://www.splunk.com/en_us/training.html)
Become a certified Splunk Expert.
-
#####
[Documentation](https://docs.splunk.com/Documentation)
Find answers about how to use Splunk.
-
#####
[User Groups](https://usergroups.splunk.com/)
Meet Splunk enthusiasts in your area.
-
#####
[Community](https://www.splunk.com/en_us/community.html)
Share knowledge and inspiration.
-
#####
[SURGe](https://www.splunk.com/en_us/surge.html)
Access timely security research and guidance.
Expand & optimize
-
#####
[Services & Support](https://www.splunk.com/en_us/customer-success.html)
It’s easy to get the help you need.
-
#####
[Splunkbase](https://splunkbase.splunk.com/)
See Splunk’s 1,000+ Apps and Add-ons.
-
#####
[Splunk Dev](https://dev.splunk.com/)
Create your own Splunk Apps.
-
[Splexicon](/Splexicon)
-
[Support](#)
-
#####
[Support Portal](http://login.splunk.com/page/sso_redirect?type=portal)
Submit a case ticket
-
#####
[Splunk Answers](https://community.splunk.com/t5/Splunk-Answers/ct-p/en-us-splunk-answers)
Ask Splunk experts questions
-
#####
[Support Programs](https://www.splunk.com/en_us/customer-success/support-programs.html)
Find support service offerings
-
#####
[System Status](https://www.splunk.com/en_us/products/system-status.html)
View detailed status
-
#####
[Contact Us](https://www.splunk.com/en_us/about-splunk/contact-us.html#customer-support)
Contact our customer support
-
#####
[Product Security Updates](https://www.splunk.com/en_us/product-security.html)
Keep your data secure
-
[Click Search Help](#)
-
[Click User Account](#)
- [Login](http://docs.splunk.com/Documentation?saml=true&redirecturl=https://docs.splunk.com%2FDocumentation%2FSplunk%2F8.0.0%2FDistSearch%2FParallelreduceoverview)
- [Sign Up](http://idp.login.splunk.com/signin/register?redirecturl=https://docs.splunk.com/Documentation/Splunk/8.0.0/DistSearch/Parallelreduceoverview)
-
[Click Search Help](#)
[logo](https://www.splunk.com)
[Login](http://docs.splunk.com/Documentation?saml=true&redirecturl=https://docs.splunk.com%2FDocumentation%2FSplunk%2F8.0.0%2FDistSearch%2FParallelreduceoverview) | [Sign Up](http://idp.login.splunk.com/signin/register?redirecturl=https://docs.splunk.com/Documentation/Splunk/8.0.0/DistSearch/Parallelreduceoverview)
-
#####
[Pricing](https://www.splunk.com/en_us/products/pricing.html)
-
#####
[Free Trials & Downloads](https://www.splunk.com/en_us/download.html)
Search
Help
Splunk ® Enterprise
Distributed Search
Splunk Cloud Platform ™ Splunk ® Enterprise Splunk ® Universal Forwarder Splunk ® Data Stream Processor (EOS) Splunk ® Cloud Services Splunk ® Attack Analyzer Splunk ® App for Splunk Attack Analyzer Splunk ® Add-on for Splunk Attack Analyzer Splunk ® Asset and Risk Intelligence Splunk ® Asset and Risk Intelligence Echo Splunk ® Add-on for Asset and Risk Intelligence Splunk ® Enterprise Security Splunk ® Mission Control Splunk ® SOAR (Cloud) Splunk ® SOAR (On-premises) Splunk ® User Behavior Analytics Splunk ® App for Fraud Analytics Splunk ® Security Essentials Splunk ® Enterprise Security Content Update Splunk ® Security for SAP ® solutions Splunk ® Security Add-on for SAP ® solutions Splunk ® Security App for SAP ® solutions Splunk ® User Behavior Analytics Monitoring App Splunk ® User Behavior Analytics Kafka Ingestion App IT Operations Overview Splunk ® IT Service Intelligence Splunk ® IT Essentials Work Splunk ® IT Essentials Learn Splunk ® App for Content Packs Splunk ® ITSI Module for Application Performance Monitoring Splunk ® ITSI Event Management SDK Splunk ® Content Packs for ITSI and IT Essentials Work Splunk ® Service Intelligence for SAP ® Solutions Splunk ® Infrastructure Monitoring Add-on Splunk ® ITSI Module for Continuous Delivery Splunk ® Supported Add-ons Splunk ® Add-on for OpenTelemetry Collector Splunk ® Add-on Builder Splunk ® Firehose Nozzle for VMware Tanzu Splunk ® Connect for Kafka Splunk ® Connect for Zoom Splunk ® Connected Experiences Splunk Add-on for AppDynamics Splunk ® Secure Gateway Splunk ® Private Spacebridge Splunk ® Edge Hub mobile app Splunk ® Edge Hub OS Splunk ® Mobile for iOS Splunk ® Mobile for Android Splunk ® TV for Apple TV (EOL) Splunk ® App for TV (EOL) Splunk ® TV Companion (EOL) Splunk ® for iPad (EOL) Splunk ® AR for iOS (EOL) Splunk ® AR for Android (EOL) Splunk ® App for Edge Hub Splunk OT Intelligence Splunk ® TV for Android and Fire TV (EOL) Splunk ® Cloud Gateway (Legacy) Splunk ® Machine Learning Toolkit Splunk ® App for Data Science and Deep Learning Splunk ® App for Anomaly Detection Splunk ® AI Assistant for SPL Splunk ® Common Information Model Add-on Splunk ® Dashboards App Splunk ® InfoSec App Splunk ® App for Lookup File Editing Splunk ® App for SOAR Splunk ® App for SOAR Export Splunk ® DB Connect Splunk ® ODBC Driver Splunk Stream ™ Splunk ® App for AWS Security Dashboards Splunk ® VMware OVA for ITSI Splunk ® Add-on for Infrastructure Data Manager Splunk ® App for PCI Compliance Splunk ® Add-on for Splunk UBA Content Pack for Amazon Web Services Dashboards and Reports Content Pack for Example Glass Tables Content Pack for ITE Work Alert Routing Content Pack for ITSI Monitoring and Alerting Content Pack for Microsoft 365 Content Pack for Microsoft Exchange Content Pack for Monitoring Citrix Content Pack for Monitoring Microsoft Windows Content Pack for Monitoring Phantom as a Service Content Pack for SOAR System Logs Content Pack for Monitoring Pivotal Cloud Foundry Content Pack for Monitoring Splunk as a Service Content Pack for ServiceNow Content Pack for Monitoring Unix and Linux Content Pack for NetApp Data ONTAP Dashboards and Reports Content Pack for Shared IT Infrastructure Components Content Pack for Splunk Infrastructure Monitoring Content Pack for Splunk Observability Cloud Content Pack for Splunk Synthetic Monitoring Content Pack for Third-party APM Content Pack for Unix Dashboards and Reports Content Pack for VMware Dashboards and Reports Content Pack for VMware Monitoring Content Pack for Windows Dashboards and Reports Content Pack for Splunk AppDynamics Content Pack for Cisco ThousandEyes Splunk ® Add-on for Windows Splunk ® Add-on for Microsoft Exchange Indexes Splunk ® OVA for VMware and NetApp Splunk ® OVA for VMware Metrics Splunk ® Supporting Add-on for VMware Splunk ® Supporting Add-on for NetApp Splunk ® Supporting Add-on for Active Directory Splunk ® Phantom App for Splunk Splunk ® Automation Broker Splunk ® Phantom Remote Search Splunk ® Add-on for Splunk Phantom Splunk ® App for Chargeback jQuery Upgrade Readiness Splunk ® SDKs Splunk ® SDK for Python Reference Splunk ® SDK for Java Reference Splunk ® SDK for JavaScript Reference Splunk ® logging for JavaScript Splunk ® logging for Java Splunk ® Web Framework Splunk ® Products Version Compatibility Splunk ® Validated Architectures Get Started with Splunk ® Community Splunk ® Answers Splunk ® Style Guide Legacy products Splunk ® Phantom (Legacy) Custom visualizations (EOL) Bullet Graph (EOL) Calendar Heat Map (EOL) Horizon Chart (EOL) Horseshoe Meter (EOL) Location Tracker (EOL) Parallel Coordinates (EOL) Punchcard (EOL) Sankey Diagram (EOL) Status Indicator (EOL) Timeline (EOL) Treemap (EOL) Splunk ® SDK for PHP Reference (deprecated) Splunk ® SDK for Ruby Reference (deprecated) Splunk ® Add-on for Microsoft Active Directory (EOL) Splunk ® Add-on for Microsoft Windows DNS (EOL) Splunk Add-on for OPC (Legacy) Splunk ® Add-on for Unix and Linux (Legacy) Splunk ® App for Windows Infrastructure (EOL) Splunk ® App for NetApp Data ONTAP (EOL) Splunk ® App for Unix and Linux (EOL) Splunk ® Business Flow (EOL) Splunk ® Deployment Monitor App (Legacy) Splunk ® Industrial Asset Intelligence (Legacy) Splunk ® for Industrial IoT (Legacy) Splunk ® ITSI Module for Cloud Services (deprecated) Splunk ® Metrics Workspace (Legacy) Splunk MINT ™ (EOL) Splunk MINT ™ Management Console (EOL) Splunk MINT ™ App (EOL) Splunk MINT ™ Add-on (EOL) Splunk MINT ™ SDK for Android (EOL) Splunk MINT ™ SDK for iOS (EOL) Splunk MINT ™ REST API (EOL) Splunk ® Mobile Access Server (Legacy) Splunk ® App for VMware (EOL) Splunk ® App for AWS (EOL) Splunk ® App for Infrastructure (EOL) Splunk ® App for Microsoft Exchange (EOL)
7.0.0 7.0.1 7.0.2 7.0.3 7.0.4 7.0.5 7.0.6 7.0.7 7.0.8 7.0.9 7.0.10 7.0.11 7.0.13 7.1.0 7.1.1 7.1.2 7.1.3 7.1.4 7.1.5 7.1.6 7.1.7 7.1.8 7.1.9 7.1.10 7.2.0 7.2.1 7.2.2 7.2.3 7.2.4 7.2.5 7.2.6 7.2.7 7.2.8 7.2.9 7.2.10 7.3.0 7.3.1 7.3.2 7.3.3 7.3.4 7.3.5 7.3.6 7.3.7 7.3.8 7.3.9 8.0.0 8.0.1 8.0.2 8.0.3 8.0.4 8.0.5 8.0.6 8.0.7 8.0.8 8.0.9 8.0.10 8.1.0 8.1.1 8.1.2 8.1.3 8.1.4 8.1.5 8.1.6 8.1.7 8.1.8 8.1.9 8.1.10 8.1.11 8.1.12 8.1.13 8.1.14 8.2.0 8.2.1 8.2.2 8.2.3 8.2.4 8.2.5 8.2.6 8.2.7 8.2.8 8.2.9 8.2.10 8.2.11 8.2.12 (see help.splunk.com for newer versions)
Toggle navigation
Distributed Search
####
[Overview of distributed search](#collapse1)
-
[About distributed search](/Documentation/Splunk/8.0.0/DistSearch/Whatisdistributedsearch)
####
[Knowledge bundle replication](#collapse2)
-
[What search heads send to search peers](/Documentation/Splunk/8.0.0/DistSearch/Whatsearchheadssend)
-
[Knowledge bundle replication overview](/Documentation/Splunk/8.0.0/DistSearch/Knowledgebundlereplication)
-
[Modify the knowledge bundle](/Documentation/Splunk/8.0.0/DistSearch/Limittheknowledgebundlesize)
-
[Classic knowledge bundle replication](/Documentation/Splunk/8.0.0/DistSearch/Classicknowledgebundlereplication)
-
[Cascading knowledge bundle replication](/Documentation/Splunk/8.0.0/DistSearch/Cascadingknowledgebundlereplication)
-
[Mounted knowledge bundle replication](/Documentation/Splunk/8.0.0/DistSearch/Mountedknowledgebundlereplication)
-
[Troubleshoot knowledge bundle replication](/Documentation/Splunk/8.0.0/DistSearch/Troubleshootknowledgebundlereplication)
####
[Deploy distributed search](#collapse3)
-
[Deploy a distributed search environment](/Documentation/Splunk/8.0.0/DistSearch/Overviewofconfiguration)
-
[System requirements and other deployment considerations for distributed search](/Documentation/Splunk/8.0.0/DistSearch/Distsearchsystemrequirements)
-
[Add search peers to the search head](/Documentation/Splunk/8.0.0/DistSearch/Configuredistributedsearch)
-
[Best practice: Forward search head data to the indexer layer](/Documentation/Splunk/8.0.0/DistSearch/Forwardsearchheaddata)
####
[Manage distributed search](#collapse4)
-
[Manage distributed server names](/Documentation/Splunk/8.0.0/DistSearch/Managedistributedservernames)
-
[Create distributed search groups](/Documentation/Splunk/8.0.0/DistSearch/Distributedsearchgroups)
-
[Remove a search peer](/Documentation/Splunk/8.0.0/DistSearch/Removeasearchpeer)
####
[View distributed search status](#collapse5)
-
[View search peer status in Settings](/Documentation/Splunk/8.0.0/DistSearch/Viewsearchpeers)
-
[Use the monitoring console to view distributed search status](/Documentation/Splunk/8.0.0/DistSearch/ViewsearchpeerswithDMC)
####
[Manage parallel reduce search processing](#collapse6)
-
[Overview of parallel reduce search processing](/Documentation/Splunk/8.0.0/DistSearch/Parallelreduceoverview)
-
[Configure parallel reduce search processing](/Documentation/Splunk/8.0.0/DistSearch/Setupparallelreduce)
-
[Apply parallel reduce processing to searches](/Documentation/Splunk/8.0.0/DistSearch/Parallelreducesearches)
####
[Overview of search head clustering](#collapse7)
-
[About search head clustering](/Documentation/Splunk/8.0.0/DistSearch/AboutSHC)
-
[Search head clustering architecture](/Documentation/Splunk/8.0.0/DistSearch/SHCarchitecture)
####
[Deploy search head clustering](#collapse8)
-
[System requirements and other deployment considerations for search head clusters](/Documentation/Splunk/8.0.0/DistSearch/SHCsystemrequirements)
-
[Deploy a search head cluster](/Documentation/Splunk/8.0.0/DistSearch/SHCdeploymentoverview)
-
[Integrate the search head cluster with an indexer cluster](/Documentation/Splunk/8.0.0/DistSearch/SHCandindexercluster)
-
[Connect the search heads in clusters to search peers](/Documentation/Splunk/8.0.0/DistSearch/Connectclustersearchheadstosearchpeers)
-
[Add users to the search head cluster](/Documentation/Splunk/8.0.0/DistSearch/AdduserstotheSHC)
-
[Use a load balancer with search head clustering](/Documentation/Splunk/8.0.0/DistSearch/UseSHCwithloadbalancers)
-
[Deploy a search head cluster in a multisite environment](/Documentation/Splunk/8.0.0/DistSearch/DeploymultisiteSHC)
-
[Deploy a single-member search head cluster](/Documentation/Splunk/8.0.0/DistSearch/DeploysinglememberSHC)
-
[Migrate settings from a standalone search head to a search head cluster](/Documentation/Splunk/8.0.0/DistSearch/Migratefromstandalonesearchheads)
-
[Migrate from a search head pool to a search head cluster](/Documentation/Splunk/8.0.0/DistSearch/Migratefromsearchheadpooling)
-
[Upgrade a search head cluster](/Documentation/Splunk/8.0.0/DistSearch/UpgradeaSHC)
-
[Perform a rolling upgrade of a search head cluster](/Documentation/Splunk/8.0.0/DistSearch/SHCrollingupgrade)
####
[Configure search head clustering](#collapse9)
-
[Configure the search head cluster](/Documentation/Splunk/8.0.0/DistSearch/SHCconfigurationoverview)
-
[Choose the replication factor for the search head cluster](/Documentation/Splunk/8.0.0/DistSearch/ChooseSHCreplicationfactor)
-
[Set a security key for the search head cluster](/Documentation/Splunk/8.0.0/DistSearch/Setsecretkey)
####
[Update search head cluster members](#collapse10)
-
[How configuration changes propagate across the search head cluster](/Documentation/Splunk/8.0.0/DistSearch/HowconfigurationworksinSHC)
-
[Configuration updates that the cluster replicates](/Documentation/Splunk/8.0.0/DistSearch/HowconfrepoworksinSHC)
-
[Use the deployer to distribute apps and configuration updates](/Documentation/Splunk/8.0.0/DistSearch/PropagateSHCconfigurationchanges)
####
[Manage search head clustering](#collapse11)
-
[Add a cluster member](/Documentation/Splunk/8.0.0/DistSearch/Addaclustermember)
-
[Remove a cluster member](/Documentation/Splunk/8.0.0/DistSearch/Removeaclustermember)
-
[Configure a cluster member to run ad hoc searches only](/Documentation/Splunk/8.0.0/DistSearch/Adhocclustermember)
-
[Control captaincy](/Documentation/Splunk/8.0.0/DistSearch/Transfercaptain)
-
[Handle failure of a search head cluster member](/Documentation/Splunk/8.0.0/DistSearch/Handlememberfailure)
-
[Use static captain to recover from loss of majority](/Documentation/Splunk/8.0.0/DistSearch/Staticcaptain)
-
[Put a search head cluster member into detention](/Documentation/Splunk/8.0.0/DistSearch/SHdetention)
-
[Restart the search head cluster](/Documentation/Splunk/8.0.0/DistSearch/RestartSHC)
-
[Back up and restore search head cluster settings](/Documentation/Splunk/8.0.0/DistSearch/BackuprestoreSHC)
####
[Troubleshoot search head clustering](#collapse12)
-
[Use the search head clustering dashboard](/Documentation/Splunk/8.0.0/DistSearch/SHCsettings)
-
[Use the CLI to view information about a search head cluster](/Documentation/Splunk/8.0.0/DistSearch/ViewSHCstatus)
-
[Use the monitoring console to view search head cluster status and troubleshoot issues](/Documentation/Splunk/8.0.0/DistSearch/ViewSHCstatusinDMC)
-
[Deployment issues](/Documentation/Splunk/8.0.0/DistSearch/SHCdeploymentissues)
-
[Runtime considerations](/Documentation/Splunk/8.0.0/DistSearch/Runtimeissues)
-
[Handle Raft issues](/Documentation/Splunk/8.0.0/DistSearch/Handleraftissues)
####
[Distributed search in action](#collapse13)
-
[How authorization works in distributed searches](/Documentation/Splunk/8.0.0/DistSearch/Howauthorizationworksindistributedsearches)
-
[How users can control distributed searches](/Documentation/Splunk/8.0.0/DistSearch/Howuserscancontroldistributedsearches)
####
[Troubleshoot distributed search](#collapse14)
-
[Use the monitoring console to view distributed search status](/Documentation/Splunk/8.0.0/DistSearch/ViewdistsearchstatusinDMC)
-
[General troubleshooting issues](/Documentation/Splunk/8.0.0/DistSearch/Troubleshootdistributedsearch)
-
[Handle slow search peers](/Documentation/Splunk/8.0.0/DistSearch/Slowpeerdisconnect)
-
[Quarantine a search peer](/Documentation/Splunk/8.0.0/DistSearch/Quarantineasearchpeer)
-
[Distributed search error messages](/Documentation/Splunk/8.0.0/DistSearch/Distributedsearcherrormessages)
Toggle navigation
[Hide Contents](#)
-
[Documentation](/Documentation)
-
[Splunk® Enterprise](/Documentation/Splunk)
-
[Distributed Search](/Documentation/Splunk/8.0.0/DistSearch)
-
[Overview of parallel reduce search processing](/Documentation/Splunk/8.0.0/DistSearch/Parallelreduceoverview)
####
[Overview of distributed search](#collapseDesktop1)
-
[About distributed search](/Documentation/Splunk/8.0.0/DistSearch/Whatisdistributedsearch)
####
[Knowledge bundle replication](#collapseDesktop2)
-
[What search heads send to search peers](/Documentation/Splunk/8.0.0/DistSearch/Whatsearchheadssend)
-
[Knowledge bundle replication overview](/Documentation/Splunk/8.0.0/DistSearch/Knowledgebundlereplication)
-
[Modify the knowledge bundle](/Documentation/Splunk/8.0.0/DistSearch/Limittheknowledgebundlesize)
-
[Classic knowledge bundle replication](/Documentation/Splunk/8.0.0/DistSearch/Classicknowledgebundlereplication)
-
[Cascading knowledge bundle replication](/Documentation/Splunk/8.0.0/DistSearch/Cascadingknowledgebundlereplication)
-
[Mounted knowledge bundle replication](/Documentation/Splunk/8.0.0/DistSearch/Mountedknowledgebundlereplication)
-
[Troubleshoot knowledge bundle replication](/Documentation/Splunk/8.0.0/DistSearch/Troubleshootknowledgebundlereplication)
####
[Deploy distributed search](#collapseDesktop3)
-
[Deploy a distributed search environment](/Documentation/Splunk/8.0.0/DistSearch/Overviewofconfiguration)
-
[System requirements and other deployment considerations for distributed search](/Documentation/Splunk/8.0.0/DistSearch/Distsearchsystemrequirements)
-
[Add search peers to the search head](/Documentation/Splunk/8.0.0/DistSearch/Configuredistributedsearch)
-
[Best practice: Forward search head data to the indexer layer](/Documentation/Splunk/8.0.0/DistSearch/Forwardsearchheaddata)
####
[Manage distributed search](#collapseDesktop4)
-
[Manage distributed server names](/Documentation/Splunk/8.0.0/DistSearch/Managedistributedservernames)
-
[Create distributed search groups](/Documentation/Splunk/8.0.0/DistSearch/Distributedsearchgroups)
-
[Remove a search peer](/Documentation/Splunk/8.0.0/DistSearch/Removeasearchpeer)
####
[View distributed search status](#collapseDesktop5)
-
[View search peer status in Settings](/Documentation/Splunk/8.0.0/DistSearch/Viewsearchpeers)
-
[Use the monitoring console to view distributed search status](/Documentation/Splunk/8.0.0/DistSearch/ViewsearchpeerswithDMC)
####
[Manage parallel reduce search processing](#collapseDesktop6)
-
[Overview of parallel reduce search processing](/Documentation/Splunk/8.0.0/DistSearch/Parallelreduceoverview)
-
[Configure parallel reduce search processing](/Documentation/Splunk/8.0.0/DistSearch/Setupparallelreduce)
-
[Apply parallel reduce processing to searches](/Documentation/Splunk/8.0.0/DistSearch/Parallelreducesearches)
####
[Overview of search head clustering](#collapseDesktop7)
-
[About search head clustering](/Documentation/Splunk/8.0.0/DistSearch/AboutSHC)
-
[Search head clustering architecture](/Documentation/Splunk/8.0.0/DistSearch/SHCarchitecture)
####
[Deploy search head clustering](#collapseDesktop8)
-
[System requirements and other deployment considerations for search head clusters](/Documentation/Splunk/8.0.0/DistSearch/SHCsystemrequirements)
-
[Deploy a search head cluster](/Documentation/Splunk/8.0.0/DistSearch/SHCdeploymentoverview)
-
[Integrate the search head cluster with an indexer cluster](/Documentation/Splunk/8.0.0/DistSearch/SHCandindexercluster)
-
[Connect the search heads in clusters to search peers](/Documentation/Splunk/8.0.0/DistSearch/Connectclustersearchheadstosearchpeers)
-
[Add users to the search head cluster](/Documentation/Splunk/8.0.0/DistSearch/AdduserstotheSHC)
-
[Use a load balancer with search head clustering](/Documentation/Splunk/8.0.0/DistSearch/UseSHCwithloadbalancers)
-
[Deploy a search head cluster in a multisite environment](/Documentation/Splunk/8.0.0/DistSearch/DeploymultisiteSHC)
-
[Deploy a single-member search head cluster](/Documentation/Splunk/8.0.0/DistSearch/DeploysinglememberSHC)
-
[Migrate settings from a standalone search head to a search head cluster](/Documentation/Splunk/8.0.0/DistSearch/Migratefromstandalonesearchheads)
-
[Migrate from a search head pool to a search head cluster](/Documentation/Splunk/8.0.0/DistSearch/Migratefromsearchheadpooling)
-
[Upgrade a search head cluster](/Documentation/Splunk/8.0.0/DistSearch/UpgradeaSHC)
-
[Perform a rolling upgrade of a search head cluster](/Documentation/Splunk/8.0.0/DistSearch/SHCrollingupgrade)
####
[Configure search head clustering](#collapseDesktop9)
-
[Configure the search head cluster](/Documentation/Splunk/8.0.0/DistSearch/SHCconfigurationoverview)
-
[Choose the replication factor for the search head cluster](/Documentation/Splunk/8.0.0/DistSearch/ChooseSHCreplicationfactor)
-
[Set a security key for the search head cluster](/Documentation/Splunk/8.0.0/DistSearch/Setsecretkey)
####
[Update search head cluster members](#collapseDesktop10)
-
[How configuration changes propagate across the search head cluster](/Documentation/Splunk/8.0.0/DistSearch/HowconfigurationworksinSHC)
-
[Configuration updates that the cluster replicates](/Documentation/Splunk/8.0.0/DistSearch/HowconfrepoworksinSHC)
-
[Use the deployer to distribute apps and configuration updates](/Documentation/Splunk/8.0.0/DistSearch/PropagateSHCconfigurationchanges)
####
[Manage search head clustering](#collapseDesktop11)
-
[Add a cluster member](/Documentation/Splunk/8.0.0/DistSearch/Addaclustermember)
-
[Remove a cluster member](/Documentation/Splunk/8.0.0/DistSearch/Removeaclustermember)
-
[Configure a cluster member to run ad hoc searches only](/Documentation/Splunk/8.0.0/DistSearch/Adhocclustermember)
-
[Control captaincy](/Documentation/Splunk/8.0.0/DistSearch/Transfercaptain)
-
[Handle failure of a search head cluster member](/Documentation/Splunk/8.0.0/DistSearch/Handlememberfailure)
-
[Use static captain to recover from loss of majority](/Documentation/Splunk/8.0.0/DistSearch/Staticcaptain)
-
[Put a search head cluster member into detention](/Documentation/Splunk/8.0.0/DistSearch/SHdetention)
-
[Restart the search head cluster](/Documentation/Splunk/8.0.0/DistSearch/RestartSHC)
-
[Back up and restore search head cluster settings](/Documentation/Splunk/8.0.0/DistSearch/BackuprestoreSHC)
####
[Troubleshoot search head clustering](#collapseDesktop12)
-
[Use the search head clustering dashboard](/Documentation/Splunk/8.0.0/DistSearch/SHCsettings)
-
[Use the CLI to view information about a search head cluster](/Documentation/Splunk/8.0.0/DistSearch/ViewSHCstatus)
-
[Use the monitoring console to view search head cluster status and troubleshoot issues](/Documentation/Splunk/8.0.0/DistSearch/ViewSHCstatusinDMC)
-
[Deployment issues](/Documentation/Splunk/8.0.0/DistSearch/SHCdeploymentissues)
-
[Runtime considerations](/Documentation/Splunk/8.0.0/DistSearch/Runtimeissues)
-
[Handle Raft issues](/Documentation/Splunk/8.0.0/DistSearch/Handleraftissues)
####
[Distributed search in action](#collapseDesktop13)
-
[How authorization works in distributed searches](/Documentation/Splunk/8.0.0/DistSearch/Howauthorizationworksindistributedsearches)
-
[How users can control distributed searches](/Documentation/Splunk/8.0.0/DistSearch/Howuserscancontroldistributedsearches)
####
[Troubleshoot distributed search](#collapseDesktop14)
-
[Use the monitoring console to view distributed search status](/Documentation/Splunk/8.0.0/DistSearch/ViewdistsearchstatusinDMC)
-
[General troubleshooting issues](/Documentation/Splunk/8.0.0/DistSearch/Troubleshootdistributedsearch)
-
[Handle slow search peers](/Documentation/Splunk/8.0.0/DistSearch/Slowpeerdisconnect)
-
[Quarantine a search peer](/Documentation/Splunk/8.0.0/DistSearch/Quarantineasearchpeer)
-
[Distributed search error messages](/Documentation/Splunk/8.0.0/DistSearch/Distributedsearcherrormessages)
###
Related answers from Splunk Community
-
[parallel reduce search processing - How do i know ...](https://community.splunk.com/t5/Knowledge-Management/parallel-reduce-search-processing-How-do-i-know-it-is-working-Do/m-p/399882?search-action-id=280042823165&search-result-uid=399882)
-
[What does stats partitions do?](https://community.splunk.com/t5/Splunk-Search/What-does-stats-partitions-do/m-p/448282?search-action-id=280042823165&search-result-uid=448282)
-
[integrating Splunk with Elasticsearch](https://community.splunk.com/t5/Getting-Data-In/integrating-Splunk-with-Elasticsearch/m-p/696593?search-action-id=280042823165&search-result-uid=696593)
-
[Get totals of sessions for each IP](https://community.splunk.com/t5/Splunk-Search/Get-totals-of-sessions-for-each-IP/m-p/425669?search-action-id=280042823165&search-result-uid=425669)
-
[Splunk Python SDK - How to call my custom search c...](https://community.splunk.com/t5/Splunk-Search/Splunk-Python-SDK-How-to-call-my-custom-search-command-only-once/m-p/455460?search-action-id=280042823165&search-result-uid=455460)
-
[EUM stops logging virtual pages when we upgraded t...](https://community.splunk.com/t5/Splunk-AppDynamics/EUM-stops-logging-virtual-pages-when-we-upgraded-the-angular-ui/m-p/735760?search-action-id=280042823165&search-result-uid=735760)
-
[Not able to see EUM Browser Data for configured Ap...](https://community.splunk.com/t5/Splunk-AppDynamics/Not-able-to-see-EUM-Browser-Data-for-configured-Application-in/m-p/737079?search-action-id=280042823165&search-result-uid=737079)
-
[Smartstore GCS: Why is there upload error status 9...](https://community.splunk.com/t5/Splunk-Enterprise/Smartstore-GCS-Why-is-there-upload-error-status-9-and-14/m-p/602390?search-action-id=280042823165&search-result-uid=602390)
[Read more...](https://community.splunk.com/t5/forums/searchpage/tab/message?filter=location&q=Overview+of+parallel+reduce+search+processing&advanced=true&location=category:en-us-splunk-answers&collapse_discussion=true&search_type=thread)
************************************************************************
We're excited to share that Splunk Enterprise documentation is now available on our updated web portal at [help.splunk.com](https://help.splunk.com/en/splunk-enterprise).
************************************************************************
For your convenience, older content on this docs.splunk.com website remains accessible for legacy reference. However, we encourage you to visit the new portal for the latest information and updates.
************************************************************************
To access newer versions of content, replace the version number in your browser's URL with a supported version such as 10.2.0 and reload the page, or navigate directly to [help.splunk.com](https://help.splunk.com/en/splunk-enterprise).
************************************************************************
Thank you for your understanding as we transition to a more streamlined and up-to-date documentation experience.
************************************************************************
This documentation does not apply to the most recent version of Splunk ® Enterprise.
For documentation on the most recent version, go to [the latest release](/Documentation/Splunk/latest/DistSearch/Parallelreduceoverview ).
# Overview of parallel reduce search processing
High-cardinality searches are searches that must match, filter, and aggregate extremely large numbers of unique field values. User IDs, session IDs, and telephone numbers are examples of fields that tend to be high in cardinality. Searches that compute aggregates over high-cardinality fields can be slow to complete. If high-cardinality searches in your Splunk platform deployment are slow, you can use parallel reduce search processing to help them complete quicker.
In a typical distributed search process, there are two broad search processing phases: a map phase and a reduce phase. The map phase takes place across the indexers in your deployment. In the map phase, the indexers locate event data that matches the search query and sort it into field-value pairs. When the map phase is complete, indexers send the results to the search head for the reduce phase. During the reduce phase, the search heads process the results through the commands in your search and aggregate them to produce a final result set.
The following diagram illustrates the standard two-phase distributed search process.
[](/File:2-phase-distributed-search-Platform-7.1.0.png)
The parallel reduce process inserts an intermediate reduce phase into the map-reduce paradigm, making it a three-phase map-reduce-reduce operation. In this intermediate reduce phase, a subset of your indexers serve as intermediate reducers . The intermediate reducers divide up the mapped results and perform reduce operations on those results for certain supported search commands. When the intermediate reducers complete their work, they send the results to the search head, where the final result reduction and aggregation operations take place. The parallel processing of reduction work that otherwise would be done entirely by the search head can result in faster completion times for high-cardinality searches that aggregate large numbers of search results.
The following diagram illustrates the three-phase parallel reduce search process.
[](/File:3-phase-distributed-search-Platform-7.1.0.png)
## Parallel reduce prerequisites
To enable parallel reduce search processing, you need the following prerequisites in place:
Prerequisite
Details
For more information see
A distributed search environment.
Parallel reduce search processing requires a distributed search deployment architecture.
[About distributed search](http://docs.splunk.com/Documentation/Splunk/8.0.0/DistSearch/Whatisdistributedsearch)
An environment where the indexers are at a single site.
Parallel reduce search processing is not site-aware. Do not use it if your indexers are in a [multisite indexer cluster](/Splexicon:Multisitecluster) , or if you have non-clustered indexers spread across several sites.
Splunk platform version 7.1.0 or later for all participating machines.
Upgrade all Splunk instances that participate in the parallel reduce process to version 7.1.0 or later. Participating instances include all indexers and search heads.
[How to upgrade Splunk Enterprise](http://docs.splunk.com/Documentation/Splunk/8.0.0/Installation/HowtoupgradeSplunk) in the Installation Manual
Internal search head data forwarded to the indexer layer.
The parallel reduce search process ignores all data on the search head. If you plan to run parallel reduce searches, the best practice is to forward all search head data to the indexer layer.
[Best Practice: Forward search head data to the indexer layer](http://docs.splunk.com/Documentation/Splunk/8.0.0/DistSearch/Forwardsearchheaddata)
A low to medium average indexer load.
Parallel reduce search processes add a significant amount of indexer load. If you attempt to run parallel reduce searches in an already overloaded indexer system, you might encounter slow performance. If you run an indexer cluster, you might see skipped heartbeats between peer nodes and the cluster master.
See [Use the monitoring console to view index and volume status](http://docs.splunk.com/Documentation/Splunk/8.0.0/Indexer/Viewindexstatus), in Managing Indexers and Clusters of Indexers
All indexers configured to allow secure communication with intermediate reducers.
Admins must set an identical pass4SymmKey security key in the [parallelreduce] stanza of server.conf for all indexers. This security key enables communication between indexers and intermediate reducers.
[Configure your indexers to communicate with intermediate reducers](http://docs.splunk.com/Documentation/Splunk/8.0.0/DistSearch/Setupparallelreduce#Configure_your_indexers_to_communicate_with_intermediate_reducers)
Users with roles that include the run_multi_phased_searches [capability](/Splexicon:Capability) .
Users must have the run_multi_phased_searches capability to use the redistribute command. The redistribute command applies parallel reduce search processing to a search.
[Apply parallel reduce processing to searches](http://docs.splunk.com/Documentation/Splunk/8.0.0/DistSearch/Parallelreducesearches)
## Next steps
Learn how to configure your deployment for parallel reduce search processing. See [Configure parallel reduce search processing](http://docs.splunk.com/Documentation/Splunk/8.0.0/DistSearch/Setupparallelreduce).
[Last modified](/index.php?title=Documentation:Splunk:DistSearch:Parallelreduceoverview:6.2.0&diff=1201560&oldid=820503&singlediff=true) on 15 October, 2020
[](/Documentation/Splunk/8.0.0/DistSearch/ViewsearchpeerswithDMC)
[Use the monitoring console to view distributed search status](/Documentation/Splunk/8.0.0/DistSearch/ViewsearchpeerswithDMC)
[Configure parallel reduce search processing](/Documentation/Splunk/8.0.0/DistSearch/Setupparallelreduce)
[](/Documentation/Splunk/8.0.0/DistSearch/Setupparallelreduce)
This documentation applies to the following versions of Splunk ® Enterprise:
7.1.0, 7.1.1, 7.1.2, 7.1.3, 7.1.4, 7.1.5, 7.1.6, 7.1.7, 7.1.8, 7.1.9, 7.1.10, 7.2.0, 7.2.1, 7.2.2, 7.2.3, 7.2.4, 7.2.5, 7.2.6, 7.2.7, 7.2.8, 7.2.9, 7.2.10, 7.3.0, 7.3.1, 7.3.2, 7.3.3, 7.3.4, 7.3.5, 7.3.6, 7.3.7, 7.3.8, 7.3.9, 8.0.0, 8.0.1, 8.0.2, 8.0.3, 8.0.4, 8.0.5, 8.0.6, 8.0.7, 8.0.8, 8.0.9, 8.0.10
## Comments
[Download manual](/index.php?title=Documentation:Splunk:DistSearch:Parallelreduceoverview:6.2.0&action=pdfbook&version=8.0.0&product=Splunk)
[Download this page](/index.php?title=Documentation:Splunk:DistSearch:Parallelreduceoverview:6.2.0&action=pdfbook&version=8.0.0&topic=1&product=Splunk)
[Back To Top](#)
## Overview of parallel reduce search processing
-
[Parallel reduce prerequisites](#Parallel_reduce_prerequisites)
-
[Next steps](#Next_steps)
Please expect delayed responses to documentation feedback while the team migrates content to a new system. We value your input and thank you for your patience as we work to provide you with an improved content experience!
## Was this topic useful?
Yes
No
Please specify the reason
Please select
The topic did not answer my question(s)
I found an error
I did not like the topic organization
Other
Please provide your comments here. Ask a question or make a suggestion.
Enter your email address if you would like someone from the documentation team to reply to your question or suggestion.
Send Feedback
Feedback submitted, thanks!
You must be logged into splunk.com in order to post comments.
[Log in now](http://docs.splunk.com/Documentation?saml=true&redirecturl=https://docs.splunk.com%2FDocumentation%2FSplunk%2F8.0.0%2FDistSearch%2FParallelreduceoverview).
Please try to keep this discussion focused on the content covered in this documentation topic.
If you have a more general question about Splunk functionality or are experiencing a difficulty with Splunk,
consider posting a question to [Splunkbase Answers](https://answers.splunk.com).
0
out of 1000 Characters
Submit Comment
Your Comment Has Been Posted Above
We use our own and third-party cookies to provide you with a great online experience. We also use these cookies to improve our products and services, support our marketing campaigns, and advertise to you on our website and other websites. Some cookies may continue to collect information after you have left our website.
[Learn more (including how to update your settings) here »](https://www.splunk.com/en_us/legal/splunk-cookie-policy.html)
Closing this box indicates that you accept our Cookie Policy.
-
[](https://twitter.com/splunk)
-
[](https://www.facebook.com/splunk)
-
[](https://www.linkedin.com/company/splunk)
-
[](https://www.youtube.com/user/splunkvideos)
-
[](https://www.instagram.com/splunk/)
© 2005-2026 Splunk LLC All rights reserved.
-
[Legal](https://www.splunk.com/en_us/legal.html)
-
[Privacy](https://www.splunk.com/en_us/legal/privacy/privacy-policy.html)
-
[Website Term of Use](https://www.splunk.com/en_us/legal/terms/terms-of-use.html)