# Create a VM from a specialized VHD disk

<a href="https://portal.azure.cn/#create/Microsoft.Template/uri/https%3A%2F%2Fraw.githubusercontent.com%2Fdafoyiming%2Fazure-quick-start-china%2Fmeat%2F201-vm-triple-nic-from-specialized-vhd%2Fazuredeploy.json" target="_blank">
    <img src="http://azuredeploy.net/deploybutton.png"/>
</a>

- 为虚拟机创建三个网卡nic1，nic2和nic3
- 创建一个虚拟网络vnet(10.0.0.0/16)
- 在vnet中创建两个子网subnet1(10.0.1.0/24)，subnet2(10.0.2.0/24)和subnet3(10.0.3.0/24)
- nic1为主网卡连接subnet1；nic2为辅网卡连接subnet2；nic3为辅网卡连接subnet3
- 使用一个已有的VHD作为操作系统磁盘创建虚拟机