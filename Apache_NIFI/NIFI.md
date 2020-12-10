## What is `Apache NiFi`?
* Apache NiFi is a software project from the Apache Software Foundation designed to automate the flow of data between software systems.
  
## NIFI
* National Issues Forums Institute.
* National Inland Fisheries Institute 
* (Fisheries Department, Bangkok, Thailand)

## Is Apache NIFI an *ETL* tool?
> Apache NiFi is an integrated data logistics platform   for automating the movement of data between disparate systems.
*  It is not an interactive ETL tool. 
*  It can be part of an ETL solution.

## NIFI & KAFKA
|--- |--- |  
|NIFI |KAFKA |  
|NiFi is primarily a data flow tool|Kafka is a broker for a pub/sub type of use pattern.|  

## How much data can NIFI handel?
* NiFi handles the data at an impressive rate of 9.56 TB  per 5 minutes
* 42.4 billion messages in 5 minites
* 32.6 GB/sec

## What is NIFI in **Big Data?**
* It provides real-time control that makes it easy to manage the movement of data between any source and any destination.

## Does NIFI need *Zookeeper* ?
* zookeeper is a fundamental part of the NiFi cluster.
* It is used to automatically determine the cluster coordinator as well as communication within the cluster.
* if you do not want to use zookeeper then you will have to use a 0.x baseline version of NiFi.
## How do i **start** NIFI?
* From a terminal window, navigate to the NiFi installation directory.
> ` bin/nifi.sh start`
## How do i stop NIFI?
* From a terminal window, navigate to the NiFi installation directory.
> `bin/nifi.sh stop`

## NiFi- General Features
* web based user interface
* Highly configurable
    * guaranteed delivery, 
    * low latency, 
    * high throughput, 
    * dynamic prioritization, 
    * back pressure
    *  modify flows on runtime.
* data provenance module
    * track and moniter data
* create custom process and reporting
* Secure Protocals
  * SSL
  * HTTPS
  * SSH
  * other encriptions
* user and role managment
  * configure LDAP for authorization

## Key concepts
* Process group
  - group of NIFI Flows 
* Flow
  - contain different processors 
* Processor
  - java module
  - add attribute or change content in flowfile
* Flowfile
  - single object
  -  CREATE, CLONE, RECEIVE, etc.
* Event
  - tracked in data provenance
* Data provenance
  - repository
  - UI
  - troubleshooting issues

## NiFi Advantages
* remote data fetching using SETP
* support clustering
  - same flow, different data
  - increases performence
* security policy on  
  - user level
  - process group
  - modules
- UI can run on HTTPS
- supports `188` processors 
- custom plugin
  
## NiFi Disadvantages
- when node disconnects from **NiFi** then the user changes on **flow.xml** is invalid.
- A node cannot connect back unless **file.xml** is copied from connected node.
- state persistent issue 

##  NiFi - Basic Concepts
![Apache Web Server]./images/(apache_web_server.jpg)
- Flowfile Repository
- Content Repository
- Provenance Repository

### Flowfile Repository

- stores 
  - state 
  - attributes
- default location
  - root of apache NiFi
- modefy location of repositery 
  > nifi.flowfile.repository.directory

### Content Repository
- change repositery 
  > org.apache.nifi.controller.repository.
>it is advisable to have enough space in the installation disk.

### Provenance Repository
- tracks and stores all the events
- two type
  - volatile provenance repository
    - data get lost after restart
      > org.apache.nifi.provenance.VolatileProvenanceRepositor
  - persistent provenance repository.
     > org.apache.nifi.provenance.PersistentProvenanceRepository

![Proviance](./images/provenance_repository.jpg)


## Environment Setup
- unix | linux
  - step 1
    - > java -version
    - > $ echo $JAVA_HOME
  - step 2
    - windows download ZIP
    - unix download TAR
    - docker image [link](https://hub.docker.com/r/apache/nifi/)
  - step 3
      - unix 
      - > $tar -xvf nifi-1.6.0-bin.tar.gz
      -  windows extract zip
   - step 4
     - exicute `run-nifi.bat`
     - > C:\nifi-1.7.1\bin>run-nifi.bat
   - step 5
     - UI
     - `http://localhost:8080/nifi/`

## NiFi UI
- user attributes
   - Active Threads
   - Total queued data
   - Transmitting Remote Process Groups
   - Not Transmitting Remote Process Groups
   - Running Components
   - Stopped Components
   - Invalid Components
   - Disabled Components
   - Up to date Versioned Process Groups
   - Locally modified Versioned Process Groups
   - Stale Versioned Process Groups
   - Locally modified and Stale Versioned Process Groups
   - Sync failure Versioned Process Groups
###  Web UI
![UI](./images/user_interface.jpg)
## Components of Apache NiFi
- *Processors*
  - User can drag the process icon on the canvas and select the desired processor for the data flow in NiFi.
   ![process](./images/add_processor.jpg)
- *Input port*
  - Below icon is dragged to canvas to add the input port into any data flow.
  ![input Port](./images/input_port.jpg)

Input port is used to get data from the processor, which is not present in that process group.
  - ![add port](./images/add_port.jpg)
- *Output port*
  - The below icon is dragged to canvas to add the output port into any data flow.

   ![output port](./images/output_port.jpg)
- *Process Group*  

   ![process group](./images/gruop_icon.jpg)
- *Remote Process Group*
   ![remote process](./images/remote_process_group.jpg) 
- *Funnel*
  - Funnel is used to transfer the output of a processor to multiple processors  
  
  ![funnel](./images/funnel_icon.jpg)
- *Template*
  - This helps to reuse the data flow in the same or different NiFi instances.
  ![template](./images/template_icon.jpg)
- *Label*
  - add text on NiFi canvas
  ![label](images/label_icon.jpg)
