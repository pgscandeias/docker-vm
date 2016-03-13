Ubuntu 14.04 base box for developing with docker containers.  
https://atlas.hashicorp.com/pgscandeias/boxes/docker-vm/

```shell
vagrant init pgscandeias/docker-vm
vagrant up --provider virtualbox
```

Includes:

- git 1.9
- docker 1.10
- docker-compose 1.6
- ansible 2.0 (you can use the ansible_local provider)

Licence: [MIT](LICENSE)
