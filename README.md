# vpn-scripts
## how to
### Go to CA server and install git
```
apt update && apt install git -y
git clone https://github.com/dumasti/vpn-scripts_v.1.4.git
mv vpn-scripts_v.1.4/create-vpn_clear ~/create-vpn
cd create-vpn/
```
### Change vars in buildCA.sh
```
chmod +x *.sh
./buildCA.sh
./vpn-server-add.sh
```

### Go to server openvpn and configure firewall and move config from /tmp/srv/ to /etc/openvpn/
```
mv /tmp/srv/* /etc/openvpn/
chmod +x /etc/openvpn/vpnNAME_SERVER/bin
systemctl start openvpn@vpnNAME_SERVER
```

### For create users certs go to CA server and run this command
```
./vpn-client-add.sh
```

## Инструкция для создания нового сервера vpn:
### Идем на CA сервер и устанавливаем git
```
apt update && apt install git -y
git clone https://github.com/dumasti/vpn-scripts_v.1.4.git
mv vpn-scripts_v.1.4/create-vpn_clear ~/create-vpn
cd create-vpn/
```
### Меняем переменные в buildCA.sh
```
chmod +x *.sh
./buildCA.sh
./vpn-server-add.sh
```

### Идем на сервер openvpn и настраиваем файервол, так же перемещаем конфигурацию впн сервера из /tmp/srv/ в /etc/openvpn/
```
mv /tmp/srv/* /etc/openvpn/
chmod +x /etc/openvpn/vpnNAME_SERVER/bin
systemctl start openvpn@vpnNAME_SERVER
```

### Для создания пользовательского сертификата идем на сервер CA и запускаем следующее
```
./vpn-client-add.sh
```
