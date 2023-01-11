# centos7-ShadowsocksR-SSR-
CentOS 7搭建ssr
搭建 ShadowsocksR (SSR) 服务端在 CentOS 7 系统上的过程非常简单。首先，你需要在你的服务器上安装 Python 环境。可以使用以下命令来安装 Python 环境：
yum install python-setuptools && easy_install pip 
然后你可以通过 pip 安装 ShadowsocksR:
pip install shadowsocks
安装完成之后，你就可以创建一个 ShadowsocksR 配置文件，并使用该配置文件来运行 ShadowsocksR 服务端。配置文件可以是 JSON 格式的，如下所示:
Mkdir /path/to/config.json
{
    "server": "服务器ip",
    "server_port": 8388,
    "password": "密码",
    "method": "aes-256-cfb",
    "timeout": 300,
    "fast_open": false
}
最后，你可以使用以下命令来启动 ShadowsocksR 服务端：
ssserver -c /path/to/config.json -d start
