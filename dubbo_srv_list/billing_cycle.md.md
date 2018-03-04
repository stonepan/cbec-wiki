4.账期查询服务<com.ztesoft.zsmart.bss.crm.bcdc.common.service.BillingCycleRemoteService>


4.1 查询所有账期类型


List<BillingCycleTypeData> queryAllBillingCycleType()


4.2 根据账期类型id，账期日期，偏移量查询账期


BillingCycleData qryBillingCycle(Long billingCycleTypeId, Date startDate, Integer offset)


7.3 根据账期类型id，账期日期，偏移量查询账期（给ZTP测试用）


BillingCycleData qryBillingCycle4Ztp(Parm4QryBillCyc parm4QryBillCyc)

# 7. 账期查询服务
服务类：
```java
com.ztesoft.zsmart.bss.crm.bcdc.common.service.BillingCycleRemoteService
```
## 7.1 查询所有账期类型(`待改造`)
返回所有账期类型列表
### 方法签名：
```java
List<BillingCycleTypeData> queryAllBillingCycleType()
```
#### 7.1.2 入参说明
无

#### 7.1.3 出参说明
##### <a name="billingCycleTypeData"></a>BillingCycleTypeData
| Name | Type | Description | Note |
| ---- | ---- | ----------- | ---- |
| billingCycleTypeId | Long | 账期类型标识 | M |
| billingCycleTypeCode | String | 账期类型编码 | O |
| billingCycleTypeName | String | 账期类型名称 | M |
| postpaid | String | 预后付费(Y:Postpaid,N:Prepaid) | M |
| beginDate | Date | 起始日期 | M |
| debtDate | Date | 欠费日期 | M |
| timeUnit | String | 时间单位 | M |
| quantity | Short | 周期数量 | M |
| runDate | Date | 运行日期 | O |
| state | String | 状态 | M |
| createdDate| Date | 创建时间 | O |
| comments | String | 备注 | O |
| spId | Long | 第三方运营商标识 | O |
| partyType | String | 参与人类型 | O |
| partyCode | String | 参与人编码 | O |

## 1.2 查询所有货币类型(`待改造`)
返回所有货币类型列表
### 方法签名：
```java
List<CurrencyType> qryAllCurrencyType()
```
#### 1.2.2 入参说明
无

#### 1.2.3 出参说明
参考[CurrencyType](#currencytype)