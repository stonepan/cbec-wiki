# 1. 余额类型查询服务
服务类：
```java
com.ztesoft.zsmart.bss.crm.bcdc.acct.service.AcctResRemoteService
```
## 1.1 余额类型列表查询
根据请求入参查询余额类型，如果入参均未指定则默认查询所有余额类型。
### 方法签名：
```java
QueryAcctResListResp queryAcctResList(QueryAcctResListReq request)
```
#### 1.1.2 入参说明
QueryAcctResListReq:
| Name | Type | Description | Note |
| ---- | ---- | ----------- | ---- |
| acctResIds | List`<Long>` | 如果指定了ID则根据ID查询，优先级1 | O |
| balType | String | 根据balType查询，优先级2 | O |
| acctResGroupId | Long | 根据余额类型组查询，优先级3 | O |


#### 1.1.3 出参说明
##### QueryAcctResListResp
| Name | Type | Description | Note |
| ---- | ---- | ----------- | ---- |
| resuleCode | String | 0-成功，其他-失败 | M |
| resultMessage | String | 返回消息 | M |
| acctResList | List`<AcctRes>` | 余额类型对象列表 | O |
##### AcctRes
| Name | Type | Description | Note |
| ---- | ---- | ----------- | ---- |
| acctResId | Long | 余额类型标识 | M |
| balType | String | 余额大类，参考BAL_TYPE域数据定义 | M |
| acctResName | String | 余额类型名称 | M |
| isCurrency | String | 是否货币类型，Y-是 | M |
| maxValue | Long | 最大余额 | O |
| packInner | String | 是否套餐专用，Y-是 | O |
| refillable | String | 可充值延长标记，参考ACCT_RES.REFILLABLE域数据定义 | O |
| stdCode | String | 余额类型编码 | O |
| priority | Long | 优先级 | O |
| currencyTypeId | Long | 货币类型标识，isCurrency=Y时必填 | O |
| unitId | Long | 单位标识 | O |
| unitPrecision | Long | 保存精度 | O |
| effType | String | 生效方式，参考ACCT_RES.EFF_TYPE域数据定义 | O |
| overdraftFlag | String | Y/N | O |