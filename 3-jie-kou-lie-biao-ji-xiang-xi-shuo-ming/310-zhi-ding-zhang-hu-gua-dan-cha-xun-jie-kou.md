### [1.1.1接口说明](https://www.gitbook.com/book/wilsonhua/nbile-api/edit#)

指定账户的挂单查询接口。

### [1.1.2访问地址](https://www.gitbook.com/book/wilsonhua/nbile-api/edit#)

```
/accounts/{account}/offers{?cursor,limit,order}
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
    "_links": {
        "self": {
            "href": "https://horizon-testnet.stellar.org/accounts/GCJ34JYMXNI7N55YREWAACMMZECOMTPIYDTFCQBWPUP7BLJQDDTVGUW4/offers?order=asc&limit=10&cursor="
        },
        "next": {
            "href": "https://horizon-testnet.stellar.org/accounts/GCJ34JYMXNI7N55YREWAACMMZECOMTPIYDTFCQBWPUP7BLJQDDTVGUW4/offers?order=asc&limit=10&cursor=122"
        },
        "prev": {
            "href": "https://horizon-testnet.stellar.org/accounts/GCJ34JYMXNI7N55YREWAACMMZECOMTPIYDTFCQBWPUP7BLJQDDTVGUW4/offers?order=desc&limit=10&cursor=121"
        }
    },
    "_embedded": {
        "records": [
            {
                "_links": {
                    "self": {
                        "href": "https://horizon-testnet.stellar.org/offers/121"
                    },
                    "offer_maker": {
                        "href": "https://horizon-testnet.stellar.org/accounts/GCJ34JYMXNI7N55YREWAACMMZECOMTPIYDTFCQBWPUP7BLJQDDTVGUW4"
                    }
                },
                "id": 121,
                "paging_token": "121",
                "seller": "GCJ34JYMXNI7N55YREWAACMMZECOMTPIYDTFCQBWPUP7BLJQDDTVGUW4",
                "selling": {
                    "asset_type": "credit_alphanum4",
                    "asset_code": "BAR",
                    "asset_issuer": "GBAUUA74H4XOQYRSOW2RZUA4QL5PB37U3JS5NE3RTB2ELJVMIF5RLMAG"
                },
                "buying": {
                    "asset_type": "credit_alphanum4",
                    "asset_code": "FOO",
                    "asset_issuer": "GBAUUA74H4XOQYRSOW2RZUA4QL5PB37U3JS5NE3RTB2ELJVMIF5RLMAG"
                },
                "amount": "23.6692509",
                "price_r": {
                    "n": 387,
                    "d": 50
                },
                "price": "7.7400000"
            },
            {
                "_links": {
                    "self": {
                        "href": "https://horizon-testnet.stellar.org/offers/122"
                    },
                    "offer_maker": {
                        "href": "https://horizon-testnet.stellar.org/accounts/GCJ34JYMXNI7N55YREWAACMMZECOMTPIYDTFCQBWPUP7BLJQDDTVGUW4"
                    }
                },
                "id": 122,
                "paging_token": "122",
                "seller": "GCJ34JYMXNI7N55YREWAACMMZECOMTPIYDTFCQBWPUP7BLJQDDTVGUW4",
                "selling": {
                    "asset_type": "credit_alphanum4",
                    "asset_code": "BAR",
                    "asset_issuer": "GBAUUA74H4XOQYRSOW2RZUA4QL5PB37U3JS5NE3RTB2ELJVMIF5RLMAG"
                },
                "buying": {
                    "asset_type": "credit_alphanum4",
                    "asset_code": "FOO",
                    "asset_issuer": "GBAUUA74H4XOQYRSOW2RZUA4QL5PB37U3JS5NE3RTB2ELJVMIF5RLMAG"
                },
                "amount": "72.0000000",
                "price_r": {
                    "n": 779,
                    "d": 100
                },
                "price": "7.7900000"
            }
        ]
    }
}
```



