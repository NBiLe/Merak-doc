## [3.1指定账户详细信息查询接口](/3-jie-kou-lie-biao-ji-xiang-xi-shuo-ming/a.md)

### [3.1.1接口说明](#311接口说明)

查询跟账户相关的信息，含有关联交易和Operation的查询链接。

### [3.1.2访问地址](#312访问地址)

/accounts/{account}

### [3.1.3参数说明](#313参数说明)

|  |  |  |  | **请求参数** |
| :--- | :--- | :--- | :--- | :--- |
| **参数名称** | **含义** | **是否必填** | **类型** | **说明/实例** |
| account | 账户标识 | 是 | String | GA2HGBJIJKI6O4XEM7CZWY5PS6GKSXL6D34ERAJYQSPYA6X6AI7HYW36 |

### [3.1.4返回实例](#314返回实例)

```
{
    "_links": {
        "self": {
            "href": "https://horizon-testnet.stellar.org/accounts/GD42RQNXTRIW6YR3E2HXV5T2AI27LBRHOERV2JIYNFMXOBA234SWLQQB"
        },
        "transactions": {
            "href": "https://horizon-testnet.stellar.org/accounts/GD42RQNXTRIW6YR3E2HXV5T2AI27LBRHOERV2JIYNFMXOBA234SWLQQB/transactions{?cursor,limit,order}",
            "templated": true
        },
        "operations": {
            "href": "https://horizon-testnet.stellar.org/accounts/GD42RQNXTRIW6YR3E2HXV5T2AI27LBRHOERV2JIYNFMXOBA234SWLQQB/operations{?cursor,limit,order}",
            "templated": true
        },
        "payments": {
            "href": "https://horizon-testnet.stellar.org/accounts/GD42RQNXTRIW6YR3E2HXV5T2AI27LBRHOERV2JIYNFMXOBA234SWLQQB/payments{?cursor,limit,order}",
            "templated": true
        },
        "effects": {
            "href": "https://horizon-testnet.stellar.org/accounts/GD42RQNXTRIW6YR3E2HXV5T2AI27LBRHOERV2JIYNFMXOBA234SWLQQB/effects{?cursor,limit,order}",
            "templated": true
        },
        "offers": {
            "href": "https://horizon-testnet.stellar.org/accounts/GD42RQNXTRIW6YR3E2HXV5T2AI27LBRHOERV2JIYNFMXOBA234SWLQQB/offers{?cursor,limit,order}",
            "templated": true
        }
    },
    "id": "GD42RQNXTRIW6YR3E2HXV5T2AI27LBRHOERV2JIYNFMXOBA234SWLQQB",
    "paging_token": "7275146318450689",
    "account_id": "GD42RQNXTRIW6YR3E2HXV5T2AI27LBRHOERV2JIYNFMXOBA234SWLQQB",
    "sequence": 7275146318446606,
    "subentry_count": 5,
    "thresholds": {
        "low_threshold": 0,
        "med_threshold": 0,
        "high_threshold": 0
    },
    "flags": {
        "auth_required": false,
        "auth_revocable": false
    },
    "balances": [
        {
            "balance": "126.8107491",
            "limit": "5000.0000000",
            "asset_type": "credit_alphanum4",
            "asset_code": "BAR",
            "asset_issuer": "GBAUUA74H4XOQYRSOW2RZUA4QL5PB37U3JS5NE3RTB2ELJVMIF5RLMAG"
        },
        {
            "balance": "294.0000000",
            "limit": "922337203685.4775807",
            "asset_type": "credit_alphanum4",
            "asset_code": "FOO",
            "asset_issuer": "GBAUUA74H4XOQYRSOW2RZUA4QL5PB37U3JS5NE3RTB2ELJVMIF5RLMAG"
        },
        {
            "balance": "9997.6802725",
            "asset_type": "native"
        }
    ],
    "signers": [
        {
            "public_key": "GD42RQNXTRIW6YR3E2HXV5T2AI27LBRHOERV2JIYNFMXOBA234SWLQQB",
            "weight": 1
        }
    ],
    "data": {
        "club": "MTAw"
    }
}
```



