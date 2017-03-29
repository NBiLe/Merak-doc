### [1.1.1接口说明](https://www.gitbook.com/book/wilsonhua/nbile-api/edit#)

指定账页详细信息查询接口。

### [1.1.2访问地址](https://www.gitbook.com/book/wilsonhua/nbile-api/edit#)

```
/ledgers/{sequence}
```

### [1.1.3参数说明](https://www.gitbook.com/book/wilsonhua/nbile-api/edit#)

|   |   |   |   | **请求参数** |
| :--- | :--- | :--- | :--- | :--- |
| **参数名称** | **含义** | **是否必填** | **类型** | **说明/实例** |
| sequence | 序列号 | 是 | number | 账页序列号，例如：69859 |

  


### [1.1.4返回实例](https://www.gitbook.com/book/wilsonhua/nbile-api/edit#)

```
{
    "_links": {
        "effects": {
            "href": "/ledgers/69859/effects/{?cursor,limit,order}",
            "templated": true
        },
        "operations": {
            "href": "/ledgers/69859/operations/{?cursor,limit,order}",
            "templated": true
        },
        "self": {
            "href": "/ledgers/69859"
        },
        "transactions": {
            "href": "/ledgers/69859/transactions/{?cursor,limit,order}",
            "templated": true
        }
    },
    "id": "4db1e4f145e9ee75162040d26284795e0697e2e84084624e7c6c723ebbf80118",
    "paging_token": "300042120331264",
    "hash": "4db1e4f145e9ee75162040d26284795e0697e2e84084624e7c6c723ebbf80118",
    "prev_hash": "4b0b8bace3b2438b2404776ce57643966855487ba6384724a3c664c7aa4cd9e4",
    "sequence": 69859,
    "transaction_count": 0,
    "operation_count": 0,
    "closed_at": "2015-07-20T15:51:52Z",
    "total_coins": "100000000000.0000000",
    "fee_pool": "0.0025600",
    "base_fee": 100,
    "base_reserve": "10.0000000",
    "max_tx_set_size": 50
}
```



