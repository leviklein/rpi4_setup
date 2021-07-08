# How to use


1. Edit hosts.yml
2. Add public ssh in remote hosts
3. `ansible-playbook playbook.yml -i hosts.yml -e "@variables.yml" --ask-vault-pass `

> Note: run `alsamixer` to change the volume output of the RPi