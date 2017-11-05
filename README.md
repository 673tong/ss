======================================================
安装ss
wget --no-check-certificate -O shadowsocks-go.sh https://github.com/673tong/ss/blob/master/shadowsocks-go.sh
chmod +x shadowsocks-go.sh
./shadowsocks-go.sh 2>&1 | tee shadowsocks-go.log

/etc/init.d/shadowsocks status

配置文件路径：vim /etc/shadowsocks/config.json
{
    "port_password":{
         "端口1":"密码",
         "端口2":"密码"

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
