### [1.1.1接口说明](https://www.gitbook.com/book/wilsonhua/nbile-api/edit#)

查询跟账户相关联的事件。

### [1.1.2访问地址](https://www.gitbook.com/book/wilsonhua/nbile-api/edit#)

```
/accounts/{account}/effects{?cursor,limit,order}
```

### [1.1.3参数说明](https://www.gitbook.com/book/wilsonhua/nbile-api/edit#)

|   |   |   |   | **请求参数** |
| :--- | :--- | :--- | :--- | :--- |
| **参数名称** | **含义** | **是否必填** | **类型** | **说明/实例** |
| account | 账户 | 是 | String | GA2HGBJIJKI6O4XEM7CZWY5PS6GKSXL6D34ERAJYQSPYA6X6AI7HYW36 |
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
                        "href": "/operations/214748368897"
                    },
                    "precedes": {
                        "href": "/effects?cursor=214748368897-1&order=asc"
                    },
                    "succeeds": {
                        "href": "/effects?cursor=214748368897-1&order=desc"
                    }
                },
                "account": "GC6NFQDTVH2YMVZSXJIVLCRHLFAOVOT32JMDFZJZ34QFSSVT7M5G2XFK",
                "paging_token": "214748368897-1",
                "starting_balance": "100.0",
                "type_i": 0,
                "type": "account_created"
            },
            {
                "_links": {
                    "operation": {
                        "href": "/operations/214748368897"
                    },
                    "precedes": {
                        "href": "/effects?cursor=214748368897-3&order=asc"
                    },
                    "succeeds": {
                        "href": "/effects?cursor=214748368897-3&order=desc"
                    }
                },
                "account": "GC6NFQDTVH2YMVZSXJIVLCRHLFAOVOT32JMDFZJZ34QFSSVT7M5G2XFK",
                "paging_token": "214748368897-3",
                "public_key": "GC6NFQDTVH2YMVZSXJIVLCRHLFAOVOT32JMDFZJZ34QFSSVT7M5G2XFK",
                "type_i": 10,
                "type": "signer_created",
                "weight": 2
            }
        ]
    },
    "_links": {
        "next": {
            "href": "/accounts/GC6NFQDTVH2YMVZSXJIVLCRHLFAOVOT32JMDFZJZ34QFSSVT7M5G2XFK/effects?order=asc&limit=10&cursor=214748368897-3"
        },
        "prev": {
            "href": "/accounts/GC6NFQDTVH2YMVZSXJIVLCRHLFAOVOT32JMDFZJZ34QFSSVT7M5G2XFK/effects?order=desc&limit=10&cursor=214748368897-1"
        },
        "self": {
            "href": "/accounts/GC6NFQDTVH2YMVZSXJIVLCRHLFAOVOT32JMDFZJZ34QFSSVT7M5G2XFK/effects?order=asc&limit=10&cursor="
        }
    }
}
```



