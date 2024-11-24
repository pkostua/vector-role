vector-role
=========

Эта роль устанавливает Vector

Требования роли
-------------

- Ansible >= 2.7

Переменные роли
--------------

Вы можете переопределить default и vars переменные  

| имя                | область переопределения | значение по умолчанию | описание                    |
|--------------------|-------------------------|-----------------------|-----------------------------|
| vector_install_dir | vars                    | /opt/vector           | путь для установки на хосте |
| vector_version     | defaults                | 0.42.0                | версия Vector               |

Пример применения в Playbook
----------------

-Добавьте роль в зависимости вашего проекта

    - src: git@github.com:pkostua/lighthouse-role.git
      scm: git
      version: "0.0.0"
      name: lighthouse-role    

-Добавьте запуск роли в playbook

    - hosts: servers
      roles:
         - lighthose-role

### Источники

* [Vector documentation](https://vector.dev/docs/)