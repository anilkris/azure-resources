# Encrypt VM DISK

## PowerShell : 

####  Login to Azure Account

Login to Azure account and create some environmental variables 

```shellscirpt
Login-AzAccount

$resourceGroup=MYRG

$location = southindia

$vmName = MYVM

$keyVaultName = myuniquekeyvault
```


#### Create a Resource Group

```shellscript
Get-AzResourceGroup -Name $ResourceGroup -Location $location
```

#### Craete a VM

```shellscript
New-AzVm -Name $vmName -ResourceGroup $resourceGroup -Location $location  -Size Standard_D2_V3 -Image  Win2016Datacenter
```

#### Create a Key Vault

```shellscript
New-AzKeyVault -Name $keyVaultName -ResourceGroupName $resourceGroup -Location $location 
```

#### Set an access poilcy for VM Disk Encryption

```shellscript
Set-AzKeyVaultAccessPolicy -VaultName $keyVaultName -ResourceGroupName $ResourceGroup -EnabledForDiskEncryption
```


#### Encrypt VM
```shellscript
$KeyVault = Get-AzKeyVault -VaultName $keyVaultName -ResourceGroup $resourceGroup

Set-AzVmDiskEcnryptionExtension -ResourceGroupName $resourceGroup -VMName $vmName $keyVault.VaultUri -DiskEncryptionKeyVaultId $KeyVault.ResourceId
```

Check the VM disk is encrypted now in the Azure portal.