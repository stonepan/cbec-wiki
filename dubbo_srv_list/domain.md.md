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
| domainDataId | Long | 域数据标识 | M |
| domainTypeCode | String | 域数据编码 | M |
| codeValue | String | 编码取值 | M |
| lookupName | String | 显示名称 | M |
| state | String | 状态 | M |
| createdDate| Date | 创建时间 | O |
| comments | String | 备注 | O |