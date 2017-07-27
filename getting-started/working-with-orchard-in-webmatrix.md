# 在WebMatrix中使用Orchard

[WebMatrix](http://www.microsoft.com/web/webmatrix/)是微软的一站式网页开发工具,能够通过让你空前简单的建立,编辑和发布网站.WebMatrix包含了一个内置的网站服务器\(IIS Express\)和一个用来编辑和客制化像Orchard这样的应用的编辑器.当你用Web Platform Installer 安装Orchard时,你可以选择安装WebMatrix用来替代IIS.

## 安装和启动WebMatrix

下载安装并启动Microsoft [Web Platform Installer](https://www.microsoft.com/web/downloads/platform.aspx),然后点击安装Microsoft WebMatrix.

![](http://docs.orchardproject.net/en/latest/Upload/screenshots/install_selectorWebMatrix.png)

接受许可条款并在安装完成后启动WebMatrix.

## 使用WebMatrix创建一个Orchard网站

在WebMatrix的启动页点击**App Gallery**从而创建一个Orchard网站.

![](http://docs.orchardproject.net/en/latest/Upload/screenshots_675/webmatrix_start_675.png)

找到**Orchard CMS**.输入一个名称作为站点的文件夹名称.例如,如果输入网站名称"Orchard CMS","Document/My Websites/Orchard CMS"的文件夹将会被建立.点击**下一步**.

![](http://docs.orchardproject.net/en/latest/Upload/screenshots_675/webmatrix_select_orchard_675.png)

点击接受**条款**.

![](http://docs.orchardproject.net/en/latest/Upload/screenshots_675/webmatrix_orchard_eula_675.png)

一个新的名为"Orchard CMS"的子文件夹将被添加到"MyWebsites"的文件夹.点击确认.你的Orchard网站将会在WebMatrix中被打开,然后Orchard的设置页面将在浏览器中打开.

在Orchard设置页面上输入关于网站的基本信息.尤其是:站点名称,站点用户名,用户密码,站点数据使用的数据库,还有Orchard配方.

如果你干刚开始使用Orchard,我们建议你选择SQL Compact Server作为数据库并选择默认的配方.输入信息并完成设置.

![](http://docs.orchardproject.net/en/latest/Upload/screenshots/setup_new_site.png)

![](http://docs.orchardproject.net/en/latest/Upload/screenshots_675/webmatrix_finish_setup_675.png)

Orchard建立了初始化网站并在浏览器中打开了站点的主页.你讲会自动以设置中的用户名登录\(在本地中是admin\).此时,点击Dashboard会把你带到可以更改网站内容的Orchard Dashboard.

![](http://docs.orchardproject.net/en/latest/Upload/screenshots_675/new_default_site_675.png)

## 通过WebMatrix运行你的网站

在任何时候,你都可以在WebMatrix中通过点击项目结点并运行你的网站.

![](http://docs.orchardproject.net/en/latest/Upload/screenshots/webmatrix_run.png)

## 处理你的文件

你可以使用WebMatrix编辑Orchard中的文件.WebMatrix提供了一个简单的编辑器涵盖了HTML着色, CSS, JavaScript, 和代码文件.

虽然WebMatrix没有提供一套用来编译代码的机制,但是Orchard自身提供了在代码被编辑时的动态编译.更多信息可以参考Orchard动态编译.

![](http://docs.orchardproject.net/en/latest/Upload/screenshots_675/webmatrix_files_675.png)

你可以通过以下[指导](http://sybak.com/blog/2011/02/changing-the-file-types-that-open-with-webmatrix/)改变WebMatrix编辑器.

比如,你可能会发现XML编辑器\(可以自动着色\)去处理`Palcement.info`文件比较有用.为了这样做在WebMatrix文件`filetypes.xml`中你必须改变`.info`文件的设置\(你可以在以下目录中找到\)

> `32-bit machines: C:\Program Files\Microsoft WebMatrix\config\filetypes.xml`
>
> `64-bit machines: C:\Program Files (x86)\Microsoft WebMatrix\config\filetypes.xml`

1\)在XML文件类型中加入`.info`文件后缀

```XML
<FileType extension=".info;.config;.csproj;.vbproj;.resx;.settings;.sitemap;.user;.wsdl;.browser;.xaml;.xml;.xoml;.xsd;.xsl;.xslt;.mxml;.dbml;.wstemplate">
    <OpenAs>XML</OpenAs>
    <TabColor>Yellow</TabColor>
    <Icon>XMLFileIcon</Icon>
    <EmitUtf8BomByDefault>True</EmitUtf8BomByDefault>
    <Description>An XML File</Description>
</FileType>
```

2\)在文本文件类型中移除`.info`文件后缀

```XML
<FileType extension=".ashx;.export;.po;.blogtemplate;.yml;.yaml;.manifest;.pl;.json;.csv">
    <OpenAs>Text</OpenAs>
    <TabColor>Gray</TabColor>
    <Icon>DefaultFileIcon</Icon>
    <EmitUtf8BomByDefault>False</EmitUtf8BomByDefault>
    <Description>Unknown file type</Description>
</FileType>
```

3\)重启WebMatrix使改变生效.

## 处理数据库

如果你在Orchard设置时选择了将**SQL Server Compact**作为数据库,你可以在WebMatri中通过选择**Databases**去打开**Orchard.sdf**数据库.

![](http://docs.orchardproject.net/en/latest/Upload/screenshots_675/webmatrix_opendatabase_675.png)

一旦数据库窗口被打开之后,你可以在浏览区域通过选择表来看见表中的内容.

![](http://docs.orchardproject.net/en/latest/Upload/screenshots_675/webmatrix_databasetable_675.png)

\(如果你已经在**Databases**工作空间,你可以右击Orchard结点然后点击**刷新**来显示数据库和表.\)

![](http://docs.orchardproject.net/en/latest/Upload/screenshots_675/webmatrix_database_refresh_675.png)

发布你的网站

当你准备好将本地的网站备份上传到Internet时,你可以点击WebMatrix工具栏的**发布**按钮.

![](http://docs.orchardproject.net/en/latest/Upload/screenshots/webmatrix_publish.png)

你第一次发布时,**发布你的站点**对话框会显示.

![](http://docs.orchardproject.net/en/latest/Upload/screenshots_675/webmatrix_publish_firsttime_675.png)

要发布一个网站,你必须要有一个主机商的帐号.如果你还没有的话,你可以选择**Get Started with Windows Azure** 或 **Find Windows Web Hosting**.如果你选择Windows Azure,你将会选择将你的网站建立为Azure Websit或者Azure Web Role.

![](http://docs.orchardproject.net/en/latest/Upload/screenshots_675/webmatrix_AzurePortal_675.png)

在你创建了一个主机商的帐号之后,供应商会给你发送一封关于你的用户名,主机名和其他相关信息的邮件.为了节省你手动操作相关信息的步骤,你还会收到一个包含这些信息"Profile XML"文件\(以`.publishsettings`后缀为名\)你可以用过导入发布配置文件.你也可以手动完成这些信息设置.

![](http://docs.orchardproject.net/en/latest/Upload/screenshots_675/webmatrix_import_settings_675.png)

在你完成发布站点之后,你可能想要做一些修改并重新发布.在你接下来的**发布**中,WebMatrix会列出自上次发布之后被修改的文件.这时候你可以选择哪些想被上传然后选择**继续**或**取消**.

![](http://docs.orchardproject.net/en/latest/Upload/screenshots_675/webmatrix_publish_preview_675.png)

一旦你发布了你的网站,你可以通过**Remote View**功能去查看远程站点的文件

![](http://docs.orchardproject.net/en/latest/Upload/screenshots_675/webmatrix_remote_view_675.png)

更多关于使用WebMatrix发布网站的信息可以点击[这里](https://www.microsoft.com/web/post/how-to-publish-a-web-application-using-webmatrix).

## Change History

Updates for Orchard 1.6

11-14-12: Updated screens and workflow.

