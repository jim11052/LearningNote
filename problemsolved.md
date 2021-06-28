# Problems Solved

## mysql deadlocks with concurrent inserts
sort the unique key by alphabetical order before insert <br>
[mysql deadlocks with concurrent inserts][MDWCI]


## block usb inserting
 ```sh
 $ echo "install usb-storage /bin/true" > /etc/modprobe.d/usb-storage.conf
 $ reboot
 ```
 
## freeze at login screen but ssh still can login
 ```sh
 $ /etc/init.d/lightdm restart
 ```

## systemctl dead
 ```sh
 $ systemctl --force reboot
 ```
 
## ssh login hang because of systemd-logind dead 
 - Try to restart the systemd-logind
 ```sh
 $ systemctl restart systemd-logind
 ```
 - Reinstall systemd-logind
 ```sh
 $ apt-get install --reinstall systemd
 ```

## ubnutu 16.04 cannot rotate the screen
 ```sh
 $ apt-get remove --purge nvidia*  # if cannot success them remove nvidia*
 $ sudo add-apt-repository ppa:graphics-drivers/ppa
 $ sudo apt-get update
 $ sudo apt-get install nvidia-384
 ```

## passwd fail to change password on ldap
```sh
[error] :
 passwd: Authentication information cannot be recovered
 passwd: password unchanged
[solution] :
 # remove use_authtok in /etc/pam.d/common-password
 # password    [success=1 user_unknown=ignore default=die] pam_ldap.so use_authtok try_first_pass
 password    [success=1 user_unknown=ignore default=die] pam_ldap.so try_first_pass
```
 
[MDWCI]: <http://thushw.blogspot.com/2010/11/mysql-deadlocks-with-concurrent-inserts.html>
