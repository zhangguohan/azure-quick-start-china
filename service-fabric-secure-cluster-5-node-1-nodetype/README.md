# Very simple deployment of a 5 Node secure Service Fabric Cluster with Azure Diagnostics enabled

<a href="https://portal.azure.cn/#create/Microsoft.Template/uri/https%3A%2F%2Fraw.githubusercontent.com%2Fdafoyiming%2Fazure-quick-start-china%2Fmeat%2Fservice-fabric-secure-cluster-5-node-1-nodetype%2Fazuredeploy.json" target="_blank">
    <img src="http://azuredeploy.net/deploybutton.png"/>
</a>

This template allows you to deploy a secure 5 node, Single Node Type Service fabric Cluster running Windows server 2012 R2 Data center on Standard_D2 Size VMs with Windows Azure diagnostics turned on. This template assumes that you already have certificates uploaded to your keyvault, else I strongly suggest you follow one of the two links below.

# 如何生成证书并上传到Azure 密钥保管库

- 载Github中提供的创建脚本：

  https://github.com/dafoyiming/Service-Fabric/blob/master/Scripts/ServiceFabricRPHelpers/ServiceFabricRPHelpers.psm1

- 加载模块：

  PS C:\Users\zhangyiming> Import-Module "C:\Users\zhangyiming\Documents\GitHub\Service-Fabric\Scripts\ServiceFabricRPHelpers\ServiceFabricRPHelpers.psm1"

- 导入本地证书.pfx(省略如何创建导出pfx)

   PS C:\Users\zhangyiming> Invoke-AddCertToKeyVault -SubscriptionId 4c1f7e7c-e47c-4688-8de0-19b1f8b58636 -ResourceGroupName zymvault -Location "china north" -VaultName zymvault -CertificateName zymcert -Password 123456 -UseExistingCertificate -ExistingPfxFilePath "C:\Windows\System32\zymcert.pfx" | Out-File -Encoding utf8 -FilePath 'C:\tmp\certinfo.txt'

- 记录下TXT中内容
