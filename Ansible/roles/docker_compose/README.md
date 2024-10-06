Role Name: Docker Compose Installation
=========

Эта роль Ansible предназначена для установки Docker Compose на Linux (Debian-based системы) и macOS.

Requirements
------------

Для использования этой роли на macOS требуется установленный пакетный менеджер homebrew.

Role Variables
--------------

Эта роль не использует переменных, так как установка Docker Compose выполняется автоматически на основании операционной системы хоста.

Dependencies
------------

Роль не имеет внешних зависимостей.

Example Playbook
----------------

Пример использования роли в playbook:

    - hosts: webservers
      become: true
      roles:
         - docker_compose

Пример инвентаря:

[webservers]
localhost ansible_connection=local

License
-------

MIT

Author Information
------------------

Author: Blokhin Nikita
GitHub: https://github.com/bignikkk
