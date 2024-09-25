# Installing Ansible

## WSL2

```shell
python3 -m venv .venv --prompt A
source .venv/bin/activate
pip3 install ansible
 ```

# Test Server

## Create Test Server

`vagrant up`

## Connect with SSH

`ssh vagrant@127.0.0.1 -p 2222 -i .vagrant/machines/default/virtualbox/private_key`

## Validate Ansible Can Connect

`ansible testserver -i inventory/vagrant.ini -m ping`

Expected response:

```shell
testserver | SUCCESS => {
    "ansible_facts": {
        "discovered_interpreter_python": "/usr/bin/python3.8"
    },
    "changed": false,
    "ping": "pong"
}
```
