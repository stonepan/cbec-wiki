# 1. 单位查询服务
服务类：
```java
com.ztesoft.zsmart.bss.crm.bcdc.common.service.UnitRemoteService
```
## 1.1 单位列表查询
根据请求入参查询单位，如果入参均未指定则默认查询所有数据。
### 方法签名：
```java
QueryUnitListResp queryUnitList(QueryUnitListReq request)
```
#### 1.1.2 入参说明
##### QueryUnitListReq
| Name | Type | Description | Note |
| ---- | ---- | ----------- | ---- |
| unitIds | List`<Long>` | 如指定了ID则根据ID查询，优先级1 | O |
| defaultUnit | Boolean | 查询所有单位类型的默认单位，优先级2 | O |


#### 1.1.3 出参说明
##### QueryUnitListResp
| Name | Type | Description | Note |
| ---- | ---- | ----------- | ---- |
| resuleCode | String | 0-成功，其他-失败 | M |
| resultMessage | String | 返回消息 | M |
| unitList | List`<Unit>` | 单位对象列表 | O |
##### Unit
| Name | Type | Description | Note |
| ---- | ---- | ----------- | ---- |
| unitId | Long | 单位标识 | M |
| unitTypeId | Long | 单位类型标识 | M |
| unitName | String | 单位名称 | M |
| unitCode | String | 单位编码 | M |
| displayScale | Long | 显示精度 | O |