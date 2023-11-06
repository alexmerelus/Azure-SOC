# Building a Honeynet + SOC with Azure
![Whiteboard design (1)](https://github.com/alexmerelus/Azure-SOC/assets/138509128/ca555d1f-b99f-4d3f-b9c0-14c741a7d3e9)
## Introduction
This image depicts a schematic for a Cloud Honeynet that I created using Microsoft Azure and combined with a Security Operations Center (SOC), illustrating the cybersecurity infrastructure using Azure cloud services. It outlines the flow of data and interaction between components such as Azure Active Directory (Azure AD), SQL Databases, and Virtual Machines that were exposed to the internet insecurely for 48 hours. 

Traffic and access attempts were monitored and managed by Network Security Groups (NSGs) to filter incoming and outgoing communications to these honeypots. All activity was logged and sent to Azure's Log Analytics Workspace for real-time analysis which then fed into Azure Sentinel, the SIEM (Security Information and Event Management) system that offers threat detection, alerting, and visualization through various maps and incident reports. I measured some security metrics in the insecure environment for 48 hours, applied some security controls to harden the environment, and measured metrics for another 24 hours. 

By simulating a real-world attack scenario, the Cloud Honeynet served as an early-warning system, identifying potential threats before they can impact an actual network and conveys the integration of these elements into a cohesive cybersecurity strategy, emphasizing the use of a honeynet decoy system intended to attract and analyze cyber attacks—as part of a SOC's defensive and monitoring operations. 

The metrics shown are:
- SecurityEvent (Windows Event Logs)
- Syslog (Linux Event Logs)
- SecurityAlert (Log Analytics Alerts Triggered)
- SecurityIncident (Incidents created by Sentinel)
- AzureNetworkAnalytics_CL (Malicious Flows allowed into our honeynet)

### [Part 1: Setting up Resources](https://github.com/alexmerelus/Azure-Resources#azure-resources)
