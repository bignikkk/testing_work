### TESTING_WORK

TESTING_WORK - работа включает в себя использование Ansible для автоматизированного развертывания докеризированного веб-приложения (nginx, php, mysql) с помощью Docker Compose. Ansible выполняет установку необходимых зависимостей и настройку Nginx, а также запускает контейнеры с использованием docker-compose.

### Автор:

Автор: Nikita Blokhin
GitHub: github.com/bignikkk

### Технологии:

Docker
Docker Compose
Ansible

### Как развернуть проект локально:

```
git clone https://github.com/bignikkk/kitty_service
```

```
cd testing_work
```

Убедитесь, что у вас установлен Docker и Docker Compose. Если их нет, установите их:

```
* Если у вас Ubuntu:

    ```
    sudo apt update
    sudo apt install docker.io docker-compose
    ```

* Если у вас macOS с использованием Homebrew:

    ```
    brew install docker docker-compose
    ```

```
Убедитесь, что у вас установлен Ansible. Если не установлен, установите его:

```
* Если у вас Ubuntu:

    ```
    sudo apt install ansible
    ```

* Если у вас macOS с использованием Homebrew:

    ```
    brew install ansible
    ```
 ```
Запустите плейбук Ansible, который настроит ваше окружение и развернет приложение:

```
ansible-playbook -i ansible/inventory.ini ansible/playbook.yml --ask-become-pass

```

### Как развернуть проект удаленно:

Откройте файл inventory.ini в директории ansible и укажите IP-адрес удалённого сервера вместо localhost:

```
[webservers]
your_server_ip ansible_user=your_username
```

Убедитесь, что у вас установлен Docker и Docker Compose. Если их нет, установите их:

```
* Для Ubuntu:

    ```
    sudo apt update
    sudo apt install docker.io docker-compose
    ```


Убедитесь, что у вас установлен Ansible. Если не установлен, установите его:

```
* Если у вас Ubuntu:

    ```
    sudo apt install ansible
    ```

Убедитесь, что у вас есть доступ к серверу по SSH. Выполните Ansible playbook, указав сервер:

    ```
    ansible-playbook -i ansible/inventory.ini ansible/playbook.yml --ask-become-pass
    ```

