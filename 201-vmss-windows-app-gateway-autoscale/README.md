### Windows VM Scale Set with Application Gateway Integration ###

This template deploys a Windows VM Scale Set integrated with Azure Application Gateway.

The Application Gateway is configured for round robin load balancing of incoming connections at port 80 (of the gateway's public IP address) to VMs in the scale set. 
 
Note that this template does not install an application on the VM Scale Set VMs, so if you want to demonstrate the round robin load balancing, the template will need to be updated (for example by adding an extension to install a web server). 

This template supports VM scale sets of up to 1,000 VMs, and uses Azure Managed Disks.

Yiming.zhang： Enable autoscale depand on "Porcessor Time". Greater than 70% will triger one instant up and Less than 30% will triger one instant down

<a href="https://portal.azure.cn/#create/Microsoft.Template/uri/https%3A%2F%2Fraw.githubusercontent.com%2Fdafoyiming%2Fazure-quick-start-china%2Fmeat%2F201-vmss-windows-app-gateway-autoscale%2Fazuredeploy.json" target="_blank">
    <img src="http://azuredeploy.net/deploybutton.png"/>
</a>
<a href="http://armviz.io/#/?load=https%3A%2F%2Fraw.githubusercontent.com%2FAzure%2Fazure-quickstart-templates%2Fmaster%2F201-vmss-windows-app-gateway%2Fazuredeploy.json" target="_blank">
    <img src="http://armviz.io/visualizebutton.png"/>
</a>

