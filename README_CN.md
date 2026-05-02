<h1 align="center">
  <br>ShellCrash<br>
</h1>




中文 | [English](README.md) 

功能简介：
--

~通过管理脚本在Shell环境下便捷使用Mihomo/Singbox内核<br>
~支持在Shell环境下管理<br>
~支持在线导入订阅及配置链接<br>
~支持配置定时任务，支持配置文件定时更新<br>
~支持在线安装及使用本地网页面板管理内置规则<br>
~支持路由模式、本机模式等多种模式切换<br>
~支持在线更新<br>

设备支持：
--

~支持各种基于OpenWrt或使用OpenWrt二次定制开发的路由器设备<br>
~支持各种运行标准Linux系统（如Debian/CenOS/Armbian等）的设备<br>
~兼容Padavan固件（保守模式）、潘多拉固件以及华硕/梅林固件<br>
~兼容各类使用Linux内核定制开发的各类型设备<br>

——————————<br>
~更多设备支持，请提issue或前往TG群反馈（需提供设备名称及运行uname -a返回的设备核心信息）<br>

## 常见问题：



~**路由设备使用curl安装**：<br>

```shell
#GitHub源(可能需要代理)
export url='https://raw.githubusercontent.com/qq6510/Crash/main' && sh -c "$(curl -kfsSl $url/install.sh)" && source /etc/profile > /dev/null
```

~**路由设备使用wget安装**：<br>

```Shell
#GitHub源(可能需要代理)
export url='https://raw.githubusercontent.com/qq6510/Crash/main' && wget -q --no-check-certificate -O /tmp/install.sh $url/install.sh  && sh /tmp/install.sh && source /etc/profile &> /dev/null
```



### **本地安装：**<br>

如使用在线安装出现问题，请参考：[本地安装ShellCrash的教程 | Juewuy's Blog](https://juewuy.github.io/bdaz) 使用本地安装！<br>

### 使用脚本：<br>

安装完成管理脚本后，执行如下命令使用~

```Shell
crash 		#进入对话
crash -h 	#帮助列表
```

#### **运行时的额外依赖**：<br>

> 大部分的设备/系统都已经预装了以下的大部分依赖，使用时如无影响可以无视之

```shell
curl/wget		必须		全部缺少时无法在线安装及更新，无法使用节点保存功能
iptables/nftables	重要		缺少时只能使用纯净模式
crontab			较低		缺少时无法启用定时任务功能
net-tools		极低		缺少时无法正常检测端口占用
ubus/iproute-doc	极低		缺少时无法正常获取本机host地址
```

