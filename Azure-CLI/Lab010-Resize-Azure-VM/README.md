# Lab 010 - Resize Azure Virtual Machine

## Method
Azure CLI

## Objective
Resize an existing Azure Virtual Machine from **Standard_B1s** to **Standard_B2s** and ensure the virtual machine is in the **Running** state after the resize.

## Azure Services
- Azure Virtual Machine (VM)
- Azure Compute
- Azure CLI

## Steps
1. Identify the target virtual machine.
2. Resize the VM from **Standard_B1s** to **Standard_B2s**.
3. Start the virtual machine.
4. Verify the resize operation completed successfully.

## Azure CLI Commands

```bash
# Resize the virtual machine
az vm resize \
  --resource-group <RESOURCE_GROUP> \
  --name datacenter-vm \
  --size Standard_B2s

# Start the virtual machine
az vm start \
  --resource-group <RESOURCE_GROUP> \
  --name datacenter-vm
```

## Outcome

Successfully resized the Azure Virtual Machine from **Standard_B1s** to **Standard_B2s** and ensured it was in the **Running** state.
