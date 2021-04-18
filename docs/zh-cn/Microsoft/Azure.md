

## 连接到 Azure Active Directory PowerShell Graph 模块

官方文档：https://docs.microsoft.com/zh-cn/microsoft-365/enterprise/connect-to-microsoft-365-powershell?view=o365-worldwide#connect-with-the-azure-active-directory-powershell-for-graph-module

## 步骤 1：安装所需软件

这些步骤只需在计算机上执行一次。 但可能需要定期更新软件

1、打开提升的 Windows PowerShell 命令提示符窗口（以管理员身份运行 Windows PowerShell）

2、运行此命令：

```powershell
Install-Module -Name AzureAD
```

默认情况下，PowerShell 库 (PSGallery) 不会配置为 **PowerShellGet** 受信任的存储库 
首次使用 PSGallery 时，你将看到以下消息：

```powershell
Untrusted repository

You are installing the modules from an untrusted repository. If you trust this repository, change
its InstallationPolicy value by running the `Set-PSRepository` cmdlet.

Are you sure you want to install the modules from 'PSGallery'?
[Y] Yes  [A] Yes to All  [N] No  [L] No to All  [S] Suspend  [?] Help (default is "N"):
```

回答“**是**”或“**全部是**”以继续安装

## 步骤 2：连接到 Microsoft 365 订阅的 Azure AD

若要使用帐户名称和密码或者多重身份验证连接到 Microsoft 365 订阅的 Azure Active Directory (Azure AD)，请在 Windows PowerShell 命令提示符中运行这些命令之一

| **Office 365 云**                                      | **命令**                                                |
| ------------------------------------------------------ | ------------------------------------------------------- |
| Office 365 全球 (+GCC)                                 | Connect-AzureAD                                         |
| 由世纪互联运营的 Office 365                            | Connect-AzureAD -AzureEnvironmentName AzureChinaCloud   |
| Office 365 德国                                        | Connect-AzureAD -AzureEnvironmentName AzureGermanyCloud |
| Office 365 美国政府版 DoD 和 Office 365 美国政府版 GCC | Connect-AzureAD -AzureEnvironmentName AzureUSGovernment |

