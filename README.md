# ss
======================================================
安装ss
wget --no-check-certificate -O shadowsocks-go.sh https://raw.githubusercontent.com/teddysun/shadowsocks_install/master/shadowsocks-go.sh
chmod +x shadowsocks-go.sh
./shadowsocks-go.sh 2>&1 | tee shadowsocks-go.log

/etc/init.d/shadowsocks status

配置文件路径：vim /etc/shadowsocks/config.json
{
    "port_password":{
         "7373":"ss73tong",
         "1567":"73tong",
         "8899":"lijinhui",
         "5473":"73tong",
		 "5411":"yanjian"
    },
    "method":"aes-256-cfb",
    "timeout":600
}

多用户
配置文件路径：vim /etc/shadowsocks/config.json
{
    "port_password":{
         "8989":"qwerasdf",
         "7373":"73tong",
         "6666":"lijinhui"        	
    },
    "method":"aes-256-cfb",
    "timeout":600
}

使用命令：
启动：/etc/init.d/shadowsocks start
停止：/etc/init.d/shadowsocks stop
重启：/etc/init.d/shadowsocks restart
状态：/etc/init.d/shadowsocks status
======================================================
