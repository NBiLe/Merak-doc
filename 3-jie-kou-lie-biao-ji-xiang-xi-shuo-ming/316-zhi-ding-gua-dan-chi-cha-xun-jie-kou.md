### [1.1.1接口说明](https://www.gitbook.com/book/wilsonhua/nbile-api/edit#)

指定两种资产之间的未成交挂单查询。

### [1.1.2访问地址](https://www.gitbook.com/book/wilsonhua/nbile-api/edit#)

```
/order_book?selling_asset_type={selling_asset_type}&selling_asset_code={selling_asset_code}&selling_asset_issuer={selling_asset_issuer}&buying_asset_type={buying_asset_type}&buying_asset_code={buying_asset_code}&buying_asset_issuer={buying_asset_issuer}
```

### [1.1.3参数说明](https://www.gitbook.com/book/wilsonhua/nbile-api/edit#)

|   |   |   |   | **请求参数** |
| :--- | :--- | :--- | :--- | :--- |
| **参数名称** | **含义** | **是否必填** | **类型** | **说明/实例** |
| selling\_asset\_type | 卖方资产类型 | 是 | string | 三种类型：native/credit\_alphanum4 /credit\_alphanum12 |
| selling\_asset\_code | 卖方资产代码 | 是 | [string](https://www.gitbook.com/book/wilsonhua/nbile-api/edit#) | 发行资产代码：USD |
| selling\_asset\_issuer | 卖方资产发行地址 | 是 | string | GA2HGBJIJKI6O4XEM7CZWY5PS6GKSXL6D34ERAJYQSPYA6X6AI7HYW36 |
| buying\_asset\_type | 买方资产类型 | 是 | [string](https://www.gitbook.com/book/wilsonhua/nbile-api/edit#) |   |
| buying\_asset\_code | 买方资产代码 | 是 | string |   |
| buying\_asset\_issuer | 买方资产发行地址 | 是 | string | GD6VWBXI6NY3AOOR55RLVQ4MNIDSXE5JSAVXUTF35FRRI72LYPI3WL6Z |

### [1.1.4返回实例](https://www.gitbook.com/book/wilsonhua/nbile-api/edit#)

```
{
    "bids": [
        {
            "price_r": {
                "n": 100000000,
                "d": 12953367
            },
            "price": "7.7200005",
            "amount": "12.0000000"
        }
    ],
    "asks": [
        {
            "price_r": {
                "n": 194,
                "d": 25
            },
            "price": "7.7600000",
            "amount": "238.4804125"
        }
    ],
    "base": {
        "asset_type": "native"
    },
    "counter": {
        "asset_type": "credit_alphanum4",
        "asset_code": "FOO",
        "asset_issuer": "GBAUUA74H4XOQYRSOW2RZUA4QL5PB37U3JS5NE3RTB2ELJVMIF5RLMAG"
    }
}
```



