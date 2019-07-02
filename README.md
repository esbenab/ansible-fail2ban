# ansible-fail2ban
A playbook to install fail2ban and setup notifications via IFTTT



```YAML
---

- hosts: all
  remote_user: esbenab
  become: yes
  become_method: sudo

  vars:
    # Fail2Ban vars
    # bantime is defined in minutes
    bantime: 3600
    findtime: 600
    maxretry: 5
    # your email, if your server is set up for it.
    destemail: "alerts@example.com"
    hook_url: "https://maker.ifttt.com/trigger/yourTriggerName/with/key/youRNoTGeTTiNGMyKey"
    #token for https://ipinfo.io
    token: "the secret token provided"
  roles:
    -  ./fail2ban
```
