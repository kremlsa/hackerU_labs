# ansible lab #1

ansible -i labs/hosts all -m ping

ansible-playbook -i labs/hosts labs/site.yaml -D
