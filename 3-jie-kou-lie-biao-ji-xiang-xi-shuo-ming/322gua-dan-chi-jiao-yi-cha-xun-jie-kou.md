### 1.1.1**接口说明**

当挂单全部或者部分成交时，将产生一个交易，此接口就是查询这些交易的接口。

### 1.1.2**访问地址**

```
/order_book/trades?selling_asset_type={selling_asset_type}&selling_asset_code={selling_asset_code}&selling_asset_issuer={selling_asset_issuer}&buying_asset_type={buying_asset_type}&buying_asset_code={buying_asset_code}&buying_asset_issuer={buying_asset_issuer}
```



### 1.1.3**参数说明**

|  |  |  |  | **请求参数** |
| :--- | :--- | :--- | :--- | :--- |
| **参数名称** | **含义** | **是否必填** | **类型** | **说明/实例** |
| selling\_asset\_type | 卖方资产类型 | 是 | string | 三种类型：native/credit\_alphanum4 /credit\_alphanum12 |
| selling\_asset\_code | 卖方资产代码 | 是 | string | 发行资产代码：USD |
| selling\_asset\_issuer | 卖方资产发行地址 | 是 | string | GA2HGBJIJKI6O4XEM7CZWY5PS6GKSXL6D34ERAJYQSPYA6X6AI7HYW36 |
| buying\_asset\_type | 买方资产类型 | 是 | string |  |
| buying\_asset\_code | 买方资产代码 | 是 | string |  |
| buying\_asset\_issuer | 买方资产发行地址 | 是 | string | GD6VWBXI6NY3AOOR55RLVQ4MNIDSXE5JSAVXUTF35FRRI72LYPI3WL6Z |
| cursor | 焦点 | 否 | string | 如果设置为now，则从请求时间开始查询，否则从设置的时间点开始查询，例如：12884905984 |
| order | 排序 | 否 | string | asc或者desc |
| limit | 显示数量 | 否 | number | 本次返回的最大数量 |



### 1.1.4**返回实例**

```
{
    "_links": {
        "self": {
            "href": "https://horizon-testnet.stellar.org/order_book/trades?order=asc&limit=10&cursor="
        },
        "next": {
            "href": "https://horizon-testnet.stellar.org/order_book/trades?order=asc&limit=10&cursor=7281919481876481-2"
        },
        "prev": {
            "href": "https://horizon-testnet.stellar.org/order_book/trades?order=desc&limit=10&cursor=7281893712072705-2"
        }
    },
    "_embedded": {
        "records": [
            {
                "_links": {
                    "self": {
                        "href": "https://horizon-testnet.stellar.org/accounts/GCJ34JYMXNI7N55YREWAACMMZECOMTPIYDTFCQBWPUP7BLJQDDTVGUW4"
                    },
                    "seller": {
                        "href": "https://horizon-testnet.stellar.org/accounts/GCJ34JYMXNI7N55YREWAACMMZECOMTPIYDTFCQBWPUP7BLJQDDTVGUW4"
                    },
                    "buyer": {
                        "href": "https://horizon-testnet.stellar.org/accounts/GD42RQNXTRIW6YR3E2HXV5T2AI27LBRHOERV2JIYNFMXOBA234SWLQQB"
                    }
                },
                "id": "7281893712072705-2",
                "paging_token": "7281893712072705-2",
                "seller": "GCJ34JYMXNI7N55YREWAACMMZECOMTPIYDTFCQBWPUP7BLJQDDTVGUW4",
                "sold_asset_type": "native",
                "buyer": "GD42RQNXTRIW6YR3E2HXV5T2AI27LBRHOERV2JIYNFMXOBA234SWLQQB",
                "bought_asset_type": "credit_alphanum4",
                "bought_asset_code": "FOO",
                "bought_asset_issuer": "GBAUUA74H4XOQYRSOW2RZUA4QL5PB37U3JS5NE3RTB2ELJVMIF5RLMAG"
            },
            {
                "_links": {
                    "self": {
                        "href": "https://horizon-testnet.stellar.org/accounts/GCJ34JYMXNI7N55YREWAACMMZECOMTPIYDTFCQBWPUP7BLJQDDTVGUW4"
                    },
                    "seller": {
                        "href": "https://horizon-testnet.stellar.org/accounts/GCJ34JYMXNI7N55YREWAACMMZECOMTPIYDTFCQBWPUP7BLJQDDTVGUW4"
                    },
                    "buyer": {
                        "href": "https://horizon-testnet.stellar.org/accounts/GD42RQNXTRIW6YR3E2HXV5T2AI27LBRHOERV2JIYNFMXOBA234SWLQQB"
                    }
                },
                "id": "7281919481876481-2",
                "paging_token": "7281919481876481-2",
                "seller": "GCJ34JYMXNI7N55YREWAACMMZECOMTPIYDTFCQBWPUP7BLJQDDTVGUW4",
                "sold_asset_type": "native",
                "buyer": "GD42RQNXTRIW6YR3E2HXV5T2AI27LBRHOERV2JIYNFMXOBA234SWLQQB",
                "bought_asset_type": "credit_alphanum4",
                "bought_asset_code": "FOO",
                "bought_asset_issuer": "GBAUUA74H4XOQYRSOW2RZUA4QL5PB37U3JS5NE3RTB2ELJVMIF5RLMAG"
            }
        ]
    }
}
```



