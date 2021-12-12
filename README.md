# ubuntuvm
user_admin - 123

sudo apt-get update
sudo apt-get upgrade

sudo apt install openssh-client
sudo apt install openssh-server
sudo apt install net-tools

sudo cp /etc/ssh/sshd_config /etc/ssh/sshd_config.original
sudo chmod a-w /etc/ssh/sshd_config.original
man /etc/ssh/sshd_config
sudo sshd -t -f /etc/ssh/sshd_config
sudo systemctl restart sshd.service

ssh-keygen -t rsa -b 4096 (одинаковая команда в Windows и Linux)
Публичный ключ прописываем в файле ~/.ssh/authorized_keys
ssh user_admin@10.8.0.106 -p 2222 - для подключения passphrase: 123
