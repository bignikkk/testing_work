Role Name: nginx_setup
=========

Эта роль устанавливает Nginx на серверах с операционной системой Linux (Debian), копирует конфигурационный файл Nginx и запускает контейнеры с использованием Docker Compose.

Requirements
------------

Для выполнения этой роли необходимо:

1) Сервер с операционной системой Linux (Debian) для установки Nginx.
2) Docker и Docker Compose должны быть предварительно установлены, если роль используется для запуска контейнеров.

Role Variables
--------------

1) ansible_facts['os_family']: используется для определения операционной системы, чтобы установить Nginx только на серверах с ОС Debian.
2) Путь для конфигурационного файла Nginx (nginx.conf.j2): роль копирует шаблон конфигурации в нужное место.

Dependencies
------------

Роль не имеет внешних зависимостей, но перед её выполнением должны быть установлены Docker и Docker Compose, чтобы команда для запуска контейнеров могла успешно выполниться.

Example Playbook
----------------

Including an example of how to use your role (for instance, with variables passed in as parameters) is always nice for users too:

    - hosts: webservers
      become: true
      roles:
         - nginx_setup

License
-------

MIT

Author Information
------------------

Author: Blokhin Nikita
GitHub: https://github.com/bignikkk
