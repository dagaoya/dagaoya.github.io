---
layout: post
title: Sublime Text 3 安装配置
category: others
---
轻量级代码编辑器

---

## 写在前面

无论是前端还是Python，市面上的IDE都较为臃肿，小项目没有必要用那么大型的IDE，所以就用这个编辑器来打造一个小而美的IDE。

我呢，就是用来了解一下Python。

## 正文

目前主流版本是Sublime Text3，在网上可以找到大量的破解版，一些前端技术交流群里面也分享很多同行们使用的集成各自的插件的版本。

自己需求不多，就记录下自己安装Sublime Text3的主要步骤。

1. 官网下载最新的安装包：[http://www.sublimetext.com/3](http://www.sublimetext.com/3)
2. 安装软件，一路默认，安装完成后打开软件，是英文界面。
3. 注册软件

在工具栏中，help --> enter license，在弹窗中输入注册码，注册码失效可以在网上搜索，有时可能要多试几次。
 
```
—– BEGIN LICENSE —–

Michael Barnes Single User License

EA7E-821385

8A353C41 872A0D5C DF9B2950 AFF6F667

C458EA6D 8EA3C286 98D1D650 131A97AB

AA919AEC EF20E143 B361B1E7 4C8B7F04

B085E65E 2F5F5360 8489D422 FB8FC1AA

93F6323C FD7F7544 3F39C318 D95E6480

FCCC7561 8A4A1741 68FA4223 ADCEDE07

200C25BE DBBC4855 C4CFB774 C5EC138C

0FEC1CEF D9DCECEC D3A5DAD1 01316C36

—— END LICENSE ——
```
 

4. 安装 Package Control

在软件中使用快捷键 ctrl + ` (数字键1前面那个)，程序界面下面会显示出Console，复制以下命令粘贴到Console，点击回车键：

Sublime Text3：
```
import urllib.request,os,hashlib; h = 'df21e130d211cfc94d9b0905775a7c0f' + '1e3d39e33b79698005270310898eea76'; pf = 'Package Control.sublime-package'; ipp = sublime.installed_packages_path; urllib.request.install_opener( urllib.request.build_opener( urllib.request.ProxyHandler) ); by = urllib.request.urlopen( 'http://packagecontrol.io/' + pf.replace(' ', '%20')).read; dh = hashlib.sha256(by).hexdigest; print('Error validating download (got %s instead of %s), please try manual install' % (dh, h)) if dh != h else open(os.path.join( ipp, pf), 'wb' ).write(by)
```

安装完成后，在工具栏Preferences下面查找Package Control，如果存在Package Control则说明安装成功。

5. 安装插件以设置语言

为了顺利使用，可以把语言设置为简体中文。

使用快捷键 Ctrl + Shift + P，打开Package Control，输入install，选择Install Package，回车，在输入Chinese，选择ChineseLocalization 插件，该插件将自动安装。安装完成后一般会自动将程序语言切换为简体中文，也可以在帮助（Help）中的Language下选择语言，目前有简体中文、繁体中文、日语、英语可供选择。

6. 安装插件

在网上搜索自己需要的环境的常用插件，我直接查找，按照第4步的方法安装。

我就安装Python的常用插件[百度一下](https://www.baidu.com/s?wd=sublimetext3+python常用插件)

---

## Tips

可以在软件安装完成（第2步）之后直接下载这个插件包，解压到插件的上级目录（替换原先的Sublime Text 3文件夹）。

插件目录在软件内找：菜单->preferences->packages

> 插件包：[SublimeText3plugin.zip]((https://raw.githubusercontent.com/dagaoya/download/master/PC/SublimeText3plugin.zip)


