# rpi-ansible
A collection of ansible roles for bootstraping devices running ArchLinuxARM (RPI 2/3).

## Manual steps on the PI
```bash
$ ssh alarm@${RPI-IP}
$ su -
$ pacman -S --noconfirm python sudo
$ echo "alarm ALL=(ALL) NOPASSWD: ALL" >> /etc/sudoers
$ passwd
$ <ctrl+d>
```

## Hosts file
`cp hosts.example hosts`

## Running ansible from the host
`ansible-playbook -i hosts rpi.yml -u alarm --ask-pass # needed only-once for the public key`
