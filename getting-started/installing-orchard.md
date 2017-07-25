# 安装Orchard

本主题面向且经过Orchard1.8版本的测试.

## 安装Orchard的几种方式

你可以通过以下四种方式安装Orchard:

* 通过Microsoft Web Platform安装程序安装.
* 通过Microsoft WebMatrix 安装,详见[在WebMatrix中使用Orchard](/getting-started/working-with-orchard-in-webmatrix.md).
* 下载Orchard.zip文件然后安装,详见[使用zip文件手动安装Orchard](/getting-started/manually-installing-orchard.md).
* 在Orchard源代码中注册然后通过命令行或Visual Studio构建Orchard.

本主题讲述了如何使用Microsoft Web Platform Installer来安装Orchard.

## 要求

以下是运行Orchard的最低要求:

* ASP.NET 4.5

* 一个诸如 IIS Express 8, 7.5 或 IIS 7.x的应用服务器.

安装IIS时,你要确保开启了ASP.NET IIS模块.同时确保你的Orchard运行在集成管道的ASP.NET4应用程序池.

Important: If you previously installed any pre-release versions of WebMatrix, ASP.NET Web Pages, or ASP.NET MVC 4, you should uninstall those products before Orchard will run correctly on your computer. To develop Orchard sites, many developers will want to use a database such as SQL Server, and a web page programming environment such as WebMatrix or Visual Studio 2013. The following installation was tested with a clean installation of Windows 8.1. It uses the Web Platform Installer and it includes Orchard, IIS 8.0 Express, and optional applications for Orchard development like WebMatrix and SQL Server Compact 4.0.

Installing Orchard

To begin, download and install the Web Platform Installer. When you're done, run it.

Find Orchard CMS and then click Add to include Orchard as an item to install.

Click Install. Accept the license terms in order to continue.

When the installation is complete, the dialog shows the list of installed tools in addition to Orchard. Click the Launch link to open the site in WebMatrix.

Running Orchard in WebMatrix

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

