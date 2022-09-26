# :computer: ROLE dginhoux.ctrl_alt_del

## :scroll: DESCRIPTION

This ansible role configure ctrl_alt_del hotkeys behaviour.
It support sysvinit and systemd.



## :nut_and_bolt: REQUIREMENTS

#### SUPPORTED PLATFORMS

This role require a supported platform. 
It will skip node with unsupported platform to avoid any compatibility problem.
This behaviour can be bypassed by settings this variable `asserts_bypass=True`.

| Platform | Versions |
|----------|----------|
| Debian | buster, bullseye |
| Fedora | 33, 34, 35, 36 |
| EL | 7, 8 |


#### ANSIBLE VERSION

Ansible >= 2.12


#### DEPENDENCIES

None.


## :inbox_tray: INSTALLATION

#### ANSIBLE GALAXY

```shell
ansible-galaxy install dginhoux.ctrl_alt_del
```

#### GIT

```shell
git clone https://github.com/dginhoux/ansible_role.ctrl_alt_del dginhoux.ctrl_alt_del
```


## :rocket: USAGE

#### EXAMPLE PLAYBOOK

```yaml
- hosts: all
  roles:
    - name: start role dginhoux.ctrl_alt_del
      ansible.builtin.include_role:
        name: dginhoux.ctrl_alt_del
      vars:
        ctrl_alt_del_state: disable
        ctrl_alt_del_systemd_unit: ctrl-alt-del.target
        ctrl_alt_del_sysvinit_disable_action: /bin/echo "CTRL-ALT-DEL is disabled"
        ctrl_alt_del_sysvinit_enable_action: /sbin/shutdown -t3 -r now
        
```


## :factory: VARIABLES
#### DEFAULT VARIABLES
Role default variables from `defaults/main.yml` : 

| Variable Name | Value |
|---------------|-------|
|ctrl_alt_del_state | <pre> disable </pre> |
|ctrl_alt_del_systemd_unit | <pre> ctrl-alt-del.target </pre> |
|ctrl_alt_del_sysvinit_enable_action | <pre> /sbin/shutdown -t3 -r now </pre> |
|ctrl_alt_del_sysvinit_disable_action | <pre> /bin/echo "CTRL-ALT-DEL is disabled" </pre> |


#### CONTEXT VARIABLES

Those variables are located in `vars/*.yml` are used to handle OS differences ; One of theses is loaded dynamically during role
runtime using the `include_vars` module and set OS specifics variable's.





## :man: AUTHOR

[![Author](https://img.shields.io/badge/maintained%20by-dginhoux-e00000?style=flat-square)](https://github.com/dginhoux)


## :bookmark_tabs: LICENSE

[![License](https://img.shields.io/github/license/dginhoux/ansible_role.ctrl_alt_del?style=flat-square)](https://github.com/dginhoux/ansible_role.ctrl_alt_del/blob/master/LICENSE)