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

## [2.2数据Data](/ming-ci-jie-shi/22-shu-ju-data.md)

NBIle区块链网络中，每个账户可以存储key/value格式的数据。其中key是Base64编码字符串。

## [2.3事件Effect](#23事件effect)

一个成功的操作（Operation）会产生零个或者更多的事件，此接口为所有的事件查询接口，事件包括了四种事件：

（1）账户事件；

（2）签名事件；

（3）信任线事件；

（4）交易事件；

事件清单如下表所示。

| **事件类型** | **操作名称** |
| :--- | :--- |
|  | **账户事件** |
| Account Created | create\_account |
| Account Removed | merge\_account |
| Account Credited | create\_account, payment, path\_payment, merge\_account |
| Account Debited | create\_account, payment, path\_payment, create\_account |
| Account Thresholds Updated | set\_options |
| Account Home Domain Updated | set\_options |
| Account Flags Updated | set\_options |
|  | **签名者事件** |
| Signer Created | set\_options |
| Signer Removed | set\_options |
| Signer Updated | set\_options |
|  | **信任线事件** |
| Trustline Created | change\_trust |
| Trustline Removed | change\_trust |
| Trustline Updated | change\_trust, allow\_trust |
| Trustline Authorized | allow\_trust |
| Trustline Deauthorized | allow\_trust |
|  | **交易事件** |
| Offer Created | manage\_offer, create\_passive\_offer |
| Offer Removed | manage\_offer, create\_passive\_offer, path\_payment |
| Offer Updated | manage\_offer, create\_passive\_offer, path\_payment |
| Trade | manage\_offer, create\_passive\_offer, path\_payment |

## 

## [1.4账页Ledger](https://www.gitbook.com/book/wilsonhua/nbile-api/edit#)

账页的属性如下表所示。

| **属性名称** | **类型** | **说明** |
| :--- | :--- | :--- |
| id | string | 账页标识号 |
| paging\_token | number | 账页页码标识符，用于查询时焦点 |
| hash | string | 账页hash值 |
| prev\_hash | string | 前一个账页的hash值 |
| sequence | number | 账页序列号 |
| transaction\_count | number | 事务数量 |
| operation\_count | number | 操作数量 |
| closed\_at | string | ISO 8601标准的账页关闭时间 |
| total\_coins | string | 流通中的所有XLM数量 |
| fee\_pool | string | 自上次通货膨胀后所有事务费用总和 |
| base\_fee | number | 当前每个操作的费用 |
| base\_reserve | string | 当前基本保证金的数量 |
| max\_tx\_set\_size | number | 账页中含有事务的最大数量 |

同时包含self、effects、operations、transactions四个链接。

一个实例如下所示：

> ```
> {
> "_links": {
> "effects": {
> "href": "/ledgers/500/effects/{?cursor,limit,order}",
> "templated": true
> },
> "operations": {
> "href": "/ledgers/500/operations/{?cursor,limit,order}",
> "templated": true
> },
> "self": {
> "href": "/ledgers/500"
> },
> "transactions": {
> "href": "/ledgers/500/transactions/{?cursor,limit,order}",
> "templated": true
> }
> },
> "id": "689f00d4824b8e69330bf4ad7eb10092ff2f8fdb76d4668a41eebb9469ef7f30",
> "paging_token": "2147483648000",
> "hash": "689f00d4824b8e69330bf4ad7eb10092ff2f8fdb76d4668a41eebb9469ef7f30",
> "prev_hash": "b608e110c7cc58200c912140f121af50dc5ef407aabd53b76e1741080aca1cf0",
> "sequence": 500,
> "transaction_count": 0,
> "operation_count": 0,
> "closed_at": "2015-07-09T21:39:28Z",
> "total_coins": "100000000000.0000000",
> "fee_pool": "0.0025600",
> "base_fee": 100,
> "base_reserve": "10.0000000",
> "max_tx_set_size": 50
> }
> ```

## [1.5挂单Ofer](https://www.gitbook.com/book/wilsonhua/nbile-api/edit#)

挂单属性如下表所示

| **属性名称** | **类型** | **说明** |
| :--- | :--- | :--- |
| id | integer | 挂单ID |
| paging\_token | string | 分页标识 |
| seller | string | 卖方 |
| selling | [Asset](https://www.gitbook.com/book/wilsonhua/nbile-api/edit#) | 卖方 |
| buying | [Asset](https://www.gitbook.com/book/wilsonhua/nbile-api/edit#) | 卖方 |
| amount | string | 卖的数量 |
| price\_r | object | 使用分数标识的买卖价格 |
| price | string | 价格 |

## [1.6操作Operation](https://www.gitbook.com/book/wilsonhua/nbile-api/edit#)

一个事务包含多个操作。

操作类型如下表所示。

| **类型** | **编号** | **说明** |
| :--- | :--- | :--- |
| CREATE\_ACCOUNT | 0 | 创建一个新账户 |
| PAYMENT | 1 | 支付操作 |
| PATH\_PAYMENT | 2 | 路径支付操作 |
| MANAGE\_OFFER | 3 | 增加、删除和修改挂单 |
| CREATE\_PASSIVE\_OFFER | 4 | 创建反向挂单 |
| SET\_OPTIONS | 5 | 操作设置 |
| CHANGE\_TRUST | 6 | 增加、更新和删除信任线 |
| ALLOW\_TRUST | 7 | 允许信任 |
| ACCOUNT\_MERGE | 8 | 删除账户并转移账户余额到目标账户 |
| INFLATION | 9 | 运行通货膨胀 |

## [1.7未成交挂单池Orderbook](https://www.gitbook.com/book/wilsonhua/nbile-api/edit#)

任意两种资产之间存在一个挂单池。

属性如下表所示。

| **属性名称** | **类型** | **说明** |
| :--- | :--- | :--- |
| bids | object | 买单 |
| asks | object | 卖单 |
| selling | Asset | 卖出资产 |
| buying | Asset | 买入资产 |

## [1.8分页Page](https://www.gitbook.com/book/wilsonhua/nbile-api/edit#)

对查询数据进行分页。

焦点Cursor，是分页的起始点。

## [1.9路径支付Payment Path](https://www.gitbook.com/book/wilsonhua/nbile-api/edit#)

路径支付属性如下表所示。

| **属性名称** | **类型** | **说明** |
| :--- | :--- | :--- |
| path | array | 可达路径 |
| source\_amount | string | 源资产数量 |
| destination\_amount | string | 目标资产数量 |
| destination\_asset\_type | string | 目标资产类型 |
| destination\_asset\_code | optional, string | 目标资产代码 |
| destination\_asset\_issuer | optional, string | 目标资产发行账户 |
| source\_asset\_type | string | 源资产类型 |
| source\_asset\_code | optional, string | 源资产代码 |
| source\_asset\_issuer | optional, string | 源资产发行方 |

## [1.10交易Trade](https://www.gitbook.com/book/wilsonhua/nbile-api/edit#)

部分或者完全成交的挂单形成交易。

路径支付也会产生交易。

交易的属性如下表所示。

| **属性名称** | **类型** | **说明** |
| :--- | :--- | :--- |
| ID | string | 交易ID |
| paging\_token | string | 分页标识 |
| seller | string | 卖方 |
| sold\_asset\_type | string | 卖方资产类型 |
| sold\_asset\_code | string | 卖方资产代码 |
| sold\_asset\_issuer | string | 卖方资产发行账户 |
| buyer | string | 买方 |
| bought\_asset\_type | string | 买方资产类型 |
| bought\_asset\_code | string | 买方资产代码 |
| bought\_asset\_issuer | string | 买方资产发行账户 |

同时，含有seller、buyer、order\_book三个链接。

## [1.11事务Transaction](https://www.gitbook.com/book/wilsonhua/nbile-api/edit#)

事务是操作的集合。

操作属性如下表所示。

| **属性名称** | **类型** | **说明** |
| :--- | :--- | :--- |
| id | string | 事务标识 |
| paging\_token | string | 分页标识 |
| hash | string | 事务Hash |
| ledger | number | 账本序列号 |
| account | string | 账户 |
| account\_sequence | number | 账户序列号 |
| fee\_paid | number | 事务支付费用 |
| operation\_count | number | 操作数量 |
| result\_code | number | 结果代码 |
| result\_code\_s | string | 结果说明字符串 |
| envelope\_xdr | string | Base64打包XDR报文 |
| result\_xdr | string | Base64结果XDR报文 |
| result\_meta\_xdr | string | Base64结果元数据XDR报文 |
| fee\_meta\_xdr | string | Base64费用元数据XDR报文 |

同时，含有self、account、ledger、operations、effects、precedes、succeeds七个链接。

