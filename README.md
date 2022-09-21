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
настройка аутентификации по сертификатам

>
### Vagrant Box для проекта
>
https://drive.google.com/file/d/1O9jSSQamoq5NoCAyyFVCddf3MRBvbmpQ/view
>
Переименовать в my при установке
