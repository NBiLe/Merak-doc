### 1.2.2接口说明

所有事件查询接口。

### [1.2.2访问地址]()

/effects{?cursor,limit,order}

### [1.2.3参数说明]()

|  |  |  |  | **请求参数** |
| :--- | :--- | :--- | :--- | :--- |
| **参数名称** | **含义** | **是否必填** | **类型** | **说明/实例** |
| cursor | 焦点 | 否 | string | 如果设置为now，则从请求时间开始查询，否则从设置的时间点开始查询，例如：12884905984 |
| order | 排序 | 否 | string | asc或者desc |
| limit | 显示数量 | 否 | number | 本次返回的最大数量 |

### [1.2.4返回实例]()

```
{
    "_embedded": {
        "records": [
            {
                "_links": {
                    "operation": {
                        "href": "/operations/279172878337"
                    },
                    "precedes": {
                        "href": "/effects?cursor=279172878337-1&order=asc"
                    },
                    "succeeds": {
                        "href": "/effects?cursor=279172878337-1&order=desc"
                    }
                },
                "account": "GBS43BF24ENNS3KPACUZVKK2VYPOZVBQO2CISGZ777RYGOPYC2FT6S3K",
                "paging_token": "279172878337-1",
                "starting_balance": "10000000.0",
                "type_i": 0,
                "type": "account_created"
            },
            {
                "_links": {
                    "operation": {
                        "href": "/operations/279172878337"
                    },
                    "precedes": {
                        "href": "/effects?cursor=279172878337-2&order=asc"
                    },
                    "succeeds": {
                        "href": "/effects?cursor=279172878337-2&order=desc"
                    }
                },
                "account": "GBRPYHIL2CI3FNQ4BXLFMNDLFJUNPU2HY3ZMFSHONUCEOASW7QC7OX2H",
                "amount": "10000000.0",
                "asset_type": "native",
                "paging_token": "279172878337-2",
                "type_i": 3,
                "type": "account_debited"
            }
        ]
    },
    "_links": {
        "next": {
            "href": "/effects?order=asc&limit=2&cursor=279172878337-2"
        },
        "prev": {
            "href": "/effects?order=desc&limit=2&cursor=279172878337-1"
        },
        "self": {
            "href": "/effects?order=asc&limit=2&cursor="
        }
    }
}
```



