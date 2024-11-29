# [来源链接](https://github.com/XIU2/CloudflareSpeedTest)

# XIU2/CloudflareSpeedTest

[![Go Version](https://img.shields.io/github/go-mod/go-version/XIU2/CloudflareSpeedTest.svg?style=flat-square&label=Go&color=00ADD8&logo=go)](https://github.com/XIU2/CloudflareSpeedTest/)
[![Release Version](https://img.shields.io/github/v/release/XIU2/CloudflareSpeedTest.svg?style=flat-square&label=Release&color=00ADD8&logo=github)](https://github.com/XIU2/CloudflareSpeedTest/releases/latest)
[![GitHub license](https://img.shields.io/github/license/XIU2/CloudflareSpeedTest.svg?style=flat-square&label=License&color=00ADD8&logo=github)](https://github.com/XIU2/CloudflareSpeedTest/)
[![GitHub Star](https://img.shields.io/github/stars/XIU2/CloudflareSpeedTest.svg?style=flat-square&label=Star&color=00ADD8&logo=github)](https://github.com/XIU2/CloudflareSpeedTest/)
[![GitHub Fork](https://img.shields.io/github/forks/XIU2/CloudflareSpeedTest.svg?style=flat-square&label=Fork&color=00ADD8&logo=github)](https://github.com/XIU2/CloudflareSpeedTest/)

国外很多网站都在使用 Cloudflare CDN，但分配给中国内地访客的 IP 并不友好（延迟高、丢包多、速度慢）。  
虽然 Cloudflare 公开了所有 [IP 段](https://www.cloudflare.com/zh-cn/ips/) ，但想要在这么多 IP 中找到适合自己的，怕是要累死，于是就有了这个软件。

**「自选优选 IP」测试 Cloudflare CDN 延迟和速度，获取最快 IP (IPv4+IPv6)**！好用的话**点个`⭐`鼓励一下叭~**

> _分享我其他开源项目：[**TrackersList.com** - 全网热门 BT Tracker 列表！有效提高 BT 下载速度~](https://github.com/XIU2/TrackersListCollection) <img src="https://img.shields.io/github/stars/XIU2/TrackersListCollection.svg?style=flat-square&label=Star&color=4285dd&logo=github" height="16px" />_  
> _[**UserScript** - 🐵 Github 高速下载、知乎增强、自动无缝翻页、护眼模式 等十几个**油猴脚本**~](https://github.com/XIU2/UserScript) <img src="https://img.shields.io/github/stars/XIU2/UserScript.svg?style=flat-square&label=Star&color=4285dd&logo=github" height="16px" />_  
> _[**SNIProxy** - 🧷 自用的简单 SNI Proxy（支持全平台、全系统、前置代理、配置简单等~](https://github.com/XIU2/SNIProxy) <img src="https://img.shields.io/github/stars/XIU2/SNIProxy.svg?style=flat-square&label=Star&color=4285dd&logo=github" height="16px" />_  

> 本项目也支持对**其他 CDN / 网站 IP** 延迟测速（如：[CloudFront](https://github.com/XIU2/CloudflareSpeedTest/discussions/304)、[Gcore](https://github.com/XIU2/CloudflareSpeedTest/discussions/303) CDN），但下载测速需自行寻找地址

> 对于**代理套 Cloudflare CDN** 的用户，须知这应为**备用方案**，而不应该是**唯一方案**，请勿过度依赖 [#382](https://github.com/XIU2/CloudflareSpeedTest/discussions/382) [#383](https://github.com/XIU2/CloudflareSpeedTest/discussions/383)

****
## \# 快速使用

### 下载运行

1. 下载编译好的可执行文件（ [Github Releases](https://github.com/XIU2/CloudflareSpeedTest/releases) / [蓝奏云](https://pan.lanpw.com/b0742hkxe) ）并解压。  
2. 双击运行 `CloudflareST.exe` 文件（Windows 系统），等待测速完成...

<details>
<summary><code><strong>「 点击查看 Linux 系统下的使用示例 」</strong></code></summary>

****

以下命令仅为示例，版本号和文件名请前往 [**Releases**](https://github.com/XIU2/CloudflareSpeedTest/releases) 查看。

``` yaml
# 如果是第一次使用，则建议创建新文件夹（后续更新时，跳过该步骤）
mkdir CloudflareST

# 进入文件夹（后续更新，只需要从这里重复下面的下载、解压命令即可）
cd CloudflareST

# 下载 CloudflareST 压缩包（自行根据需求替换 URL 中 [版本号] 和 [文件名]）
wget -N https://github.com/XIU2/CloudflareSpeedTest/releases/download/v2.2.5/CloudflareST_linux_amd64.tar.gz
# 如果你是在国内网络环境中下载，那么请使用下面这几个镜像加速之一：
# wget -N https://download.scholar.rr.nu/XIU2/CloudflareSpeedTest/releases/download/v2.2.5/CloudflareST_linux_amd64.tar.gz
# wget -N https://ghproxy.cc/https://github.com/XIU2/CloudflareSpeedTest/releases/download/v2.2.5/CloudflareST_linux_amd64.tar.gz
# wget -N https://ghproxy.net/https://github.com/XIU2/CloudflareSpeedTest/releases/download/v2.2.5/CloudflareST_linux_amd64.tar.gz
# wget -N https://gh-proxy.com/https://github.com/XIU2/CloudflareSpeedTest/releases/download/v2.2.5/CloudflareST_linux_amd64.tar.gz
# wget -N https://mirror.ghproxy.com/https://github.com/XIU2/CloudflareSpeedTest/releases/download/v2.2.5/CloudflareST_linux_amd64.tar.gz
# 如果下载失败的话，尝试删除 -N 参数（如果是为了更新，则记得提前删除旧压缩包 rm CloudflareST_linux_amd64.tar.gz ）

# 解压（不需要删除旧文件，会直接覆盖，自行根据需求替换 文件名）
tar -zxf CloudflareST_linux_amd64.tar.gz

# 赋予执行权限
chmod +x CloudflareST

# 运行（不带参数）
./CloudflareST

# 运行（带参数示例）
./CloudflareST -dd -tll 90
```

> 如果平**均延迟非常低**（如 0.xx），则说明 CloudflareST **测速时走了代理**，请先关闭代理软件后再测速。  
> 如果在**路由器**上运行，建议先关闭路由器内的代理（或将其排除），否则测速结果可能会**不准确/无法使用**。

</details>

****

> _在**手机**上独立运行 CloudflareST 测速的简单教程：**[Android](https://github.com/XIU2/CloudflareSpeedTest/discussions/61)、[Android APP](https://github.com/xianshenglu/cloudflare-ip-tester-app)、[IOS](https://github.com/XIU2/CloudflareSpeedTest/discussions/321)**_

> 注意！本软件仅适用于网站，**不支持给 Cloudflare WARP 优选 IP**，具体见：[#392](https://github.com/XIU2/CloudflareSpeedTest/discussions/392)

### 结果示例

测速完毕后，默认会显示**最快的 10 个 IP**，示例：

``` bash
IP 地址           已发送  已接收  丢包率  平均延迟  下载速度 (MB/s)
104.27.200.69     4       4       0.00    146.23    28.64
172.67.60.78      4       4       0.00    139.82    15.02
104.25.140.153    4       4       0.00    146.49    14.90
104.27.192.65     4       4       0.00    140.28    14.07
172.67.62.214     4       4       0.00    139.29    12.71
104.27.207.5      4       4       0.00    145.92    11.95
172.67.54.193     4       4       0.00    146.71    11.55
104.22.66.8       4       4       0.00    147.42    11.11
104.27.197.63     4       4       0.00    131.29    10.26
172.67.58.91      4       4       0.00    140.19    9.14
...

# 如果平均延迟非常低（如 0.xx），则说明 CloudflareST 测速时走了代理，请先关闭代理软件后再测速。
# 如果在路由器上运行，请先关闭路由器内的代理（或将其排除），否则测速结果可能会不准确/无法使用。

# 因为每次测速都是在每个 IP 段中随机 IP，所以每次的测速结果都不可能相同，这是正常的！

# 注意！我发现电脑开机后第一次测速延迟会明显偏高（手动 TCPing 也一样），后续测速都正常
# 因此建议大家开机后第一次正式测速前，先随便测几个 IP（无需等待延迟测速完成，只要进度条动了就可以直接关了）

# 软件在 默认参数 下的整个流程大概步骤：
# 1. 延迟测速（默认 TCPing 模式，HTTPing 模式需要手动加上参数）
# 2. 延迟排序（延迟 从低到高 排序并按条件过滤，不同丢包率会分开排序，因此可能会有一些延迟低但丢包的 IP 排到后面）
# 3. 下载测速（从延迟最低的 IP 开始依次下载测速，默认测够 10 个就会停止）
# 4. 速度排序（速度从高到低排序）
# 5. 输出结果（通过参数控制是否输出到命令行(-p 0)或输出到文件(-o "")）

# 注意：输出的结果文件 result.csv 通过微软 Excel 表格打开会中文乱码，这是正常的，其他表格软件/记事本都显示正常
```

测速结果第一行就是**既下载速度最快、又平均延迟最低的最快 IP**！

完整结果保存在当前目录下的 `result.csv` 文件中，用**记事本/表格软件**打开，格式如下：

```
IP 地址, 已发送, 已接收, 丢包率, 平均延迟, 下载速度 (MB/s)
104.27.200.69,4,4,0.00,146.23,28.64
```

> _大家可以按自己需求，对完整结果**进一步筛选处理**，或者去看一看进阶使用**指定过滤条件**！_

****
## \# 进阶使用

直接运行使用的是默认参数，如果想要测速结果更全面、更符合自己的要求，可以自定义参数。

```css
C:\>CloudflareST.exe -h

****

## 感谢项目

- _https://github.com/Spedoske/CloudflareScanner_

> _因为该项目已经很长时间没更新了，而我又产生了很多功能需求，所以我临时学了下 Go 语言就上手了（菜）..._  
> _本软件基于该项目制作，但**已添加大量功能及修复 BUG**，并根据大家的使用反馈积极添加、优化功能（闲）..._

****

## 手动编译

<details>
<summary><code><strong>「 点击展开 查看内容 」</strong></code></summary>

****

为了方便，我是在编译的时候将版本号写入代码中的 version 变量，因此你手动编译时，需要像下面这样在 `go build` 命令后面加上 `-ldflags` 参数来指定版本号：

```bash
go build -ldflags "-s -w -X main.version=v2.3.3"
# 在 CloudflareSpeedTest 目录中通过命令行（例如 CMD、Bat 脚本）运行该命令，即可编译一个可在和当前设备同样系统、位数、架构的环境下运行的二进制程序（Go 会自动检测你的系统位数、架构）且版本号为 v2.3.3
```

如果想要在 Windows 64位系统下编译**其他系统、架构、位数**，那么需要指定 **GOOS** 和 **GOARCH** 变量。

例如在 Windows 系统下编译一个适用于 **Linux 系统 amd 架构 64 位**的二进制程序：

```bat
SET GOOS=linux
SET GOARCH=amd64
go build -ldflags "-s -w -X main.version=v2.3.3"
```

例如在 Linux 系统下编译一个适用于 **Windows 系统 amd 架构 32 位**的二进制程序：

```bash
GOOS=windows
GOARCH=386
go build -ldflags "-s -w -X main.version=v2.3.3"
```

> 可以运行 `go tool dist list` 来查看当前 Go 版本支持编译哪些组合。

****

当然，为了方便批量编译，我会专门指定一个变量为版本号，后续编译直接调用该版本号变量即可。  
同时，批量编译的话，还需要分开放到不同文件夹才行（或者文件名不同），需要加上 `-o` 参数指定。

```bat
:: Windows 系统下是这样：
SET version=v2.3.3
SET GOOS=linux
SET GOARCH=amd64
go build -o Releases\CloudflareST_linux_amd64\CloudflareST -ldflags "-s -w -X main.version=%version%"
```

```bash
# Linux 系统下是这样：
version=v2.3.3
GOOS=windows
GOARCH=386
go build -o Releases/CloudflareST_windows_386/CloudflareST.exe -ldflags "-s -w -X main.version=${version}"
```

</details>

****

## License

The GPL-3.0 License.
