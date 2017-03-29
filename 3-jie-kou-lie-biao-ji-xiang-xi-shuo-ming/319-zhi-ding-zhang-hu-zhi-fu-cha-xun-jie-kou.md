### [1.1.1接口说明](https://www.gitbook.com/book/wilsonhua/nbile-api/edit#)

针对指定账户的支付操作查询接口。

### [1.1.2访问地址](https://www.gitbook.com/book/wilsonhua/nbile-api/edit#)

```
/accounts/{id}/payments{?cursor,limit,order}
```

### [1.1.3参数说明](https://www.gitbook.com/book/wilsonhua/nbile-api/edit#)

|   |   |   |   | **请求参数** |
| :--- | :--- | :--- | :--- | :--- |
| **参数名称** | **含义** | **是否必填** | **类型** | **说明/实例** |
| id | 账户ID | 是 | String | GA2HGBJIJKI6O4XEM7CZWY5PS6GKSXL6D34ERAJYQSPYA6X6AI7HYW36 |
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
                    "self": {
                        "href": "/operations/12884905984"
                    },
                    "transaction": {
                        "href": "/transaction/6391dd190f15f7d1665ba53c63842e368f485651a53d8d852ed442a446d1c69a"
                    },
                    "precedes": {
                        "href": "/account/GCEZWKCA5VLDNRLN3RPRJMRZOX3Z6G5CHCGSNFHEYVXM3XOJMDS674JZ/payments?cursor=12884905984&order=asc{?limit}",
                        "templated": true
                    },
                    "succeeds": {
                        "href": "/account/GCEZWKCA5VLDNRLN3RPRJMRZOX3Z6G5CHCGSNFHEYVXM3XOJMDS674JZ/payments?cursor=12884905984&order=desc{?limit}",
                        "templated": true
                    }
                },
                "id": 12884905984,
                "paging_token": "12884905984",
                "type_i": 0,
                "type": "payment",
                "sender": "GCEZWKCA5VLDNRLN3RPRJMRZOX3Z6G5CHCGSNFHEYVXM3XOJMDS674JZ",
                "receiver": "GCXKG6RN4ONIEPCMNFB732A436Z5PNDSRLGWK7GBLCMQLIFO4S7EYWVU",
                "asset": {
                    "code": "XLM"
                },
                "amount": 1000000000,
                "amount_f": 100
            }
        ]
    },
    "_links": {
        "next": {
            "href": "/account/GCEZWKCA5VLDNRLN3RPRJMRZOX3Z6G5CHCGSNFHEYVXM3XOJMDS674JZ/payments?cursor=12884905984&order=asc{?limit}",
            "templated": true
        },
        "self": {
            "href": "/account/GCEZWKCA5VLDNRLN3RPRJMRZOX3Z6G5CHCGSNFHEYVXM3XOJMDS674JZ/payments"
        }
    }
}
```



