#Problems Solved

## ssh login hang because og systemd-logind dead 
 - try to restart the systemd-logind
   ```sh
   $ systemctl restart systemd-logind
   ```
 - reinstall systemd-logind
   ```sh
   $ apt-get install --reinstall systemd
   ```
  
