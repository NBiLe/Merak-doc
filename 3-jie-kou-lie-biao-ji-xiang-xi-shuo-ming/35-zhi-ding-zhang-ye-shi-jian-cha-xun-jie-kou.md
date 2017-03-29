### [1.1.1接口说明](https://www.gitbook.com/book/wilsonhua/nbile-api/edit#)

查询跟账页相关的事件接口。

### [1.1.2访问地址](https://www.gitbook.com/book/wilsonhua/nbile-api/edit#)

```
/ledgers/{id}/effects{?cursor,limit,order}
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
                    "operation": {
                        "href": "/operations/141733924865"
                    },
                    "precedes": {
                        "href": "/effects?cursor=141733924865-1&order=asc"
                    },
                    "succeeds": {
                        "href": "/effects?cursor=141733924865-1&order=desc"
                    }
                },
                "account": "GBS43BF24ENNS3KPACUZVKK2VYPOZVBQO2CISGZ777RYGOPYC2FT6S3K",
                "paging_token": "141733924865-1",
                "starting_balance": "10000000.0",
                "type_i": 0,
                "type": "account_created"
            },
            {
                "_links": {
                    "operation": {
                        "href": "/operations/141733924865"
                    },
                    "precedes": {
                        "href": "/effects?cursor=141733924865-2&order=asc"
                    },
                    "succeeds": {
                        "href": "/effects?cursor=141733924865-2&order=desc"
                    }
                },
                "account": "GBRPYHIL2CI3FNQ4BXLFMNDLFJUNPU2HY3ZMFSHONUCEOASW7QC7OX2H",
                "amount": "10000000.0",
                "asset_type": "native",
                "paging_token": "141733924865-2",
                "type_i": 3,
                "type": "account_debited"
            },
            {
                "_links": {
                    "operation": {
                        "href": "/operations/141733924865"
                    },
                    "precedes": {
                        "href": "/effects?cursor=141733924865-3&order=asc"
                    },
                    "succeeds": {
                        "href": "/effects?cursor=141733924865-3&order=desc"
                    }
                },
                "account": "GBS43BF24ENNS3KPACUZVKK2VYPOZVBQO2CISGZ777RYGOPYC2FT6S3K",
                "paging_token": "141733924865-3",
                "public_key": "GBS43BF24ENNS3KPACUZVKK2VYPOZVBQO2CISGZ777RYGOPYC2FT6S3K",
                "type_i": 10,
                "type": "signer_created",
                "weight": 2
            }
        ]
    },
    "_links": {
        "next": {
            "href": "/ledgers/33/effects?order=asc&limit=10&cursor=141733924865-3"
        },
        "prev": {
            "href": "/ledgers/33/effects?order=desc&limit=10&cursor=141733924865-1"
        },
        "self": {
            "href": "/ledgers/33/effects?order=asc&limit=10&cursor="
        }
    }
}
```



