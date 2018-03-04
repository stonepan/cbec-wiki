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

## 7.2 根据账期类型标识，账期日期，偏移量查询账期(`待改造`)
返回符合条件的账期数据
### 方法签名：
```java
BillingCycleData qryBillingCycle(Long billingCycleTypeId, Date startDate, Integer offset)
```
#### 7.2.2 入参说明
##### <a name="7.2.2"></a>
| Name | Type | Description | Note |
| ---- | ---- | ----------- | ---- |
| billingCycleTypeId | Long | 所属账期类型标识 | M |
| startDate | Date | 账期日期 | M |
| offset | Integer | 偏移量 | M |
根据前两个条件定位出唯一BillingCycle，按偏移量返回最终BillingCycle

#### 7.2.3 出参说明
##### <a name="billingCycleData"></a>BillingCycleData
| Name | Type | Description | Note |
| ---- | ---- | ----------- | ---- |
| billingCycleId | Long | 账期标识 | M |
| billingCycleTypeId | Long | 账期类型标识 | M |
| cycleBeginDate | Date | 账期起始日期 | M |
| cycleEndDate | Date | 账期结束日期 | M |
| state | String | 状态(A:未出帐,B:出帐中,C:出帐完成) | M |
| debtDate | Date | 欠费日期 | M |
| runDate | Date | 账务处理开始日期 | M |
| seq | Long | 顺序 | M |
| spId | Long | 第三方运营商标识 | O |
| partyType | String | 参与人类型 | O |
| partyCode | String | 参与人编码 | O |

## 7.3 根据账期类型标识，账期日期，偏移量查询账期(给ZTP测试用)(`待改造`)
返回符合条件的账期数据
### 方法签名：
```java
BillingCycleData qryBillingCycle4Ztp(Parm4QryBillCyc parm4QryBillCyc)
```
#### 7.3.2 入参说明
##### Parm4QryBillCyc 
见[7.2.2](#7.2.2)

#### 7.3.3 出参说明
##### <a name="billingCycleData"></a>BillingCycleData
见[BillingCycleData](#billingCycleData)