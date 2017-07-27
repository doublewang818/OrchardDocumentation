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

