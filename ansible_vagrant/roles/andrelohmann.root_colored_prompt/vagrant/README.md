# Test your role with vagrant

Test your role with vagrant

## Prerequisites

  * Virtualbox is installed
  * Vagrant is installed

## Test process

```
cd vagrant
vagrant up
```

The ansible role will be applied automatically during the vagrant up process.

### Test with molecule from inside vagrant

```
cd /etc/ansible/roles/ansible-role-root_colored_prompt
yamllint .
ansible-lint .
molecule test
```
