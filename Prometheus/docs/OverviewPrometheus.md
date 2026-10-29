# Overview | Prometheus

- 来源: https://prometheus.io/docs/
- 归档时间: 2026-10-29
- 说明: 官方文档页面的 Markdown 快照（由 HTML 转换，格式为自动生成）

---

[Prometheus](/) [Docs](/docs/introduction/overview/)[Download](/download/)[Community](/community/)[Support & Training](/support-training/)[Blog](/blog/)
Ctrl + K
[](https://github.com/prometheus)
Show nav [Introduction](#required-for-focus) [Overview](/docs/introduction/overview/)[First steps](/docs/introduction/first_steps/)[Comparison to alternatives](/docs/introduction/comparison/)[FAQ](/docs/introduction/faq/)[Roadmap](/docs/introduction/roadmap/)[Design documents](/docs/introduction/design-doc/)[Media](/docs/introduction/media/)[Glossary](/docs/introduction/glossary/)[Long-term support](/docs/introduction/release-cycle/)
[Concepts](#required-for-focus) [Data model](/docs/concepts/data_model/)[Metric types](/docs/concepts/metric_types/)[Jobs and instances](/docs/concepts/jobs_instances/)
[Prometheus Server](#required-for-focus)
[Getting started](/docs/prometheus/latest/getting_started/)[Installation](/docs/prometheus/latest/installation/)[Configuration](#required-for-focus) [Configuration](/docs/prometheus/latest/configuration/configuration/)[Recording rules](/docs/prometheus/latest/configuration/recording_rules/)[Alerting rules](/docs/prometheus/latest/configuration/alerting_rules/)[Template examples](/docs/prometheus/latest/configuration/template_examples/)[Template reference](/docs/prometheus/latest/configuration/template_reference/)[HTTP configuration for promtool](/docs/prometheus/latest/configuration/promtool/)[Unit testing for rules](/docs/prometheus/latest/configuration/unit_testing_rules/)[HTTPS and authentication](/docs/prometheus/latest/configuration/https/)
[Agent Mode](/docs/prometheus/latest/prometheus_agent/)[Querying](#required-for-focus) [Basics](/docs/prometheus/latest/querying/basics/)[Operators](/docs/prometheus/latest/querying/operators/)[Functions](/docs/prometheus/latest/querying/functions/)[Examples](/docs/prometheus/latest/querying/examples/)[HTTP API](/docs/prometheus/latest/querying/api/)[Remote Read API](/docs/prometheus/latest/querying/remote_read_api/)
[Storage](/docs/prometheus/latest/storage/)[Federation](/docs/prometheus/latest/federation/)[HTTP SD](/docs/prometheus/latest/http_sd/)[Management API](/docs/prometheus/latest/management_api/)[Command Line](#required-for-focus) [prometheus](/docs/prometheus/latest/command-line/prometheus/)[promtool](/docs/prometheus/latest/command-line/promtool/)
[Migration](/docs/prometheus/latest/migration/)[API stability](/docs/prometheus/latest/stability/)[Feature flags](/docs/prometheus/latest/feature_flags/)
[Visualization](#required-for-focus) [Expression browser](/docs/visualization/browser/)[Grafana](/docs/visualization/grafana/)[Perses](/docs/visualization/perses/)[Console templates](/docs/visualization/consoles/)
[Instrumenting](#required-for-focus) [Client libraries](/docs/instrumenting/clientlibs/)[Writing client libraries](/docs/instrumenting/writing_clientlibs/)[Pushing metrics](/docs/instrumenting/pushing/)[Exporters and integrations](/docs/instrumenting/exporters/)[Writing exporters](/docs/instrumenting/writing_exporters/)[Exposition formats](/docs/instrumenting/exposition_formats/)[UTF-8 escaping schemes](/docs/instrumenting/escaping_schemes/)[Content negotiation](/docs/instrumenting/content_negotiation/)
[Operating](#required-for-focus) [Security](/docs/operating/security/)[Integrations](/docs/operating/integrations/)
[Alertmanager](#required-for-focus)
[Alerting overview](/docs/alerting/latest/overview/)[Alertmanager](/docs/alerting/latest/alertmanager/)[Configuration](/docs/alerting/latest/configuration/)[High Availability](/docs/alerting/latest/high_availability/)[Notification Integrations](/docs/alerting/latest/integrations/)[Alerts API](/docs/alerting/latest/alerts_api/)[Notification template reference](/docs/alerting/latest/notifications/)[Notification template examples](/docs/alerting/latest/notification_examples/)[Management API](/docs/alerting/latest/management_api/)[HTTPS and authentication](/docs/alerting/latest/https/)
[Best practices](#required-for-focus) [Metric and label naming](/docs/practices/naming/)[Consoles and dashboards](/docs/practices/consoles/)[Instrumentation](/docs/practices/instrumentation/)[Histograms and summaries](/docs/practices/histograms/)[Alerting](/docs/practices/alerting/)[Recording rules](/docs/practices/rules/)[When to use the Pushgateway](/docs/practices/pushing/)[Remote write tuning](/docs/practices/remote_write/)[The Zen of Prometheus](/docs/practices/the_zen/)
[Guides](#required-for-focus) [Basic auth](/docs/guides/basic-auth/)[Monitoring Docker container metrics using cAdvisor](/docs/guides/cadvisor/)[Contributing](/docs/guides/contributing/)[Use file-based service discovery to discover scrape targets](/docs/guides/file-sd/)[Instrumenting a Go application](/docs/guides/go-application/)[Understanding and using the multi-target exporter pattern](/docs/guides/multi-target-exporter/)[Monitoring Linux host metrics with the Node Exporter](/docs/guides/node-exporter/)[OpenTelemetry](/docs/guides/opentelemetry/)[UTF-8 in Prometheus](/docs/guides/utf8/)[Docker Swarm](/docs/guides/dockerswarm/)[OpenMetrics 2.0 Migration Guide for Client Libraries](/docs/guides/open_metrics_2_0_migration/)[Query log](/docs/guides/query-log/)[TLS encryption](/docs/guides/tls-encryption/)
[Tutorials](#required-for-focus) [Understanding metric types](/docs/tutorials/understanding_metric_types/)[Instrumenting HTTP server written in Go](/docs/tutorials/instrumenting_http_server_in_go/)[Visualizing metrics using Grafana](/docs/tutorials/visualizing_metrics_using_grafana/)[Alerting based on metrics](/docs/tutorials/alerting_based_on_metrics/)
[Specifications](#required-for-focus) [Native Histograms](/docs/specs/native_histograms/)[OpenMetrics](#required-for-focus) [1.0](/docs/specs/om/open_metrics_spec/)[2.0](/docs/specs/om/open_metrics_spec_2_0/)
[Remote Write](#required-for-focus) [1.0](/docs/specs/prw/remote_write_spec/)[2.0](/docs/specs/prw/remote_write_spec_2_0/)
# Overview
## What is Prometheus?[](#what-is-prometheus)
[Prometheus](https://github.com/prometheus) is an open-source systems
monitoring and alerting toolkit originally built at
[SoundCloud](https://soundcloud.com). Since its inception in 2012, many
companies and organizations have adopted Prometheus, and the project has a very
active developer and user [community](/community/). It is now a standalone open source project
and maintained independently of any company. To emphasize this, and to clarify
the project's [governance](/governance/) structure, Prometheus joined the
[Cloud Native Computing Foundation](https://cncf.io/) in 2016
as the second hosted project, after [Kubernetes](http://kubernetes.io/).
Prometheus collects and stores its metrics as time series data, i.e. metrics information is stored with the timestamp at which it was recorded, alongside optional key-value pairs called labels.
For more elaborate overviews of Prometheus, see the resources linked from the
[media](/docs/introduction/media/) section.
### Features[](#features)
Prometheus's main features are:
- a multi-dimensional [data model](/docs/concepts/data_model/) with time series data identified by metric name and key/value pairs
- PromQL, a [flexible query language](/docs/prometheus/latest/querying/basics/)
to leverage this dimensionality
- no reliance on distributed storage; single server nodes are autonomous
- time series collection happens via a pull model over HTTP
- [pushing time series](/docs/instrumenting/pushing/) is supported via an intermediary gateway
- targets are discovered via service discovery or static configuration
- multiple modes of graphing and dashboarding support
### What are metrics?[](#what-are-metrics)
Metrics are numerical measurements in layperson terms. The term time series refers to the recording of changes over time. What users want to measure differs from application to application. For a web server, it could be request times; for a database, it could be the number of active connections or active queries, and so on.
Metrics play an important role in understanding why your application is working in a certain way. Let's assume you are running a web application and discover that it is slow. To learn what is happening with your application, you will need some information. For example, when the number of requests is high, the application may become slow. If you have the request count metric, you can determine the cause and increase the number of servers to handle the load.
### Components[](#components)
The Prometheus ecosystem consists of multiple components, many of which are
optional:
- the main [Prometheus server](https://github.com/prometheus/prometheus) which scrapes and stores time series data
- [client libraries](/docs/instrumenting/clientlibs/) for instrumenting application code
- a [push gateway](https://github.com/prometheus/pushgateway) for supporting short-lived jobs
- special-purpose [exporters](/docs/instrumenting/exporters/) for services like HAProxy, StatsD, Graphite, etc.
- an [alertmanager](https://github.com/prometheus/alertmanager) to handle alerts
- various support tools
Most Prometheus components are written in [Go](https://go.dev/), making
them easy to build and deploy as static binaries.
### Architecture[](#architecture)
This diagram illustrates the architecture of Prometheus and some of
its ecosystem components:
Prometheus scrapes metrics from instrumented jobs, either directly or via an
intermediary push gateway for short-lived jobs. It stores all scraped samples
locally and runs rules over this data to either aggregate and record new time
series from existing data or generate alerts. [Grafana](https://grafana.com/) or
other API consumers can be used to visualize the collected data.
## When does it fit?[](#when-does-it-fit)
Prometheus works well for recording any purely numeric time series. It fits
both machine-centric monitoring as well as monitoring of highly dynamic
service-oriented architectures. In a world of microservices, its support for
multi-dimensional data collection and querying is a particular strength.
Prometheus is designed for reliability, to be the system you go to
during an outage to allow you to quickly diagnose problems. Each Prometheus
server is standalone, not depending on network storage or other remote services.
You can rely on it when other parts of your infrastructure are broken, and
you do not need to set up extensive infrastructure to use it.
## When does it not fit?[](#when-does-it-not-fit)
Prometheus values reliability. You can always view what statistics are
available about your system, even under failure conditions. If you need 100%
accuracy, such as for per-request billing, Prometheus is not a good choice, as
the collected data will likely not be detailed and complete enough. In such a
case, you would be best off using some other system to collect and analyze the
data for billing, and Prometheus for the rest of your monitoring.
[Edit
Edit this page](https://github.com/prometheus/docs/blob/main/docs/introduction/overview.md)[Issue
Report an issue](https://github.com/prometheus/docs/issues/new?title=docs%3A%20Issue%20with%20%22Overview%22&body=**Page%3A**%20https%3A%2F%2Fprometheus.io%2Fdocs%2Fintroduction%2Foverview%2F%0A%0A**Describe%20the%20issue%3A**%0A%0A)
[Next
First steps](/docs/introduction/first_steps/)
On this page
© Prometheus Authors 2014- 2026 | All components are available under the [Apache 2 License](http://www.apache.org/licenses/LICENSE-2.0) on [GitHub](https://github.com/prometheus).
© 2026 The Linux Foundation. All rights reserved. The Linux Foundation has registered trademarks and uses trademarks. For a list of trademarks of The Linux Foundation, please see our [Trademark Usage](https://www.linuxfoundation.org/trademark-usage) page.