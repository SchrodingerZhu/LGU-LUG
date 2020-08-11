# Linux 101: Choose A Linux Distro 4 Great Fun

Linux可以算是 CSE LGUer 的必备技能了。如果你在实验室搬砖或是上过 CSC3150，CSC4005 这些必修的课程，你应当或多或少的都使用过一些 Linux 的发行版。在LGU 最流行的 Distro 应该是 Ubuntu 了，但是 Linux 的精彩世界原不止于 Ubuntu，如果想要了解更多常用的发行版，或是想要为自己选择一个桌面操作系统，不妨来阅读一下这篇文章里的讨论。

严格意义上，Linux 是由 Linus 开发的操作系统内核，单独的 Linux Kernel 谈不上真正意义上的操作系统；在此基础上，GNU Project 为 Linux 开发了一系列关键的工具和应用，进而组成了最基础的 Linux 系统。今日我们所说的 Linux 系统，实际上是指 GNU/Linux。从这里我们就可以看出，Linux 内核和周边的开发是分开的，这与 FreeBSD 等操作系统的管理模式截然不同，也为 Linux 拥有如此多样的发行版奠定了基础。

Linux 发行版多样性另一个原因是不通开发群体对系统持有不同的理念，比如一些人更倾向于各种 old-school 的配置和文件组织方式，另一些人则喜欢比较激进的修改；一些发行版更看中 server，而另一些则把注意力集中在 desktop. 下面，我们就来对比一些常见的 Distros：

## Debian: 自由的社会契约

<img height=100 src="https://i.imgur.com/yYcnXqv.png"></img>

Debian 是一款由社区推动开发的 Linux 发行版，在 Linux 家族中算得上元老。Debian 一向倡导自主，原生的开发，并制定了 `Debian Social Constract` 作为指导。 从 0.93 版本开始，Debian 引入了著名的`.deb` 格式的软件包，如果你使用过黑苹果，你可能已经接触过这一格式。时至今日，这一软件包格式仍是最受欢迎的格式之一。很多国外知名软件以及网易云，WPS 等一系列国产软件都提供了官方版的`.deb`软件包。后面将要讲到的 Ubuntu 和 Deepin 都可以算是基于 Debian 进行二次开发的衍生版本，因此也沿用了很多 Debian 的特性。但是，Debian 本身的目标和 Ubuntu以及 Deepin 很不一样，默认的分发版本中没有那么多图形化的辅助功能，稳定版本的 package 相对老旧。这些特性为服务器创造了更稳定，更轻量的运行环境，但也为新手入门造成了一些额外的负担。

Deb 包系列常用的包管理器是`apt`，经过多个版本的迭代，`apt`已经变得越来越智能。和很多其它包管理器一样，`apt` 能够比较智能地处理各种依赖关系，这使得它使用起来比较方便。

```plaintext
apt moo
         (__) 
         (oo) 
   /------\/ 
  / |    ||   
 *  /\---/\ 
    ~~   ~~   
...."Have you mooed today?"...
```
但是，当一个包存在多个版本时，`deb` 系列常见的行为是加一个版本后缀，比如：

- `gcc-7`
- `gcc-8`
- `gcc-9`

就代表了三个不同版本的 GNU 编译器，在一些比较特殊的场合，这样的命名方式可能会产生一定的问题。

另外一点就是前面说到的稳定版本更新比较保守的问题，这意味着一些 Geeks 不能在第一时间体验新的特性。

## Ubuntu：开箱即用的傻瓜操作系统

<img height=50 src="https://i.imgur.com/sEsYpq5.png"></img>

Ubuntu 绝对是最广为认知的发行版之一，以极高的易用性和用户友好著名。它基于 Debian，但相对 Debian 增加了大量图形化工具（例如图形化的 Live CD 、安装程序和软件中心），使新手在几乎没有 Linux 知识的情况下也可以方便地进行安装、使用、更新等操作。由于系统安装时预置图形化桌面，同时预装了大量生产力工具（例如浏览器 Firefox、音乐播放器 RhythmBox 和办公套件 LibreOffice 等），Ubuntu 系统在自动安装完成后就可以立即投入使用，省去费神费力的大量系统基础配置过程。同时，其大量的用户基数也使得关于 Ubuntu 的文章和问题数量远高于其它发行版，因此，使用时发生的许多问题都可以在互联网上找到前人留下的现成解决方案。在软件数量上，Ubuntu 也不输其它发行版：用户可以通过 PPA 方便地安装和更新不在官方软件源中的软件包。

同时，Ubuntu 因为一些较为激进的更改（例如 snap 及 cloud-init）提高了用户的使用和维护难度而受到广泛批评。

亦有基于不同桌面和/或不同使用需求打造的基于 Ubuntu 的衍生发行版，例如：
* 使用 KDE 桌面的 Kubuntu
* 使用 Xfce 桌面的 Xubuntu
* 为创作特别打造的 Ubuntu Studio


## Deepin： 国产之光

<img height=100 src="https://i.imgur.com/rAWpFh2.png"></img>

Deepin 由武汉深之度公司开发和维护的。自带的 DDE 桌面环境在国内外取得了广泛好评。

<iframe src="//player.bilibili.com/player.html?aid=59860590&bvid=BV1Nt411n7E8&cid=104264193&page=1" scrolling="no" border="0" frameborder="no" framespacing="0" allowfullscreen="true"> </iframe>

最新版的 Deepin 基于 Debian 稳定版，软件版本比较旧，但非常稳定。Deepin 本身和国内很多厂商由合作，所以对 WPS 等国产办公软件有着最为优秀的支持。对于 QQ 等没有能用的官方 Linux 支持度软件，深度也专门调试了 wine 版本，支持效果非常好。

如果你是 Linux 的新手，且离不开国内常见的 IM 工具，可以考虑一下 Deepin.


## Arch Linux：论以用户为中心

<img height=100 src="https://i.imgur.com/rZTr2tw.png"></img>

> BTW I use Arch.

Arch Linux 可以说是在 meme 领域最出名的发行版之一：由于 Arch Linux 提供给用户的便利实在太少，很多工作都需要用户自己做，安装和使用 Arch Linux 已经在某种程度上成为了一个能用来炫耀的成就，而在和人谈话时顺便加一句「我用 Arch Linux」就会让谈话者觉得自己高人一等（这也是 Arch 用户有时候不受其它用户欢迎的原因之一）。

本文提到的大多数发行版，都会提供图形界面或命令行界面帮用户进行系统配置，或者至少给用户一个界面配置网络连接；Arch Linux 不是这样。Arch Linux 的 Live CD 启动后，留给用户的只有一个空旷的终端界面 (tty)，想连接网络？自己去写网络配置；想给硬盘分区？自己去用 gdisk（只有命令行界面唷）；想设置时区？自己去做软链接...总而言之，「自己动手丰衣足食」。不过，较高的门槛也使得 Arch Linux 的用户平均水平较高，社群氛围较其它发行版略好一筹。

Arch Linux 的基本哲学之一是「用户中心」(User centrality)。这个「用户中心」，指的不是 Ubuntu 的「用户友好」，而是



## Manjaro：自由与妥协

<img height=100 src="https://i.imgur.com/Df4hGf1.png"></img>

## OpenSUSE：风滚草与蜥蜴

<img height=100 src="https://i.imgur.com/xyjoLbw.png"></img>

OpenSUSE 也是一款有强大公司做后盾的发行版，采用`rpm`打包格式。自带的`zypper`包管理器采用了非常先进的算法和并提供了优秀的交互体验。

但 OpenSUSE 最为称道的是它强大的图形化管理系统，防火墙，局域网，类似于注册表的环境配置，包管理，磁盘快照，在 YaST2 管理中心里应有尽有。这些功能都是开箱即用的。OpenSUSE提供了4GiB的安装镜像，使用它你可以高度定制你的系统，甚至不需要在安装后再做调整。如果你使用默认的根分区格式（Btrfs），快照功能就会自动启用，这样，如果你某次更新产生了意外，可以很方便的恢复。

OpenSUSE提供了两种发行方式：周期更新和滚动更新（Tumbleweed 风滚草），两者的稳定性都还可以。

作为欧洲的发行版，OpenSUSE的打包受到限制，因此专有驱动和一些专利相关的软件不能包含在官方源中，但是社区提供了`packman`软件源来绕过这些限制。另外，OpenSUSE 提供了类似于 AUR 的软件托管平台 OBS，使得用户可以较为方便的获得第三方软件包 （OBS 没有国内镜像）。

OpenSUSE的后台公司是 KDE 的上游贡献者，所以 OpenSUSE 自带的 KDE 桌面环境有很好的优化和美化。


## Fedora：礼帽与小白鼠

<img height=100 src="https://i.imgur.com/1tSHY7Y.png"></img>

很多人会把用 Fedora 的人说成小白鼠，这是因为 Fedora 很像是 Redhat 新技术的试验场。很多激进的功能都是先引入 Fedora，经过测试后再引入到红色帽的企业系统和 CentOS。和 OpenSUSE 一样 Fedora 也使用 `rpm` 包格式，包管理器则经历了`yum`到`dnf`的换代。现任的包管理器能够良好的处理依赖和冲突，也提供了一些比较 fancy 的功能，比如：

- 模块化软件包：把一些存在冲突的软件包作为可选模块。比如，按照需求你可以启用`postgresql-10`或是`postgresql-11`，这样就在一定程度上解决了冲突
- COPR: 相当于 Arch 的 AUR，Ubuntu 的 PPA。

Fedora 稳定版虽然引入了各式各样的崭新功能，但是日常使用的稳定性是有保障的。而且 Fedora 的发行模式也不是滚动更新 （Rawhide版本除外），所以这里小白鼠和不稳定并不能完全挂钩。所以，如果你想要体验前沿的 Linux 功能（高级的tracing等等），Fedora实际上是一个很好的选择。

红帽是 Plymouth 和 GDM 等软件的积极维护者，因此在美工和品味方面，Fedora 也是不错的。

在安全性方面，Fedora默认开启了 SELinux 和 firewalld，这为配置服务器环境带来了一定的麻烦。


## Gentoo：原教旨主义者

<img height=100 src="https://i.imgur.com/01wUhpS.png"></img>

Gentoo 和 Arch 一样没有图形化的安装界面，一切配置都需要用户自己去做。不同于 Arch 的是，Gentoo 更加倾向于使用 BSD 风格的 ports 软件管理方式，除了二进制分发以外，Gentoo 提供了大量官方维护的源码供用户本地编译安装，从而更好地定制和优化。但是这样也就需要更多的深入了解和更加强大的硬件。

一些 old-school 的人可能会比较喜欢这个发行版，因为它高度可定制，可以自选 init，很好地保持 KISS 原则。


## NixOS：激进的无状态发行版

<img height=100 src="https://i.imgur.com/i3oybAx.png"></img>

每次重装 Linux 时人们或多或少的都需要重新配置一下环境，每到这个时候人们总想要一个自动化的工具来帮他们完成任务。而 NixOS 的出现就解决了这个问题。理论上，NixOS 的所有配置都可以用 Nix 函数式语言来完成，只要配置文件一致，Nix 就可以帮你创造一个完全一致的操作系统环境。更近一步，当你升级软件时，实际上是对整个系统进行了一次 rebuild ，而 Nix 默认是保留每一次 build 的，这样如果更新产生了非期待结果，你就可以回退到上一个版本

前面说到，不同的包管理器在处理版本问题上有着不同的方式，而 Nix 的做法可谓是别具一格了，每一个软件版本都对应在不同的沙盒里，那么如果`X`依赖`A v2.0`， `Y`依赖`A v3.0`, 他们也可以和平的共处了。当然，代价肯定是有的：

1. 更多的空间占用
2. 不标准的文件组织

对于问题1，Nix 本身一些优化工具来尽可能的减少重复文件；但问题2解决起来可能有些棘手。举个例子，很多时候，你在网上找到了一个 shell 脚本，第一行可能是这么写的：
```bash
#!/bin/bash
```
这个标注意味着这个脚本应该被`/bin/bash`执行。但是 Nix 上的大部分文件都在`/nix/store`里面，上面的写法就会产生问题。当然，开发者如果使用
```bash
#!/usr/bin/env bash
```
这样的写法就可以极大的提高兼容性，但是大部分人可能都不会注意到传统写法可能存在的问题，这就使得很多软件在 Nix 上不是开箱即用的，你需要根据自己的需求进行再打包。

由于特殊的软件分发方式，NixOS 目前没有有效的国内镜像；官方源使用 fastly CDN，在大陆速度很差，使用时需注意。

## CentOS：Server 主力

<img height=100 src="https://i.imgur.com/dM3OIUA.png"></img>


## Qubes OS：安全第一

<img height=100 src="https://i.imgur.com/uF8maUA.png"></img>

Android 和 iOS 的一个重要的安全特性，就是把每个应用程序放在一个沙箱中运行。这可以使各个应用程序不互相干扰，从而提高系统的安全性。那么桌面系统上呢？其实早在 2012 年，一个叫做 Qubes OS 的发行版就实现了类似的功能。在 Qubes OS 中，程序运行在互相隔离的虚拟机中。即使其中一个虚拟机被入侵，余下的虚拟机也不受影响。这个机制带来的另一个特点是，用户在其中不仅可以运行 Linux 发行版，还可以运行 Windows。多虚拟机的代价是性能和兼容性的牺牲，不过对于那些追求「没有最安全，只有更安全」的用户来说，只要安全性有提升，什么代价都是值得的。

Qubes OS 使用的 `Xen` 架构，为了保证安全，`Dom 0` 的内核保持在比较旧的版本，如果你想从事内核开发，Qubes 不是一个最佳选项。很多安全问题都是由`driiver`引起的，为了隔离这些问题，Qubes 使用了一个专门的虚拟化区域来处理设备连接和网络，但是兼容性存在较大的问题。`Nvidia`的私有显卡驱动是被社区认为是不安全的，因此`Qubes`社区没有去做太多的支持（官方现有安装教程已经`broken`）。


## 其它

### 实验类

#### Tiny Core Linux

#### Tails

#### Linux from Scratch (LFS)

#### Bedrock

### 容器类

#### Alpine Linux