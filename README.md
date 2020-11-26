# Clickhouse cluster and webUI on Docker


### Usage
1. Clone this respo
2. Run bash command:

``` bash
cd docker-clickhouse
docker-compose up
```

3.The cluster have runnig in port:

```Host: 127.0.0.1``` 

```Port:  8811 8812 8813 8814```



### Cluster Config

The cluster has 4 nodes, including 2 shards and 2 replicas。

```xml
        <ua_cluster>
            <!-- shard 01 -->
            <shard>
                <replica>
                    <host>ch1</host>
                    <port>9000</port>
                </replica>
                <replica>
                    <host>ch2</host>
                    <port>9000</port>
                </replica>
            </shard>

            <!-- shard 02 -->
            <shard>
                <replica>
                    <host>ch3</host>
                    <port>9000</port>
                </replica>
                <replica>
                    <host>ch4</host>
                    <port>9000</port>
                </replica>
            </shard>
        </ua_cluster>
```



