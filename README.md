# thriftserver-chart

This helm chart will install a simple thrift server.

To install clone this repository then:

```
cd thriftserver-chart/thriftserver
helm install thriftserver .
```

The server will install. Once the server is in running state it can be interrogated for example with beeline.

The following example uses port forwarding.

```
kubectl port-forward deployment/thriftserver 10001:10000 
``` 

Then beeline can be used to connect and peform operations.

```
beeline -u jdbc:hive2://127.0.0.1:10001
```


