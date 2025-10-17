[![Review Assignment Due Date](https://classroom.github.com/assets/deadline-readme-button-22041afd0340ce965d47ae6ef1cefeee28c7c493a6346c4f15d667ab976d596c.svg)](https://classroom.github.com/a/vMONzaIj)
# VG1-APACHE

The appearance of independent work - Vagrant, SSH and Apache

Samostana prace - Vagrant, SSH, a Apache

- V Teams kliknete na odkaz Github Classrom, tim se Vam vytvori Vas repository pro toto zadani
- Vytvorte si Clon Vaseho prvniho repository
- Vytvorte v nem adresar pro Vas prvni server vytvoreny pomoci Vagrant
- Do nej vlozte Vagrantfile z projektoveho repository - Vyberte si oblibenou Linux distribuci [2025-sposdk-osy](https://github.com/sposdknl/2025-sposdk-osy/)
- Upravte Vagrantfile, aby fungoval portforward z portu 80 na port 8080
- Zajistete import Vaseho SSH verejneho klice do instalovane VM
- Zajistete instalaci web serveru Apache pomoci scriptu psaneho v bash
- Vse bude konfigurovano automaticky, po vytvoreni VM bude funkcni SSH z Putty autentizovano pomoci SSH klice a na http://localhost:8080 bude bezet Webserver Apache 
- Upravre README tak, aby bylo jasne co Vas projekt dela, strucne zdokumentujte.
- Funkcni Vagrant deployment bude pridan do Vaseho repository na Guthub

## Documentation

- [Vagrant - Shell Provisioner](https://developer.hashicorp.com/vagrant/docs/provisioning/shell)
- [Vagrant - File Provisioner](https://developer.hashicorp.com/vagrant/docs/provisioning/file)

## Examples commands

```console
git clone https://github.com/sposdknl/VASPROJEKT
cd VASPROJEKT && mkdir LinuxServer && cd LinuxServer
cp ../2025-sposdk-osy/XYZ/Vagrantfile Vagrantfile
vim Vagrantfile
vim install-apache.sh
vim .gitignore

git add LinuxServer/*
git commit "Add new VM + Automatizace"
git push
```


## Dokumentace
Tento projekt slouží k vytvoření virtuálního serveru Debian pomocí nástroje Vagrant.
Po spuštění se automaticky nainstaluje webový server Apache2 a nastaví se přístup přes SSH pomocí veřejného klíče.

Po dokončení instalace je možné server otevřít v prohlížeči na adrese:
http://localhost:8080
Zobrazí se výchozí stránka Apache s textem „It works!“.

Postup použití
Naklonuj repozitář z GitHubu.
Otevři složku projektu v terminálu.
Spusť příkaz:

vagrant up

Tím se automaticky vytvoří a nakonfiguruje Debian s Apache2.
Po dokončení se připoj přes PuTTY pomocí:
Host name: 127.0.0.1
Port: 2222
User: vagrant
Po přihlášení můžeš ověřit stav Apache příkazem:
sudo systemctl status apache2

Co projekt dělá
Vytvoří virtuální server Debian 12.

Přidá SSH veřejný klíč pro přihlášení bez hesla.
Automaticky nainstaluje a spustí Apache2.
Nastaví přesměrování portu 8022 → 8080.
.
