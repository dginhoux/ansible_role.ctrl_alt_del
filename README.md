# ROLE dginhoux.ctrl_alt_del



## DESCRIPTION

This ansible role configure `ctrl+alt+del` hotkey behaviour.



## REQUIREMENTS

#### SUPPORTED PLATFORMS

This role require a supported platform.<br />
It will skip node with unsupported platform to avoid any compatibility problem.<br />
This behaviour can be bypassed by settings the following variable `asserts_bypass=True`.

| Platform | Versions |
|----------|----------|
| Debian | buster, bullseye |
| Fedora | 33, 34, 35, 36 |
| EL | 7, 8 |

#### ANSIBLE VERSION

Ansible >= 2.12

#### DEPENDENCIES

None.



## INSTALLATION

#### ANSIBLE GALAXY

```shell
ansible-galaxy install dginhoux.ctrl_alt_del
```
#### GIT

```shell
git clone https://github.com/dginhoux/ansible_role.ctrl_alt_del dginhoux.ctrl_alt_del
```


## USAGE

#### EXAMPLE PLAYBOOK

```yaml
- hosts: all
  roles:
    - name: start role dginhoux.ctrl_alt_del
      ansible.builtin.include_role:
        name: dginhoux.ctrl_alt_del
```


## VARIABLES

#### DEFAULT VARIABLES

Default variables defined in `defaults/main.yml` : 

```yaml
# ctrl_alt_del_state: enable
ctrl_alt_del_state: disable

ctrl_alt_del_systemd_unit: ctrl-alt-del.target

ctrl_alt_del_sysvinit_enable_action: /sbin/shutdown -t3 -r now
ctrl_alt_del_sysvinit_disable_action: /bin/echo "CTRL-ALT-DEL is disabled"
```

#### DEFAULT OS SPECIFIC VARIABLES

Those variables files are located in `vars/*.yml` are used to handle OS differences.<br />
One of theses is loaded dynamically during role runtime using the `include_vars` module and set OS specifics variable's.

`NOT USED BY THIS ROLE`



## AUTHOR

Dany GINHOUX - https://github.com/dginhoux



## LICENSE

MIT
