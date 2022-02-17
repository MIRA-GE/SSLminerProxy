
安装好之后记得改掉默认的访问端口；文件名是config.yml；用记事本打开更换！linux要改root目录下
SSLminerProxy里的config，不是root目录下的；
linux改好端口之后输入supervisorctl restart all 后生效！

如果之前被攻击过，记得改完web端口之后，还要改下服务器默认的管理端口！！

# 新增加linux服务器一键安装脚本
```bash
bash <(curl -s -L https://raw.githubusercontent.com/MIRA-GE/SSLminerProxy/main/install.sh)

#无法访问github的大陆服务器请使用这个：
bash <(curl -s -L https://cdn.jsdelivr.net/gh/MIRA-GE/SSLminerProxy/install_cdn.sh)

（提示"screen: 未找到命令" 请先安装screen 再安装SSLminerProxy）
```
纯转发模式使用后算力截图，算力几乎无损耗。
![img_9.png](img_9.png)

# 矿工交流 TG电报群：https://t.me/SSLminerProxy 
# QQ群：923469225

SSL请申请一年的免费域名证书（自行百度）申请后下载nginx版本证书，将.crt文件改名cert.crt ，将.key文件改成key.pem

# windows-手动安装
```bash
解压缩后复制到服务器，运行“win守护”然后用浏览器访问 “公网ip:你改好的端口”；密码默认:123456789  进入管理界面 

设置你的转发矿池/端口；可选择“不抽水”(自用) 或者“抽水”(分担服务器费用)；

支持LINUX，WINDOWS服务器，支持纯转发和自定抽水比例；包含自启动和进程守护；

还在被所谓的直连\中转IP抽水吗？自建转发；支持SSL加密；高并发，稳定一键搞定！

（如果遇到打不开管理界面，请开放服务器对应的端口）
```

# Liunx-手动安装
```bash
mkdir SSLminerProxy
cd SSLminerProxy
wget https://raw.githubusercontent.com/MIRA-GE/SSLminerProxy.git 
chmod 777 SSLminerProxy_linux 
nohup ./SSLminerProxy_linux & (后台运行，注意：& 也需要复制，运行完再敲几下回车)
tail -f nohup.out (后台运行时查看)

运行成功后访问 IP:提示的端口 (如：127.0.0.1:提示的端口 注意开放端口；记得修改端口) 进行配置即可。 
```


# 后台运行时关闭

```bash
killall SSLminerProxy_linux
```

### 后台运行时查看
```bash
tail -f nohup.out
```
![img_4.png](img_4.png)
