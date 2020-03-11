## 安装

```
git clone https://github.com/xuds029/linux_ssr_install.git    // 下载安装脚本
cd linux_ssr_install
cp ssr /usr/local/bin/
chmod +x /usr/local/bin/ssr
ssr install   // 安装
```

## 配置文件
```
[root@localhost ~]# ssr config 		// 配置文件路径 /usr/local/share/shadowsocksr/config.json
{
    "server": "0..0.0.0",	// ssr服务器ip
    "server_ipv6": "::",
    "server_port": 8080,	// ssr服务器端口
    "local_address": "127.0.0.1",
    "local_port": 1080,

    "password": "123456",		// 对应password
    "method": "none",			// 这里对应SSGlobal配置中的Encryption
    "protocol": "auth_chain_a",		//对应protocl
    "protocol_param": "",
    "obfs": "http_simple",		//对应obfs
    "obfs_param": "hello.world",	//对应obfs_param
    "speed_limit_per_con": 0,
    "speed_limit_per_user": 0,

    "additional_ports" : {}, // only works under multi-user mode
    "additional_ports_only" : false, // only works under multi-user mode
    "timeout": 120,
    "udp_timeout": 60,
    "dns_ipv6": false,
    "connect_verbose_info": 0,
    "redirect": "",
    "fast_open": false
}
```


## 启动/关闭
```
ssr start
ssr stop
```

## 卸载
```
ssr uninstall 
```
