#Problems Solved

## ssh login hang because og systemd-logind dead 
 - Try to restart the systemd-logind
 ```sh
 $ systemctl restart systemd-logind
 ```
 - Reinstall systemd-logind
 ```sh
 $ apt-get install --reinstall systemd
 ```

