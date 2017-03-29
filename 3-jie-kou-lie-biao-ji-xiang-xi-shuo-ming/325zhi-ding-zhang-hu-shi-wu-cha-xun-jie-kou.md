

### 1.1.1**接口说明**

针对指定的账户查询事务接口。

### 1.1.2**访问地址**

```
/accounts/{account_id}/transactions{?cursor,limit,order}
```

### 1.1.3**参数说明**

|  |  |  |  | **请求参数** |
| :--- | :--- | :--- | :--- | :--- |
| **参数名称** | **含义** | **是否必填** | **类型** | **说明/实例** |
| account\_id | 账页ID | 是 | number | 账页序列号，例如：69859 |
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
                        "href": "/accounts/GBRPYHIL2CI3FNQ4BXLFMNDLFJUNPU2HY3ZMFSHONUCEOASW7QC7OX2H"
                    },
                    "effects": {
                        "href": "/transactions/2a2beb163e2c68bd2377aab243d68225626d70263444a85556ec7271d4e46e03/effects{?cursor,limit,order}",
                        "templated": true
                    },
                    "ledger": {
                        "href": "/ledgers/33"
                    },
                    "operations": {
                        "href": "/transactions/2a2beb163e2c68bd2377aab243d68225626d70263444a85556ec7271d4e46e03/operations{?cursor,limit,order}",
                        "templated": true
                    },
                    "precedes": {
                        "href": "/transactions?cursor=141733924864&order=asc"
                    },
                    "self": {
                        "href": "/transactions/2a2beb163e2c68bd2377aab243d68225626d70263444a85556ec7271d4e46e03"
                    },
                    "succeeds": {
                        "href": "/transactions?cursor=141733924864&order=desc"
                    }
                },
                "id": "2a2beb163e2c68bd2377aab243d68225626d70263444a85556ec7271d4e46e03",
                "paging_token": "141733924864",
                "hash": "2a2beb163e2c68bd2377aab243d68225626d70263444a85556ec7271d4e46e03",
                "ledger": 33,
                "created_at": "2015-09-09T02:46:44Z",
                "account": "GBRPYHIL2CI3FNQ4BXLFMNDLFJUNPU2HY3ZMFSHONUCEOASW7QC7OX2H",
                "account_sequence": 1,
                "max_fee": 0,
                "fee_paid": 0,
                "operation_count": 1,
                "result_code": 0,
                "result_code_s": "tx_success",
                "envelope_xdr": "AAAAAGL8HQvQkbK2HA3WVjRrKmjX00fG8sLI7m0ERwJW/AX3AAAACgAAAAAAAAABAAAAAAAAAAAAAAABAAAAAAAAAAAAAAAAZc2EuuEa2W1PAKmaqVquHuzUMHaEiRs//+ODOfgWiz8AAFrzEHpAAAAAAAAAAAABVvwF9wAAAEAhwIlmkDnlvOaUnj5NMyGlu7XlGLUqUoigWbbMwLS0Em99ZrEh/Gd85pz7hGtAxNMj335utvGDUOAm9WAewEYE",
                "result_xdr": "KivrFj4saL0jd6qyQ9aCJWJtcCY0RKhVVuxycdTkbgMAAAAAAAAACgAAAAAAAAABAAAAAAAAAAAAAAAAAAAAAA==",
                "result_meta_xdr": "AAAAAAAAAAEAAAABAAAAIQAAAAAAAAAAYvwdC9CRsrYcDdZWNGsqaNfTR8bywsjubQRHAlb8BfcBY0V4XYn/9gAAAAAAAAABAAAAAAAAAAAAAAAAAAAAAAEAAAAAAAAAAAAAAAAAAAAAAAABAAAAAgAAAAAAAAAhAAAAAAAAAABlzYS64RrZbU8AqZqpWq4e7NQwdoSJGz//44M5+BaLPwAAWvMQekAAAAAAIQAAAAAAAAAAAAAAAAAAAAAAAAAAAQAAAAAAAAAAAAAAAAAAAAAAAAEAAAAhAAAAAAAAAABi/B0L0JGythwN1lY0aypo19NHxvLCyO5tBEcCVvwF9wFi6oVND7/2AAAAAAAAAAEAAAAAAAAAAAAAAAAAAAAAAQAAAAAAAAAAAAAAAAAAAA=="
            }
        ]
    },
    "_links": {
        "next": {
            "href": "/accounts/GBS43BF24ENNS3KPACUZVKK2VYPOZVBQO2CISGZ777RYGOPYC2FT6S3K/transactions?order=asc&limit=1&cursor=141733924864"
        },
        "prev": {
            "href": "/accounts/GBS43BF24ENNS3KPACUZVKK2VYPOZVBQO2CISGZ777RYGOPYC2FT6S3K/transactions?order=desc&limit=1&cursor=141733924864"
        },
        "self": {
            "href": "/accounts/GBS43BF24ENNS3KPACUZVKK2VYPOZVBQO2CISGZ777RYGOPYC2FT6S3K/transactions?order=asc&limit=1&cursor="
        }
    }
}
```



