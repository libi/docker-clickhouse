# Clickhouse cluster and WebUI on Docker


### usage
1. clone this resp
2. run bash command:

``` bash
cd docker-clickhouse
docker-compose up
```

3.cluster have runnig in Port:

```host: 127.0.0.1``` 

```Port:  8811 8812 8813 8814```



### cluster config

cluster have 4 node , include 2 shard and 2 replica 。

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



