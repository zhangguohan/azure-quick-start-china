# Create a VM from a specialized VHD disk

<a href="https://portal.azure.cn/#create/Microsoft.Template/uri/https%3A%2F%2Fraw.githubusercontent.com%2Fdafoyiming%2Fazure-quick-start-china%2Fmeat%2F201-vm-multiple-nic-from-specialized-vhd%2Fazuredeploy.json" target="_blank">
    <img src="http://azuredeploy.net/deploybutton.png"/>
</a>

- 为虚拟机创建两个网卡nic1和nic2
- 创建一个虚拟网络vnet
- 在vnet中创建两个子网subnet1和subnet2
- nic1 为主网卡连接subnet1；nic2为辅网卡连接subnet2
- 使用一个已有的VHD作为操作系统磁盘创建虚拟机