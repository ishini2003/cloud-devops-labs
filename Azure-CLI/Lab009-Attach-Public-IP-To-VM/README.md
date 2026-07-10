# Lab 009 - Attach Public IP to Azure Virtual Machine

## Method
Azure CLI

## Objective
Attach an existing Public IP address to the Network Interface Card (NIC) of an existing Azure Virtual Machine using Azure CLI.

## Azure Services
- Azure Virtual Machine (VM)
- Network Interface (NIC)
- Public IP Address
- Resource Group
- Azure CLI

## Steps
1. List available Network Interfaces.
2. Identify the correct Resource Group.
3. List available Public IP addresses.
4. View the NIC IP configuration.
5. Attach the Public IP to the NIC.
6. Verify the configuration.

## Azure CLI Commands

```bash
# List available Network Interfaces
az network nic list -o table

# List available Public IP addresses
az network public-ip list -o table

# View the NIC IP configuration
az network nic ip-config list \
  --resource-group <RESOURCE_GROUP> \
  --nic-name xfusion-vm-pipVMNic \
  -o table

# Attach the Public IP to the NIC
az network nic ip-config update \
  --resource-group <RESOURCE_GROUP> \
  --nic-name xfusion-vm-pipVMNic \
  --name ipconfigxfusion-vm-pip \
  --public-ip-address xfusion-pip
```

## Outcome

Successfully attached the existing **xfusion-pip** Public IP address to the Network Interface Card of the **xfusion-vm-pip** virtual machine using Azure CLI.