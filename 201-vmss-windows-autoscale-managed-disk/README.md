### Autoscale a Windows VM Scale Set with \\NetworkInterface\\BytesTransmitted ###

The following template deploys a Windows VM Scale Set integrated with Azure autoscale 



The template deploys a Windows VMSS with a desired count of VMs in the scale set. Once the VM Scale Sets is deployed, user can deploy an application inside each of the VMs (either by directly logging into the VMs or via a custom script extension)

The Autoscale rules are configured as follows
- sample for Network (\\NetworkInterface\\BytesTransmitted) in each VM every 1 Minute
- if the Percent Processor Time is greater than 200000000 for 5 Minutes, then the scale out action (add more VM instances, one at a time) is triggered
- once the scale out action is completed, the cool down period is 1 Minute


<a href="https://portal.azure.cn/#create/Microsoft.Template/uri/https%3A%2F%2Fraw.githubusercontent.com%2Fdafoyiming%2Fazure-quick-start-china%2Fmeat%2F201-vmss-windows-autoscale-managed-disk%2Fazuredeploy.json" target="_blank">
    <img src="http://azuredeploy.net/deploybutton.png"/>
</a>
<a href="http://armviz.io/#/?load=https%3A%2F%2Fraw.githubusercontent.com%2FAzure%2Fazure-quickstart-templates%2Fmaster%2F201-vmss-windows-autoscale%2Fazuredeploy.json" target="_blank">
    <img src="http://armviz.io/visualizebutton.png"/>
</a>
