# Самоконтроль выполненения задания

1. Где расположен файл с `some_fact` из второго пункта задания?
```shell
~/ansible/example-ansible-base$ cat group_vars/all/examp.yml
---
  some_fact: 12
```

2. Какая команда нужна для запуска вашего `playbook` на окружении `test.yml`?
```shell
ansible-playbook site.yml -i inventory/test.yml
```

3. Какой командой можно зашифровать файл?
```shell
ansible-vault encrypt <path/filename>
```

4. Какой командой можно расшифровать файл?
```shell
ansible-vault dencrypt <path/filename>
```

5. Можно ли посмотреть содержимое зашифрованного файла без команды расшифровки файла? Если можно, то как?
```shell
ansible-vault view <path/filename>
```

6. Как выглядит команда запуска `playbook`, если переменные зашифрованы?
* При ручном вводе пароля:
```shell
ansible-playbook site.yml -i inventory/prod.yml --ask-vault-password
```

* При считывании пароля из файла:
```shell
ansible-playbook site.yml -i inventory/prod.yml --vault-password-file ansible-vault-pass
```

7. Как называется модуль подключения к host на windows?
* [Windows Remote Management](https://docs.ansible.com/ansible/latest/user_guide/windows_winrm.html)
* [PowerShell Remoting Protocol](https://docs.ansible.com/ansible/latest/collections/ansible/builtin/psrp_connection.html)

8. Приведите полный текст команды для поиска информации в документации ansible для модуля подключений ssh
```shell
ansible-doc -t connection ssh
```

9. Какой параметр из модуля подключения `ssh` необходим для того, чтобы определить пользователя, под которым необходимо совершать подключение?
```shell
remote_user
```