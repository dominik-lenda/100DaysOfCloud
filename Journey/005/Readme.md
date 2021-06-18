# Questions and confusions
I see confusion between a container as a placeholder and a container that is a piece of software, which includes its dependencies.

## Notes about Blobs

Blob (Binary Large Object data) - a form of data that represents wide range of things, e.g. images, videos, documents. Good for when dealing with unstructured data.

You can store blobs inside of storage accounts, containers that store other data types such as files, tables, queues.

Types of blobs:
- Block blobs - blobs up to 4/75TB divided into blocks of 100MB to make management of large blobs more efficient.

- Append blobs - blobs optimized for appending new data, e.g. log data. It is useful when the data never need to be modified after it is written.

- Page blobs - collections of individual 'pages' of up to 4MB each, which are optimized for random read/write operations. 


copy/pasting now to make notes from it:
"There are a few properties specific to storage accounts in this section:

    The Status indicates that the Primary storage location is Available. In the event of an outage in Azure, you may see a different value here. This storage account has no secondary storage location, but you can create storage accounts with primary and secondary storage locations. The Replication property of a storage account determines this.
    The Performance can be standard or premium. When you need guaranteed latency you should use premium storage. Premium storage has much higher storage costs because they use solid-state drives (SSDs) whereas standard storage uses magnetic spinning hard disk drives (HDDs).
    Access tier optimizes the storage and cost based on how frequently data is accessed. The Hot tier is for frequently accessed data and carries the highest cost for storage but the lowest cost for accessing the data. The cool and archive tiers reduce are suited for less frequently accessed data with archive offering the lowest cost for storage but the highest cost for accessing data. The archive tier actually stores the data offline and the data needs to be "rehydrated" to the hot or cool storage before it can be read. Cool and archive tiers also include a penalty if you delete the blob within 30 days and 180 days, respectively, of when they are first moved into these tiers.
    The Replication sets the durability and availability of the storage. The following options are available:
        Locally-redundant storage (LRS) is the cheapest option and stores the data in a single data center. If that data center goes offline you will not be able to access the data.
        Zone-redundant storage (ZRS) stores data across three data centers in a region. It can tolerate individual data center outages but not regional outages.
        Geo-redundant storage (GRS) stores data across multiple data centers in two regions, a primary region and a secondary region. This option is more expensive but can tolerate entire regional outages. There is also read-access geo-redundant storage (RA-GRS) which allows you to read from the secondary region compared to GRS which only allows you to access the secondary in the case of a Microsoft-initiated region failover to the secondary.
    Finally, the Account kind describes if the storage account is general-purpose or specialized. General-purpose accounts allow storage of blobs, tables, files, and queues whereas specialized kinds only allow one type such as only blob storage. There are different pricing models for each account kind so a specialized kind may reduce your costs. StorageV2 is the recommended default.
"

"Notice you can configure the Blob type, Access tier, and Upload to folder to organize your container. Although a storage account also has an access tier, it only sets the default value for each blob. You can override the default value for each blob and this is the only possible way to set the archive access tier since it cannot be set at the storage account level."

### DISKS
Azure virtual machines (VMs) use Azure disks as their attached disk storage. Azure disks are built-on top of page blobs which are the type of blobs optimized for random access. When you create Azure disks you can choose to manage the storage account yourself or to use managed disks where Azure manages the storage account for you. Managed disks are the preferred option. Within managed disks you can choose between:

    Ultra SSDs which provide the best throughput and I/O operations per second (IOPS) performance characteristics but at the highest prices. Consider Ultra SSDs for mission-critical I/O intense applications such as running databases.
    Premium SSDs are the next best performing and are well-suited to production workloads with all but the highest performance I/O requirements that may benefit from using Ultra SSDs.
    Standard SSDs are the least expensive SSD option and are suitable for production workloads with low I/O performance requirements such as web servers and lightly used applications.
    Standard HDDs use spinning disk technology and are therefore the least expensive option but also provide the lowest performance. Use them for backups and infrequently accessed applications.

Azure disks give you the freedom to attach and detach from different VMs. They will maintain their data but the data is only usable when a disk is attached to a VM. You will inspect a VM with two disks attached to it in this Lab Step.



"Each VM has one OS disk which contains the operating system and is used to boot the VM. The OS disk is a Standard SSD in this case. In addition to the OS disk, VMs can have zero or more Data disks attached. This VM has one data disk that is a 4 GiB Standard HDD. All disks are encrypted at rest automatically and transparently to any users. This means if someone were to steal a physical disk from an Azure data center the physical disk would be encrypted and unusable. This is true for all data in Azure storage accounts. However, for Azure disks, you can also encrypt the virtual disk at the operating system level. This is referred to as Azure Disk Encryption (ADE). This protects against someone attempting to copy your Azure disk and attach it to an Azure VM because they would not be able to decrypt the data without the encryption key. Azure recommends enabling ADE for production workloads."
**Add a cover photo like:**
![placeholder image](https://via.placeholder.com/1200x600)

# New post title here

## Introduction

✍️ (Why) Explain in one or two sentences why you choose to do this project or cloud topic for your day's study.

## Prerequisite

✍️ (What) Explain in one or two sentences the base knowledge a reader would need before describing the the details of the cloud service or topic.

## Use Case

- 🖼️ (Show-Me) Create an graphic or diagram that illustrate the use-case of how this knowledge could be applied to real-world project
- ✍️ (Show-Me) Explain in one or two sentences the use case

## Cloud Research

- ✍️ Document your trial and errors. Share what you tried to learn and understand about the cloud topic or while completing micro-project.
- 🖼️ Show as many screenshot as possible so others can experience in your cloud research.

## Try yourself

✍️ Add a mini tutorial to encourage the reader to get started learning something new about the cloud.

### Step 1 — Summary of Step

![Screenshot](https://via.placeholder.com/500x300)

### Step 1 — Summary of Step

![Screenshot](https://via.placeholder.com/500x300)

### Step 3 — Summary of Step

![Screenshot](https://via.placeholder.com/500x300)

## ☁️ Cloud Outcome

✍️ (Result) Describe your personal outcome, and lessons learned.

## Next Steps

✍️ Describe what you think you think you want to do next.

## Social Proof

✍️ Show that you shared your process on Twitter or LinkedIn

[link](link)
