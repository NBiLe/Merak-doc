### [1.1.1接口说明]()

针对指定账户的所有操作查询接口。

### [1.1.2访问地址]()

```
/accounts/{account}/operations{?cursor,limit,order}
```

### [1.1.3参数说明]()

|  |  |  |  | **请求参数** |
| :--- | :--- | :--- | :--- | :--- |
| **参数名称** | **含义** | **是否必填** | **类型** | **说明/实例** |
| account | 账户 | 是 | String | GA2HGBJIJKI6O4XEM7CZWY5PS6GKSXL6D34ERAJYQSPYA6X6AI7HYW36 |
| cursor | 焦点 | 否 | string | 如果设置为now，则从请求时间开始查询，否则从设置的时间点开始查询，例如：12884905984 |
| order | 排序 | 否 | string | asc或者desc |
| limit | 显示数量 | 否 | number | 本次返回的最大数量 |



### [1.1.4返回实例]()

```
{
    "_embedded": {
        "records": [
            {
                "_links": {
                    "effects": {
                        "href": "/operations/46316927324160/effects/{?cursor,limit,order}",
                        "templated": true
                    },
                    "precedes": {
                        "href": "/operations?cursor=46316927324160&order=asc"
                    },
                    "self": {
                        "href": "/operations/46316927324160"
                    },
                    "succeeds": {
                        "href": "/operations?cursor=46316927324160&order=desc"
                    },
                    "transactions": {
                        "href": "/transactions/46316927324160"
                    }
                },
                "account": "GBBM6BKZPEHWYO3E3YKREDPQXMS4VK35YLNU7NFBRI26RAN7GI5POFBB",
                "funder": "GBIA4FH6TV64KSPDAJCNUQSM7PFL4ILGUVJDPCLUOPJ7ONMKBBVUQHRO",
                "id": 46316927324160,
                "paging_token": "46316927324160",
                "starting_balance": 1000000000,
                "type_i": 0,
                "type": "create_account"
            }
        ]
    },
    "_links": {
        "next": {
            "href": "/accounts/GBBM6BKZPEHWYO3E3YKREDPQXMS4VK35YLNU7NFBRI26RAN7GI5POFBB/operations?order=asc&limit=10&cursor=46316927324160"
        },
        "prev": {
            "href": "/accounts/GBBM6BKZPEHWYO3E3YKREDPQXMS4VK35YLNU7NFBRI26RAN7GI5POFBB/operations?order=desc&limit=10&cursor=46316927324160"
        },
        "self": {
            "href": "/accounts/GBBM6BKZPEHWYO3E3YKREDPQXMS4VK35YLNU7NFBRI26RAN7GI5POFBB/operations?order=asc&limit=10&cursor="
        }
    }
}
```



