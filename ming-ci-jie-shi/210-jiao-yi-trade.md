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

