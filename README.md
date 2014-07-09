#Bonita Database Connection Samples

This set of processes aims to provide a survival guide to working with databases and BonitaBPM

Each process is a compound of 4 basic tasks ie Create Read Update Delete (CRUD)

Each process relies on a simple set of data and focuses on binding forms to queries input/outputs, configuring connectors and sometime using groovy scripts


## POSTGRESQL SAMPLE

#### Using docker

docker pull bonita_crud_pg

docker run -v /tmp/data:/data -d -p 49153:5432 -e POSTGRESQL_DB="bonita"  -e POSTGRESQL_USER="bonita"-e POSTGRESQL_PASS="bonita"  -t docker_crud_pg 


Do not forget to update pool variables in process if changes are commited to your environment.

Default jdbc url is jdbc:postgresql://localhost/bonita and should be updated to match your configuration if you are running a database on a remote host

#### Using a typical postgresql installation

use [attached pg dump](bonitaBPM-crud-pg-samples.gz)

gunzip -c bonitaBPM-crud-pg-samples.gz | psql -U bonita -h localhost -d bonita

~                                 

