### Customize fresh Ubuntu after installation

Copy repository to local machine

Install ansible-core

`$ sudo apt install ansible-core ansible`

### Configure sudo

From directory where are unzipped files run command

`$ ansible-playbook -C -K ubuntu-sudo.yml`

or

`$ ansible-playbook -K ubuntu-sudo.yml -e "ansible_user_id=user_name"`

### Install software of your choice

There are three files which content apps
- apt-packages.yml
- flatpak-packages.yml
- snap-packages.yml


Review list of packages and add any custom. Snap and flatpak contain same list of packages, choose prefered source with tags.


Run playbook in check mode 

`$ ansible-playbook -C ubuntu-conf-soft.yml --tags apt,snap`


Run playbook

`$ ansible-playbook ubuntu-conf-soft.yml --tags apt,snap`
