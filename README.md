# xrdp-ubuntu
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
sudo systemctl status xrdp
```
sudo systemctl enable xrdp
```