# ansible lab 1

Скопировать в корень директории папку labs и ключи для ssh

### Проверить доступность хостов
ansible -i labs/hosts all -m ping

### Выполнить плейбук
ansible-playbook -i labs/hosts labs/site.yaml -D

### Выполнить плейбук c паролем для root (заменить ...)
ansible-playbook -i labs/hosts labs/site.yaml -D --extra-vars "ansible_sudo_pass=..."
