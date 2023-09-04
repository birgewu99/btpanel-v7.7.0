# btpanel-v7.7.0
btpanel-v7.7.0-backup 

**Centos/Ubuntu/Debian安装命令 独立运行环境（py3.7）**

```Bash
curl -sSO https://raw.githubusercontent.com/birgewu99/btpanel-v7.7.0/main/install/install_panel.sh && bash install_panel.sh
```
移除
```Bash
sed -i "s|if (bind_user == 'True') {|if (bind_user == 'REMOVED') {|g" /www/server/panel/BTPanel/static/js/index.js
```
```Bash
rm -rf /www/server/panel/data/bind.pl
```

直接宝塔文件管理当中，打开目录/www/server/panel/class找到并编辑panelplugin.py文件
使用Ctrl+F搜索并找到softList['list'] = tmpList这段代码，在其下方添加如下代码：

softList['pro'] = 1
        for soft in softList['list']:
            soft['endtime'] = 0

修改完成后重启面板
