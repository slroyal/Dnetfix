51.222.14.176:25571

apt install python3-pip -y

mkdir -p ~/.config/pip && echo -e "[global]\nbreak-system-packages = true" > ~/.config/pip/pip.conf


sudo nano /etc/systemd/system/unixbot.service

[Unit]
Description=UnixBot Discord Bot
After=network.target

[Service]

User=root

WorkingDirectory=/root

# Environment Variables

Environment="PYTHONUNBUFFERED=1"

Environment="DISCORD_TOKEN=YOUR_DISCORD_BOT_TOKEN"

Environment="MAIN_ADMIN_ID=YOUR_ADMIN_ID"

# Start Bot

ExecStart=/usr/bin/python3 /root/bot.py

# Auto-Restart

Restart=always

RestartSec=5

[Install]

WantedBy=multi-user.target


sudo systemctl daemon-reload

sudo systemctl restart unixbot




# if you use Ubuntu

sudo apt update && sudo apt upgrade -y

sudo apt install lxc lxc-utils -y

sudo apt install snapd -y

sudo systemctl enable --now snapd.socket

sudo snap install lxd

sudo usermod -aG lxd $USER


newgrp lxd

sudo lxd init


sudo apt update


sudo apt install lxc lxc-utils bridge-utils uidmap -y


# if you use debain 

sudo apt install snapd -y

sudo systemctl enable --now snapd.socket

sudo ln -s /var/lib/snapd/snap /snap

sudo snap install lxd

sudo usermod -aG lxd $USER

newgrp lxd

sudo lxd init



