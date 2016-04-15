ansible-role-fail2ban
=========

An simple ansible role for installing fail2ban.

Role Variables
--------------

```yml
---
fail2ban_ignoreips:
  - 127.0.0.1/8
fail2ban_bantime: 600
fail2ban_maxretry: 3
fail2ban_findtime: 600
fail2ban_destemail: root@localhost
fail2ban_usedns: no

fail2ban_jail_ssh_enabled: true
fail2ban_jail_sshddos_enabled: true

# Start service by default (started/stopped)
fail2ban_service_state: started
# Enable service on boot
fail2ban_service_enabled: yes
```

Example Playbook
----------------

```yml
---
- hosts: localhost
  roles:
  - banbanchs.fail2ban
```

License
-------

MIT
