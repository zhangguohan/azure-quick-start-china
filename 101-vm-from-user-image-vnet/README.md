# Create a Virtual Machine from a User Image

<a href="https://portal.azure.cn/#create/Microsoft.Template/uri/https%3A%2F%2Fraw.githubusercontent.com%2Fdafoyiming%2Fazure-quick-start-china%2Fmeat%2F101-vm-from-user-image-vnet%2Fazuredeploy.json" target="_blank">
    <img src="http://azuredeploy.net/deploybutton.png"/>
</a>
<a href="http://armviz.io/#/?load=https%3A%2F%2Fraw.githubusercontent.com%2FAzure%2Fazure-quickstart-templates%2Fmaster%2F101-vm-from-user-image%2Fazuredeploy.json" target="_blank">
    <img src="http://armviz.io/visualizebutton.png"/>
</a>

- 可以新建或者指定已有虚拟网络和虚拟机子网
- 可以将虚拟机创建在一个已经存在的可用性集中（虚拟机所在虚拟网络及虚拟子网应该与该可用性集下其他虚拟机在同一虚拟网络和虚拟子网）
- 虚拟机会创建在Image所在的存储账号