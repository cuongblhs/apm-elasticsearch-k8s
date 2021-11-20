# apm-elasticsearch-k8s
Application Performance Monitoring (APM) with Elasticsearch

# Elasticsearch
After applying elasticsearch on k8s need to set password for Built-in users to login into kibana:
- Access to elasticsearch pod: _kubectl exec -it < pod name > -c < container name > -- bash_
- Run command: _bin/elasticsearch-setup-passwords interactive_
- Enter password for Built-in users
- Access to kibana and login with _elasric_ user
---
**elastic**
A built-in superuser.\\
**kibana_system**
The user Kibana uses to connect and communicate with Elasticsearch.
**logstash_system**
The user Logstash uses when storing monitoring information in Elasticsearch.
**beats_system**
The user the Beats use when storing monitoring information in Elasticsearch.
**apm_system**
The user the APM server uses when storing monitoring information in Elasticsearch.
**remote_monitoring_user**
The user Metricbeat uses when collecting and storing monitoring information in Elasticsearch. It has the and built-in roles.