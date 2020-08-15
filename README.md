# Scripts
## enable-hibernate-reboot
Based on [this article](https://gist.github.com/setzer22/77b1dc4b226fdf2dee83e6399e30558b).
 
Usage: 
1. Place `disable-hibernate-reboot` script to `/usr/lib/systemd/system-sleep`. It would be executed after waking up.
2. Perform a one-time reboot to Windows:
   ```shell
   sudo enable-hibernate-reboot
   sudo efibootmgr --bootnext 0002 # Where 0002 is a Windows Boot Manager boot entry.
   sudo systemctl hibernate
   ```
