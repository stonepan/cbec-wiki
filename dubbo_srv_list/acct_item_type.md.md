#### 1.账目类型查询服务`<com.ztesoft.zsmart.bss.crm.bcdc.acct.service.AcctItemTypeRemoteService>`
1.1 查询所有账目类型
>
`List<AcctItemTypeData> qryAllAcctItemType()`
  
1.2 根据账目类型id查询账目类型
>
`AcctItemTypeData qryAcctItemTypeById(Long acctItemTypeId)`

1.3 根据余额类型ID查询账目类型
>
`List<AcctItemTypeData> qryAcctItemTypeByAcctResId(Long acctResId)`




# 5. 账目类型查询服务
服务类：
```java
com.ztesoft.zsmart.bss.crm.bcdc.acct.service.AcctItemTypeRemoteService
```
## 5.1 查询所有账目类型(`待改造`)
返回所有账目类型列表
### 方法签名：
```java
List<AcctItemTypeData> qryAllAcctItemType()
```
#### 5.1.2 入参说明
无

#### 5.1.3 出参说明
##### <span id='acctItemTypaData'>AcctItemTypeData</span>
| Name | Type | Description | Note |
| ---- | ---- | ----------- | ---- |
| acctItemTypeId | Long | 账目类型标识 | M |
| acctItemTypeCode | String | 账目类型编码 | M |
| acctItemTypeName | String | 账目类型名称 | M |
| acctResId | Long | 关联余额类型 | M |
| parentId | Long | 父级账目类型标识 | O |
| exchangeItemTypeId | Long | 兑换账目类型标识 | O |
| usageType | String | 费用类型(A:税,B:优惠金额) | O |
| comments | String | 备注 | O |
| spId | Long | 第三方运营商标识 | O |
| gstType | String | 增值税类型 | O |
| isCurrency | String | (冗)关联余额类型是否为货币 | O |
| currencyTypeId | Long | (冗)关联余额类型的货币类型标识 | O |
| unitId | Long | (冗)关联余额类型的单位标识  | O |

## 1.2 根据账目类型id查询账目类型(`待改造`)
返回符合条件的结果货币类型
### 方法签名：
```java
AcctItemTypeData qryAcctItemTypeById(Long acctItemTypeId)
```
#### 1.2.2 入参说明
| Name | Type | Description | Note |
| ---- | ---- | ----------- | ---- |
| acctItemTypeId | Long | 账目类型标识 | M |

#### 1.2.3 出参说明
参考[AcctItemTypeData](#acctItemTypaData)