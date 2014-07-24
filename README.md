## Graphite, Carbon, Grafana, Elasticsearch, Statsd, Collectd

An all-in-one image running graphite with carbon, StatsD, CollectD, and Grafana as a front end dashboard 

- `80`: the graphite web interface
- `81`: the grafana web interface
- `2003`: the carbon-cache line receiver (the standard graphite protocol)
- `2004`: the carbon-cache pickle receiver
- `7002`: the carbon-cache query port (used by the web interface)
- `8125`: the statsd port

To run
```
./build
./start
```



Modified from many different Github Dockerfiles

**NOTE**: In this basic setup, the time zone is set to -0700 or America/Denver for the time settings. If installing in other location, the time zone information needs to be changed in Graphite's `local_settings.py` as well as Grafana's `config.js`.