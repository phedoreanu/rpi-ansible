# rpi-ansible
A collection of ansible roles for bootstraping devices running ArchLinuxARM (RPI 3/4).

## Manual steps on the PI
```bash
$ ssh alarm@${RPI_IP}
$ su -
$ pacman -Syyu --noconfirm python sudo htop vim raspberrypi-firmware
$ echo "alarm ALL=(ALL) NOPASSWD: ALL" >> /etc/sudoers
$ passwd
$ <ctrl+d>
```

## Hosts file
`$ cp hosts.example hosts`

## Wifi creds
`$ cp roles/wifi/vars/main.yml.example roles/wifi/vars/main.yml`

## Running ansible from the host
`$ ansible-playbook -i hosts rpi.yml -u alarm --ask-pass # needed only-once for the public key`
