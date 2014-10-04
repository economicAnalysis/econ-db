


##Useful commands

###ssh into the container
```
$ ssh root@localhost -p 50002 -i ssh_key
```

```
ansible-playbook -i hosts playbooks/app-db/deploy.yml --extra-vars "host=local" --extra-vars "@extravars/sample.yml" --verbose
```

##Useful details
Ports of Docker containers are very configurable. The port mapping is configured
in the `normalstart-db.yml` file. Concretely,
```
docker run -d --name {{ ident }}_db_monogo -p {{ port_db_mongo }}:27017 -p {{ port_db_mongo_ssh }}:22 econ/econ-db-latest
```

The value of variable `port_db_mongo` is `27017`. We've also set port forwarding
in the Vagrantfile to forward 27017.

