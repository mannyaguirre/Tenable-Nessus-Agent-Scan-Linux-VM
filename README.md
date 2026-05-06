# Tenable-Nessus-Agent-Scan-Linux-VM

## Overview

In this lab I provisioned a Linux machine, created a Nesuss Agent Group in Tenable, created a Basic Agent Scan under Nessus Agent, configured the scan to be triggered scan with a filename start.txt, connected to the linux VM via SSH with an optional Bashion connection via Azure,  linked the Nessus agent to sensor.cloud.tenable.com using a linking key, triggered the basic agent scan by creating the start.txt file in root via terminal, observed the results of the scan, deleted the Linux VM

## Lab Objectives

By the end of this lab I was able to:

Provisioned a Linux Virtual Machine
Create a Nesuss Agent Group in Tenable
Create a Basic Agent Scan
Configure a triggered scan
Use SSH  to connect to Linux VM
Link the Nessus Agent to Tenable Vulnerability Management
Trigger the scam with file name start.txt
Review the vulnerability results
Performed clean up of VM

## Tools Used

Tenable Vulnerability Management
Microsoft Azure
Linux Virtual Machine
SSH
Nessus Agent

## Lab Environment

| Component | Description |
|---|---|
| Endpoint | Linux Virtual Machine |
| Scanner Type | Nessus Agent |
| Platform | Tenable Vulnerability Management |
| Platform | Microsoft Azure |
| Scan Type | Basic Agent Scan |
| Trigger File | `start.txt` |
| Connection | SSH |

# Lab Steps

## Step 1: Provision a Linux Virtual Machine

The first step was to provision a Linux virtual machine using Microsoft Azure

### Why This Step Matters

The VM will act as the endpoint for the Basic Agent Scan

<img width="1918" height="978" alt="Lab1" src="https://github.com/user-attachments/assets/c6086683-9c63-4262-8b44-8b30f1db8d86" />



## Step 2: Create a Nessus Agent Group in Tenable

The second step was to create a nessus agent group in tenable. To create a Nessus Agent Group the following steps were taken:

cloud.tenable.com
Settings
Sensonrs
Nessus Agents
Agent Groups
Add Agent Group

### Why This Step Matters

A Nessus Agent Group groups together different endpoints acrross an organization and helps tailor scans according to business needs. For the purpose of the lab we only created one VM which was included in the Linux-Agent-Group-1. Had we created mutiple Linux VMs, then those Vms could have been grouped into the same Linux-Agent-Group-1.

<img width="1918" height="978" alt="Lab2" src="https://github.com/user-attachments/assets/c4fe6d51-ca01-4105-92bb-d8b436f0143e" />

## Step 3: Create a Basic Agent Scan in Tenable

The third step was to create a Basic Agent Scan. The scan type was set as a triggered scan. I chose a trigger scan with filename start.txt for the purpose of this lab in order to quicker feedback from the Tenable. In an enterprise enviroment a more commmon scan type would be interval which can be configured to from daily to weekly scans according to business needs. 

Scan Type: Trigger Scan
<img width="1918" height="980" alt="lab3" src="https://github.com/user-attachments/assets/67a0054e-3aaa-42e1-8aff-200991849dc3" />

Scan Type: Interval Scan
<img width="1918" height="927" alt="lab10" src="https://github.com/user-attachments/assets/9b59ac56-2393-4f54-8860-9db3270c6827" />

## Step 4: Obtain key to link Linux VM to Tenable Vulnerability Management

The fourth step was to obtain the key to link our VM to Tenable. The location of the key is below:

cloud.tenable.com
Settings
Sensonrs
Nessus Agents
Add Nessus Agent

### Why This Step Matters

The key is a neccessary component to link the virtual machine (or any target endpoint) to Tenable. Without the key, Tenable will not be able to be linked and will not be able to scan the endpoint. 

<img width="1918" height="982" alt="Lab4" src="https://github.com/user-attachments/assets/1b8f7f35-7f83-499d-af9c-aca4fc55ee6b" />

## Step 5: Connect to LInux VM via SSH

the fifth step was to connect to our VM in terminal via SSH. Another option to connect to the VM was using bashion in Azure. 

### Why This Step Matters

If we are not able to connect to our virtual machine then we cannot link the Nessus agent to the endpoint.

connection via SSH
<img width="1918" height="1072" alt="Lab6" src="https://github.com/user-attachments/assets/09f55bed-5f63-40d9-9d70-2878e62767e8" />

connection via bashion
<img width="1918" height="979" alt="Lab5" src="https://github.com/user-attachments/assets/601ac8c1-3ba4-4f28-b13f-c070aaa9698a" />

## Step 6: Link Tenable to endpoint

The sixth step was to use sudo -i for root access and link the endpoint to tenable. 

### Why This Step Matters

If you dont complete the link Tenable will not be able to scan the endpoint. 

<img width="1918" height="1073" alt="lab7" src="https://github.com/user-attachments/assets/12ea361e-344a-4e72-a377-5409b5ef942d" />

## Step 7: Review scan results and vulnarebilities

The seventh step was to review the results from the scan and observe the vulnerebilties found. 

### Why This Step Matters

By anazalying the scan you can find the proper ways to remedeate the vulnarebilites found 

## Step 8: Clean up

the last step was to unlink the agent and delete the linux virtual machine.

## Key Takeaways

Nessus Agents are installed directly on the endpoints.
Agent Groups help group together endpoints based on business needs.
Trigger scans are used when you want Tenable to scan based on filename or interval times. 
Cleanup is important to avoid unused cloud resources.

## Conclusion

In this lab I succesfully configured a nessus agent on a linux virtual machine, scanned for vulnarebilities and observed the restuls. 

This lab help me enforce my understanding on nessus agents, nessus agent groups and data collection of endpoints.


```text
Author        : Manuel Aguirre
LinkedIn      : linkedin.com/in/mannyaguirre/
GitHub        : github.com/mannyaguirre
Date Created  : May 6, 2026
Last Modified : May 6, 2026
Version       : 1.0



