# Create podman network and run the container

used image is **harisekhon/hbase** because of the issues in setup discovered using **ofrir119/hbase:1.0.0***

```zshc
podman network create hbase-net && podman run -d --name hbase --network hbase-net -p 16010:16010 -p 2181:2181 -p 8080:8080 -p 9090:9090 -p 9091:9091 -p 16000:16000 -p 16201:16201 -p 16301:16301 harisekhon/hbase
```

# Results of the practical task HBase:

The schreenshots with results in this repo under /screenshots folder