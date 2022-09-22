# hackerU_labs

### Задание
https://hackmd.io/BDsbtzCeQa6IVhQIKm9T9g?view
>
### Скопировать в корень директории ключи для ssh
>
### Проверить доступность хостов
>
ansible -i hosts all -m ping
>
### Выполнить плейбук
все задачи
>
ansible-playbook -i hosts site.yml -D --extra-vars "ansible_sudo_pass=&PASSWORD%"
>
только настроить сеть
>
ansible-playbook -i hosts site.yml --tags networks -D --extra-vars "ansible_sudo_pass=&PASSWORD%"
>
генерация сертификатов
>
ansible-playbook -i hosts site.yml -D --tags cert-create --extra-vars "ansible_sudo_pass=123123"
>
настройка аутентификации по сертификатам
>
ansible-playbook -i hosts site.yml -D --tags cert --extra-vars "ansible_sudo_pass=123123"
>
### Vagrant Box для проекта
>
https://drive.google.com/file/d/1O9jSSQamoq5NoCAyyFVCddf3MRBvbmpQ/view
>
Переименовать в my при установке


### Check connection
>
curl --cacert ca_cert/ca.crt --cert ca_cert/client.crt --key ca_cert/client.key -L 127.0.0.1:8081
>

### Example
>
ckib@ckibvm:~/PycharmProjects/hackerU_labs$ curl --cacert ca_cert/ca.crt --cert ca_cert/client.crt --key ca_cert/client.key -L 127.0.0.1:8081
<html>
<h1> Greetings from nginx-2 !!! </h1>
</html>
