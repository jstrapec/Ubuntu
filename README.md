### Customize fresh Ubuntu after installation

Copy repository to local machine

### Configure sudo
From directory where are unzipped files run command

`$ ansible-playbook -C -K ubuntu-conf.yml`

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
