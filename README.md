vector-role
=========

Роль, создана из Playbook для задания 08.03 Roles - были вынесены tasks, vars, templates и handlers. Является частью работы над разделом по изучению Ansible.  

Requirements
------------

Role проверяется и настраивается для работы только на Ubuntu 20.04

Role Variables
--------------

| Variable | Descrition                     | Default value |
| ----- |--------------------------------|--------|
| lighthouse_vcs | Адрес git-репозитория с lihghthouse. Используется ветка master. | http://github.com/VKCOM/lighthouse.git |
| lighthouse_location_dir | Путь для размещения lighthouse | /tmp/lighthouse | 
| lighthouse_access_log_name | Имя access log-файла для nginx, где будут храниться все обработанные им входящие подключения при работе с lighthouse | access |

Dependencies
------------

Роль не использует зависимости с другими ролями.

Example Playbook
----------------

Including an example of how to use your role (for instance, with variables passed in as parameters) is always nice for users too:

    - name: Install lighthouse
      hosts: localhost-lighthouse
      roles:
        - lighthouse-role

```bash
  ansible-galaxy role install -r ./requirements.yml -p roles --force
```

License
-------

MIT

Author Information
------------------

Vladimir Baksheev
