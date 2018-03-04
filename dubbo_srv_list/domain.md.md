# 6. 域类型数据查询服务
服务类：
```java
com.ztesoft.zsmart.bss.crm.bcdc.common.service.DomainRemoteService
```
## 6.1 根据域类型编码查询域表数据(`待改造`)
返回符合条件的结果域类型数据列表
### 方法签名：
```java
List<DomainData> queryPublicDimList(String domainTypeCode)
```
#### 6.1.2 入参说明
##### 
| Name | Type | Description | Note |
| ---- | ---- | ----------- | ---- |
| domainTypeCode | String | 域类型编码 | M |


#### 6.1.3 出参说明
##### DomainData
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
