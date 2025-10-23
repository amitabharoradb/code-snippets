## Example of Kafka streaming instance on AWS us-west-2
[Link to Code Cell](https://e2-demo-field-eng.cloud.databricks.com/editor/notebooks/2894186667377732?o=1444828305810485#command/8149239478210946) in dbdemos.ai(streaming-session) in notebook **00-Delta-session-PRODUCER**
```python
from confluent_kafka import Producer
import json
import random

kafka_bootstrap_servers_tls = "b-1.oneenvkafka.fso631.c14.kafka.us-west-2.amazonaws.com:9094,b-2.oneenvkafka.fso631.c14.kafka.us-west-2.amazonaws.com:9094,b-3.oneenvkafka.fso631.c14.kafka.us-west-2.amazonaws.com:9094"
#kafka_bootstrap_servers_tls = "<Replace by your own kafka servers>"
# Also make sure to have the proper instance profile to allow the access if you're on AWS.

conf = {
    'bootstrap.servers': kafka_bootstrap_servers_tls,
    'security.protocol': 'SSL'
}

producer = Producer(conf)
```