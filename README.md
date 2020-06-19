## Boomer_locust

Boomer locust with prometheues and grafana example. Using docker-compose.yml.

## Usage

```
# get code
git clone git@github.com:ShaoNianyr/boomer_locust.git

# add venv
python3 -m venv env .

# activate venv
source env/bin/activate

# install locust
pip3 install locust

# vi prometheus_exporter.py
targets: ['your_ip:8089']  # replace your real ip

# install and run grafana & prometheus
docker-compose up -d

# run locust master
locust --master -f prometheus_exporter.py

# run goland slave
go run baidu.go

# view your urls
grafana http://localhost:3000
locust http://localhost:8089
```

## View

![code](code.png)

![grafana](grafana.png)

## Contributing

[locust](https://github.com/locustio/locust)

[boomer](https://github.com/myzhan/boomer)