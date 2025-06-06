
Professional Cloud Architect Certification Learning Path: https://partner.cloudskillsboost.google/paths/77
*************************************************************************************************************

Learning Path: Professional Cloud Architect Certification
1 Google Cloud Platform Fundamentals   	      - Core Infrastructure(On-demand Training)
  1.1 Google Cloud Platform Fundamentals      - Core Infrastructure
			
2 Architecting with Google Compute Engine(On-demand Training)
  2.1 Essential Cloud Infrastructure	    : Foundation
  2.2 Essential Cloud Infrastructure 	    : Core Services
  2.3 Elastic Google Cloud Infrastructure   : Scaling and Automation
			
3 Getting Started with Google Kubernetes Engine(On-demand Training)
  3.1 Getting Started with Google Kubernetes Engine
			
4 Logging, Monitoring, and Observability in Google Cloud(On-demand Training)
  4.1 Logging, Monitoring and Observability in Google Cloud
			
5 Reliable Google Cloud Infrastructure		   : Design and Process(On-demand Training)
  5.1 Reliable Google Cloud Infrastructure   : Design and Process
			
6 Taking the Professional Cloud Architect through Instructor Led Training(ILT)
  6.1 Taking the Professional Cloud Architect through Instructor Led Training
			
7 Create and Manage Cloud Resources(Qwiklabs Quest)
  7.1 A Tour of Google Cloud Hands-on Labs
  7.2 Creating a Virtual Machine
  7.2 Compute Engine                   : Qwik Start - Windows
  7.3 Getting Started with Cloud Shell and gcloud
  7.4 Kubernetes Engine                : Qwik Start
  7.5 Set Up Network and HTTP Load Balancers
  7.6 Create and Manage Cloud Resources: Challenge Lab
			
8 Perform Foundational Infrastructure Tasks in Google Cloud(Qwiklabs Quest)
  8.1 Cloud Storage                    			: Qwik Start - Cloud Console
  8.1 Cloud Storage                    			: Qwik Start - CLI/SDK
  8.2 [MS] Cloud IAM                   			: Qwik Start
  8.3 Cloud Monitoring                 			: Qwik Start
  8.4 Cloud Functions                  			: Qwik Start - Command Line
  8.4 Cloud Functions                  			: Qwik Start - Console
  8.5 Google Cloud Pub/Sub             			: Qwik Start - Console
  8.5 Google Cloud Pub/Sub             			: Qwik Start - Python
  8.5 Google Cloud Pub/Sub             			: Qwik Start - Command Line
  8.6 Perform Foundational Infrastructure Tasks in Google Cloud : Challenge Lab
			
9 Set Up and Configure a Cloud Environment in Google Cloud(Qwiklabs Quest)
  9.1 [MS] Cloud IAM					: Qwik Start
  9.2 Introduction to SQL for BigQuery and Cloud SQL
  9.3 Multiple VPC Networks
  9.4 Cloud Monitoring					: Qwik Start
  9.5 Deployment Manager - Full Production [ACE]
  9.6 Managing Deployments Using Kubernetes Engine
  9.7 Set Up and Configure a Cloud Environment in Google Cloud: Challenge Lab
			
10 Automating Infrastructure on Google Cloud with Terraform(Qwiklabs Quest)
  10.1 Terraform Fundamentals
  10.2 Infrastructure as Code with Terraform
  10.3 Interact with Terraform Modules
  10.4 Managing Terraform State
  10.5 Automating Infrastructure on Google Cloud with Terraform: Challenge Lab
			
11 Deploy and Manage Cloud Environments with Google Cloud(Qwiklabs Quest)
  11.1 Orchestrating the Cloud with Kubernetes
  11.2 Deployment Manager - Full Production [ACE]
  11.3 Continuous Delivery Pipelines with Spinnaker and Kubernetes Engine
  11.4 Multiple VPC Networks
  11.5 Site Reliability Troubleshooting with Cloud Monitoring APM
  11.6 Deploy and Manage Cloud Environments with Google Cloud: Challenge Lab
					
12 Optimize Costs for Google Kubernetes Engine(Badge)
  12.1 Managing a GKE Multi-tenant Cluster with Namespaces
  12.2 Exploring Cost-optimization for GKE Virtual Machines
  12.3 Understanding and Combining GKE Autoscaling Strategies
  12.4 GKE Workload Optimization
  12.5 Optimize Costs for Google Kubernetes Engine: Challenge Lab
			
13 Preparing for the Google Cloud Professional Cloud Architect Exam(On-demand Training)
  13.1 Preparing for the Google Cloud Professional Cloud Architect Exam
  13.2 PCA Sample Questions
			
14 PCA Completion Quiz
  14.1 PCA Completion Quiz
			
15 Professional Cloud Architect Exam(Certification)
  15.1 Professional Cloud Architect


Google Cloud Fundamentals: Core Infrastructure
**********************************************
google cloud offerings can be broadly classified into 5 categories
	1) COMPUTE
	2) STORAGE
	3) BIG DATA
	4) MACHINE LEARNING
	5) APPLICATION SERVICES

	
Essential Google Cloud Infrastructure: Foundation
******************************************************
Ref: https://partner.cloudskillsboost.google/course_sessions/4802316/video/393757


- Projects
- Networks
- Sub-networks


Projects:
----------
- associates objects & services with billing.
- default of 15 networks in each of the project that can be shared/peered. additional quota can be added.
- there is no specific IP range for these networks. i.e. each resource is assigned a specific IP & togther it construct all of IP addresses.
- there are 3 types of Networks	
	> Default
	> Auto
	> custom
	
	Default Networks:
	--------------------
	- every project is provisioned with default VPC network with preset subnets and firewall rules.
	- Each subnet is allocated for each region with non-overlapping CIDR blocks (unique blocks for IP address range) & firewall rules that allows
	  Ingress traffic for ICMP, RDP, SSH traffic from anywhere.
		 
	Auto-Mode Network:
	----------------------
	- one subnet will be created in each region.
	- IP addresses have a range with /20 mask that can be expanded to /16
		 
		 
	custom Mode
	----------
	- No deafult subnets created
	- IP ranges expandable upto user specified.
	- conversion of Auto-mode to custom mode is possible, but other way around is not possible.
		 
 
 Routes & firewall rules
 ---------------------------
- by default, every instances in a network will have routes that can send traffic to each other & also to subnets.
- by default, every network will have a default route that directs packets to destination that are outside the network.
- for packets to reach destination, firewall must configured accordingly.
- default networks have pre-defined firewall rules that allow all instances to talk to each other. for manually created networks, we need to define firewalls.
- A Route will be created when
	> new network is created
	> new subnet is created.
	
 

Essential Google Cloud Infrastructure: Foundation
***************************************************
https://partner.cloudskillsboost.google/course_templates/50/video/451475

Virtual Machines
---------------
- Compute options:

There are four Compute Engine machine families.
	1) General-purpose, 
	2) Compute-optimized, 
	3) Memory-optimized, 
	4) Accelerator-optimized

General-purpose: best price-performance with flexible vCPU to Memory ratios. 
-----------------
	Series: E2
	Workload: Day-to-Day use with low cost.
	Applications: 
		- Web server
		- app server
		- back office apps
		- small-medium databases
		- Micro-services
	
	
	series: N2, N2D,N1
	Workload: Balanced use with price/performance for wide range of VM Shapes.
	Applications: 
		- Web server
		- app server
		- Cache
		- Medium-medium databases
		- Media-streaming
		
	
	series: Tau T2D,Tau T2A
	Workload: (scale-out optmized) use for scale-out workloads.
	Applications: 
		- scale-out workloads
		- web server
		- containerized Micro-services
		- Media-transcoding
		- Large-scale Java applications
		

Compute-optimized machine family:  highest performance per core on Compute Engine and is optimized for compute-intensive workloads.
---------------------------------
	
	series: C2
	Workload: Ultra-high performance for high compute-intensive workloads.
	Applications: 
		- high compute workloads
		- Gaming
		- Ad-Serving
		- AI/ML
		
	series: C2D
	Workload: Ultra-high performance for high compute-intensive workloads.
	Applications: 
		- high compute workloads
		- Gaming
		- Ad-Serving
		- AI/ML
	
Pricing
----------
per-second billing, with minimum of 1 minute
	- vCPU, GPU, GB of memory
	
Resource-based pricing
	- Each vCPU and GB of memory is billed seperately.
	
Disks
---------
Persistent Disks: 
this disk will be attached to VM via network interface.
- disk not directly attached to VM, so it can survive the VM termination.
- Bootable: can attach to VM & boot frm there.
- Dynalically resize while its running.
- this same disk can be attached to many VM as Read-only.
- offers replication across zone, regions which can be good option of high-performance foro high availability.

- when performing Zonal or Regional replication, user can select one of the disk types
	> Std Persistent disks (pd-standard)    : these are backed by std hard disks that are suitable for large data processing workloads that primarily use sequential I/O's.
	> SSD Persistent disks (pd-ssd)         : these are backed by solid-state drives that are suitable for Enterprise apps that needs low latency and use more IOPS than std Persistent disks.
	> Balanced Persistent disk (pd-Balanced): are also backed by solid-state drives, these are alternative to (pd-ssd) balances performance and cost.
	uses maximum IOPS similar to pd-ssd and use lower IOPS / GB. these kind of disk offer better performance & value for money for general-purpose apps.
	> Extreme Persistent disk (pd-extreme): are Zonal only. are backed by solid-state drives. meant of high-end database workloads. 
	here, user can have desired IOPS. 
	
Local SSD:
- physically connected to virtual machine, provide high IOPS.
- data will be saved for reset, but not on VM Terminate.
- cannot attach to other VM.

RAM disk:
- use tmpfs to store data in memory.
- suitable for fast performance on small set of data.

Elastic Google Cloud Infrastructure: Scaling and Automation
************************************************************
	Interconnecting Networks:
	---------------------------
	Cloud VPN -
	there are 2 types of cloud VPN
	1) HA VPN
	2) Classic VPN : connects on-premises network to Google cloud VPN via IPsec VPN tunnel.

	HA VPN:
	----------
	- is a High-availability VPN solution.
	- connects On-Premises network to Google cloud via IPSec tunnel.
	- when user creates a HA VPN, google cloud automatically chooses 2 external IP for 2 of its fixed interfaces.
	- each HA VPN gateway supports multiple tunnels.
	- user can create multiple HA VPN gateways.
	- VPN tunnels using HA VPN must use dynamic Routing (BGP)
	- user can create Active/Active or Active/Passive depending on the Route priorities.
	- HA VPN supports Site-to-site VPN in one of the below scenarios.
		> an HA VPN Gateway to Peer VPN devices.
		> an HA VPN gatewyas to AWS private Gateway.
		> 2 HA VPN Gateways connected to each other.
	
	- there are 3 peer gateway configuration for HA VPN
		> an HA VPN Gateway for 2 seperate peer VPN Devices, with ach having its own IP address.
		> an HA VPN gateway for 1 peer VPN Device that uses 2 IP addresses.
		> an HA VPN gateway for 1 peer VPN Device that uses 1 IP addresses.
	
	
Classic VPN : 
----------
	- connects on-premises network to Google cloud VPN via IPsec VPN tunnel.
	- traffic between these 2 networks are encrypted by VPN Gateway.
	- does not support "dial in " to VPN using client VPN software.
	- supports:
		> STATIC Route
		> DYNAMIC Route
		> site-to-siteVPN
		> IKEv1 & IKEv2 ciphers.
	
Note: for On-premises, the max transfer unit (MTU) cannot be greater than 1460 bytes.

Cloud interconnect & peering
******************************
	- way to connect user's infrastructure to google Network.
	- these services can be split into 
		> Dedicated connections
		> shared connections
		> Layer 2 connections
		> layer 3 connections


	* Direct Peering
	* Career Peering
	* dedictaed Interconnect
	* Partner Interconnect
	
		> Dedicated connections:
		-----------------------------
		- provide direct connection to google networks.
	
		> shared connections
		--------------------------
		- provides a connection to google network through a partner.
			
		> Layer 2 connections
		-----------------------
		- uses a VLAN that pipes directly into GCP Environment. 
	
		> Layer 2 connections
		-----------------------
		- provides access to google workspace service like Youtube & google cloud API's using public IP addresses. 



2.2 Essential Google Cloud Infrastructure: Core Services
---------------------------------------------------------
Big Query:
	- is a google cloud's Data Warehouse which is serverless, highly-scalable.
Cloud Dataflow:
	- fully managed service for transforming & enriching data in stream & batch modes.
	- lot of infrastructure set up & maintenance can be done.

Cloud Dataprep:
	- used for exploring, cleaning & preparing structured/unstructured data for analysis reporting & machine learning.

Dataproc:
	- fully managed service for running Apache spark, hadoop clusters.

04 Essential Google Cloud Infrastructure: Core Services
********************************************************
- Identity & access Management (IAM)
- Storage & database services 
- Resource Management
- Resource Monitoring


	- Identity & access Management (IAM)
	-----------------------------------------
		- Organization
		- Roles
		- Members
		- Service Accounts
		- Organization restrictions


		Google cloud resources are organized in heirarchy as shown below.
		1. Organization
		2. Folders
		3. Projects
		4. Resources
		
	
		- Each resource has exactly one parent.
		- The organization resource represents your company.
		- roles granted by each level are inherited by other components below the heirarchy.
		- folder resource could represent your department.
		
					Organization Node:
					- is a root node for cloud resources.
					- roles: 
						> Organization admin : control over all the cloud resources.
						> Project creator 	 : can create projects.
						> G suite or Identity access admin can assign organization admin role to users.
					
				
					Folders:
					- roles:
						> Admin   : full control over resources in that folder.
						> Creator : Browse Hierarchy & create folders.
						> Viewer  : view folders, projects below the resources.
						
					Projects:
					- roles:
						> creator : create new projects (automatic owner) & migrate new projects into organization.
						> Deleter : Delete projects.
				
				
			
			Roles
			----------
				There are three types of roles in Cloud IAM, 
				> Basic roles
				> Predefined roles
				> Custom roles.
				
				Basic role types:
					> Owner			: full administrative access. This includes the ability to add and remove members and delete projects.
					> Editor 		:  modify and delete access. This allows the developer to deploy applications and modify or configure its resources.
					> Viewer		: read only access.
					> billing administrator : manage billing and add or remove administrators without the right to change the resources in the project.
				
			
			Predefined roles:
				> provides members with granular access to specific GCP resources and prevents unwanted access to other resources.
				> Compute engine has predefined rules.
					~ Compute Admin: Full control on compute resources.
					~ network Admin: Full control on Network resources except firewall & SSL Certificates.
							 In other words, the network admin role allows read only access to firewall rules SSL certificates, and instances to view their ephemeral IP addresses.
					~ storage Admin: Permissions to create, modify, delete images & snapshots.
			
		
			Members: WHO on google cloud..
			-----------------
			Any email address that is associated with a Google account can be an identity, including gmail.com or other domains.
			
			There are five different types of members: 
			- Google Accounts, 
			- Service Accounts, 
			- Google Groups, 
			- Google Workspace domains, and 
			- Cloud Identity domains.
			
					
		service accounts:
		---------------------
		There are three types of service accounts: 
		- user-created or custom accounts
		- built-in accounts
		- Google APIs service accounts
		- This account is identifiable by the email project-number-compute@developer.gserviceaccount.com
		
		

Storage and Database Services
----------------------------------
In this module, we will cover 
- Cloud Storage
- Filestore
- Cloud SQL 
- Cloud Spanner 
- AlloyDB
- Firestore
- Cloud Bigtable 
- Memorystore

		when to use which database services
		-------------------------------------
		1) if your data is STRUCTURED?
			if NO, then ask if you need file sharing system.
				if YES, select Filestore,
				   if No, select Cloud storage.
				   
		
		
		
		Cloud storage:
		------------------
		- it's an object storage service.
		- used for
			> website content
			> data archival
			> Disaster Recovery or Distributing large object data to users via Direct download.
		- features
			> scalable to exabytes of data.
			> time to first byte in milliseconds.
			> highly scalable across all storage classes.
			> single API across all storage classes.
			
		- it is NOT like a files in filesystem.
		- it is a collection of buckets that you place bucket into.
		- you have specific URL to access Objects.
		- Cloud storage has 4 types of storage classes.
			> standard
			> Nearline
			> coldline
			> Archive
			
			Standard: 
			-----------
			- suitable for frequently accessing data.
			- Hot 
			- stored for brief period (very less days)
			- most expensive.
		
		cloud storage is broken down into different items
			- Buckets
			- Objects
			- Access
			
	Filestore:
	------------
		- Fully managed NAS(network access storage) for COMPUTE ENGINE & GKE instances.
		
		
	cloudSQL:
		- Fully managed database service (MySQL, MSSQL server, PostGreSQL)
		- 
		
		qwiklabs-gcp-01-9749ba0e9c85:us-central1:wordpress-db
		
		export SQL_CONNECTION=qwiklabs-gcp-01-9749ba0e9c85:us-central1:wordpress-db]
		
		
		
		
		
		
			
			
			
			
