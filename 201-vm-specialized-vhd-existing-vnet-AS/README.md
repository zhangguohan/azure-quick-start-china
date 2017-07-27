# Create a specialized virtual machine in an existing virtual network

<a href="https://portal.azure.cn/#create/Microsoft.Template/uri/https%3A%2F%2Fraw.githubusercontent.com%2Fdafoyiming%2Fazure-quick-start-china%2Fmeat%2F201-vm-specialized-vhd-existing-vnet-AS%2Fazuredeploy.json" target="_blank">
    <img src="http://azuredeploy.net/deploybutton.png"/>
</a>
<a href="http://armviz.io/#/?load=https%3A%2F%2Fraw.githubusercontent.com%2FAzure%2Fazure-quickstart-templates%2Fmaster%2F201-vm-specialized-vhd-existing-vnet%2Fazuredeploy.json" target="_blank">
    <img src="http://armviz.io/visualizebutton.png"/>
</a>

- 通过一个指定得VHD创建VM
- 指定一个已经存在的虚拟网络和子网
- 指定一个可用性集，该可用性集下的其他虚拟机必须也在之前的已经存在的虚拟网络中
- 同时创建一个用于诊断的存储账号
- 为PIP指定DNS名称