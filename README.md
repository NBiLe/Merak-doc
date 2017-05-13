# [1使用说明](#1使用说明)


Merak产品提供访问NBILedger区块链网络的接口，是应用系统与NBILedger区块链网络交互的桥梁。功能包括：创建账户、查询信息、事务操作等。


## [1.1SDK](#11sdk)

提供JS、Go、Java、Ruby、Python和C\#等版本的SDK。SDK下载地址为：

JavaScript语言版本SDK：[https://github.com/NBiLe/MerakJSSDK](https://github.com/NBiLe/MerakJSSDK)

Go语言版本SDK：[https://github.com/NBiLe/MerakGoSDK](https://github.com/NBiLe/MerakGoSDK)

Java语言版本SDK：[https://github.com/NBiLe/MerakJavaSDK](https://github.com/NBiLe/MerakJavaSDK)

Ruby语言版本SDK：[https://github.com/NBiLe/MerakRubySDK](https://github.com/NBiLe/MerakRubySDK)

Python语言版本SDK：[https://github.com/NBiLe/MerakPySDK](https://github.com/NBiLe/MerakPySDK)

C\#语言版本SDK：[https://github.com/NBiLe/MerakCsharpSDK](https://github.com/NBiLe/MerakCsharpSDK)

## [1.2沙箱环境](#12沙箱环境)

| **环境说明** | **访问地址** |
| :--- | :--- |
| 测试沙箱环境URL | [http://api.t.nbile.com/](http://api.t.nbile.com/) |
| network\_passphrase | Public Global NBiLe Network 201612 |

## [1.3Merak产品UI产品Lab](/13-13-merak-chan-pin-ui-chan-pin-lab.md)

Lab为针对Merak提供的UI体验产品，涵盖Merak产品的所有开放接口。用于用户体验、验证和测试接口功能。

## [1.4错误返回码](/14-14-cuo-wu-fan-hui-ma.md)

Merak的异常时返回的信息字段如下表所示。

| **字段说明** | **类型** | **描述** |
| :--- | :--- | :--- |
| type | url | 错误标识，通过浏览器访问该URL可以直接导向一个问题的详细描述页面。 |
| title | string | 错误简短提示。 |
| status | number | HTTP状态返回码。 |
| detail | string | 错误详细描述。 |
| instance | string | 请求的唯一标识，用于日志记录。 |

状态返回码如下表所示。

| **返回状态吗** | **描述** |
| :--- | :--- |
| 400 | 无效参数，请求错误/交易失败/交易格式错误 |
| 403 | 非授权禁止访问 |
| 404 | 服务不存在 |
| 406 | 响应数据不正确 |
| 410 | 历史账本数据不全 |
| 429 | 访问请求太多，速度受限访问 |
| 500 | 服务内部错误 |
| 501 | 未提供请求服务 |
| 503 | 历史账页数据太旧 |

## [1.5返回数据格式](#15返回数据格式)

返回格式是JSON数据格式。数据格式采用HAL，具体细节请参考

[http://stateless.co/hal\_specification.html](http://stateless.co/hal_specification.html)

