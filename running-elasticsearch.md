## 安装并运行 Elasticsearch

### 安装 Java

安装 Elasticsearch 之前，需要先安装最新版本的 Java，可以从 www.java.com 下载。


### 获取 Elasticsearch

从 Elastic 官网获取，地址：https://www.elastic.co/cn/downloads/elasticsearch 。

### 启动 Elasticsearch

```
cd elasticsearch-7.6.1
./bin/elasticsearch  
```

### 测试 Elasticsearch 是否安装成功

、、、
curl 'http://localhost:9200/?pretty'
、、、

如果能看到类似下面的结果

```
{
  "name" : "Tom Foster",
  "cluster_name" : "elasticsearch",
  "cluster_uuid" : "eeEzroFPRZ26OzRvXHaxoA",
  "version" : {
    "number" : "7.6.1",
    "build_flavor" : "default",
    "build_type" : "tar",
    "build_hash" : "aa751e09be0a5072e8570670309b1f12348f023b",
    "build_date" : "2020-02-29T00:15:25.529771Z",
    "build_snapshot" : false,
    "lucene_version" : "8.4.0",
    "minimum_wire_compatibility_version" : "6.8.0",
    "minimum_index_compatibility_version" : "6.0.0-beta1"
  },
  "tagline" : "You Know, for Search"
}
```
说明 Elasticseach 已经成功运行了。



