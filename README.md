# uTorrent
uTorrent ini di instal pada ubuntu 20.4

## Instal Dependency

    sudo apt update
    
    sudo apt -y install libssl1.0.0 libssl-dev

## Install & Buka
  
    x64 bits
    wget http://download.ap.bittorrent.com/track/beta/endpoint/utserver/os/linux-x64-ubuntu-13-04 -O utserver.tar.gz

    x32 bits
    wget http://download.ap.bittorrent.com/track/beta/endpoint/utserver/os/linux-i386-ubuntu-13-04 -O utserver.tar.gz

    extract ke /opt/
    sudo tar xvf utserver.tar.gz -C /opt/

## Buat Server
    
    create symbilic link
    sudo ln -s /opt/utorrent-server-alpha-v3_3/utserver /usr/bin/utserver
    
    run with comand
    utserver -settingspath /opt/utorrent-server-alpha-v3_3/ -daemon
    
    uTorrent akan listen pada 0.0.0.0:8080, -daemon akan menjalankan uTorrent di background.
    
## Beberapa Konfigurasi Penting
      
     akses web
     http://ip-torrent-server:8080/gui
     http://192.168.0.7:8080/gui
     
     username : admin
     password : -
     
## Lakukan

    Klik Settings (roda gigi)
    Directories
    
    
## Location of Downloaded Files

    Put new downloads in: /home/share/bittorent/_actives
    Move completed downloads to: /home/share/bittorent


## Location of .torrents

    Store .torrents in: /home/share/bittorent/_torrents
    Move .torrents for finished jobs to: /home/share/bittorent/_torrents
    Automatically load .torrents from: /home/share/bittorent/_torrents
    

## Web UI

    Authentication
    username admin
    password 123456789
    Connectivity 9090
    
    
## Buat folder di shell
    
    mkdir -p /home/share/bittorent/_torrents
    
    mkdir -p /home/share/bittorent/_actives
    
    chmod -Rf 777 /home/share
    
    chown -Rf nobody: /home/share
    
   
   
 ## Referensi
 
      1. http://onnocenter.or.id/wiki/index.php/UTorrent:_Install_di_Ubuntu_18.04
      2. https://www.linuxbabe.com/ubuntu/install-utorrent-ubuntu-18-04-19-04
    
    
    
    
