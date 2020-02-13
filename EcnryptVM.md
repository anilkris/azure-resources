# Encrypt VM

## PowerShell : 

*Login-AzAccount*

$resourceGroup=MYRG
$location = southindia

$vmName = MYVM

$keyVaultName = myuniquekeyvault

### Create a Resource Group
*Get-AzResourceGroup -Name $ResourceGroup -Location $location*

#### Craete a VM

*New-AzVm -Name $vmName -ResourceGroup $resourceGroup -Location $location  -Size Standard_D2_V3*





#### Create a Key Vault
*New-AzKeyVault -Name $keyVaultName -ResourceGroupName $resourceGroup -Location $location* 

#### Set an access poilcy for VM Disk Encryption
*Set-AzKeyVaultAccessPolicy -VaultName $keyVaultName -ResourceGroupName $ResourceGroup -EnabledForDiskEncryption*


#Encrypt VM
*$KeyVault = Get-AzKeyVault -VaultName $keyVaultName -ResourceGroup $resourceGroup*

*Set-AzVmDiskEcnryptionExtension -ResourceGroupName $resourceGroup -VMName $vmName $keyVault.VaultUri -DiskEncryptionKeyVaultId $KeyVault.ResourceId*