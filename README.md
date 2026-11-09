# Azure Virtual Machine Deployment Using ARM Template

## Overview

This project demonstrates the deployment of an Azure Virtual Machine using an Azure Resource Manager (ARM) Template.

Developed as part of the AMACE Azure Administrator practical examination.

## Architecture

The ARM template provisions the following Azure resources:

- Azure Virtual Machine (Ubuntu Server 22.04 LTS)
- Azure Virtual Network (VNet)
- Network Security Group (NSG)
- Network Interface (NIC)
- Static Public IP Address

## VM Configuration

| Property | Value |
|---|---|
| VM Name | amace-arm-vm |
| Region | East Asia |
| VM Size | Standard_B2ats_v2 |
| Operating System | Ubuntu Server 22.04 LTS |
| Authentication | Username and password |
| Deployment Method | ARM Template (JSON) |

## Deployment

1. Sign in to the Azure Portal.
2. Search for **Deploy a custom template**.
3. Select **Build your own template in the editor**.
4. Upload `vm_deploy.json`.
5. Configure the deployment parameters.
6. Select **Review + Create**, then **Create**.
7. Verify that the deployment succeeds.

## Results

The ARM template was successfully deployed to Azure.

The virtual machine reached the **Running** state, and the associated networking resources were provisioned successfully.

## Security

- Administrator passwords are provided through a `secureString` parameter.
- SSH inbound access is restricted by the source address parameter.
- No credentials or private keys are stored in this repository.

## Cleanup

Delete the resources created specifically for this lab after completion to avoid unnecessary Azure charges.
