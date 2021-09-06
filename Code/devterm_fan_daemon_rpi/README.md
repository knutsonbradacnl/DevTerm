# Fan control daemon for devterm cm3(rpi os)
 
## Install

**Devterm is pre-installed this package, so devterm cm3 users do not need to repeat the installation steps**

```
wget -O - https://raw.githubusercontent.com/clockworkpi/apt/main/debian/KEY.gpg | sudo apt-key add -
echo "deb https://raw.githubusercontent.com/clockworkpi/apt/main/debian/ stable main" | sudo tee -a /etc/apt/sources.list.d/clockworkpi.list

sudo apt update && sudo apt install -y devterm-fan-temp-daemon-rpi 
```

## Change the threshold temperature

Edit `/usr/local/bin/temp_fan_daemon.py`

line starts with `MAX_TEMP=80`

For devterm cm3(rpi os) the  recommended MAX_TEMP is in range 60-80 

then restart systemd service to take effect

`sudo systemctl restart devterm-fan-temp-daemon`


