### [1.1.1接口说明](https://www.gitbook.com/book/wilsonhua/nbile-api/edit#)

查询可行的路径支付查询接口。

### [1.1.2访问地址](https://www.gitbook.com/book/wilsonhua/nbile-api/edit#)

```
/paths?destination_account={da}&source_account={sa}&destination_asset_type={at}&destination_asset_code={ac}&destination_asset_issuer={di}&destination_amount={amount}
```

### [1.1.3参数说明](https://www.gitbook.com/book/wilsonhua/nbile-api/edit#)

|   |   |   |   | **请求参数** |
| :--- | :--- | :--- | :--- | :--- |
| **参数名称** | **含义** | **是否必填** | **类型** | **说明/实例** |
| destination\_account | 目标资产账户 | 是 | string | GAEDTJ4PPEFVW5XV2S7LUXBEHNQMX5Q2GM562RJGOQG7GVCE5H3HIB4V |
| destination\_asset\_type | 目标资产类型 | 是 | string | 三种类型：native/credit\_alphanum4 /credit\_alphanum12 |
| destination\_asset\_code | 目标资产代码 | 是 | string | 发行资产代码：USD |
| destination\_asset\_issuer | 目标资产发行地址 | 是 | string | GA2HGBJIJKI6O4XEM7CZWY5PS6GKSXL6D34ERAJYQSPYA6X6AI7HYW36 |
| destination\_amount | 目标资产数量 | 是 | string | 10.1 |
| source\_account | 源账户 | 是 | string | GARSFJNXJIHO6ULUBK3DBYKVSIZE7SC72S5DYBCHU7DKL22UXKVD7MXP |

  


### [1.1.4返回实例](https://www.gitbook.com/book/wilsonhua/nbile-api/edit#)

```
{
    "_embedded": {
        "records": [
            {
                "destination_amount": "20.0000000",
                "destination_asset_code": "EUR",
                "destination_asset_issuer": "GDSBCQO34HWPGUGQSP3QBFEXVTSR2PW46UIGTHVWGWJGQKH3AFNHXHXN",
                "destination_asset_type": "credit_alphanum4",
                "path": [],
                "source_amount": "30.0000000",
                "source_asset_code": "USD",
                "source_asset_issuer": "GDSBCQO34HWPGUGQSP3QBFEXVTSR2PW46UIGTHVWGWJGQKH3AFNHXHXN",
                "source_asset_type": "credit_alphanum4"
            },
            {
                "destination_amount": "20.0000000",
                "destination_asset_code": "EUR",
                "destination_asset_issuer": "GDSBCQO34HWPGUGQSP3QBFEXVTSR2PW46UIGTHVWGWJGQKH3AFNHXHXN",
                "destination_asset_type": "credit_alphanum4",
                "path": [
                    {
                        "asset_code": "1",
                        "asset_issuer": "GDSBCQO34HWPGUGQSP3QBFEXVTSR2PW46UIGTHVWGWJGQKH3AFNHXHXN",
                        "asset_type": "credit_alphanum4"
                    }
                ],
                "source_amount": "20.0000000",
                "source_asset_code": "USD",
                "source_asset_issuer": "GDSBCQO34HWPGUGQSP3QBFEXVTSR2PW46UIGTHVWGWJGQKH3AFNHXHXN",
                "source_asset_type": "credit_alphanum4"
            },
            {
                "destination_amount": "20.0000000",
                "destination_asset_code": "EUR",
                "destination_asset_issuer": "GDSBCQO34HWPGUGQSP3QBFEXVTSR2PW46UIGTHVWGWJGQKH3AFNHXHXN",
                "destination_asset_type": "credit_alphanum4",
                "path": [
                    {
                        "asset_code": "21",
                        "asset_issuer": "GDSBCQO34HWPGUGQSP3QBFEXVTSR2PW46UIGTHVWGWJGQKH3AFNHXHXN",
                        "asset_type": "credit_alphanum4"
                    },
                    {
                        "asset_code": "22",
                        "asset_issuer": "GDSBCQO34HWPGUGQSP3QBFEXVTSR2PW46UIGTHVWGWJGQKH3AFNHXHXN",
                        "asset_type": "credit_alphanum4"
                    }
                ],
                "source_amount": "20.0000000",
                "source_asset_code": "USD",
                "source_asset_issuer": "GDSBCQO34HWPGUGQSP3QBFEXVTSR2PW46UIGTHVWGWJGQKH3AFNHXHXN",
                "source_asset_type": "credit_alphanum4"
            }
        ]
    },
    "_links": {
        "self": {
            "href": "/paths"
        }
    }
}
```



