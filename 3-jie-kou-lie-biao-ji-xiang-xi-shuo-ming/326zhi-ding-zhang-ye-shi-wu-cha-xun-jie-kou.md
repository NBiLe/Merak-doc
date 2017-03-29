

### 1.1.1**接口说明**

针对指定账页查询事务的接口。

### 1.1.2**访问地址**

```
/ledgers/{id}/transactions{?cursor,limit,order}
```

### 1.1.3**参数说明**

|  |  |  |  | **请求参数** |
| :--- | :--- | :--- | :--- | :--- |
| **参数名称** | **含义** | **是否必填** | **类型** | **说明/实例** |
| id | 账页ID | 是 | number | 账页序列号，例如：69859 |
| cursor | 焦点 | 否 | string | 如果设置为now，则从请求时间开始查询，否则从设置的时间点开始查询，例如：12884905984 |
| order | 排序 | 否 | string | asc或者desc |
| limit | 显示数量 | 否 | number | 本次返回的最大数量 |





### 1.1.4**返回实例**

```
{
    "_embedded": {
        "records": [
            {
                "_links": {
                    "account": {
                        "href": "/accounts/GBS43BF24ENNS3KPACUZVKK2VYPOZVBQO2CISGZ777RYGOPYC2FT6S3K"
                    },
                    "effects": {
                        "href": "/transactions/fa78cb43d72171fdb2c6376be12d57daa787b1fa1a9fdd0e9453e1f41ee5f15a/effects{?cursor,limit,order}",
                        "templated": true
                    },
                    "ledger": {
                        "href": "/ledgers/146970"
                    },
                    "operations": {
                        "href": "/transactions/fa78cb43d72171fdb2c6376be12d57daa787b1fa1a9fdd0e9453e1f41ee5f15a/operations{?cursor,limit,order}",
                        "templated": true
                    },
                    "precedes": {
                        "href": "/transactions?cursor=631231343497216&order=asc"
                    },
                    "self": {
                        "href": "/transactions/fa78cb43d72171fdb2c6376be12d57daa787b1fa1a9fdd0e9453e1f41ee5f15a"
                    },
                    "succeeds": {
                        "href": "/transactions?cursor=631231343497216&order=desc"
                    }
                },
                "id": "fa78cb43d72171fdb2c6376be12d57daa787b1fa1a9fdd0e9453e1f41ee5f15a",
                "paging_token": "631231343497216",
                "hash": "fa78cb43d72171fdb2c6376be12d57daa787b1fa1a9fdd0e9453e1f41ee5f15a",
                "ledger": 146970,
                "created_at": "2015-09-24T10:07:09Z",
                "account": "GBS43BF24ENNS3KPACUZVKK2VYPOZVBQO2CISGZ777RYGOPYC2FT6S3K",
                "account_sequence": 279172874343,
                "max_fee": 0,
                "fee_paid": 0,
                "operation_count": 1,
                "result_code": 0,
                "result_code_s": "tx_success",
                "envelope_xdr": "AAAAAGXNhLrhGtltTwCpmqlarh7s1DB2hIkbP//jgzn4Fos/AAAACgAAAEEAAABnAAAAAAAAAAAAAAABAAAAAAAAAAAAAAAA2ddmTOFAgr21Crs2RXRGLhiAKxicZb/IERyEZL/Y2kUAAAAXSHboAAAAAAAAAAAB+BaLPwAAAECDEEZmzbgBr5fc3mfJsCjWPDtL6H8/vf16me121CC09ONyWJZnw0PUvp4qusmRwC6ZKfLDdk8F3Rq41s+yOgQD",
                "result_xdr": "AAAAAAAAAAoAAAAAAAAAAQAAAAAAAAAAAAAAAAAAAAA=",
                "result_meta_xdr": "AAAAAAAAAAEAAAACAAAAAAACPhoAAAAAAAAAANnXZkzhQIK9tQq7NkV0Ri4YgCsYnGW/yBEchGS/2NpFAAAAF0h26AAAAj4aAAAAAAAAAAAAAAAAAAAAAAAAAAABAAAAAAAAAAAAAAAAAAAAAAAAAQACPhoAAAAAAAAAAGXNhLrhGtltTwCpmqlarh7s1DB2hIkbP//jgzn4Fos/AABT8kS2c/oAAABBAAAAZwAAAAAAAAAAAAAAAAAAAAABAAAAAAAAAAAAAAAAAAAA"
            }
        ]
    },
    "_links": {
        "next": {
            "href": "/ledgers/146970/transactions?order=asc&limit=10&cursor=631231343497216"
        },
        "prev": {
            "href": "/ledgers/146970/transactions?order=desc&limit=10&cursor=631231343497216"
        },
        "self": {
            "href": "/ledgers/146970/transactions?order=asc&limit=10&cursor="
        }
    }
}
```



