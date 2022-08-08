# ansible-wordpress
Install wordpress + nginx + php + myslq dengan ansible
# OS Client
Ubuntu 20.04 lts
#silahkan clone
git clone ...
# Setup Host Ansible
Contoh disini : host nya 192.168.3.83

cek di file host
# Setup key client
 ssh-copy-id root@192.168.3.83
# Setup domain
Ganti di file install-wordpress.yml

wp_sitename: 192.168.3.83
    
wp_install_dir: "/var/www/192.168.3.83"

Ganti IP dengan domain mu jika menggunakan domain

Jika di setting di local silahkan sesuaikan IP nya

# Mulai Jalankan
ansible-playbook -i host install-wordpress.yml -v

# Jika berhasil

PLAY RECAP *******************************************************************************************************************************************************
192.168.3.83               : ok=22   changed=16   unreachable=0    failed=0    skipped=2    rescued=0    ignored=0

# Akses wordpress
http://IPaddr

atau

http://domain
