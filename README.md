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
