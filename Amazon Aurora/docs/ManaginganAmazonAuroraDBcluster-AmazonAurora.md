# Managing an Amazon Aurora DB cluster - Amazon Aurora

- 来源: https://docs.aws.amazon.com/AmazonRDS/latest/AuroraUserGuide/CHAP_Aurora.html
- 归档时间: 2026-10-29
- 说明: 官方文档页面的 Markdown 快照（由 HTML 转换，格式为自动生成）

---

[View a markdown version of this page](CHAP_Aurora.md)
[](/pdfs/AmazonRDS/latest/AuroraUserGuide/aurora-ug.pdf#CHAP_Aurora)
[Documentation](/index.html)[Amazon RDS](/rds/index.html)[User Guide for Aurora](CHAP_AuroraOverview.html)
# Managing an Amazon Aurora DB cluster
This section shows how to manage and maintain your Aurora DB cluster.
Aurora involves clusters of database servers that are connected in a replication topology. Thus,
managing Aurora often involves deploying changes to multiple servers and making sure that all
Aurora Replicas are keeping up with the source server. Because Aurora transparently scales
the underlying storage as your data grows, managing Aurora requires relatively little management
of disk storage. Likewise, because Aurora automatically performs continuous backups, an Aurora
cluster does not require extensive planning or downtime for performing backups.
###### Topics
- [Stopping and starting an Amazon Aurora DB cluster](./aurora-cluster-stop-start.html)
- [Automatically connecting an EC2 instance and an Aurora DB cluster](./ec2-rds-connect.html)
- [Automatically connecting a Lambda function and an Aurora DB cluster](./lambda-rds-connect.html)
- [Modifying an Amazon Aurora DB cluster](./Aurora.Modifying.html)
- [Adding Aurora Replicas to a DB cluster](./aurora-replicas-adding.html)
- [Managing performance and scaling for Aurora DB clusters](./Aurora.Managing.Performance.html)
- [Cloning a volume for an Amazon Aurora DB cluster](./Aurora.Managing.Clone.html)
- [Integrating Aurora with other AWS services](./Aurora.Integrating.html)
- [Maintaining an Amazon Aurora DB cluster](./USER_UpgradeDBInstance.Maintenance.html)
- [Rebooting an Amazon Aurora DB cluster or Amazon Aurora DB instance](./USER_RebootCluster.html)
- [Failing over an Amazon Aurora DB cluster](./aurora-failover.html)
- [Deleting Aurora DB clusters and DB instances](./USER_DeleteCluster.html)
- [Tagging Amazon Aurora andAmazon RDS resources](./USER_Tagging.html)
- [Amazon Resource Names (ARNs) in Amazon RDS](./USER_Tagging.ARN.html)
- [Amazon Aurora updates](./Aurora.Updates.html)
[Document Conventions](/general/latest/gr/docconventions.html)
Tutorial: Creating a MySQL DB cluster with a custom parameter
group
Stopping and starting a cluster
Did this page help you? - Yes
Thanks for letting us know we're doing a good job!
If you've got a moment, please tell us what we did right so we can do more of it.
Did this page help you? - No
Thanks for letting us know this page needs work. We're sorry we let you down.
If you've got a moment, please tell us how we can make the documentation better.