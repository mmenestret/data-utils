# Kafka utils

## Console consume a topic

```
bin/kafka-console-consumer.sh --bootstrap-server kakfanode:9092 --topic yourtopic --from-beginning
```

## Activer JMX (sur un broker)

Ajouter au démarrage du broker:

```
KAFKA_JMX_OPTS="-Dcom.sun.management.jmxremote=true -Dcom.sun.management.jmxremote.authenticate=false -Dcom.sun.management.jmxremote.ssl=false -Djava.rmi.server.hostname=hostname -Dcom.sun.management.jmxremote.port=jmxport -Dcom.sun.management.jmxremote.rmi.port=jmxport" \
```

__Penser à mapper le port si lancé containerisé.__