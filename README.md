# ansible lab 1

Скопировать в корень директории папку labs и ключи для ssh

### Создать vault для sudo пароля
>
ansible-vault create sudo_pass.yml
>
ввести ключ на хранилище
>
текст файла хранилища:
my_test1_sudo_pass: %PASSWORD%

### Проверить доступность хостов
>
ansible -i labs/hosts all -m ping

### Выполнить плейбук (ввести ключ на хранилище)
>
ansible-playbook -i labs/hosts labs/site.yaml -D --ask-vault-pass --extra-vars '@sudo_pass.yml'
