# ArgoCD Disaster Recovery

This repository contains manifests for backup and restore of Cluster disaster with an emphasis on ArgoCD's Data using ACM and OADP, as well as a Kyverno policy and sample applications for simulation.

## Active-Cluster

The following manifests are available for the Active Cluster:
### OADP
- `ScheduledBackup.yaml`: Schedule a periodically backup for the Cluster data
- `DataApplicationProtection.yaml`: Set the connection to the storage location (Where the backups stored)
### OCM-policy
- `policy.yaml`: A policy using open-cluster-management which inform on ArgoCD un-labeled nessecry resources.

## Active-Cluster

The following manifests are available for the Passive Cluster:
### OADP
- `Restore.yaml`: Schedule aמ interval restore for the Backup Data.
- `DataApplicationProtection.yaml`: Set the connection to the storage location (Where the backups stored)
### Kyverno-Policy
- `policy.yaml`: Enforces all existing `AppProject` to contain block type window sync.

## apps

Applications for simulation

## HLD

![HLD](https://ibb.co/k1TGr6Q)


Note: These manifests are provided for simulation purposes only and should be customized for your specific use case

