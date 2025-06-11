---
tags : mod cs
---
Created: 2025-06-02

## Storage Hierarchy
**most important** 
- speed
- cost (linked to speed)

## Direct Memory Access Structure
- Memory
- Direct Memory Access Structure (DMAS)
- CPU

## Internal Structure
![[graph Internal structure]]

## How a Modern Computer Works
![[file-20250602160550647.png]]

## Clustered Systems
This
![[file-20250602162908643.png]]

You work as a Network administrator at Dunis. You have decided to upgrade your computers networks (storage, brand new computers, vendors, memory ect...).
1/ After designing the network topology of the school please describe how did you manage storage
2/ Please propose a clustering system of the storage network
3/ the school internet connectivity is 100mb 50 uploading and 50 downloading you need to connect 300 computers, allowing YouTube and movie download, how would you handle this issue.
4/ In some computers the I/O controller is not responding, why? How would you fix this? What conflicts might exist between the cluster system and the device manager.

### 1. Storage Management:
- The network administrator implemented a common **Storage Area Network (SAN)**.
- All computers access shared storage over the network.
- A clear file hierarchy with **access control** was set for students, staff, and administrators.
- **Backups** and **redundancy** were integrated in case of data loss.

### 2. Clustering System Proposal:
- A clustered system was set up using multiple servers.
- Each server runs services and monitors others.
- If one server fails, another takes over to maintain uptime.
- The shared storage is accessed by all computers acting as cluster nodes via the SAN.

### 3. Internet Connectivity (100 Mbps total, 50 up/50 down, 300 PCs):

- A **bandwidth management system** was configured to prioritize traffic.
- **Content filtering** and **download limits** were enforced during school hours.
- **caching servers** store frequently accessed content like YouTube videos.
- Having a high bandwidth and low latency

### 4. I/O Controller Issues:

- Some I/O controllers failed due to **driver conflicts**, outdated firmware, or hardware faults.
- The administrator updated drivers and replaced faulty components.
- Conflicts may occur if the **cluster system’s resource allocation** clashes with the **device manager**.
- Standardizing hardware and synchronizing configurations across nodes solved the issue.

Test on : 
- Mass Storage
- Operating System
- Clustered System 
- Storage Hierarchy
- 