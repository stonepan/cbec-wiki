# 1. 标准地址查询服务
服务类：
```java
com.ztesoft.zsmart.bss.crm.bcdc.addr.service.StdAddrRemoteService
```
## 1.1 标准地址完整名称批量查询
根据入参条件查询标准地址完整名称。
### 方法签名：
```java
QueryDisplayAddrResp queryDisplayAddr(QueryDisplayAddrReq request)
```
#### 1.1.2 入参说明
##### QueryDisplayAddrReq 
| Name | Type | Description | Note |
| ---- | ---- | ----------- | ---- |
| addrList| List\<QryDisplayAddrData\>| 标准地址查询入参原子类列表 | M |
##### QryDisplayAddrData
| Name | Type | Description | Note |
| ---- | ---- | ----------- | ---- |
| stdAddrId| Long | 末级标准地址ID,根据其解析完整的上级地址 | M |
| streetAddr| String| 街道地址详情,用于对标准地址进行补充 | O |


#### 1.1.3 出参说明
##### QueryDisplayAddrResp 
| Name | Type | Description | Note |
| ---- | ---- | ----------- | ---- |
| resuleCode | String | 0-成功，其他-失败 | M |
| resultMessage | String | 返回消息 | M |
| dispAddrList| List\<DisplayAddrData\>| 标准地址查询出参参原子类列表 | O |
##### DisplayAddrData
| Name | Type | Description | Note |
| ---- | ---- | ----------- | ---- |
| stdAddrId| Long | 传入的末级标准地址id | M |
| displayAddr | String | 标准地址完整名称 | O |