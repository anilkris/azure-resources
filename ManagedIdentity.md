# Managed Idenity

![Managed Identity](https://docs.microsoft.com/en-us/azure/active-directory/managed-identities-azure-resources/media/overview/msi-vm-vmextension-imds-example.png)





#### Login to Az Account and create some variables 

```shellscirpt
Login-AzAccount

$resourceGroup='MYRG'

$location='southindia'

$vmName='MYVM'

$myos='UbuntuLTS'

```


#### Create a Resource Group
```shellscirpt
New-AzResourceGroup -Name $ResourceGroup -Location $location
```

#### Craete a VM

```shellscript
New-AzVm -Name $vmName -ResourceGroup $resourceGroup -Location $location  -Size Standard_B1s  -Image $myos -OpenPorts 22 
```

### Get VM and update it to System identity

```shellscript
$vm = Get-AzVM  -ResourceGroupName $resourceGroup -Name $vmName

Update-AzVM -ResourceGroupName $resourceGroup -VM $vm -AssignIdentity:$SystemAssigned
```


### Get Object ID of VM

```shellscript

$vmId = Get-AzADServicePrincipal -displayname $vmName

```

### Get Object ID of the Group // AD Group

If the Group does not exist create one

```shellscript
$myGroup = Get-AzADGroup | searchstring 'MYGROUP'
```

### Add the VM's service principal to the group

```shellscript
Add-AzADGroupMember -MemberObjectId $vmId.Id -TargetGroupObjectId $myGroup.Id
```

### Remove a VM

'''shellscript
Remove-AzVm -Name $vmName -ResourceGroup $resourceGroup

''''