# WAX版本安装教程



#### 用法一

嫌麻烦的同学可以直接在github页面右侧的【Releases】处下载最新的打包版本，该版本只支持windows 64位系统，建议在win10系统上运行，把压缩包里的目录解压出来，双击运行【gui.exe】即可，命令行版本可运行【main.exe】，使用命令行版本前需手工修改配置文件【user.yml】

对安全性有要求，喜欢捣鼓代码的，建议从源码运行，根据下面的步骤一步步来

#### 用法二

1. 点击当前页面的【Code】=> git clone 源码到本地，或 Download ZIP 下载源码到本地
2.  下载安装python3 (版本须大于等于python3.7)

    请到python官网下载最新版本： [https://www.python.org/downloads/](https://www.python.org/downloads/)

    【注意】安装时请记得勾选【Add Python 3.10 to PATH】
3. 双击运行 【install\_depends.py】 来安装依赖包，一台电脑只需要安装一次即可 【注意】安装依赖包前请关闭翻墙代理，关闭科学上网，不然无法从豆瓣pypi镜像站下载依赖包
4. 安装Chrome浏览器，并升级到最新版（用当前版本也行，确保和ChromeDriver版本一致）
5. 下载ChromeDriver，版本确保和Chrome版本一致

[https://chromedriver.chromium.org/downloads](https://chromedriver.chromium.org/downloads)

```
比如我的Chrome版本是 97.0.4664.45

那么我就下载 ChromeDriver 97.0.4664.45

其实小版本不一致也没关系，大版本号97一致就行
```

windows系统的话下载【chromedriver\_win32.zip】 6. 将下载的 ChromeDriver 压缩包中的 chromedriver.exe 文件，解压到本项目的源码目录中（和 main.py 在一个目录中） 7. 修改配置文件【user.yml】

1. 复制一份 user.yml.example 文件，改名为 user.yml
2. 按照你的实际情况设置各个参数（修改user.yml推荐使用nodepad++编辑器，下载链接：[点击下载nodepad++编辑器](https://github.com/notepad-plus-plus/notepad-plus-plus/releases/download/v8.2/npp.8.2.Installer.x64.exe)）
3. wax\_account: (wax账号，也就是wax钱包地址,以.wam结尾)
4. proxy: (可设置http代理，格式为127.0.0.1:10809，不需要代理的话设置为null)
5. 下面的（build、mining、chicken、cow、plant、mbs)分别对应建造、采集资源、养鸡、养牛、种地、会员点击，需要程序自动化的操作，设置为true，不需要程序自动化的操作，设置为false，比如你只种地的话，plant: true 即可，其它全部为false，这样减少不必要的网络操作，提高运行效率
6. recover\_energy: 500 (能量不够时恢复到多少能量，默认500，请准备足够的肉，程序不会自动去买肉)
7. 建造、采集资源、养鸡、养牛、种地、会员点击，需要程序自动化的操作，设置为true
8. 其他参数按照你的实际情况设置
9. 修改完配置文件后，双击 【main.py】 运行脚本，程序如果异常退出，可以到 logs 文件夹下查看日志
10. 脚本启动后，会弹出一个Chrome窗口并自动打开 FarmersWorld 官网，第一次启动请手工登录游戏，登录成功后，脚本会开始自动化操作
11. 如果需要手工操作，请勿在脚本打开的Chrome窗口中操作，脚本打开的Chrome窗口，最小化即可，尽量不要动它，需要手工操作的时候，请另开Chrome浏览器登录游戏，该游戏本身就可同时在多个浏览器中登录，不会把脚本Chrome中的游戏T下线
12. 注意，一个账号第一次运行脚本，脚本第一次自动收割农作物的时候，Chrome浏览器中可能会弹出WAX钱包授权窗口，并停在那里不动了，这个时候需要勾选自动确认交易，并同意交易，这样脚本以后就能自动处理了，其实和人工操作是一样的，第一次收割的时候，也要点自动同意交易，否则每次都要弹出授权窗口来，脚本只负责收割农作物，不处理授权的事情，是否自动授权取决于用户账号设置
13. 脚本多开，请把整个源码目录复制一份，在另一个目录中修改配置文件【user.yaml】为另一个账号，双击运行 【main.py】 启动第二个脚本，以此类推，多开互不干扰
14. 正确关闭程序，请点击脚本控制台窗口右上角的X，稍等几秒钟便会关闭，或者点击脚本控制台窗口后，按Ctrl+C，尽量不要直接关闭脚本控制的Chrome窗口，否则webdriver容易产生一些僵尸进程

> ！！！如果因为环境问题双击打不开python文件，可以使用命令行

#### 命令行运行脚本

> 前提是完成上面的步骤，安装好python环境，安装好依赖

打开命令行工具（建议下载cmder命令行工具，下载链接：[点击下载cmder命令行工具](https://github.com/cmderdev/cmder/releases/download/v1.3.18/cmder\_mini.zip)）

进入项目目录（假设项目放在D盘的OpenFarmer目录）

1、在命令行工具输入 D: 【按回车】

2、cd D:/OpenFarmer 【按回车】

（如果未安装依赖，可以先执行 python install\_depends.py ）

3、python main.py 【按回车】（有些环境是py main.py）
