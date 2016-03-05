# ansible-praspi
Einletung Install Seafile-Server PRO with osmc (Debian 8 Jessie) on a Raspberry Pi 2 with ansible

1. Install OSMC auf die SD-Karte über andere Rechner mit Kartenlesser.
   https://osmc.tv/download/
   ```   
   gzip -dc OSMC_TGT_rbp2_20160130.img.gz | pv | sudo dd of=/dev/sdd && sync
   ```
2. Die SSH-Key von PR kopieren, als osmc, password osmc
   ```
   ssh-copy-id -i ~/.ssh/id_rsa_PR osmc@192.168.3.39
   # Das hier sollte ansible machen, aber ich habe die Geduld verloren:
   ssh osmc@192.168.3.39 "sudo mkdir -p /root/.ssh && sudo chmod 700 /root/.ssh && sudo cp ~/.ssh/authorized_keys  /root/.ssh/"
   ```
3. Dependences und Vorbereitung mit Ansible 
   ```
   ansible-playbook praspi.yml
   ansible-playbook praspi.yml reboot=yes
   ```
4. Manuell Installieren von seafile, als root von raspi
   Doku: https://cloud.seafile.de/d/a888216da8/files/?p=/LIESMICH.md
   ```
   ssh root@192.168.3.39
   time bash /root/seafile_v5_debian
   ```
5. Ansible kann die SSL-Keys konfigurieren:
   ```
   ansible-playbook praspi-after.yml
   ```
   
6. TODO: Change password osmc im Script
