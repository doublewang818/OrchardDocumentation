# 手动安装Orchard

_本主题面向且经过Orchard1.8版本的测试._

本主题讲述了你用zip文件安装过程中需要执行的步骤.

我们会使用三种不同的方式:

* IIS.
* WebMatrix 和 IISExpreee
* Visual Studio 和 the Visual Studio Development Server.

> **注意**
>
> 如果你倾向于使用 Web Platform Installer,或者你打算用 WebMatrix 开发你的网站,你可能需要看这篇文章[安装Orchard](/getting-started/installing-orchard.md),文中讲述了使用Web Platform Installer安装 Orchard 而且在安装过程中包含了WebMatrix.

Downloading the .zip File

## 下载zip文件

访问网页[Releases Section of Orchard in GitHub](https://github.com/OrchardCMS/Orchard/releases).

你可以找到两个zip文件.

* Orchard.Web.1.x.xx.zip:在这个文件中,网站已经建立好不用编译就可以直接运行了.它不包含所有的源代码
* Orchard.Source.1.x.xx.zip :这个文件包含了源代码.如果你打算自己开发模块的话你可能会倾向于使用这个.你可以通过Visual Studio很方便的使用它,而且有大量的源文件可以让你知道其中的所有奥秘.

## 通过IIS运行站点

_这个过程是在纯净的Windows 8.1 企业版中进行的._

首先让我们来设置服务器.在你的系统中搜索"添加删除程序".然后点击执行.

![](http://docs.orchardproject.net/en/latest/Attachments/Manually-installing-Orchard-zip-file/IISSearchForAddRemovePrograms.png)

点击开启/关闭系统功能.

![](http://docs.orchardproject.net/en/latest/Attachments/Manually-installing-Orchard-zip-file/IISTurnOnWindowsFeatures.png)

点击 **Internet Information Services** -&gt; **ASP.NET 4.5**. 点击**完成**.

![](http://docs.orchardproject.net/en/latest/Attachments/Manually-installing-Orchard-zip-file/IISEnableIISAndASP45.png)

在这时候我们建议你重启一下系统.通过这种方式可以确保必要的服务是被开启的.

系统重启后,在[这里](https://github.com/OrchardCMS/Orchard/releases/latest)下载Orchard.Web.1.x.xx.zip.解压zip文件到你的桌面.解压后的文件夹包含了一些文件以及一个Orchard文件夹.

把Orchard文件夹拷贝到C:\inetpub\wwwroot.

在资源管理器中进入Orchard文件夹.让我们从App\_Data文件夹开始.

这个文件夹中存储了Orchard的网站设置.右击App_Data_文件夹,点击**属性**然后在**安全**标签页中给IIS\_IUSRS用户设置修改和读权限.

然后给以下文件夹重复以上过程.

* _Modules_.如果你想通过gallery安装模块的话这是必须的.\(我们建议你在生产环境中移除**读/写**权限\).
* Tehems.如果你想通过gallery安装主题的话这是必须的.\(我们建议你在生产环境中移除**读/写**权限\).
* _Media_.这个文件夹是Orchard用来存储媒体文件的\(如图片等\).

![](http://docs.orchardproject.net/en/latest/Attachments/Manually-installing-Orchard-zip-file/IISSetFolderPermissions.png)

> **提示**:如果你想将Orchard网站的设置重置到默认设置,你可以删除App\_Data目录中的内容.这将会移除你所有的自定义设置,用户和配置以及你在网站中添加的自定义内容.如果你删除了App\_Data文件夹中的内容后,还想删除你在网站中添加的自定义图片,你也可以将Media文件夹中的内容删除.必要的文件会在下一次Orchard重启时被重建.

现在你可以建立你的新网站了.搜索 **Internet Information Services \(IIS\) Manager**然后执行.

![](http://docs.orchardproject.net/en/latest/Attachments/Manually-installing-Orchard-zip-file/IISOpenIISManager.png)

点击**默认站点**并**停用**.这将给我们自己的网站使用80端口.

![](http://docs.orchardproject.net/en/latest/Attachments/Manually-installing-Orchard-zip-file/IISStopDefaultWebSite.png)

右击**站点**并**添加网站**.

![](http://docs.orchardproject.net/en/latest/Attachments/Manually-installing-Orchard-zip-file/IISAddANewWebsite.png)

给你的网站起名并将**物理地址**指向你的Orchard文件夹.点击**完成**.

![](http://docs.orchardproject.net/en/latest/Attachments/Manually-installing-Orchard-zip-file/IISAddWebsiteScreen.png)

在警告对话框中点击**是**从而使用80端口.

![](http://docs.orchardproject.net/en/latest/Attachments/Manually-installing-Orchard-zip-file/IISPort80Conflict.png)

现在你的网站已经在运行了.点击**浏览**去访问它.

![](http://docs.orchardproject.net/en/latest/Attachments/Manually-installing-Orchard-zip-file/IISBrowseToSite.png)

你将会在浏览器中看见Orchard的设置界面.

## 使用WebMatrix和IISExpress运行网站

在[这里](https://github.com/OrchardCMS/Orchard/releases/latest)下载Orchard.Web.1.x.xx.zip文件.解压Orchard zip文件到本地文件夹.启动WebMatrix,在**快速启动**界面中,点击**打开**选择**文件夹**.

![](http://docs.orchardproject.net/en/latest/Attachments/Manually-installing-Orchard-zip-file/IISWMOpenFolder.png)

打开你解压后的zip文件夹,选择名为Orchard的文件夹,然后点击**选择文件夹**去打开网站.

![](http://docs.orchardproject.net/en/latest/Attachments/Manually-installing-Orchard-zip-file/IISWMSelectFolder.png)

要运行网站,在WebMatrix工作空间中选择Orchard根目录点击**运行**按钮在下拉列表中选择一款浏览器.

![](http://docs.orchardproject.net/en/latest/Attachments/Manually-installing-Orchard-zip-file/IISWMRun.png)

你将会在你的浏览器中看到Orchard设置界面.

## 使用Visual Studio和Visual Studio开发服务器运行网站

_这个过程是在Visual Studio 2013 Update 1中进行的._

虽然你可以在Visual Studio中运行预编译版本的Orchard,但是你会发现在Visual Studio中使用完整的源代码版本会更简单.在[这里](https://github.com/OrchardCMS/Orchard/releases/latest)下载源代码.将zip文件解压到本地文件夹.

![](http://docs.orchardproject.net/en/latest/Attachments/Manually-installing-Orchard-zip-file/contents_of_source_zip_file.png)

启动Visual Studio然后选择 **File **&gt; **Open** &gt; **Project/Solution**.导航到你解压zip文件的文件夹然后打开名为src的文件夹,选择Orchard.sln**解决方案**文件.

![](http://docs.orchardproject.net/en/latest/Attachments/Manually-installing-Orchard-zip-file/VSOpenSolution.png)

点击Ctrl+F5运行网站.你将会在你的浏览器中看到Orchard设置界面.

## 建立一个站点

Orchard第一次运行时,你将会在你的浏览器中看到Orchard设置界面

![](http://docs.orchardproject.net/en/latest/Upload/screenshots/get_started_dialog_1.png)

默认情况下,Orchard包含了一个内置的数据库,这样你就可以不用另外再安装一个单独的数据库服务器.如果你选择了这个选项你不需要配置任何数据库信息.一个名为SQL Server CE的迷你版本SQL Server将自动运行在你的网站.它将数据存储在App\_Data文件夹下的一个内嵌数据库.

然而,如果你自己安装了SQL Server或者SQL Server Express,你可以通过指定数据库连接字符串来指定使用这些数据库.在Orchard配置之前,你必须建立好数据库以及数据库字符连接串.只要在你的数据库服务器上建一个空的数据库,建用户,仅此而已.Orchard会在配置过程中自动装载所有的表和数据.

视情况需要,你可以键入一个表前缀\(table prefix\)从而让多个Orchard程序共享同一个数据库但与此同时又让他们的数据是保持独立的.

![](http://docs.orchardproject.net/en/latest/Upload/screenshots_85/setup_sqlserver.png)

在设置界面中还有一个区域可以让你选择一个Orchard配方去建立你的网站.你可以选择以下几种Orchard配方:

* **默认**
  .建立一个经常被使用的Orchard功能的网站.
* **博客**
  .建立一个作为个人博客的网站.
* **核心**
  .建立一个只有Orchard框架用于开发使用的网站.

![](http://docs.orchardproject.net/en/latest/Upload/screenshots/get_started_recipe.png)

更多关于配方的信息以及如何制作一个自定义的配方,可以参考制作一个网站配方.

当你在设置界面输完必要信息之后,点击**完成设置**.设置过程完成后,你新站点的主页就显示出来了.

![](http://docs.orchardproject.net/en/latest/Attachments/Installing-Orchard/first_frontend.png)

现在你可以开始配置你的网站了.

默认情况下,Orchard包含了一个内置的数据库,这样你就可以不用另外再安装一个单独的数据库服务器.然而,如果你自己安装了SQL Server或者SQL Server Express,你可以通过指定数据库连接字符串来指定使用这些数据库.视情况需要,你可以键入一个表前缀\(table prefix\)从而让多个Orchard程序共享同一个数据库但与此同时又让他们的数据是保持独立的.

![](http://docs.orchardproject.net/en/latest/Upload/screenshots_85/setup_sqlserver.png)

在设置界面中还有一个区域可以让你选择一个Orchard配方去建立你的网站.你可以选择以下几种Orchard配方:

* **默认**
  .建立一个经常被使用的Orchard功能的网站.
* **博客**
  .建立一个作为个人博客的网站.
* **核心**
  .建立一个只有Orchard框架用于开发使用的网站.

![](http://docs.orchardproject.net/en/latest/Upload/screenshots/get_started_recipe.png)

更多关于配方的信息以及如何制作一个自定义的配方,可以参考制作一个网站配方.

当你在设置界面输完必要信息之后,点击**完成设置**.设置过程完成后,你新站点的主页就显示出来了.

![](http://docs.orchardproject.net/en/latest/Attachments/Installing-Orchard/first_frontend.png)

现在你可以开始配置你的网站了.

