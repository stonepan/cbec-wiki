# 8. 支付方式数据查询服务
服务类：
```java
com.ztesoft.zsmart.bss.crm.bcdc.pay.service.PaymentMethodRemoteService
```
## 8.1 查询所有支付方式(`待改造`)
返回所以支付方式列表
### 方法签名：
```java
List<PaymentMethodData> queryAllPaymentMethod()
```
#### 8.1.2 入参说明
无

#### 8.1.3 出参说明
##### PaymentMethodData
| Name | Type | Description | Note |
| ---- | ---- | ----------- | ---- |
| paymentMethodId | Long | 支付方式标识 | M |
| paymentType | String | 付款类型 | M |
| paymentMethodName | String | 支付方式名称 | M |
| paymentMethodCode | String | 支付方式编码 | O |
| systemReserved | String | 是否系统预留(Y:是,N:否) | M |
| state | String | 状态 | M |
| createdDate| Date | 创建时间 | O |
| comments | String | 备注 | O |
| spId | Long | 第三方运营商标识 | O |
| partyType | String | 参与人类型 | O |