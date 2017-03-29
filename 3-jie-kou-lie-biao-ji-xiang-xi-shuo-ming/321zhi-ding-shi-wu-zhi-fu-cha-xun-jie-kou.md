### 1.1.1**接口说明**

针对某一个特定事务的支付操作查询接口。

### 1.1.2**访问地址**

```
/transactions/{hash}/payments{?cursor,limit,order}
```

### 1.1.3**参数说明**

|  |  |  |  | **请求参数** |
| :--- | :--- | :--- | :--- | :--- |
| **参数名称** | **含义** | **是否必填** | **类型** | **说明/实例** |
| hash | 事务Hash值 | 是 | number | 事务Hash，例如：6391dd190f15f7d1665ba53c63842e368f485651a53d8d852ed442a446d1c69a |
| [cursor]() | 焦点 | 否 | string | 如果设置为now，则从请求时间开始查询，否则从设置的时间点开始查询，例如：12884905984 |
| order | 排序 | 否 | string | asc或者desc |
| limit | 显示数量 | 否 | number | 本次返回的最大数量 |





### 1.1.4**返回实例**

```
{
    "_embedded": {
        "records": [
            {
                "_links": {
                    "effects": {
                        "href": "/operations/46428596473856/effects/{?cursor,limit,order}",
                        "templated": true
                    },
                    "precedes": {
                        "href": "/operations?cursor=46428596473856&order=asc"
                    },
                    "self": {
                        "href": "/operations/46428596473856"
                    },
                    "succeeds": {
                        "href": "/operations?cursor=46428596473856&order=desc"
                    },
                    "transactions": {
                        "href": "/transactions/46428596473856"
                    }
                },
                "account": "GAKLBGHNHFQ3BMUYG5KU4BEWO6EYQHZHAXEWC33W34PH2RBHZDSQBD75",
                "funder": "GBIA4FH6TV64KSPDAJCNUQSM7PFL4ILGUVJDPCLUOPJ7ONMKBBVUQHRO",
                "id": 46428596473856,
                "paging_token": "46428596473856",
                "starting_balance": 1000000000,
                "type_i": 0,
                "type": "create_account"
            }
        ]
    },
    "_links": {
        "next": {
            "href": "?order=asc&limit=10&cursor=46428596473856"
        },
        "prev": {
            "href": "?order=desc&limit=10&cursor=46428596473856"
        },
        "self": {
            "href": "?order=asc&limit=10&cursor="
        }
    }
}
```





