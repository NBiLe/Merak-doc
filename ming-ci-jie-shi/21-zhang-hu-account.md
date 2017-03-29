## [2.1账户Account](/ming-ci-jie-shi/21-zhang-hu-account.md)

所有的数据都账户进行关联，账户是贯串所有数据的重要维度。

一个账户的包含属性如下标识。

| **属性名** | **类型** | **说明** |
| :--- | :--- | :--- |
| id | string | 账户ID |
| account\_id | string | base32编码的账户公钥 |
| sequence | number | 账户的当前序列号 |
| subentry\_count | number | 账户实体数量 |
| balances | array of objects | 账户余额 |
| thresholds | object | 账户阈值 |
| signers | array of objects | 账户签名者 |
| data | object | 账户数据 |

其中还包含了数据、事件、挂单、操作、支付、交易、事务7类对象的URL链接。

一个实例如下所示：

```
{
"_links": {
"self": {
"href": "https://horizon-testnet.stellar.org/accounts/GBRTWTVW65NO4AER7W6G5CTVWGZCLQJIKJTAX523Q5GPU6TNJONXOR23"
},
"transactions": {
"href": "https://horizon-testnet.stellar.org/accounts/GBRTWTVW65NO4AER7W6G5CTVWGZCLQJIKJTAX523Q5GPU6TNJONXOR23/transactions{?cursor,limit,order}",
"templated": true
},
"operations": {
"href": "https://horizon-testnet.stellar.org/accounts/GBRTWTVW65NO4AER7W6G5CTVWGZCLQJIKJTAX523Q5GPU6TNJONXOR23/operations{?cursor,limit,order}",
"templated": true
},
"payments": {
"href": "https://horizon-testnet.stellar.org/accounts/GBRTWTVW65NO4AER7W6G5CTVWGZCLQJIKJTAX523Q5GPU6TNJONXOR23/payments{?cursor,limit,order}",
"templated": true
},
"effects": {
"href": "https://horizon-testnet.stellar.org/accounts/GBRTWTVW65NO4AER7W6G5CTVWGZCLQJIKJTAX523Q5GPU6TNJONXOR23/effects{?cursor,limit,order}",
"templated": true
},
"offers": {
"href": "https://horizon-testnet.stellar.org/accounts/GBRTWTVW65NO4AER7W6G5CTVWGZCLQJIKJTAX523Q5GPU6TNJONXOR23/offers{?cursor,limit,order}",
"templated": true
},
"trades": {
"href": "https://horizon-testnet.stellar.org/accounts/GBRTWTVW65NO4AER7W6G5CTVWGZCLQJIKJTAX523Q5GPU6TNJONXOR23/trades{?cursor,limit,order}",
"templated": true
},
"data": {
"href": "https://horizon-testnet.stellar.org/accounts/GBRTWTVW65NO4AER7W6G5CTVWGZCLQJIKJTAX523Q5GPU6TNJONXOR23/data/{key}",
"templated": true
}
},
"id": "GBRTWTVW65NO4AER7W6G5CTVWGZCLQJIKJTAX523Q5GPU6TNJONXOR23",
"paging_token": "",
"account_id": "GBRTWTVW65NO4AER7W6G5CTVWGZCLQJIKJTAX523Q5GPU6TNJONXOR23",
"sequence": "26509955490119684",
"subentry_count": 1,
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
"balance": "9999.9999600",
"asset_type": "native"
}
],
"signers": [
{
"public_key": "GBRTWTVW65NO4AER7W6G5CTVWGZCLQJIKJTAX523Q5GPU6TNJONXOR23",
"weight": 1
}
],
"data": {
"club": "MTAw"
}
}
```



