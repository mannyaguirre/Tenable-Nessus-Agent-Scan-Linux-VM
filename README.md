# Tenable-Nessus-Agent-Scan-Linux-VM

## Overview

In this lab I provisioned a Linux machine, created a Nesuss Agent Group in Tenable, created a Basic Agent Scan under Nessus Agent, configured the scan to be triggered scan with a filename start.txt, connected to the linux VM via bashion in Azure with an optional SSH connection via terminal on windows,  linked the Nessus agent to sensor.cloud.tenable.com using a linking key, triggered the basic agent scan by creating the start.txt file in root via terminal, observed the results of the scan, deleted the Linux VM

## Lab Objectives

By the end of this lab I was able to:

Provisioned a Linux Virtual Machine
Create a Nesuss Agent Group in Tenable
Create a Basic Agent Scan
Configure a triggered scan
Use SSH and Bashion to connect to Linux VM
Link the Nessus Agent to Tenable Vulnerability Management
Trigger the scam with file name start.txt
Review the vulnerability results
Performed clean up of VM

## Tools Used

Tenable Vulnerability Management
Microsoft Azure
Linux Virtual Machine
Bashion
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
| Connection | Bashion |

# Lab Steps

## Step 1: Provision a Linux Virtual Machine

The first step was to provision a Linux virtual machine using Microsoft Azure

### Why This Step Matters

The VM will act as the endpoint for the Basic Agent Scan

<img width="1918" height="977" alt="Lab1" src="https://github.com/user-attachments/assets/63b63625-5d4b-4c5b-a7e4-079ca9846e62" />

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








