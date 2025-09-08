### wireguard-ansible

A simple ansible playbook for installing and configuring Wireguard on Ubuntu.

```bash
ansible-playbook playbooks/sydney-play.yml
```

```
.
├── ansible.cfg
├── group_vars
│   └── sydney.yml
├── inventory.ini
├── playbooks
│   └── sydney-play.yml                  # a sample playbook which invokes all the roles
├── README.md
└── roles
    ├── ssh-hardening                    # tasks that restrict SSH access to the host
    │   └── tasks
    │       ├── firewall.yml
    │       ├── main.yml
    │       └── sshd.yml
    ├── user-management                  # tasks for adding users
    │   ├── tasks
    │   │   └── main.yml
    │   └── vars
    └── wireguard                        # wireguard installation tasks
        ├── tasks
        │   ├── main.yml
        │   ├── peers-configs.yml
        │   ├── peers-keys.yml
        │   ├── server-keys.yml
        │   ├── server.yml
        │   └── validate-peers.yml
        └── templates
            ├── client.conf.j2
            └── wg0.conf.j2
```
