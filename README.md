<h1>InfluxDB 1.8 Install on Ubuntu</h1>

```
$ wget -q https://repos.influxdata.com/influxdb.key
```
```
$ echo '23a1c8836f0afc5ed24e0486339d7cc8f6790b83886c4c96995b88a061c5bb5d influxdb.key' | sha256sum -c && cat influxdb.key | gpg --dearmor | sudo tee /etc/apt/trusted.gpg.d/influxdb.gpg > /dev/null
$ echo 'deb [signed-by=/etc/apt/trusted.gpg.d/influxdb.gpg] https://repos.influxdata.com/debian stable main' | sudo tee /etc/apt/sources.list.d/influxdata.list
```

```
$ sudo apt-get update && sudo apt-get install influxdb
```

```
$ sudo service influxdb start
```

```
$ sudo apt-get update && sudo apt-get install influxdb
```

```
$ sudo systemctl unmask influxdb.service
```

```
$ sudo systemctl start influxdb
```

### Use InfluxDB  ##

```
$ influx

> show DATABASES
> CREATE DATABASE initDB
> USE initDB
> 

```




