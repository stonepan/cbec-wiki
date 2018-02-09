# 1. 货币类型查询服务
服务类：
```java
com.ztesoft.zsmart.bss.crm.bcdc.common.service.CurrencyTypeRemoteService
```
## 1.1 货币类型查询
根据请求入参查询货币类型对象
### 方法签名：
```java
QueryCurrencyTypeResp queryCurrencyType(QueryCurrencyTypeReq request)
```
#### 1.1.2 入参说明
##### QueryCurrencyTypeReq
| Name | Type | Description | Note |
| ---- | ---- | ----------- | ---- |
| currencyTypeId | Long | 货币类型标识，优先级1 | O |
| currencyTypeCode | String | 货币类型编码，优先级2 | O |


#### 1.1.3 出参说明
##### QueryCurrencyTypeResp
| Name | Type | Description | Note |
| ---- | ---- | ----------- | ---- |
| resuleCode | String | 0-成功，其他-失败 | M |
| resultMessage | String | 返回消息 | M |
| currencyType | CurrencyType | 货币类型对象 | O |
##### CurrencyType
| Name | Type | Description | Note |
| ---- | ---- | ----------- | ---- |
| currencyTypeId | Long | 货币类型标识 | M |
| currencyCode | String | 货币编码 | O |
| currencyName | String | 货币名称 | M |
| currencySymbol | String | 货币符号 | M |
| savePrecision | Long | 保存精度 | M |
| displayScale | Long | 显示精度 | O |
| rateDisplayScale | Long | 费率配置显示精度 | O |
| roundMethod | String | 四舍五入方式，参考ROUND_METHOD域数据定义 | O |

## 1.2 查询所有货币类型
返回所有货币类型列表
### 方法签名：
```java
List<CurrencyType> qryAllCurrencyType()
```
#### 1.2.2 入参说明
无

#### 1.2.3 出参说明
CurrencyType(#CurrencyType)