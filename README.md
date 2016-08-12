# Cloudera-Hbase-Docker

----
## Why?
Because we were tired of installing gateway services on machines and maintaining the aspects of server lifecycle in CDH.  Using this container allows us to scale our apps independently.

## Usage

This container is really more designed to be used as a base image for other projects that require the Cloudera hbase gateway services to be installed and configured.  If you want to say run hbase shell or something similar you could do the following:

Modify the docker-compose.yml file and set the environment variables to whatever makes sense for your environment (see below).  

    docker-compose up


## Environment Variables

The following env variables are supported.  Also see docker-compose.yml for examples

HA_ZOOKEEPER_QUORUM=hdp01dn0001.example.com:2181,hdp01dn0002.example.com:2181,hdp01dn0003.example.com:2181,hdp01dn0004.example.com:2181,hdp01dn0005.example.com:2181
DFS_NAMENODE1_RPC_ADDRESS=hdp01mn0001.example.com:8020
DFS_NAMENODE1_SERVICERPC_ADDRESS=hdp01mn0001.example.com:8022
DFS_NAMENODE1_HTTP_ADDRESS=hdp01mn0001.example.com:50070
DFS_NAMENODE1_HTTPS_ADDRESS=hdp01mn0001.example.com:50470
HBASE_ZOOKEEPER_QUORUM=hdp01dn0002.example.com,hdp01dn0003.example.com,hdp01dn0005.example.com,hdp01dn0004.example.com,hdp01dn0001.example.com
