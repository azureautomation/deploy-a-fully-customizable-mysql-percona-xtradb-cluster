Deploy a fully customizable MySQL Percona XtraDB Cluster
========================================================

            

This runbook provides a way to deploy a fully customizable MySQL Percona XtraDB Cluster (PXC) 5.6 on CentOS 6.5 and Ubuntu 12.04 LTS in the specified Azure environment. It provisions network, storage and compute resources for the cluster, and leverages
 Azure Linux custom script VM extension to run a bash script to install and configure MySQL on each node. It also optionally stripes disks to improve IO throughput.  


Once the cluster is deployed, access MySQL from the provisioned internal load balancer with the preconfigured user account. Then inside the MySQL environment, run 'show status like 'wsrep%';' to make sure wsrep_cluster_size shows the number of cluster nodes
 specified, and wsrep_ready is 'ON'.     


Although the runbook is capable of provisioning a second NIC for the cluster nodes, Azure Automation currently runs on a PowerShell Azure SDK version that doesn't support multiple NICs.  Once Azure SDK for Automation is updated, the runbook will automatically
 support second NIC. 


 

 
 

        
    
TechNet gallery is retiring! This script was migrated from TechNet script center to GitHub by Microsoft Azure Automation product group. All the Script Center fields like Rating, RatingCount and DownloadCount have been carried over to Github as-is for the migrated scripts only. Note : The Script Center fields will not be applicable for the new repositories created in Github & hence those fields will not show up for new Github repositories.
