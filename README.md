composed-mesos
--------------

Quick and portable way of setting up a mesos ecosystem for local dev environments. 



Quick Start
--------------------
```sh
$ docker compose up -d
```


```
Creating composedmesos_zookeeper_1
Creating composedmesos_mesosmaster_1
Creating composedmesos_mesosslave_1
Creating composedmesos_marathon_1
Creating composedmesos_chronos_1
```

Find your docker machine IP address.

```sh
$ docker-machine ip
192.168.99.100 
```

Services are available at:

```
http://192.168.99.100:5050/  - Mesos
http://192.168.99.100:8080/  - Marathon
http://192.168.99.100:4400/  - Chronos
```

To deploy an app via Marathon

```sh
curl -X POST -H "Content-Type: application/json" http://192.168.99.100:8080/v2/apps -d@my_app.json
```