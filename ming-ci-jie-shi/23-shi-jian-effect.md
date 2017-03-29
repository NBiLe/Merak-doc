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



