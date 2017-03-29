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



