# ElasticDataSearchEngine


## Setup Instructions:

# Step-1: Download , Install and Run Elastic-Search 6.4.3

This section includes information on how to setup Elasticsearch and get it running, including:

1. Downloading
2. Installing
3. Starting
4. Configuring

Java (JVM):

- Elasticsearch is built using Java, and requires at least Java 8 in order to run. Only Oracle’s Java and the OpenJDK are supported.

- The same JVM version should be used on all Elasticsearch nodes and clients.

- We recommend installing Java version 1.8.0_131 or a later version in the Java 8 release series.

- We recommend using a supported LTS version of Java. Elasticsearch will refuse to start if a known-bad version of Java is used.

- The version of Java that Elasticsearch will use can be configured by setting the JAVA_HOME environment variable.



Download URL:

https://www.elastic.co/guide/en/elasticsearch/reference/current/setup.html


Mac OSX:

# Install va homebrew

If you don't have homebrew installed -  [get homebrew here](http://brew.sh/)

Then run:  `brew install elasticsearch`

# Configuration

Update the elasticsearch configuration file in ` /usr/local/etc/elasticsearch/elasticsearch.yml`.

Set the value below to false:

    discovery.zen.ping.multicast.enabled: false #(it's true by default)

# How to start it

Other sources say to use a removed `brew services` command. You get it via `brew tap gapple/services`. Then you're supposed to run `brew services start <package-to-start>`.

If brew `services start elasticsearch` doesn't work for you, check the instructions when you run `brew info elasticsearch`.

Mine says:

==> Downloading https://artifacts.elastic.co/downloads/elasticsearch/elasticsearch-oss-6.4.3.tar.gz
######################################################################## 100.0%
==> /usr/local/Cellar/elasticsearch/6.4.3/bin/elasticsearch-keystore create
==> Caveats
Data:    /usr/local/var/lib/elasticsearch/elasticsearch_lakshmikanth/
Logs:    /usr/local/var/log/elasticsearch/elasticsearch_lakshmikanth.log
Plugins: /usr/local/var/elasticsearch/plugins/
Config:  /usr/local/etc/elasticsearch/

To have launchd start elasticsearch now and restart at login:
  brew services start elasticsearch
Or, if you don't want/need a background service you can just run:
  elasticsearch
==> Summary
🍺  /usr/local/Cellar/elasticsearch/6.4.3: 118 files, 36MB, built in 22 seconds

# Sources

- [Quick Elasticsearch / Kibana / Logstash (ELK stack) Install (for your local mac dev box) - gist.github.com](https://gist.github.com/squarism/8fa9cdd7d6b36c9fcb45)
- [Important Configuration Changes - www.elastic.co](https://www.elastic.co/guide/en/elasticsearch/guide/current/_important_configuration_changes.html#_prefer_unicast_over_multicast)



Windows:
```
- The zip and tar.gz packages are suitable for installation on any system and are the easiest choice for getting started with Elasticsearch on most systems.

- Install Elasticsearch with .zip or .tar.gz or Install Elasticsearch with .zip on Windows

- https://www.elastic.co/guide/en/elasticsearch/reference/current/zip-targz.html

```
Linux:
```

1. apt-get update

2. apt-get install -y elasticsearch

```


# Running Elasticsearch from the command line:

1. Elasticsearch can be started from the command line as follows:

./bin/elasticsearch

By default, Elasticsearch runs in the foreground, prints its logs to the standard output (stdout), and can be stopped by pressing Ctrl-C.

2. Running as a daemon:

To run Elasticsearch as a daemon, specify -d on the command line, and record the process ID in a file using the -p option:

./bin/elasticsearch -d -p pid

3. Log messages can be found in the $ES_HOME/logs/ directory.

4. To shut down Elasticsearch, kill the process ID recorded in the pid file:

kill `cat pid`

Note:
The startup scripts provided in the RPM and Debian packages take care of starting and stopping the Elasticsearch process for you.


# Step-2: Setup and Run ElasticDataLoader Project:

- Git Project page: https://github.com/kanthgithub/ElasticDataLoader


# Step3: Setup and Run ElasticDataQuery Project:

- Git Project Details: (https://github.com/kanthgithub/ElasticDataQuery)


