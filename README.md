# elk-dcos
Monitor your DCOS Cluster using Elastic search Logstash Kibana and Filebeat

This project have for main goal to document and automate the deployment of the ELK stack on a DCOS cluster.

When deployed, you should be able to see all the logs from your cluster (Master + Nodes) on Kibana

Project under development, tested and coded for Azure ACS

## Prerequisites

* OS = Ubuntu


## How-to
1. Clone this repo on the Master
2. Copy your private key inside the folder deploy/yourKey
3. Make sure your private key have the chmod 600
4. Verify or replace the value inside the infrastructure/deploy.sh file
5. Deploy Marathon-lb from the universe
6. Execute `sh deploy.sh` from the infrastructure directory
7. Execute `sh copyPrerequisitesNodes.sh` from the filebeat directory


## Documentation

* [Log Management in DC/OS with ELK](https://docs.mesosphere.com/1.8/administration/logging/elk/)
* [Marathon REST API](https://docs.mesosphere.com/1.8/usage/marathon/rest-api)
* [Monitoring](https://dcos.io/docs/1.8/administration/monitoring/)


### TODO :

* Comments the scripts
* Aggregate to one and only script
* CLean the output of the deploy.json script, hide the json answer
* Smart lookup of the PrivateKey
* Callback of the universe package deployment (Elastic, Logstash, Kibana)
* Username for ssh in copyPrerequisitesNodes.sh
