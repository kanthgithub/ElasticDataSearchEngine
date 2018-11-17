# ElasticDataSearchEngine


## Setup Instructions:

# Step-1: Download , Install and Run Elastic-Search 6.0.0

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
```
1. open terminal

2. Run command:

    brew install elastic

3.

4.

5.

6.

```
Windows:
```
- The zip and tar.gz packages are suitable for installation on any system and are the easiest choice for getting started with Elasticsearch on most systems.

- Install Elasticsearch with .zip or .tar.gz or Install Elasticsearch with .zip on Windows

- https://www.elastic.co/guide/en/elasticsearch/reference/current/zip-targz.html

```
Linux:
```

- The deb package is suitable for Debian, Ubuntu, and other Debian-based systems. Debian packages may be downloaded from the Elasticsearch website or from our Debian repository.

- Install Elasticsearch with Debian Package

- https://www.elastic.co/guide/en/elasticsearch/reference/current/deb.html


- The rpm package is suitable for installation on Red Hat, Centos, SLES, OpenSuSE and other RPM-based systems. RPMs may be downloaded from the Elasticsearch website or from our RPM repository.

- Install Elasticsearch with RPM:

- https://www.elastic.co/guide/en/elasticsearch/reference/current/rpm.html

```


# Running Elasticsearch from the command line:

```
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
```


# Step-2: Setup and Run ElasticDataLoader Project:

```
Clone Git Project:
```






# Step3: Setup and Run ElasticDataQuery Project:

```
Clone Git Project:
```