Ansible Role : dginhoux.ctrl_alt_del
=========

This ansible role configure ctrl_alt_del hotkeys behaviour. It support sysvinit and systemd.


Requirements
------------

This role require a supported platform defined in `meta/main.yml`.
It will skip node with unsupported platform ; this behaviour can be bypassed by settings this variable `asserts_bypass=True`.



Role Variables
--------------

```yaml
ctrl_alt_del_state: disable
# ctrl_alt_del_state: enable

ctrl_alt_del_systemd_unit: ctrl-alt-del.target
ctrl_alt_del_sysvinit_enable_action: /sbin/shutdown -t3 -r now
ctrl_alt_del_sysvinit_disable_action: /bin/echo "CTRL-ALT-DEL is disabled"
```


Dependencies
------------

none


Example Playbook
----------------



License
-------

BSD


Author Information
------------------

https://github.com/dginhoux/
