### [1.1.1接口说明](https://www.gitbook.com/book/wilsonhua/nbile-api/edit#)

查询所有的账页接口。

### [1.1.2访问地址](https://www.gitbook.com/book/wilsonhua/nbile-api/edit#)

```
/ledgers{?cursor,limit,order}
```

### [1.1.3参数说明](https://www.gitbook.com/book/wilsonhua/nbile-api/edit#)

|   |   |   |   | [**请求参数**](https://www.gitbook.com/book/wilsonhua/nbile-api/edit#) |
| :--- | :--- | :--- | :--- | :--- |
| **参数名称** | **含义** | **是否必填** | **类型** | **说明/实例** |
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
                        "href": "/ledgers/1/effects/{?cursor,limit,order}",
                        "templated": true
                    },
                    "operations": {
                        "href": "/ledgers/1/operations/{?cursor,limit,order}",
                        "templated": true
                    },
                    "self": {
                        "href": "/ledgers/1"
                    },
                    "transactions": {
                        "href": "/ledgers/1/transactions/{?cursor,limit,order}",
                        "templated": true
                    }
                },
                "id": "e8e10918f9c000c73119abe54cf089f59f9015cc93c49ccf00b5e8b9afb6e6b1",
                "paging_token": "4294967296",
                "hash": "e8e10918f9c000c73119abe54cf089f59f9015cc93c49ccf00b5e8b9afb6e6b1",
                "sequence": 1,
                "transaction_count": 0,
                "operation_count": 0,
                "closed_at": "1970-01-01T00:00:00Z",
                "total_coins": "100000000000.0000000",
                "fee_pool": "0.0000000",
                "base_fee": 100,
                "base_reserve": "10.0000000",
                "max_tx_set_size": 50
            },
            {
                "_links": {
                    "effects": {
                        "href": "/ledgers/2/effects/{?cursor,limit,order}",
                        "templated": true
                    },
                    "operations": {
                        "href": "/ledgers/2/operations/{?cursor,limit,order}",
                        "templated": true
                    },
                    "self": {
                        "href": "/ledgers/2"
                    },
                    "transactions": {
                        "href": "/ledgers/2/transactions/{?cursor,limit,order}",
                        "templated": true
                    }
                },
                "id": "e12e5809ab8c59d8256e691cb48a024dd43960bc15902d9661cd627962b2bc71",
                "paging_token": "8589934592",
                "hash": "e12e5809ab8c59d8256e691cb48a024dd43960bc15902d9661cd627962b2bc71",
                "prev_hash": "e8e10918f9c000c73119abe54cf089f59f9015cc93c49ccf00b5e8b9afb6e6b1",
                "sequence": 2,
                "transaction_count": 0,
                "operation_count": 0,
                "closed_at": "2015-07-16T23:49:00Z",
                "total_coins": "100000000000.0000000",
                "fee_pool": "0.0000000",
                "base_fee": 100,
                "base_reserve": "10.0000000",
                "max_tx_set_size": 100
            }
        ]
    },
    "_links": {
        "next": {
            "href": "/ledgers?order=asc&limit=2&cursor=8589934592"
        },
        "prev": {
            "href": "/ledgers?order=desc&limit=2&cursor=4294967296"
        },
        "self": {
            "href": "/ledgers?order=asc&limit=2&cursor="
        }
    }
}
```



