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

点击接受条款.

![](http://docs.orchardproject.net/en/latest/Upload/screenshots_675/webmatrix_orchard_eula_675.png)

一个新的名为"Orchard CMS"的子文件夹将被添加到"MyWebsites"的文件夹.点击确认.你的Orchard网站将会在WebMatrix中被打开,然后Orchard的设置页面将在浏览器中打开.

在Orchard设置页面上输入关于网站的基本信息.尤其是:站点名称,站点用户名,用户密码,站点数据使用的数据库,还有Orchard配方.

如果你干刚开始使用Orchard,我们建议你选择SQL Compact Server作为数据库并选择默认的配方.输入信息并完成设置.

![](http://docs.orchardproject.net/en/latest/Upload/screenshots/setup_new_site.png)

![](http://docs.orchardproject.net/en/latest/Upload/screenshots_675/webmatrix_finish_setup_675.png)

Orchard建立了初始化网站并在浏览器中打开了站点的主页.你讲会自动以设置中的用户名登录\(在本地中是admin\).此时,点击Dashboard会把你带到可以更改网站内容的Orchard Dashboard.

![](http://docs.orchardproject.net/en/latest/Upload/screenshots_675/new_default_site_675.png)

