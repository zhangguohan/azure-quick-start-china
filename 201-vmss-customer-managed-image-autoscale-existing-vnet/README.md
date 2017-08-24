### Autoscale a VM Scale Set For Windows Server Customer Image with Managed Disks ###

## 操作系统准备 ##

- Windows 操作系统

打开目前执行Sysprep.exe

c:\windows\system32\sysprep\sysprep.etc

1. Enter System Out-of-Box Experience (OOBE)
2. Generalize
3. Shutdown

![Sysprep](assets/README-4401a.pngassets/README-4401a.png)

- Linux 操作系统

sudo waagent-deprovision

## 捕获虚拟机镜像 ##

- 定义变量

  $vmName = "myVM"

  $rgName = "myresourcegroup"

  $location = "chinanorth"

  $imageName = "myImage"

- 保证虚拟机已经关机

    Stop-AzureRmVM -ResourceGroupName $rgName -Name $vmName -Force

- 通用化虚拟机

    Set-AzureRmVm -ResourceGroupName $rgName -Name $vmName -Generalized

- 声明VM变量

    $vm = Get-AzureRmVM -Name $vmName -ResourceGroupName $rgName

    $image = New-AzureRmImageConfig -Location $location -SourceVirtualMachineId $vm.ID

- 创建镜像

    New-AzureRmImage -Image $image -ImageName $imageName -ResourceGroupName $rgName

- 获得镜像ID

    (Get-AzureRmImage -ResourceGroupName $rgName -ImageName $imageName).Id

• 镜像ID后续将添加到模板的参数中，形如:

    /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/xxxxx/providers/Microsoft.Compute/images/xxxxx

## 在管理门户中捕获 ##

![Capture](assets/README-e7b1a.pngassets/README-e7b1a.png)

![ImageID](assets/README-d4ac7.pngassets/README-d4ac7.png)

![ImageID2](assets/README-32161.pngassets/README-32161.png)

The Autoscale rules are configured as follows
- sample for CPU (\\Processor\\PercentProcessorTime) in each VM every 1 Minute
- if the Percent Processor Time is greater than 50% for 5 Minutes, then the scale out action (add more VM instances, one at a time) is triggered
- once the scale out action is completed, the cool down period is 1 Minute


<a href="https://portal.azure.cn/#create/Microsoft.Template/uri/https%3A%2F%2Fraw.githubusercontent.com%2Fdafoyiming%2Fazure-quick-start-china%2Fmeat%2F201-vmss-customer-managed-image-autoscale-existing-vnet%2Fazuredeploy.json" target="_blank">
    <img src="http://azuredeploy.net/deploybutton.png"/>
</a>
