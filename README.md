## Documentation

# Table of Contents
1. [System configuraitons](/aboutme/pages/1_system_setup.md.md)
2. Containerd Installation
3. Kubernets Installation
4. Helm Installation
...

# Pre Installation
## Overview
This document provides the basic steps and minimum requirements for installing and setting up the iBASEt iSeries environment.
### Organization of Document
This document is split up into several sections. Depending on whether you are installing the iSeries for the first time (Fresh Install with no connected data), performing a maintenance update from an existing iSeries environment, or upgrading from the G-Series you are required to review and perform the steps as defined below.
- **Fresh Install** (with <ins>no connected data</ins>) – Requires the following:
   - All prerequites are met. The information defined in this section (***Pre-Installation***) including all referenced documents.
   - All steps in the Setting Up the Environment section (starting on page 8) are completed.
   - All steps in the Installation section (starting on page 15) are completed.
   - Requires review Technical Notes section and implementat based on your environment.
- **Upgrade from the G-Series or i0.1.0** (with connected data) – See the Fresh Install bullet points above.
> :warning: **Important:**  
>  When copying any of the examples provided within this document, it is recommended to:   
>  1.	Copy/Paste examples first into a text editor such as Notepad, WordPad, Notepad++, ...   
>  2.	Adjust the text so that it is specific for the environment you are working in, as many of the examples require IP Address, version number, and so on.   
>  3.	Copy/Paste updated commands into your Command Prompt.   

## Assumptions
This document assumes that the reader is familiar with:
 
- Linux (Redhat/CentOS)
- NFS Server
- Mongo DB
- Elasticsearch, Logstash, Kibana (ELK)
- Kubernetes, Workload Controllers, Services, Networking

> :memo: **Note:**   
  > 1. If you have already created a Docker Hub “service account”, skip to Step #2.
  > 2. If you have not created an account, go to https://docs.docker.com/docker-id to create your account. This requires an email address, user ID, and password.

| Feature or Functionality| Limitation
|----------- | ----------- |
| High Availability      | Node downtime due to the non-fault-tolerant topology. |
| Maintainability   | Node downtime during maintenance. |
| Load Balancing | Not available |
| Scalability | Not available |
| Performance | Possible performance impact due to lower number of replicas of the services. |

```
# setenforce 0
# sed -i 's/^SELINUX=enforcing$/SELINUX=disabled/' /etc/selinux/config
```
This is updated as  am saving it preview qwill be available

