# Upgrading Search to 7.3 Overview

Liferay 7.3 supports only Elasticsearch 7.9.0+ via the out-of-the-box Liferay Connector to Elasticsearch. The matrix of pre-upgrade stacks you are migrating from is more numerous, and it's important to undestand the high-level steps required to safely navigate from your existing stack to the Liferay 7.3 stack. 

Find the scenario that matches your Liferay version and Liferay Enterprise Search (LES) version (if you're using LES), and your current search engine stack. Use the *Upgrade Steps* column to guide your upgrade.

| Pre-Upgrade Liferay Version [+ LES Version] | Pre-Upgrade Search Engine | Upgrade Steps |
| :-------- | :---------------- | :-------------- |
| **Liferay 7.2** | Elasticsearch 7.9+ | 1. [Connect Liferay to Elasticsearch 7.](./elasticsearch/connecting-to-elasticsearch.md)<br><br>2. [Configure security.](./elasticsearch/securing-elasticsearch.md)<br><br>3. [Upgrade Liferay.](../../installation-and-upgrades/upgrading-liferay/upgrade-basics/upgrade-overview.md)<br><br>4. [Re-index search & spell check indexes.](../../installation-and-upgrades/upgrading-liferay/upgrade-basics/post-upgrade-considerations.md) |
| **Liferay 7.2 + LES 3.0** (*Monitoring*, *Learning to Rank*) | Elasticsearch 7.9+ | 1. Connect Liferay to Elasticsearch 7.<br><br>2. Configure security.<br><br>3. Install Kibana 7.9+ if you are currently using *Kibana and Monitoring*.<br><br>4. Install and deploy LES Monitoring if you are currently using Kibana and *Elasticsearch Monitoring/X-Pack Monitoring*.<br><br>5. Configure the *Elasticsearch Monitoring* connector if you are using *LES Monitoring* or *Connector to X-Pack Monitoring*.<br><br>6. [Upgrade Liferay.](../../installation-and-upgrades/upgrading-liferay/upgrade-basics/upgrade-overview.md)<br><br>7. [Re-index search & spell check indexes.](../../installation-and-upgrades/upgrading-liferay/upgrade-basics/post-upgrade-considerations.md) |
| **Liferay 7.2** | Elasticsearch 7.3.x-7.8.x | 1. [Install Elasticsearch 7.9+.](./elasticsearch/installing-elasticsearch.md)<br><br>2. Follow [Common Upgrade Steps](#common-upgrade-steps) |
| **Liferay 7.2 + LES 2.0** (*Monitoring*, *Learning to Rank*) | Elasticsearch 7.3.x-7.8.x | 1. [Install Elasticsearch 7.9+.](./elasticsearch/installing-elasticsearch.md)<br><br>2. Follow [LES Upgrade Steps](#les-upgrade-steps) |
| **Liferay 7.2** | Elasticsearch 6.x | 1. [Install Elasticsearch 7.9+.](./elasticsearch/installing-elasticsearch.md)<br><br>2. Follow [Common Upgrade Steps](#common-upgrade-steps) |
| **Liferay 7.2 + LES 2.0** (*Monitoring*, *Learning to Rank*) | Elasticsearch 6.x | 1. [Install Elasticsearch 7.9+.](./elasticsearch/installing-elasticsearch.md)<br><br>2. Follow [LES Upgrade Steps](#les-upgrade-steps) |
| **Liferay 7.1** | Elasticsearch 6.x | 1. [Install Elasticsearch 7.9+.](./elasticsearch/installing-elasticsearch.md)<br><br>2. Follow [Common Upgrade Steps](#common-upgrade-steps) |
| **Liferay 7.1 + LES 2.0** (*Monitoring*, *Learning to Rank*) | Elasticsearch 6.x | 1. [Install Elasticsearch 7.9+.](./elasticsearch/installing-elasticsearch.md)<br><br>2. Follow [LES Upgrade Steps](#les-upgrade-steps) |
| **Liferay 7.0** | Elasticsearch 6.x | 1. [Install Elasticsearch 7.9+.](./elasticsearch/installing-elasticsearch.md)<br><br>2. Follow [Common Upgrade Steps](#common-upgrade-steps) |
| **Liferay 7.0 + LES 2.0** (*Monitoring*, *Learning to Rank*) | Elasticsearch 5.x | 1. [Install Elasticsearch 7.9+.](./elasticsearch/installing-elasticsearch.md)<br><br>2. Follow [LES Upgrade Steps](#les-upgrade-steps) |
| **Liferay 7.0** | Elasticsearch 2.x | 1. [Install Elasticsearch 7.9+.](./elasticsearch/installing-elasticsearch.md)<br><br>2. Follow [Common Upgrade Steps](#common-upgrade-steps) |
| **Liferay 7.2, 7.1** | Solr 7.x | **Switch to Elasticsearch:**<br><br>1. [Install Elasticsearch 7.9+.](./elasticsearch/installing-elasticsearch.md)<br><br>2. Follow [Common Upgrade Steps](#common-upgrade-steps) for configuring Liferay 7.3 with Elasticsearch<br> or follow [LES Upgrade Steps](#les-upgrade-steps) for Liferay 7.3 + Liferay Enterprise Search (LES) 3.0<br><br>**or**<br><br><br>**Upgrade Solr (deprecated):**<br><br>1. [Set up Solr 8.x.](./solr.md)<br><br>2. [Upgrade Liferay.](../../installation-and-upgrades/upgrading-liferay/upgrade-basics/upgrade-overview.md)<br><br>3. [Re-index search & spell check indexes.](../../installation-and-upgrades/upgrading-liferay/upgrade-basics/post-upgrade-considerations.md) |
| **Liferay 7.0** | Solr 5.x | Use steps for Solr 7.x above. |

## Common Upgrade Steps

Upgrade scenarios for systems not including LES apps will include these steps:

1. [Connect Liferay to Elasticsearch 7.](../connecting-to-elasticsearch.md)

1. [Configure security.](../securing-elasticsearch.md)

1. [Upgrade Liferay.](../../installation-and-upgrades/upgrading-liferay/upgrade-basics/upgrade-overview.md)

1. [Re-index the search and spell check indexes.](../../installation-and-upgrades/upgrading-liferay/upgrade-basics/post-upgrade-considerations.md)

1. [Re-index the Workflow Metrics indexes.](../../../../process-automation/workflow/user-guide/workflow-metrics-reports.md#re-indexing-workflow-metrics)

## LES Upgrade Steps

Systems using LES apps will use these steps to upgrade:

1. Connect Liferay to Elasticsearch 7.

1. Configure security.

1. Install Kibana 7.9+ if you are currently using *Kibana and Monitoring*.

1. Install and deploy LES Monitoring if you are currently using Kibana and *Elasticsearch Monitoring/X-Pack Monitoring*.

1. Configure the *Elasticsearch Monitoring* connector if you are using *LES Monitoring* or *Connector to X-Pack Monitoring*.

1. [Upgrade Liferay.](../../../../installation-and-upgrades/upgrading-liferay/upgrade-basics/upgrade-overview.md)

1. Re-index search & spell check indexes.

## What's Next 

Now that you know your upgrade path, start upgrading to use Liferay 7.3 with the latest [Elasticsearch](./elasticsearch/upgrading-elasticsearch.md) (*recommended*) or [Solr](./solr.md) (now deprecated as of Liferay 7.3) search engine.

## Additional Information 

* [Upgrading Elasticsearch](./elasticsearch/getting-started-with-elasticsearch.md)
* [Getting Started with Elasticsearch](./elasticsearch/getting-started-with-elasticsearch.md)
* [Installing Elasticsearch](./elasticsearch/installing-elasticsearch.md)
* [Connecting to Elasticsearch](./elasticsearch/connecting-to-elasticsearch.md)
* [Securing Elasticsearch](./elasticsearch/securing-elasticsearch.md)
* [Upgrading Liferay](../../installation-and-upgrades/upgrading-liferay/upgrade-basics/upgrade-overview.md)