## 和 Elasticsearch 交互

### Java API




### RESTful API with JSON over HTTP

所有其他语言可以使用 RESTful API 通过端口 9200 和 Elasticsearch 进行通信，你可以用你最喜爱的 web 客户端访问 Elasticsearch ，甚至可以使用 curl 命令来和 Elasticsearch 交互。

一个 Elasticsearch 请求和任何 HTTP 请求一样由若干相同的部件组成：

```
curl -X<VERB> '<PROTOCOL>://<HOST>:<PORT>/<PATH>?<QUERY_STRING>' -d '<BODY>'
```

例如，计算集群中文档的数量，我们可以用这个:

```
curl -XGET 'http://localhost:9200/_count?pretty' -d '
{
    "query": {
        "match_all": {}
    }
}
'
```

Elasticsearch 返回一个 HTTP 状态码（例如：200 OK）和（除`HEAD`请求）一个 JSON 格式的返回值。前面的 curl 请求将返回一个像下面一样的 JSON 体：

```
{
    "count" : 0,
    "_shards" : {
        "total" : 5,
        "successful" : 5,
        "failed" : 0
    }
}
```

我们将用缩写格式显示：

```
GET /_count
{
    "query": {
        "match_all": {}
    }
}
```



