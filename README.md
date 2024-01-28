# Local Docker Development Logging Stack

Components:
- Filebeats
- Elasticsearch
- Kibana


## Installation

```shell
docker compose up -d
```

After the stack is up and running, the stdio of all containers will be collected and logged.

In order to ignore certain containers, add the following label:

```yaml
service:
  my-service:
    labels:
      co.elastic.logs/enabled: false
```


## 


## Credits

The main parts of the stack were taken from here: https://github.com/elkninja/elastic-stack-docker-part-one
I've reduced the complexity of the original stack to the minimal required components.