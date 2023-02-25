# fragment

## XDG
[XDG Base Directory Specification](https://specifications.freedesktop.org/basedir-spec/latest/index.html)

[Linux 基本目录规范 XDG](https://winddoing.github.io/post/ef694e1f.html)

## Homebrew
#### 术语
- Formulae：软件包，包括了这个软件的依赖、源码位置及编译方法等；
- Casks：已经编译好的应用包，如图形界面程序等。
#### Homebrew提供了两种安装软件的方式
1. brew install

&emsp;brew是下载源码解压，然后./configure && make install，同时会包含相关依赖库，然后放在统一的目录中（/usr/local/Cellar）并自动配置各种环境变量。

2. brew cask install

&emsp;brew cask是针对已经编译好了的应用包（.dmg/.pkg）下载解压，然后放在统一的目录中（/usr/local/Caskroom），省掉了自己下载、解压、安装等步骤。

简单来说，`brew install` 用来安装一些不带界面的命令行工具和第三方库。`brew cask install`用来安装一些带界面的应用软件。

常用brew命令：
~~~markdown
brew update               # 更新brew版本
brew list                 # 本地已安装软件库列表
brew search xxx           # 查找软件包
brew install xxx          # 安装软件包
brew uninstall xxx
brew cask install xxx     # 安装软件
brew cask uninstall xxx
~~~

&emsp;brew还会创建自己的缓存目录$HOME/Library/Caches/Homebrew，brew会将其作为资源下载的缓存目录。与
