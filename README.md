# Ansible-VPS

Image: Ubuntu 16.04

## Pre configuration

``` bash
ssh-copy-id -i .ssh/id_rsa.pub root@vps.jarrekk.com
ssh root@vps.jarrekk.com apt-get install python -y
```

## Configuration

1. Edit **inventory**, make it to your vps ip or domain name.
2. Encrypt shadowsocks password and Dropbox token if need, see [Tutorial](https://gist.github.com/jarrekk/f4661e666d9f5472878e964b3d200b72) for more information
3. Deploy your vps with command `ansible-playbook -i inventory vps-deploy.yml --vault-password-file .vault_pass.txt` at root path of this project. **.vault_pass.txt** is salt file you encrypt shadowsocks password and dropbox token.
