# How to use


1. Edit hosts.yml
2. Add public ssh in remote hosts
3. `ansible-playbook playbook.yml -i hosts.yml -e "@variables.yml" --ask-vault-pass `

> Note: run `alsamixer` to change the volume output of the RPi

TODO 20210812: Add updating of libseccomp2 to fix container errors. Was done manually today using:
```bash
sudo apt-key adv --keyserver keyserver.ubuntu.com --recv-keys 04EE7237B7D453EC 648ACFD622F3D138
echo "deb http://deb.debian.org/debian buster-backports main" | sudo tee -a /etc/apt/sources.list.d/buster-backports.list
sudo apt update
sudo apt install -t buster-backports libseccomp2
```

source: https://www.reddit.com/r/Readarr/comments/ixajkk/working_docker_image_for_raspberry_pi_os_buster/