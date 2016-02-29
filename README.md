
  Einletung Install osmc auf praspi

1. Install OSMC auf die SD-Karte über andere Rechner mit Kartenlesser.
   https://osmc.tv/download/
   Evtl. ist schon hier: /data/ISOs/OSMC/OSMC_TGT_rbp2_20160130.img.gz

2. Die SSH-Key von PR kopieren, als osmc
   ssh-copy-id -i ~/.ssh/id_rsa_PR osmc@192.168.3.39
   # Das hier sollte ansible machen, aber ich habe die Geduld verloren:
   ssh osmc@192.168.3.39 "sudo mkdir -p /root/.ssh && sudo chmod 700 /root/.ssh && sudo cp ~/.ssh/authorized_keys  /root/.ssh/"
   
   
3. Ansible kann es übernehmen
   ansible-playbook praspi.yml



