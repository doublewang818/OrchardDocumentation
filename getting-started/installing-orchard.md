# 安装Orchard

本主题面向且经过Orchard1.8版本的测试.

## 安装Orchard的几种方式

你可以通过以下四种方式安装Orchard:

* 通过Microsoft Web Platform Installer安装.
* 通过Microsoft WebMatrix 安装,详见[在WebMatrix中使用Orchard](/getting-started/working-with-orchard-in-webmatrix.md).
* 下载Orchard.zip文件然后安装,详见[使用zip文件手动安装Orchard](/getting-started/manually-installing-orchard.md).
* 在Orchard源代码中注册然后通过命令行或Visual Studio构建Orchard.

本主题讲述了如何使用Microsoft Web Platform Installer来安装Orchard.

## 要求

以下是运行Orchard的最低要求:

* ASP.NET 4.5

* 一个诸如 IIS Express 8, 7.5 或 IIS 7.x的应用服务器.

安装IIS时,你要确保开启了ASP.NET IIS模块.同时确保你的Orchard运行在集成管道的ASP.NET4应用程序池.

> **重点**:如果你以前安装过任何预览版的WebMatrix,ASP.NET Web Pages或者ASP.NET MVC4,为了让Orchard正确的在你的电脑上运行,你应该卸载这些产品.开发一个Orchard网页,许多开发者会使用像SQL Server这样的数据库以及像WebMatrix或者Visual Studio 2013这样的网页开发环境.以下的安装过程是在一个比较干净的Windows8.1系统中进行的.它使用了Web Platform Installer并且包含了Orchard,IIS 8.0 Express,还有WebMatrix和SQL Server Compact 4.0之类的用于Orchard开发的可选的应用程序.

## 安装Orchard

首先,你需要下载和安装[Web Platform Installer](https://www.microsoft.com/web/downloads/platform.aspx).如果你已经完成了,运行它

To begin, download and install the Web Platform Installer. When you're done, run it.

找到Orchard CMS然后点击Add按钮把Orchard选中为一个安装选项.

![](http://docs.orchardproject.net/en/latest/Attachments/Installing-Orchard/webpi_install.png)

点击安装.接受许可条款继续.

![](http://docs.orchardproject.net/en/latest/Attachments/Installing-Orchard/Install_acceptterms.png)

安装完成之后,对话框会显示已经安装的除了Orchard之外的工具列表.点击启动链接从而在WebMatrix中打开网站.

![](http://docs.orchardproject.net/en/latest/Attachments/Installing-Orchard/Install_success.png)

## 在WebMatrix中运行Orchard

WebMatrix启动后,它会立刻在默认的浏览器中启东Orchard.你也可以点击**运行**下拉按钮并选择浏览器启动Orchard如果没有自动启动.在WebMatrix中你可以点击**文件**工作空间查看Orchard网站的内容.

![](http://docs.orchardproject.net/en/latest/Attachments/Installing-Orchard/launch_Orchard_WebMatrix.png)

Orchard第一次运行时,你将会在你的浏览器中看到Orchard设置界面

![](http://docs.orchardproject.net/en/latest/Upload/screenshots/get_started_dialog_1.png)

默认情况下,Orchard包含了一个内置的数据库,这样你就可以不用另外再安装一个单独的数据库服务器.然而,如果你自己安装了SQL Server或者SQL Server Express,你可以通过指定数据库连接字符串来指定使用这些数据库.视情况需要,你可以键入一个表前缀\(table prefix\)从而让多个Orchard程序共享同一个数据库但与此同时又让他们的数据是保持独立的.

![](http://docs.orchardproject.net/en/latest/Upload/screenshots_85/setup_sqlserver.png)

在设置界面中还有一个区域可以让你选择一个Orchard配方去建立你的网站.你可以选择以下几种Orchard配方:

* **默认**.建立一个经常被使用的Orchard功能的网站.
* **博客**.



