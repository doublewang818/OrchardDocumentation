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

> **重点**:如果你以前安装过任何先行版本的WebMatrix,ASP.NET Web Pages或者ASP.NET MVC4,为了让Orchard正确的在你的电脑上运行,你应该卸载这些产品.开发一个Orchard网页,许多开发者会使用像SQL Server这样的数据库以及像WebMatrix或者Visual Studio 2013这样的网页开发环境.以下的安装过程是在一个比较干净的Windows8.1系统中进行的.它使用了Web Platform Installer并且包含了Orchard,IIS 8.0 Express,还有WebMatrix和SQL Server Compact 4.0之类的用于Orchard开发的可选的应用程序.

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

After WebMatrix starts, it should inmediately launch Orchard in the default browser. If not, you can launch Orchard by clicking the Run drop-down button, and selecting which browser to use. In WebMatrix you can click the Files workspace to see the contents of the Orchard site.

The first time Orchard is launched, you see in your browser the Orchard setup screen.

By default, Orchard includes a built-in database that you can use without installing a separate database server. However, if you are running SQL Server or SQL Server Express, you can configure Orchard to use either of those products instead by specifying a connection string. Optionally, you can enter a table prefix so that multiple Orchard installations can share the same database but keep their data separate.

The setup screen also includes a section where you can choose an Orchard recipe to set up your site. You can choose from the following Orchard recipes:

Default. Sets up a site with frequently used Orchard features.

Blog. Sets up a site as a personal blog.

Core. Sets up a site that has only the Orchard framework for development use.

For information about recipes and how to make a custom recipe, see Making a Web Site Recipe.

After you've entered the required information on the setup screen, click Finish Setup. When the setup process is complete, your new site's home page is displayed.

You can now begin configuring your site.

