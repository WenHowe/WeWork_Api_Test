## 技术准备
- Java | Python
- RestAssured | Requests
- 待测环境：企业微信官方
- Jenkins持续集成


## 企业微信
- 注册一个企业
- 后台首页：https://work.weixin.qq.com/wework_admin/frame
- 服务端API地址：https://work.weixin.qq.com/api/doc/90000/90135/90664

## 公用数据
AgentId:            1000002
Secret:             FJ3g3ufj8Fa27_-t0tQr3IiNFitf7rF8Sv2Ovc5-Png
corpid(企业ID):      ww40ff430e2f0f74a1


## 待测业务
- 部门的增删改查
- 成员的增删改查


## API说明
- 0) 所有的接口需使用HTTPS协议、JSON数据格式、UTF8编码
- 1) 请求方式，标明接口调用的HTTP方法，区分HttpGet/HttpPost请求。所有的请求都为https协议。
- 2) 请求地址，参数中标注大写的单词，表示为需要替换的变量。
- 3) 请求包体/参数说明，标明请求参数示例及说明，参数说明包括字段含义、取值范围，开发者在设计数据结构时，应参考该定义范围。
- 4) 权限说明，标明接口的使用范围，开发者应特别留意调用场景。比如，同步通讯录的接口必须要用通讯录同步助手的access_token，发送消息指定的范围必须是应用可见范围内的结点等。
- 5) 返回结果/参数说明，标明返回参数示例及说明。特别留意，所有接口在调用失败时返回包里都有errcode、errmsg（部分接口在调用成功时没有返回errcode和errmsg）。开发者需根据errcode存在且不为0判断为失败，否则为成功。而errmsg仅作参考，后续可能会有变动，因此不可作为是否调用成功的判据。