composed-mesos
--------------

Quick and portable way of setting up a mesos ecosystem for local dev environments. 



Quick Start
--------------------
```sh
$ docker compose up -d
```


```
Starting composedmesos_mesosmaster_1
Starting composedmesos_mesosslave_1
Starting composedmesos_marathon_1
Starting composedmesos_zookeeper_1
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
```

To deploy an app via Marathon

```sh
curl -X POST -H "Content-Type: application/json" http://192.168.99.100:8080/v2/apps -d@my_app.json
```