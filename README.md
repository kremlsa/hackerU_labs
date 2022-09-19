# hackerU_labs

https://hackmd.io/BDsbtzCeQa6IVhQIKm9T9g?view

Скопировать в корень директории папку labs и ключи для ssh

Проверить доступность хостов

ansible -i labs/hosts all -m ping

Выполнить плейбук

ansible-playbook -i hosts site.yml -D --extra-vars "ansible_sudo_pass=&PASSWORD%"

only network configuration

ansible-playbook -i hosts site.yml --tags networks -D --extra-vars "ansible_sudo_pass=&PASSWORD%"

