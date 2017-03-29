### [1.1.1接口说明](https://www.gitbook.com/book/wilsonhua/nbile-api/edit#)

针对指定的事务的所有操作查询接口。

### [1.1.2访问地址](https://www.gitbook.com/book/wilsonhua/nbile-api/edit#)

```
/transactions/{hash}/operations{?cursor,limit,order}
```

### [1.1.3参数说明](https://www.gitbook.com/book/wilsonhua/nbile-api/edit#)

|   |   |   |   | [**请求参数**](https://www.gitbook.com/book/wilsonhua/nbile-api/edit#) |
| :--- | :--- | :--- | :--- | :--- |
| **参数名称** | **含义** | **是否必填** | **类型** | **说明/实例** |
| hash | 事务Hash值 | 是 | number | 事务Hash，例如：6391dd190f15f7d1665ba53c63842e368f485651a53d8d852ed442a446d1c69a |
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
                        "href": "/operations/352573865332736/effects/{?cursor,limit,order}",
                        "templated": true
                    },
                    "precedes": {
                        "href": "/operations?cursor=352573865332736&order=asc"
                    },
                    "self": {
                        "href": "/operations/352573865332736"
                    },
                    "succeeds": {
                        "href": "/operations?cursor=352573865332736&order=desc"
                    },
                    "transactions": {
                        "href": "/transactions/352573865332736"
                    }
                },
                "account": "GBU3FDYZK5VTU7A3SIGC443E5OV6MXUI5DXOI22SPT3OPK7AGIIWOZLF",
                "funder": "GBIA4FH6TV64KSPDAJCNUQSM7PFL4ILGUVJDPCLUOPJ7ONMKBBVUQHRO",
                "id": 352573865332736,
                "paging_token": "352573865332736",
                "starting_balance": 1000000000,
                "type_i": 0,
                "type": "create_account"
            }
        ]
    },
    "_links": {
        "next": {
            "href": "/transactions/e648b8f9b00c6a04267b3d204c97d08181a13a9b8f3dce8ba28e96b03114b149/operations?order=asc&limit=10&cursor=352573865332736"
        },
        "prev": {
            "href": "/transactions/e648b8f9b00c6a04267b3d204c97d08181a13a9b8f3dce8ba28e96b03114b149/operations?order=desc&limit=10&cursor=352573865332736"
        },
        "self": {
            "href": "/transactions/e648b8f9b00c6a04267b3d204c97d08181a13a9b8f3dce8ba28e96b03114b149/operations?order=asc&limit=10&cursor="
        }
    }
}
```



