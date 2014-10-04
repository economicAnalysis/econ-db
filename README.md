


##Useful commands

###ssh into the container
```
$ ssh root@localhost -p 50002 -i <ssh_key>

`ansible-playbook -i hosts playbooks/app-db/deploy.yml --extra-vars "host=local" --extra-vars "@extravars`/sample.yml" --verbose`