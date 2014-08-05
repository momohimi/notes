# Sublime TexT 3 使用记录

## 安装Sublime Text 3

下载地址：[http://www.sublimetext.com/3][1]


----------


## 安装Pack Control

使用**Ctrl+`快捷键**或者**通过View->Show Console菜单**打开命令行，粘贴如下代码：

    import urllib.request,os; pf = 'Package Control.sublime-package'; ipp = sublime.installed_packages_path(); urllib.request.install_opener( urllib.request.build_opener( urllib.request.ProxyHandler()) ); open(os.path.join(ipp, pf), 'wb').write(urllib.request.urlopen( 'http://sublime.wbond.net/' + pf.replace(' ','%20')).read())


----------


## 推荐插件

 - [Emmet][2]
    Emmet is a plugin for many popular text editors which greatly improves HTML & CSS workflow.
    前身是zen conding，提升HTML&CSS开发效率。

 - [SidebarEnhancements][3]
    Provides enhancements to the operations on Sidebar of Files and Folders for Sublime Text.
    增加侧边栏右键菜单功能。

 - [Git][4]
    Git integration: it's pretty handy. Who knew, right?
    Git，大家都懂的。

 - [CSScomb][5]
    Make your css beautiful.
    CSS属性进行排序的格式化插件，让css更美。
 
 - [DocBlockr][6]
    Simplifies writing DocBlock comments in Javascript, PHP, CoffeeScript, Actionscript, C & C++.
    轻松的生成代码注释

 - [主题：Afterglow][7]
    个人喜欢

  [1]: http://www.sublimetext.com/3
  [2]: http://emmet.io/
  [3]: https://github.com/titoBouzout/SideBarEnhancements/tree/st3
  [4]: https://github.com/kemayo/sublime-text-git
  [5]: http://csscomb.com/
  [6]: https://github.com/spadgos/sublime-jsdocs
  [7]: https://github.com/YabataDesign/afterglow-theme
