
cd /root/
cp v2-ui_ltim.tar.gz /usr/local/
cd /usr/local/
tar zxvf v2-ui_ltim.tar.gz
rm v2-ui_ltim.tar.gz -f
cd v2-ui
chmod +x v2-ui bin/v2ray-v2-ui bin/v2ctl
cp -f v2-ui.service /etc/systemd/system/
systemctl daemon-reload
systemctl enable v2-ui
systemctl restart v2-ui

cp v2-ui_sh /usr/bin/v2-ui
chmod +x /usr/bin/v2-ui
