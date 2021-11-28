# xrdp-ubuntu

```
sudo apt-get update
```

```
sudo apt install xrdp
```

```
sudo apt install xserver-xorg-core
```

```
sudo apt install xorgxrdp
```

```
sudo nano /etc/polkit-1/localauthority.conf.d/01-allow-colrd.conf
```

```
polkit.addRule(function(action, subject) {
if ((action.id == “org.freedesktop.color-manager.create-device” || action.id == “org.freedesktop.color-manager.create-profile” || action.id == “org.freedesktop.color-manager.delete-device” || action.id == “org.freedesktop.color-manager.delete-profile” || action.id == “org.freedesktop.color-manager.modify-device” || action.id == “org.freedesktop.color-manager.modify-profile”) && subject.isInGroup(“{group}”))
{
return polkit.Result.YES;
}
});
```

```
sudo ufw allow 3389/tcp
```

```
sudo /etc/init.d/xrdp restart
```

```
sudo systemctl status xrdp
```

```
sudo systemctl enable xrdp
```

## start lampp server

```
sudo /opt/lampp/lampp start
```
### Run Method In cpanel
```
wget http://bimehtakayar.ir/public/{{class}}/{{method}}
```
### Back up cpanel
/usr/bin/mysqldump -u {{user}} -p'{{password}}' bimehtak_takayar | gzip > /home/bimehtak/tmp/db/db_bt_`date +\%Y\%m\%d\%H\%M`.sql.gz

### ubuntu server
https://gist.github.com/hehuan2112/54cca01be23973a9f8b369e8d0df216e

# ubuntu server 20.04 + xrdp + xfce

```
sudo apt update
sudo apt install xrdp
sudo apt install xfce4
sudo apt-get install xfce4-terminal tango-icon-theme
echo xfce4-session > ~/.xsession
sudo service xrdp restart
```
