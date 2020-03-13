# 1. Introduction

Quantel AI, Inc ("Quantel AI") is committed to ensuring the confidentiality, privacy, integrity, and availability of all electronically protected information such as PII data it receives, maintains, processes and/or transmits on behalf of its Customers. As providers of compliant, hosted infrastructure used by many of its customers in various verticals, Quantel AI strives to maintain compliance, proactively address information security, mitigate risk for its Customers, and assure known breaches are completely and effectively communicated in a timely manner. The following documents address core policies used by Quantel AI to maintain compliance and assure the proper protections of infrastructure used to store, process, and transmit for Quantel AI Customers.

Quantel AI provides secure and compliant software deployed on-premises within the firewalls of its clients as well as hosted cloud-based software. The hosted software falls into two broad categories: 1) **Platform as a Service (PaaS)** and 2) **Platform Add-ons**. These Categories are cited throughout policies as Customers in each category inherit different policies, procedures, and obligations from Quantel AI.

## 1.1 Container based Service on on-prem hardware
Enterprise clients deploying Quantel AI software as an on-prem solution will deploy a wholly contained software on their hardware. This hardware along with this software will be managed by professional services team engaged by the client. The professional services may or may not be employees of Quantel AI. Client would be responsible for appropriate compliance and preventing unauthorized access to the system.


## 1.2 Platform as a Service (PaaS)

PaaS Customers utilize hosted software and infrastructure from Quantel AI to deploy, host, and scale custom developed applications and configured databases. These customers are deployed into compliant containers run on systems secured and managed by Quantel AI. Quantel AI does not have insight or access into application level data of PaaS Customers and, as such, does not have the ability to secure or manage risk associated with application level vulnerabilities and security weaknesses. Quantel AI makes every effort to reduce the risk of unauthorized disclosure, access, and/or breach of PaaS Customer data through network (firewalls, dedicated IP spaces, etc) and server settings (encryption at rest and in transit, OSSEC throughout the Platform, etc).

## 1.3 Compliance Inheritance

Quantel AI provides compliant hosted software infrastructure for its Customers. Quantel AI's service offerings are currrently available on AWS.

Quantel AI signs business associate agreements (BAAs) with its Customers. These BAAs outline Quantel AI obligations and Customer obligations, as well as liability in the case of a breach. In providing infrastructure and managing security configurations that are a part of the technology requirements, as well as future compliance frameworks, Quantel AI manages various aspects of compliance for Customers. The aspects of compliance that Quantel AI manages for Customers are inherited by Customers, and Quantel AI assumes the risk associated with those aspects of compliance. In doing so, Quantel AI helps Customers achieve and maintain compliance, as well as mitigates Customers' risk.

Quantel AI does not act as a covered entity. When Quantel AI does operate as a business associate (not a subcontractor), Quantel AI does not interface with users to obtain or provide access to sensitive Customer data. Access to sensitive Customer data is through our customers' applications.

Certain aspects of compliance cannot be inherited. Because of this, Quantel AI Customers, in order to achieve full compliance, must implement certain organizational policies. These policies and aspects of compliance fall outside of the services and obligations of Quantel AI.


## 1.4 Quantel AI Organizational Concepts

The physical infrastructure environment of Quantel AI's hosted platform is hosted at [Amazon Web Services](https://aws.amazon.com/) (AWS). The network components and supporting network infrastructure are contained within the AWS infrastructure and managed by AWS. Quantel AI does not have physical access into the network components. Quantel AI environment consists of Cisco firewalls; nginx web servers; Java and Python application servers; PostgreSQL database servers; Logstash logging servers; Linux Ubuntu monitoring servers; Docker containers; Kubernetes orchestration and developer tool servers running on Linux Ubuntu servers.

Within Quantel AI Platform on AWS, all data transmission is encrypted and all hard drives are encrypted so data at rest is also encrypted; this applies to all servers - those hosting Docker containers, databases, APIs, log servers, etc. Quantel AI assumes all data *may* contain sensitive Customer data, and provides appropriate protections based on that assumption.

In the case of PaaS Customers, it is the responsibility of the Customer to restrict, secure, and assure the privacy of all sensitive Customer data at the Application Level, as this is not under the control or purview of Quantel AI.

The data and network segmentation mechanism differs depending on the primitives offered by the underlying cloud provider infrastructure:

* Within AWS, hosted load balancers segment data across dedicated Virtual Private Clouds for PaaS Customers and for Platform Add-ons.

The segmentation strategies employed by Quantel AI effectively create RFC 1918, or dedicated, private segmented and separated networks and IP spaces, for each PaaS Customer and for Platform Add-ons.

Additionally, IPtables is used on each server for logical segmentation. IPtables is configured to restrict access to only justified ports and protocols. Quantel AI has implemented strict logical access controls so that only authorized personnel are given access to the internal management servers. The environment is configured so that data is transmitted from the load balancers to the application servers over a TLS encrypted session.

In the case of Platform Add-ons, once the data is received from the application server, a series of Application Programming Interface (API) calls is made to the database servers where the sensitive Customer data resides. The sensitive Customer data is separated into PostgreSQL and Percona¶ databases through programming logic built so that access to one database server will not present you with the full sensitive Customer data spectrum¶.

The VPN server, nginx web server, and application servers are externally facing and accessible via the Internet. The database servers, where the sensitive Customer data resides, are located on the internal Quantel AI network and can only be accessed through a bastion host over a VPN connection. Access to the internal database is restricted to a limited number of personnel and strictly controlled to only those personnel with a business-justified reason. Remote access to internal servers is not accessible except through load balancers.

All Platform Add-ons and operating systems are tested end-to-end for usability, security, and impact prior to deployment to production.

## 1.5 Requesting Audit and Compliance Reports

Quantel AI, at its sole discretion, will shares audit reports, with customers on a case by case basis. All audit reports are shared under explicit NDA in Quantel AI format between Quantel AI and party to receive materials. Audit reports can be requested by Quantel AI workforce members for Customers or directly by Quantel AI Customers.

The following process is used to request audit reports:

1. Email is sent to compliance-reports@quantel.ai¶. In the email, please specify the type of report being requested and any required timelines for the report.
2. Quantel AI staff will log an issue with the details of the request into the Quantel AI Quality Management System. Quantel AI Quality Management System is used to track requests' status and outcomes.
3. Quantel AI will confirm if a current NDA is in place with the party requesting the audit report. If there is no NDA in place, Quantel AI will send one for execution.
4. Once it has been confirmed that an NDA is executed, Quantel AI staff will move the issue to "Under Review".
5. Quantel AI Security Officer or Privacy Officer must Approve or Reject the Issue. If the Issue is rejected, Quantel AI will notify the requesting party that we cannot share the requested report.
6. If the issue has been Approved, Quantel AI will send the customer the requested audit report and complete the Quality Management System issue for the request.

## 1.6 Version Control

Refer to the GitHub repository at [https://github.com/Quantelytics/QuantelAI-Policies/](https://github.com/Quantelytics/QuantelAI-Policies/) for the full version history of these policies.

## 1.7 Acknowledgement 

The Policy documents drafted by Quantel AI is based on Datica's Open Sourced Policy Documents. We would like to place our sincere gratitude to Datica for their generous contribution to the Open Source community 
