# Ansible bug reproduction

It looks like that if you use `include_role` or `import_role` instead of the `roles` directive, the defaults and vars can't be used to assign to the `environment` directive.

This repository reproduces a minimal use-case scenario.

You can run this with

```shell
ansible-playbook -i hosts deploy.yml --private-key=~/.ssh/id_rsa
```

Make sure to change the `hosts` file with a host you have access to.
