### [1.1.1接口说明](https://www.gitbook.com/book/wilsonhua/nbile-api/edit#)

针对指定账页的所有操作查询接口。

### [1.1.2访问地址](https://www.gitbook.com/book/wilsonhua/nbile-api/edit#)

```
/ledgers/{id}/operations{?cursor,limit,order}
```

### [1.1.3参数说明](https://www.gitbook.com/book/wilsonhua/nbile-api/edit#)

|   |   |   |   | [**请求参数**](https://www.gitbook.com/book/wilsonhua/nbile-api/edit#) |
| :--- | :--- | :--- | :--- | :--- |
| **参数名称** | **含义** | **是否必填** | **类型** | **说明/实例** |
| id | 账页ID | 是 | number | 账页序列号，例如：69859 |
| cursor | 焦点 | 否 | string | 如果设置为now，则从请求时间开始查询，否则从设置的时间点开始查询，例如：12884905984 |
| order | 排序 | 否 | string | asc或者desc |
| limit | 显示数量 | 否 | number | 本次返回的最大数量 |

  


### [1.1.4返回实例](https://www.gitbook.com/book/wilsonhua/nbile-api/edit#)

```
{
    "_embedded": {
        "records": [
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
        ]
    },
    "_links": {
        "next": {
            "href": "/ledgers/18/operations?order=asc&limit=10&cursor=77309415424"
        },
        "prev": {
            "href": "/ledgers/18/operations?order=desc&limit=10&cursor=77309415424"
        },
        "self": {
            "href": "/ledgers/18/operations?order=asc&limit=10&cursor="
        }
    }
}
```



