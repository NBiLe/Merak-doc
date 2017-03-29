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

