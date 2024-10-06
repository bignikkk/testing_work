Role Name: Docker и Docker Compose Setup
=========

Эта роль Ansible предназначена для установки Docker на Linux (Debian-based системы) и macOS.

Requirements
------------

Для использования роли вам потребуется установленный Ansible версии 2.9 или выше. На macOS должен быть установлен пакетный менеджер homebrew для выполнения установки Docker.

Role Variables
--------------

В этой роли не используется переменных, требующих настройки. Все действия по установке Docker выполняются автоматически в зависимости от операционной системы хоста.

Dependencies
------------

Роль не имеет зависимостей от других ролей.

Example Playbook
----------------

Пример использования роли в playbook:

    - hosts: webservers
      become: true
      roles:
         - docker

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
