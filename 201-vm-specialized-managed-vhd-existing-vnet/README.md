# Create a specialized virtual machine in an existing virtual network by managed disk

<a href="https://portal.azure.cn/#create/Microsoft.Template/uri/https%3A%2F%2Fraw.githubusercontent.com%2Fdafoyiming%2Fazure-quick-start-china%2Fmeat%2F201-vm-specialized-managed-vhd-existing-vnet%2Fazuredeploy.json" target="_blank">
    <img src="http://azuredeploy.net/deploybutton.png"/>
</a>
<a href="http://armviz.io/#/?load=https%3A%2F%2Fraw.githubusercontent.com%2FAzure%2Fazure-quickstart-templates%2Fmaster%2F201-vm-specialized-vhd-existing-vnet%2Fazuredeploy.json" target="_blank">
    <img src="http://armviz.io/visualizebutton.png"/>
</a>

- 通过一个指定的管理磁盘创建VM
- 指定一个已经存在的虚拟网络和子网
- 同时创建一个用于诊断的存储账号
- 为PIP指定DNS名称

托管磁盘ID 为磁盘的resourceid 形如：/subscriptions/4c1f7e7c-e47c-4688-8de0-19b1f8b58636/resourceGroups/zymmanaged/providers/Microsoft.Compute/disks/zymmanaged_OsDisk_1_fec96d98af8a401d96918ae7745d713c