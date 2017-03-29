### [1.1.1接口说明](https://www.gitbook.com/book/wilsonhua/nbile-api/edit#)

针对指定的操作的详细信息查询接口。

### [1.1.2访问地址](https://www.gitbook.com/book/wilsonhua/nbile-api/edit#)

```
/operations/{id}
```

### [1.1.3参数说明](https://www.gitbook.com/book/wilsonhua/nbile-api/edit#)

|   |   |   |   | **请求参数** |
| :--- | :--- | :--- | :--- | :--- |
| **参数名称** | **含义** | **是否必填** | **类型** | **说明/实例** |
| id | 操作ID | 是 | number | 操作ID，例如：77309415424 |

  


### [1.1.4返回实例](https://www.gitbook.com/book/wilsonhua/nbile-api/edit#)

```
{
    "_links": {
        "effects": {
            "href": "/operations/77309415424/effects/{?cursor,limit,order}",
            "templated": true
        },
        "precedes": {
            "href": "/operations?cursor=77309415424&order=asc"
        },
        "self": {
            "href": "/operations/77309415424"
        },
        "succeeds": {
            "href": "/operations?cursor=77309415424&order=desc"
        },
        "transactions": {
            "href": "/transactions/77309415424"
        }
    },
    "account": "GBIA4FH6TV64KSPDAJCNUQSM7PFL4ILGUVJDPCLUOPJ7ONMKBBVUQHRO",
    "funder": "GCEZWKCA5VLDNRLN3RPRJMRZOX3Z6G5CHCGSNFHEYVXM3XOJMDS674JZ",
    "id": 77309415424,
    "paging_token": "77309415424",
    "starting_balance": 100000000000000,
    "type_i": 0,
    "type": "create_account"
}
```



