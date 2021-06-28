# Storage

## Introduction

Azure Storage, which is a service that you can use to store files, messages, tables, and other types of information. 
It is used by virtual machines and other IaaS, and platform as a service cloud services.

A storage account provides a unique namespace for your Azure Storage data that's accessible from anywhere in the world over HTTP or HTTPS. Data in this account is secure, highly available, durable, and massively scalable.

## Disk Storage
Provides disks for Azure Virtual Machines

- HDDs
- SSDs
- premium SSD
- ultra 

## Azure Blob

It is an object storage solution that stores many types of data. It is unstructured.

Ideal for:
- images
- files for distributed access
- streaming video, audio
- backup, restore, disaster recovery

It has no hierarchical folder structure.
- Hot (frequent retrieval) 
- Cool (infrequent, > 30 days), archive 
- Archive (backup, the lowest costs, > 180 days)  

## Azure Files (?)
It is a file share system. 
Good for:
- migrations from on-premises applications using file shars
- storing config files on a file share and accessing them from many VMs
- diagnostics, metrics, crash dumps to analyze it later (?)

It has hierarchical structures. Service for Windows servers.