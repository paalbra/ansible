# Ansible

## CentOS/Fedora

```
dnf install git ansible
git clone https://github.com/paalbra/ansible.git
cd ansible
cp playbook_simple.sample.yml playbook.yml
# Change playbook.yml as you wish
ansible-playbook -K playbook.yml
```

## Development

Try to write fairly strict YAML. E.g.

```
yamllint -d '{"extends": "default", "rules": {"quoted-strings": {"quote-type": "double", "required": true}, "line-length": {"max": 200}}}' .
```
