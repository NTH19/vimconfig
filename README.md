# ArchVim

小彭老师的个人 Vim 插件和配置整合包（也支持 NeoVim）。

## 一键安装

从 [GitHub release](https://github.com/archibate/vimrc/releases) 下载 `vimrc-install.sh`。

为了提升速度，国内用户也可以从 [Gitee 的镜像](https://gitee.com/archibate/vimrc/releases) 下载。

直接运行这个脚本： `bash vimrc-install.sh`

他会花一些时间检测你的 Linux 发行版，并安装下列这些部分插件所需的包：

> ripgrep, ccls, nodejs (12.x 及以上)

... 并安装所有插件。安装完成后, 运行 `vim` 开始畅玩吧。

目前支持的 Linux 发行版有：

- Arch Linux (测过)
- Manjano Linux (没测)
- Ubuntu (只测了 20.04)
- Debian (没测)
- Kali Linux (没测)
- Raspbian (没测)
- MacOS (感谢 @RakerZh)
- Fedora (感谢 @justiceeem)
- OpenSUSE (感谢 @sleeplessai)
- CentOS (感谢 @xxy-im)
- Deepin (感谢 @zhangasia)

如果是其他发行版（比如 CentOS），会默认从源码安装 fzf 和 ripgrep（很慢）。

## 参与贡献

如果你知道如何在你的 Linux 发行版上安装这些包（或者你是 MacOS、Windows），你可以通过修改这个仓库
中的 [.vim/install.sh](.vim/install.sh) 来贡献你的力量，并通过 PR 提交更改给我们。

要测试的话，先运行 [.vim/package.sh](.vim/package.sh) 来生成一键安装脚本 `vimrc-install.sh`。
然后用 Docker 等工具在相应的隔离环境中测试是否能正确安装。

## 手动安装（不推荐）

手动安装方法见 [.vim/init.vim](.vim/init.vim) 中的注释。

# NeoVim 用户

使用 NeoVim 的用户，请创建一个文件 `~/.config/nvim/init.vim`，内容如下：

```vim
set runtimepath^=~/.vim runtimepath+=~/.vim/after
let &packpath = &runtimepath
source ~/.vimrc
```
