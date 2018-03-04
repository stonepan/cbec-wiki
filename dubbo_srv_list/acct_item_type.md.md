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
## 5.1 查询所有账目类型
返回所有账目类型列表
### 方法签名：
```java
List<AcctItemTypeData> qryAllAcctItemType()
```
#### 5.1.2 入参说明
无

#### 5.1.3 出参说明
##### AcctItemTypeData
| Name | Type | Description | Note |
| ---- | ---- | ----------- | ---- |
| acctItemTypeId | Long | 账目类型标识 | M |
| acctItemTypeCode | String | 账目类型编码 | M |
| acctItemTypeName | String | 账目类型名称 | M |
| parentId | Long | 父级账目类型标识 | O |
| acctResId | Long | 关联余额类型 | M |
| savePrecision | Long | 保存精度 | M |
| displayScale | Long | 显示精度 | O |
| rateDisplayScale | Long | 费率配置显示精度 | O |
| roundMethod | String | 四舍五入方式，参考ROUND_METHOD域数据定义 | O |



    /**
     *
     * 表字段 : acct_item_type.GST_TYPE
     */
    private String gstType;

    /**
     *
     * 表字段 : acct_item_type.ACCT_RES_ID
     */
    private Long acctResId;

    /**
     *
     * 表字段 : acct_item_type.PARENT_ID
     */
    private Long parentId;

    /**
     *
     * 表字段 : acct_item_type.EXCHANGE_ITEM_TYPE_ID
     */
    private Long exchangeItemTypeId;



    /**
     *
     * 表字段 : acct_item_type.COMMENTS
     */
    private String comments;

    /**
     *
     * 表字段 : acct_item_type.ACCT_ITEM_TYPE_CODE
     */
    private String acctItemTypeCode;

    /**
     * A 表示税  ， B 表示 优惠金额
     * 表字段 : acct_item_type.USAGE_TYPE
     */
    private String usageType;

    /**
     *
     * 表字段 : acct_item_type.SP_ID
     */
    private Long spId;

    /**
     * acct_res.IS_CURRENCY
     */
    private String isCurrency;

    /**
     * acct_res.CURRENCY_TYPE_ID
     */
    private Long currencyTypeId;




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